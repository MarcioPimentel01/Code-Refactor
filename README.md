# Code Refactor Starter Code


## Readme.md file main porpuse

This document contains information related to the Week One challenge for HTML, CSS, and Git: Code Refactor from the UCF Coding Bootcamp.
> **Important**: All the changes made to this code follow the amount of knowledge learned throughout the first part of the program. New tools and technologies may exist; however, they are not part of this segment of the program.

### The Challenge

We'll be going to work with a commoly used software development format know as **agile project management** to handle this task.

### Refactor Changes
The refactor changes aim for web **accessibility**, ensuring that people with **disabilities** can access website information using assistive technologies like video captions, screen readers, and braille keyboards.

Please see below the changes made to the code to adhere to the accessibility concept.

* Added the name of the company to the <title> element
```html
  <title>Horiseon website</title>`
```
* added favicon 
```html
 <link rel="icon" type="image/ico" href="./assets/images/favicon.ico">
```
* Header element changed from `<div>` to `<nav>`

```html
<!-- In this part of the code, I replaced <div class="header"> with the semantic element <header>. -->
<!-- Additionally, I inserted the <nav> element between the navigation links for 'Search Engine Optimization', 'Online Reputation Management', and 'Social Media Marketing'. -->
<!-- The <nav> semantic element aids accessibility when using assistive technologies like screen readers. -->
<!-- In summary, <nav> promotes a better semantic structure in HTML. -->
<header class="header">
    <h1>Hori<span class="seo">seo</span>n</h1>
    <nav>
        <ul>
            <li>
                <a href="#search-engine-optimization">Search Engine Optimization</a>
            </li>
            <li>
                <a href="#online-reputation-management">Online Reputation Management</a>
            </li>
            <li>
                <a href="#social-media-marketing">Social Media Marketing</a>
            </li>
        </ul>
    </nav>
</header>
```
* The CSS behavier for the semantic element `<header>` had to be changed. Please see below the CSS code.
* I also chaged the color for the class `.header h1 seo` to a darker color to better display the major segment of the business.
* All classes that conteined the `div` as identifier was changed to `nav`.

  ---

  ## CSS Styling for .header

```css
/* In this CSS code, I'm styling the header section with semantic elements and navigation. */
.header {
    padding: 20px;
    font-family: 'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
    background-color: #2a607c;
    color: #ffffff;
}

.header h1 {
    display: inline-block;
    font-size: 48px;
}

.header h1 .seo {
    color: #96959e;
}

.header nav {
    padding-top: 15px;
    margin-right: 20px;
    float: right;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    font-size: 20px;
}

.header nav ul {
    list-style-type: none;
}

.header nav ul li {
    display: inline-block;
    margin-left: 25px;
}
```
 * For the following block the `<section>` semantic element replaced the `<div>` HTML element.

```html
 <section class="hero"></section>
```
* For the following block the `<section>` semantic element replaced the `<div>` HTML element. There was also the inclusion of `<figure>` and `<figcaption>` to the elements `<img>` and `<h2>`.
* `alt=""` attributes were added to all pictures.
 ```html
<section class="content">
            <section id="search-engine-optimization" class="search-engine-optimization">
                <figure>
                <img src="./assets/images/search-engine-optimization.jpg" class="float-left" alt="SEO strategy and tools for effective Search Engine Optimization">
                    <figcaption>
                        <h2>Search Engine Optimization</h2>
                    </figcaption>
                </figure>
                    <p>
                    The dominance of mobile internet use means that users are searching for the right business as they travel, shop, or sit on their couch at home. Search Engine Optimization (SEO) allows you to increase your visibility and find the right customers for your business.
                    </p>
            </section>
            <section id="online-reputation-management" class="online-reputation-management">
                <figure>
                <img src="./assets/images/online-reputation-management.jpg" class="float-right" alt="Monitoring and managing online reputation to build a positive brand image">
                    <figcaption>
                        <h2>Online Reputation Management</h2>
                    </figcaption>
                </figure>
                    <p>
                    The web is full of opinions, and some of these can be negative. Social media allows anyone with an internet connection to say whatever they want about your business. Online Reputation Management gives you the control over what potential customers see when they search for your business.
                    </p>
            </section>
            <section id="social-media-marketing" class="social-media-marketing">
                <figure>
                <img src="./assets/images/social-media-marketing.jpg" class="float-left" alt="Social Media Marketing: Utilizing platforms to enhance brand visibility and engage with the audience">
                    <figcaption>
                        <h2>Social Media Marketing</h2>
                    </figcaption>
                </figure>
                    <p>
                    Social media continues to have a sizable influence on buying habits. Social media marketing helps you determine which platforms are suited to your brand, using analytics to find the right markets and increase your lead generation.
                    </p>
            </section>
```

