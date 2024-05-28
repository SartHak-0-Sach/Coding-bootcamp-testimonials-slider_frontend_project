# Coding Bootcamp Testimonial Slider

## Welcome! 👋

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [How to setup the project](#how-to-setup-the-project)
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

The challenge is to create a testimonial slider component showcasing reviews from participants of a coding bootcamp course. 

Users should be able to-
- View the optimal layout for the component depending on their device's screen size
- Navigate through the slider seamlessly using either their mouse/trackpad or keyboard.

### How to setup the project

To set up the project locally, follow these steps:

1. Clone the repository using GitHub Desktop or Git Bash:
    ```bash
    git clone https://github.com/SartHak-0-Sach/Coding-bootcamp-testimonials-slider_frontend_project.git
    ```
2. Open the project folder in your code editor.
3. Run the project using a live server extension or deploy it using Netlify, Vercel, or another web hosting and deployment service.

### Screenshot

![Design preview](/design/desktop-design-slide-1.jpg)

### Links

- Solution URL: [GitHub Repository](https://github.com/SartHak-0-Sach/Coding-bootcamp-testimonials-slider_frontend_project)
- Live Site URL: [Live Site](https://coding-bootcamp-app.netlify.app/)

## My process

### Built with

- HTML5
- CSS3
- JavaScript

You will find all the required assets in the `/images` folder. The assets are already optimized.

There is also a `style-guide.md` file containing the information you'll need, such as color palette and fonts.

### What I learned

This project has been a great learner of knowing how to make the slider animation using simple JavaScript functions and do DOM manipulation to make it look very seamless and interactive as shown-

```
let currentSlide = 0
let maxSlides = testimonials.length;

function transitionSlide() {
    testimonialsWrapper.style.transform = `translateX(${currentSlide * -100}%)`;
}

function resizeUpdate() {
    if (document.body.offsetWidth >= 576) {
        buttonGroup.style.left = 'calc(' + getPhotoLeftPosition(currentSlide) + 'px + 2vw + 1rem)';
        buttonGroup.style.top = getPhotoBottomPosition(currentSlide) - buttonGroup.getBoundingClientRect().height / 2 + 'px';
    } else {
        buttonGroup.style.left = '0';
        buttonGroup.style.top = getPhotoBottomPosition(currentSlide) - buttonGroup.getBoundingClientRect().height / 2 + 'px';
    }
}

buttonPrevious.addEventListener('click', () => {
    // Get previous slide number
    currentSlide = (currentSlide - 1 < 0 ? maxSlides - 1 : currentSlide - 1);
    transitionSlide();
}, false);
buttonNext.addEventListener('click', () => {
    // Get next slide number
    currentSlide = (currentSlide + 1 === maxSlides ? 0 : currentSlide + 1);
    transitionSlide();
}, false);

window.addEventListener('load', resizeUpdate, false);
window.addEventListener('resize', resizeUpdate, false);

resizeUpdate();
```

### Continued development

The continuously learning journey of a programmer never ends. This project made me realize that there are many concepts that I need to work upon including fundamentals like flex-box and its properties, to more complex concepts like working with fetch and async await in javascript. These areas are some that I think I need to work more upon in the upcoming future as they highlight some of the most significant regions of web development that are important for every developer to know of. 

These key points mentioned here will help me grow accountable and consistent towards improving at writing good quality code and be a successful full stack developer one day.

### Useful resources

- [Harkirat Singh course notes](https://github.com/SartHak-0-Sach/harkirat-singh-course_code_and_notes) - I have added notes of all lectures along with code and lecture insights of all weeks along with bonus lectures to help you all as much as I can.
- [My development code and notes](https://github.com/SartHak-0-Sach/cwh-web-dev-playlist_code_and_notes) - These are my notes that I made while working on my development skills in initial days and did these courses. Make sure to star the repository if you like it.✨💫

## Author

<b><strong>Sarthak Sachdev</strong></b>
- Website - [Sarthak Sachdev](https://itsmesarthak.netlify.app/)
- LeetCode - [@sarthak_sachdev](https://leetcode.com/u/sarthak_sachdev/)
- Twitter - [@sarthak_sach69](https://www.twitter.com/sarthak_sach69)

## Acknowledgments

I feel like the solutions provided on the website and the continuous doubt solving by industry experts on discord for free is something that is unmatched by anyone else and need to be acknowledged for their efforts in improving me as a developer by suggesting the best practices in your respective tech stack.

## Got feedback for me?

I love receiving feedback! I am always looking to improve my code and take up new innovative ideas to work upon. So if you have anything you'd like to mention, please email 'hi' at saarsaach30[at]gmail[dot]com.

If you liked this project make sure to spread the word and share it with all your friends.

**Happy coding!** ☺️🚀
