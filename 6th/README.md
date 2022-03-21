# Conquering Responsive Layouts--6th challenge

## Table of contents

- [Overview](#overview)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

In this challenge I had to :

- Get all the navigation items next to one another
- Add a space between all the items

### Links

- This course you can find: [on this webiste](https://courses.kevinpowell.co/view/courses/conquering-responsive-layouts/)

## My process

This is what I've done so far.

```css
nav > .nav__list {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
```

nav is parent and nav-list is child, so I put display flex , what move them next to each other, aling items on center so in that place they will be centered and horizontally space between so they will be separated from each other.  
This is with lists so in our child nav list we need to use list style none.
And button with little padding and border radious.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What I learned

While working on this challenge I learned :

- I learned how to make navigation bar with flexbox.

## Author

- Frontend Mentor - [@Holllyyyy](https://www.frontendmentor.io/profile/Holllyyyy)
- Twitter - [@svetlanajokic](https://twitter.com/svetlanajokic)
- LinkedIn - [@Svetlana Jokic](https://www.linkedin.com/in/svetlana-jokic-787432100/)
