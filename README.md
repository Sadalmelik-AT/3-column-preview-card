# Frontend Mentor - 3-column preview card component solution

This is a solution to the [3-column preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/3column-preview-card-component-pH92eAR2-). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements
- Personal extra: smoothly animate the buttons when hovered

### Links

- Solution repository: [GitHub](https://github.com/Sadalmelik-AT/3-column-preview-card)
- Live Site URL: [Live site](https://sadalmelik-at.github.io/3-column-preview-card/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Scss
- Flexbox
- Mobile-first workflow

### What I learned

I challenged myself to give an smooth animation to the buttons when hovered. To do so I used pseudo-elemets and animated them through a class (btn), as pseudo-elements are not compatible with the hover pseudo-class.

This the HTML:

```html
<button class="btn">Learn More</button>
```

This is the CSS:

This selector targets the  pseudo-element when any element with the class btn is hovered

```css
.btn:hover:before {
  transform: translateX(-130px);
  transition: all 0.2s ease-in;
}
```

I add a transition porperty to make is move to the left smoothly

This selector targets the pseudo-element and allows me to style it. I gave it a z-indez of -1 so the text can be seen.

```css
.btn::before {
  content: "";
  background-color: $white;
  height: 100%;
  width: 100%;
  position: absolute;
  z-index: -1;
  top: 0;
  left: 0;
  transform: translateX(0);
  transition: all 0.2s ease-in;
}
```

The last 2 properties are here to re-introduce the white bacground in the button when hovered out to make the animation smoother.

### Continued development

This project really allowed me to get a grip on flexbox. I feel more confident in my ability to understand and re-use at will.

However there is always room for improvement therefore I will continue on doing flexbox based projects to build even better responsive designs

### Useful resources

- [How to reverse an animation on mouse out after hover](https://stackoverflow.com/questions/16516793/how-to-reverse-an-animation-on-mouse-out-after-hover) - This helped me reverse the animation to make it smoother.

## Author

- Frontend Mentor - [@PyZziie](https://www.frontendmentor.io/profile/yourusername)
- Twitter - [@sadalmel1k](https://twitter.com/Sadalmel1k)
