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
   `<title>Horiseon website</title>`
* added favicon `<link rel="icon" type="image/ico" href="Module01-Challenge01/assets/images/favicon.ico">`
* Header element changed to `<div>` to `<nav>`


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

* The following CSS Classes were changed, for the semantic element <header>
    
## CSS Styling for .header

```css
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
