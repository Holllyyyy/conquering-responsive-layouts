# Conquering Responsive Layouts--8th challenge

## Table of contents

- [Overview](#overview)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

In this challenge I had to :

- Make the navigation layout work on both mobile and large screens.
- Mobile-first, so mobile styles first, then add the large screen styles inside the existing media query


![ss-10](https://user-images.githubusercontent.com/92860927/159507577-e963da35-3c0b-40b8-8a90-d61d165e5d0b.png)
![ss-11](https://user-images.githubusercontent.com/92860927/159507583-575a7b34-54b9-4e77-8a3f-abe6ff8a550c.png)
![ss-12](https://user-images.githubusercontent.com/92860927/159507590-54ad474a-16f1-4473-803e-a0817ccba62e.png)



### Links

- This course you can find: [https://courses.kevinpowell.co/view/courses/conquering-responsive-layouts/](https://courses.kevinpowell.co/view/courses/conquering-responsive-layouts/)
- My solution for this challenge: [https://kaleidoscopic-brioche-bd59f6.netlify.app/](https://kaleidoscopic-brioche-bd59f6.netlify.app/)

## My process

From the last challenge and this the only thing what changed is navigation menu.  

  <header>
      <div class="container row">
        <button class="nav-toggle" aria-label="open navigation">
          <span class="hamburger"></span>
        </button>
        <a class="logo" href="#">
          <img src="img/logo.svg" alt="conquering responsive layouts" />
        </a>
        <nav class="nav">
          <ul class="nav__list nav__list--primary">
            <li class="nav__item"><a href="#" class="nav__link">Home</a></li>
            <li class="nav__item"><a href="#" class="nav__link">About</a></li>
            <li class="nav__item"><a href="#" class="nav__link">Contact</a></li>
          </ul>
          <ul class="nav__list nav__list--secondary">
            <li class="nav__item"><a href="#" class="nav__link">Sign In</a></li>
            <li class="nav__item">
              <a href="#" class="nav__link nav__link--button">Sign up</a>
            </li>
          </ul>
        </nav>
      </div>
    </header>
Here is added button  with few classes what is connected with JavaScript and CSS and what will let on small screens to be visible.

In JavaScript file is this:

```js
const navToggle = document.querySelector(".nav-toggle");
const nav = document.querySelector(".nav");

navToggle.addEventListener("click", () => {
  nav.classList.toggle("nav--visible");
});
```

Here is selected nav toggle , and nav where is added event listener where on click will open menu. And also .nav--visible what we will custom on our css.

So in our CSS, the mobile view first is like this:

```css
header {
  background: #136c72;
  padding: 1em 0;
  text-align: center;
}
  .nav {
    width: 100%;
  }

  .nav-toggle {
    cursor: pointer;
    border: 0;
    width: 3em;
    height: 3em;
    padding: 0em;
    border-radius: 50%;
    background: #072a2d;
    color: white;
    transition: opacity 250ms ease;
    position: absolute;
    left: 0;
  }

  .nav-toggle:focus,
  .nav-toggle:hover {
    opacity: 0.75;
  }

  .hamburger {
    width: 50%;
    position: relative;
  }

  .hamburger,
  .hamburger::before,
  .hamburger::after {
    display: block;
    margin: 0 auto;
    height: 3px;
    background: white;
  }

  .hamburger::before,
  .hamburger::after {
    content: "";
    width: 100%;
  }
  .hamburger::before {
    transform: translateY(-6px);
  }
  .hamburger::after {
    transform: translateY(3px);
  }
  /* made changes here from video
   to make it more accessible.
   
   Works the same :) */
  .nav {
    visibility: hidden;
    height: 0;
    position: absolute;
    font-size: 1rem;
  }
  .nav--visible {
    visibility: visible;
    height: auto;
    position: relative;
  }

  .nav__list {
    margin: 0;
    padding: 0;
    list-style: none;
  }
  .nav__list--secondary {
    margin-top: 2em;
  }
  .nav__item {
    margin-top: 0.75em;
  }
  .nav__link {
    text-transform: uppercase;
    text-decoration: none;
    color: #fff;
  }
  .nav__link--button {
    padding: 0.25em 0.75em;
    background-color: #fff;
    color: #23424a;
    border-radius: 100px;
  }
  .nav__link:hover,
  .nav__link:focus {
    opacity: 0.75;
  }

  .logo {
    height: 30px;
  }
}
```

This is the first part of writing css, where nav taking 100% width. and than we have class nav-toggle with some stuff inide it. Using position absolute and relative . Hamburger is here also as well with before and after, and managed to be seen on phone but not on large devices.

And for larger devices is here:

```css

@media (min-width: 800px) {
  .nav-toggle {
    display: none;
  }

  .nav {
    visibility: visible;
    display: flex;
    height: auto;
    align-items: center;
    position: relative;
    justify-content: end;
  }
  .nav__list {
    display: flex;
    margin: 0;
  }
  .nav__item {
    margin: 0 0 0 1.5em;
  }

  .nav__list--primary {
    margin: 0 auto;
  }
```

In this part class toggle we put to be none, so it wont show up on large screens, will stay just on small screens.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- JavaScript

### What I learned

While working on this challenge I learned :

- how to start with mobile first view, a little use of JavaScript, and how to use before and after with all of it.

## Author

- Frontend Mentor - [@Holllyyyy](https://www.frontendmentor.io/profile/Holllyyyy)
- Twitter - [@svetlanajokic](https://twitter.com/svetlanajokic)
- LinkedIn - [@Svetlana Jokic](https://www.linkedin.com/in/svetlana-jokic-787432100/)
