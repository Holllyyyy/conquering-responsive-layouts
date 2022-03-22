# Conquering Responsive Layouts--5th challenge

## Table of contents

- [Overview](#overview)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)

## Overview

In this challenge I had to :

- make image to be in the right side but in same div as heading,paragraph and button
- and in the next part to make text to be left and aside element right



![ss-7](https://user-images.githubusercontent.com/92860927/159505474-53406323-23a7-44cb-9e5b-61095e634927.png)


![ss-8](https://user-images.githubusercontent.com/92860927/159505482-7c4b427a-8e00-4ad5-b658-80b7542985c9.png)



### Links

- This course you can find: [https://courses.kevinpowell.co/view/courses/conquering-responsive-layouts/](https://courses.kevinpowell.co/view/courses/conquering-responsive-layouts/)
- My solution for this challenge: [https://melodic-mousse-c97900.netlify.app/](https://melodic-mousse-c97900.netlify.app/)

## My process
This is how i started and what Ive done so far.

``` HTML

  <div class="hero">
      <div class="container row">
        <div class="hero__text">
          <h1>Responsive layouts don’t have to be a struggle</h1>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim
            ad minim veniam.
          </p>
          <a href="#" class="btn">I want to learn</a>
        </div>
        <div class="hero__img">
          <img src="./img/hero-img.jpg" alt="hero image" />
        </div>
      </div>
    </div>
```
This is first part of HTML. And its upper part of this page.  At the very beggining I have div class hero. And after it i have div class container and row together.  
That is basically one div container one div row or what is easier to say its display- flex, flex-direction- row what is default for flexbox.
 So this means automatically this div or container, or what is inside will be display flex and row.  Inside this div are two divs. 
 First div is hero__text who consist of:
- h1 element
- p element
Second div is hero__img who consist of:
- img element.

When we have container row , it's taking children and putting them to row. So here we have two children and thats why my picture will be beside text on the right side. It will be close to each other, so for this we need to use CSS.

```CSS
*,
*::before,
*::after {
  box-sizing: border-box;
}

body {
  margin: 0;
  font-family: "Roboto", sans-serif;
  font-size: 1.3rem;
}
img {
  max-width: 100%;
}
```
Here we just used to apply on all elements box sizing to be border box, so we wont have problem with margins,paddings,height and width, all will be inside our box, and we will use space of that  box.

For body is margin 0, and some font-family and font-sizee, that I will later change for every element.
Image is set of max-width of 100%, so I dont need to worry if my image would have any problems, and it would be responsive.
So whatever we do, we should be sure to always put max-width of 100% for our images.

```CSS
.container {
  width: 80%;
  max-width: 1100px;
  margin: 0 auto;
}

.row {
  display: flex;
  justify-content: space-between;
 
}
```
Here is div container of 80% , where is taking 80% and max-width of 1100px. Margin 0 auto, to be centered. Row is using display of flex, and justify content just to make some space between images and text.

Now rest of the page:

- HTML
Here  is main tag, because of accessibility it's so important for every page to have main tag. After  I put my main tag I used main container row.  So it will apply same role as earlier, cause I've already in my CSS written about it. But by default will make my page on two parts, two sides. Left and right.
After I wrote my main I added section with elements: h2 and two p elements.

```HTML
  <main class="main container row">
      <section class="primary-content">
        <h2 class="section-title">
          Quality designs made custom, on demand, just for you
        </h2>

        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam. Lorem ipsum dolor sit amet, consectetur adipiscing elit,
          sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
          enim ad minim veniam.
        </p>

        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam. Lorem ipsum dolor sit amet, consectetur adipiscing elit,
          sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
          enim ad minim veniam.
        </p>
      </section>
```

And here I added aside tag, because it's going to be on the side.  This aside tag has h2 and p elements. 

      ```HTML
      <aside class="side-bar">
        <h2 class="side-title">Cheap</h2>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam.
        </p>
        <h2 class="side-title">Quick</h2>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam.
        </p>
        <h2 class="side-title">Quality</h2>
        <p>
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
          eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad
          minim veniam.
        </p>
      </aside>
    </main>
```
In my CSS I gave my section width of 62% and my aside element I gave 32%.
For the first part it's the same just instead of aside there is picture.

```CSS
.hero__text {
  width: 62%;
}

.hero__img {
  width: 32%;
  align-self: flex-start;
}

.primary-content {
  width: 62%;
  margin-top: 3rem;
}
.section-title {
  color: #136c72;
}
.side-bar {
  width: 32%;
  background-color: #136c72;
  color: #fff;
  text-align: center;
  margin-top: 3rem;
}
```
### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox

### What I learned

While working on this challenge I learned :

- I learned how to put image to be on the right side inside parent element
- also about section and aside element how I can manage it to make it to be beside each other

## Author

- Frontend Mentor - [@Holllyyyy](https://www.frontendmentor.io/profile/Holllyyyy)
- Twitter - [@svetlanajokic](https://twitter.com/svetlanajokic)
- LinkedIn - [@Svetlana Jokic](https://www.linkedin.com/in/svetlana-jokic-787432100/)
