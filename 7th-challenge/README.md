# Conquering Responsive Layouts--7th challenge

## Table of contents

- [Overview](#overview)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

In this challenge I had to :

- make navigation menu to have logo on the left side, on mid to be three navigation links and on the right side two.

### Links

- This course you can find: [on this webiste](https://courses.kevinpowell.co/view/courses/conquering-responsive-layouts/)

## My process

This is how i started and what I've done so far.

In this challenge, I will just explain this part of navigation.
In my HTML I wrote a header on what is semantic tag and very important for accessibility.
After it, I made navigation, nav tag, and wrote a few lists.
Gave some classes as well as names of that classes.
I wanted to add a logo image.
So what I've done here, is I put one div after the header and named container row what is for default flexbox.
And it's connected in whole this page.
After it, in my nav tag, for navigation, I wanted to separate nav links, so what I needed to do, is to put two unorder lists inside my links. In one I put 3 and another 2.
Class nav**list is the main class name, and nav**list--primary nav\_\_list--secondary, are just independent CSS blocks to reuse them later separately.

``HTML

  <header>
    <div class="container  row">
     <a href="#" class="logo">
        <img src="./logo.svg" alt="Conquering Responsive design"></a>
      <nav class="nav">
        <ul class="nav__list nav__list--primary">
          <li class="nav__item"><a href="#" class="nav__link">Home</a></li>
          <li class="nav__item"><a href="#" class="nav__link">About</a></li>
          <li class="nav__item"><a href="#" class="nav__link">Contact</a></li>
        </ul>
        <ul class="nav__list  nav__list--secondary">
          <li class="nav__item"><a href="#" class="nav__link">Sign In</a></li>
          <li class="nav__item"><a href="#" class="nav__link nav__link--button">Sign up</a></li>
        </ul>
      </nav>
    </div>
  </header>
``

In the CSS, the first thing I've done, I gave to nav class of nav tag display flex, and space between, align-items center, so all be centered vertically.
And it's the first step because nav has two children unorder lists(ul).
For the logo, just a little 1em margin-left so the list will have some space between it.

```CSS
 .nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-grow;1;
  }
```

Here we can see that there's the nav list and later nav list primary.
Nav list is the main class of ul tag, which will be applied on both children of nav tag.

```css
.nav__list {
  margin: 0;
  padding: 0;
  list-style: none;
  display: flex;
  align-items: center;
}
```
and this part will be applied just for the first child of the nav tag, by setting these 3 items from ul to center.

```css
.nav__list--primary {
  margin: auto;
}
```
### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What I learned

While working on this challenge I learned :

- how to add picture inside navigation menu, and to center some links and some to put right.

## Author

- Frontend Mentor - [@Holllyyyy](https://www.frontendmentor.io/profile/Holllyyyy)
- Twitter - [@svetlanajokic](https://twitter.com/svetlanajokic)
- LinkedIn - [@Svetlana Jokic](https://www.linkedin.com/in/svetlana-jokic-787432100/)
