# Random Background Color Changer

A lightweight JavaScript application that updates the page background to a random dark color from a predefined palette and displays the active hex code.

Built to demonstrate DOM manipulation, array usage, randomization logic, and event-driven UI updates.

---

## Live Demo

https://sharpsanders.github.io/random-background-changer/

<img src="./img/Screenshot-random-background-changer.png" alt="Random Background Color Changer Screenshot">

---

## Overview

The interface includes:

- A page title  
- A live hex color display  
- A “Change Background Color” button  

Each button click:

1. Selects a random hex value from a predefined color array  
2. Updates the document background color  
3. Displays the selected hex code in the UI  

---

## Technical Highlights

- Controlled random index generation using `Math.random()` and `Math.floor()`
- Array-driven color palette management
- Direct DOM element selection with `querySelector`
- Dynamic style updates via `element.style`
- Event handling using button click listeners

---

## Core Logic (JavaScript)

```js
const darkColorsArr = [
  "#2C3E50",
  "#34495E",
  "#2C2C2C",
  "#616A6B",
  "#4A235A",
  "#2F4F4F",
  "#0E4B5A",
  "#36454F",
  "#2C3E50",
  "#800020",
];

function getRandomIndex() {
  return Math.floor(darkColorsArr.length * Math.random());
}

const body = document.querySelector("body");
const bgHexCodeSpanElement = document.querySelector("#bg-hex-code");

function changeBackgroundColor() {
  const color = darkColorsArr[getRandomIndex()];
  bgHexCodeSpanElement.innerText = color;
  body.style.backgroundColor = color;
}

const btn = document.querySelector("#btn");
btn.onclick = changeBackgroundColor;
Tech Stack
HTML5

CSS3

JavaScript (ES6+)

No frameworks or build tools — fully client-side and dependency-free.

Project Structure
random-background-changer/
  index.html
  styles.css
  script.js
  img/
    Screenshot-random-background-changer.png
Run Locally
Clone the repository

Open index.html in your browser

No installation or build process required.

Skills Demonstrated
Managing and accessing structured data with arrays

Generating bounded random values

Updating text content dynamically

Applying inline style changes programmatically

Basic UI interaction patterns

Potential Enhancements
Copy-to-clipboard hex code support

Display RGB and HSL equivalents

Add transition animations for smoother background changes

Track recently used colors

Author
Trevyn Sanders
Better Endeavors LLC