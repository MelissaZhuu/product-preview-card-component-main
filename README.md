# Frontend Mentor - Product preview card component

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa).

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshots](#screenshots)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

The challenge is to build out this product preview card component and get it looking as close to the design as possible.

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Screenshots

Mobile:  
![](/images/product-card-mobile-screenshot.png)

Desktop:  
![](/images/product-card-desktop-screenshot.png)

On hover:  
![](/images/product-card-hover-screenshot.png)

### Links

- Solution URL: [https://github.com/MelissaZhuu/product-preview-card-component-main](https://github.com/MelissaZhuu/product-preview-card-component-main)
- Live Site URL: [https://melissazhuu.github.io/product-preview-card-component-main/](https://melissazhuu.github.io/product-preview-card-component-main/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow
- Sass preprocessor

### What I learned

I learned a lot about mobile-first and responsive design in this project, mainly how to include responsive images. I also learned about CSS Grid and used a mix of Grid and Flexbox in my styling.

I had some issues with responsive images that taught me a lot. At first, I was trying to use 'srcset' and 'sizes' attributes to display my two images and was having trouble getting the browser to choose the right image. It was a weird situation since the larger, desktop image had a smaller width than the zoomed-in, mobile image. 

```html
    <img class="product-image" 
    src="images/image-product-mobile.jpg" 
    srcset="images/image-product-mobile.jpg 686w, 
            images/image-product-desktop.jpg 600w"
    sizes="(max-width: 600px) 686px, 600px"
    alt="A square bottle of Chanel Gabrielle Perfume and some leaves on a white surface">
```

Upon further researching, I found that I was focused on 'resolution switching' when I should have been addressing the 'art direction' and using the 'picture' element, which allows you to specify which media conditions should use which image.

```html
    <picture>
      <source media="(max-width: 599px)" srcset="images/image-product-mobile.jpg" />
      <source media="(min-width: 600px)" srcset="images/image-product-desktop.jpg" />
      <img src="images/image-product-desktop.jpg" alt="A square bottle of Chanel Gabrielle Perfume and some leaves on a white surface" class="product-image"/>
    </picture>
```

### Continued development

In future projects, I would like to continue to familiarize myself with responsive design best practices and become comfortable with making all kinds of content types, whether that's text, images, icons or videos, look amazing on all screens.

### Useful resources

Resources that helped me understand responsive images:  
- [LiveFire Dev - Optimizing images](https://livefiredev.com/optimize-image-without-loss-of-quality/)
- [LiveFire Dev - Using srcset](https://livefiredev.com/srcset-not-working-getting-wrong-images/)
- [MDN Web Docs - Responsive images](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images) - This one was particularly helpful.

Resources that helped me with CSS Grid:  
- [CSS Tricks - Guide to CSS Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [Learn CSS Grid](https://learncssgrid.com/)
- [Josh Comeau - An Interactive Guide to CSS Grid](https://www.joshwcomeau.com/css/interactive-guide-to-grid/) - This site is not only built really cool but was the most helpful for me due to its interactive examples and explanations! Definitely worth checking out.

## Author

- Website - [Github](https://github.com/MelissaZhuu)
- Frontend Mentor - [@MelissaZhuu](https://www.frontendmentor.io/profile/MelissaZhuu)
