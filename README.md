# Frontend Mentor - Clipboard landing page solution

This is a solution to the [Clipboard landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/clipboard-landing-page-5cc9bccd6c4c91111378ecb9). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
    - [The challenge](#the-challenge)
    - [Screenshot](#screenshot)
    - [Links](#links)
- [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
    - [Continued development](#continued-development)
    - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)


## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page

### Screenshot

![](./images/screenshot.jpg)


### Links

- Solution URL: [https://github.com/gchristofferson/clipboard-landing-page](https://github.com/gchristofferson/clipboard-landing-page)
- Live Site URL: [https://gchristofferson.github.io/clipboard-landing-page/](https://gchristofferson.github.io/clipboard-landing-page/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow
- BEM methodology

### What I learned

One of my major learnings in this project was how to change the color of an .svg image on hover using CSS filters.  What I learned was that in order to change the color, first I needed to convert a hex color code to a CSS filter.  This is not something someone can easily do without the help of a tool. I used [Barret Sonntag's](https://codepen.io/sosuke) [CSS filter generator](https://codepen.io/sosuke/pen/Pjoqqp).  I highly recommend this tool if you need to do something like this.  

To get this to work in your projects, first add the SVG image using either using an `<img>` tag or like I did, using CSS background image.  Here's the div I added the .svg image as a background to:

```html
<div class="social__icon social__icon--facebook"></div>
```

Here is the CSS to where I added the background svg image:
```css
.social__icon--facebook {
    background-image: url("../images/icon-facebook.svg");
}
```
Out of the box, this .svg is black, which is perfect for this design.  However, on hover, I needed to change the color to the cyan color.  This is where the css filter came to the rescue:
```css
.social__icon:hover,
.social__icon:focus {
  color: var(--strong-cyan);
  filter: invert(57%)
  sepia(89%)
  saturate(360%)
  hue-rotate(121deg)
  brightness(90%)
  contrast(89%);
}
```

### Continued development

Going forward I will continue using the CSS filters technique mentioned above to change the color of .svg images.  I also want to deepen my knowledge in general in the use of svg's and CSS filters  because there is so much more that can be done with them. 

### Useful resources

- [stackoverflow: How to change the color of an svg element?](https://stackoverflow.com/questions/22252472/how-to-change-the-color-of-an-svg-element#:~:text=You%20can%27t%20change%20the%20color%20of%20an%20image,it%20using%20%3Cobject%3E%2C%20%3Ciframe%3E%20or%20using%20%3Csvg%3E%20inline.) - This post is where I learned how to use CSS filters to change the color of svg images.
- [MDN - SVG filter](https://developer.mozilla.org/en-US/docs/Web/CSS/filter#svg_filter) - This article goes more into depth in explaining all the filter functions used in this technique.


## Author

- Frontend Mentor - [@gchristofferson](https://www.frontendmentor.io/profile/gchristofferson)
- Twitter - [@GreggChristoff2](https://www.twitter.com/GreggChristoff2)

## Acknowledgments

I want to give a shout-out to [Barret Sonntag](https://codepen.io/sosuke).  I wouldn't have been able to complete this project without his awesome CSS filter generator!

