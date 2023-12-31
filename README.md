# Scroll Animations Demo

This project demonstrates scroll-triggered animations on a webpage using HTML, CSS, and JavaScript.

## Table of Contents

- [Description](#description)
- [Demo](#demo)
- [Features](#features)
- [How to Use](#how-to-use)
- [Dependencies](#dependencies)
- [Additional Resources](#additional-resources)
- [License](#license)

## Description

The project showcases the implementation of scroll-triggered animations. As the user scrolls down the page, various elements come to life, providing an engaging and visually appealing experience. The animations are achieved through a combination of CSS and JavaScript.

## Demo

You can view a live demo [here](https://imjignesh.com/viewer/?id=368&file=index-js.html).

![Demo](demo-screenshot.png)

## Features

- **Scroll-triggered Animations:** The project utilizes JavaScript to trigger animations based on the user's scroll position.

  The JavaScript code below is responsible for detecting when each section of the webpage comes into view during scrolling. As a section becomes visible, it adds the "is-inview" class to trigger associated animations.

  ```javascript
  var sections = document.querySelectorAll("section");
  var container = document.querySelector(".scroll__container");

  container.addEventListener("scroll", function () {
    sections.forEach((e, i) => {
      var top = e.getBoundingClientRect().top;

      if (top == 0) {
        e.classList.add("is-inview");
      } else {
        e.classList.remove("is-inview");
      }
    });
  });

  // Dispatch a scroll event to initialize the state based on the initial scroll position
  container.dispatchEvent(new CustomEvent("scroll"));
  ```

More info on:
[scroll Based Animations](https://imjignesh.com/how-to-trigger-css-animation-on-scroll/) |
[Trigger CSS Animation On Scroll](https://imjignesh.com/how-to-trigger-css-animation-on-scroll/)

## How to Use

1. Clone the repository:

```bash
git clone https://github.com/imJignesh/scroll-animations-demo-1.git
cd scroll-animations-demo-1
```
