# Frontend Mentor - NFT preview card component solution

This is a solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![](./images/SolutionNftPreviewCardComponent.png)

### Links

- Solution URL: [Github pages](https://appithe.github.io/Frontend-Mentor/nft-preview-card-component-main/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- BEM css
- Mobile-first workflow

### What I learned

to make the hover state in the image create a container and center its content, apply a blur and contrast filter to the image so that it looks a little white. for the eye I put a z-index of 1 so that it would be on top of the image and opacity 0, when hovering in the container the opacity would change to 1 keeping the image filter

```html
<div class="container">
  <img class="card__image" src="./images/image-equilibrium.jpg" alt="equilibrium">
  <img class="overlay" src="./images/icon-view.svg" alt="eye">
</div>
```
```css

.container {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 300px;
  height: 300px;
  margin: 15px;
}

.card__image {
  width: 300px;
  height: 300px;
  border-radius: 10px;
  position: absolute;
  z-index: 0;
}

.card__image:hover {
  cursor: pointer;
  filter: blur(1px) contrast(50%);
  opacity: 1;
}

.overlay {
  position: relative;
  z-index: 1;
  opacity: 0;
}

.container:hover .overlay {
  opacity: 1;
}
```

### Useful resources

- [BEM CSS](http://getbem.com/) - This helped to me for naming the css classes

## Author

- Joel Avilés
- Frontend Mentor - [@Appithe](https://www.frontendmentor.io/profile/Appithe)
- Twitter - [@joelaviles413](https://twitter.com/joelaviles413)
