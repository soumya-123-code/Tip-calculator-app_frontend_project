# Tip Calculator App

## Easily calculate tips and track payments with the Tip Calculator app. Perfect for calculating tips for services and keeping track of past payments.

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

Easily calculate tips and track payments with the Tip Calculator app. Perfect for calculating tips for services and keeping track of past payments.

Users should be able to:

- View the optimal layout for the component depending on their device's screen size
- See the social media share links when they click the share icon

### Screenshot

![Design Preview](./design/active-states.jpg)

### Links

- Solution URL: [GitHub Repository](https://github.com/soumya-123-code/Tip-calculator-app_frontend_project)
- Live Site URL: [Live Site](https://tip-calculator-frontend.netlify.app/)

## My process

### Built with

- HTML5
- CSS3
- JavaScript

You will find all the required assets in the `/design` folder. The assets are already optimized.

There is also a `style-guide.md` file containing the information you'll need, such as color palette and fonts.

### What I learned

- Implementing interactive features such as tip calculation and payment tracking
- Utilizing local storage to store and retrieve past payment data
- Enhancing user experience with hover states and interactive elements

```js
function initializeTipButtons() {
  let i = 0;
  for (i = 0; i < tipButtons.length - 1; i++) {
    tipButtons[i].addEventListener("click", function () {
      tipPercentValue = parseInt(this.textContent.substring(0, this.textContent.length - 1)) * 0.01;
      calculate();
    })
    tipButtons[i].addEventListener("click", function () {
      customTip.value = "";
    })
    tipButtons[i].addEventListener("click", changeBg, false);
  }
  customTip.addEventListener("input", function () {
    if (/^\d*?\d*$/.test(this.value)) {
      tipPercentValue = parseInt(this.value) * 0.01;
      calculate();
    } else {
      if (tipPercentValue > 0) {
        this.value = parseInt(tipPercentValue * 100).toString();
      } else {
        this.value = "";
      }

      this.classList.add("shake");
      setTimeout(function () {
        customTip.classList.remove("shake");
      }, 1000);
    }
  })
  customTip.addEventListener("click", resetColors, false);
}
```

### Continued development

- Adding additional features such as currency conversion and multiple payment methods
- Improving accessibility and usability for a wider range of users
- Enhancing responsive design for seamless experience across devices

The continuously learning journey of a programmer never ends. This project made me realize that there are many concepts that I need to work upon including fundamentals like flex-box and its properties, to more complex concepts like working with fetch and async await in JavaScript. These areas are some that I think I need to work more upon in the upcoming future as they highlight some of the most significant regions of web development that are important for every developer to know of.

These key points mentioned here will help me grow accountable and consistent towards improving at writing good quality code and be a successful full stack developer one day.

### Useful resources

- [Harkirat Singh course notes](https://github.com/soumya-123-code/harkirat-singh-course_code_and_notes) - I have added notes of all lectures along with code and lecture insights of all weeks along with bonus lectures to help you all as much as I can.
- [My development code and notes](https://github.com/soumya-123-code/cwh-web-dev-playlist_code_and_notes) - These are my notes that I made while working on my development skills in initial days and did these courses. Make sure to star the repository if you like it.✨💫
- [MDN documentation hover state for CSS](https://developer.mozilla.org/en-US/docs/Web/CSS/:hover) - This is an amazing article which helped me finally understand hover states. I'd recommend it to anyone still learning this concept.

## Author

<b><strong>Soumya Ranjan Nayak</strong></b>
- Website - [Soumya Ranjan Nayak](https://itsmesoumya.netlify.app/)
- LeetCode - [@soumya_ranjan](https://leetcode.com/u/soumya_ranjan/)
- Twitter - [@soumya_ranjan69](https://www.twitter.com/soumya_ranjan69)

## Acknowledgments

I feel like the solutions provided on the website and the continuous doubt solving by industry experts on Discord for free is something that is unmatched by anyone else and need to be acknowledged for their efforts in improving me as a developer by suggesting the best practices in your respective tech stack.

## Got feedback for me?

I love receiving feedback! I am always looking to improve my code and take up new innovative ideas to work upon. So if you have anything you'd like to mention, please email 'hi' at soumya050794@gmail.com.

If you liked this project make sure to spread the word and share it with all your friends.

**Easily calculate tips and track payments with the Tip Calculator app.** 💰💻📱

