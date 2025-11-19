# Random Background Color Changer

A simple JavaScript app that changes the page background to a random dark color from a predefined palette and displays the current hex code.

Built to practice arrays, randomization, DOM selection, and basic styling.

---

## Demo

The page shows:

- A title: **Random Background Color changer**
- A text line: **Hex Code: #xxxxxx**
- A **Change Background Color** button

Each click on the button:

1. Picks a random hex code from an array of dark colors.
2. Updates the page background.
3. Updates the displayed hex code.

---

## Tech Stack

- **HTML** – structure of the heading, hex display, and button.
- **CSS** – base color variables, button styling, typography.
- **JavaScript** – random color selection and DOM updates.

---

## How It Works (JavaScript Overview)

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
  const randomIndex = Math.floor(darkColorsArr.length * Math.random());
  return randomIndex;
}
darkColorsArr holds a list of dark hex color codes.

getRandomIndex() returns a random valid index into that array.

js
Copy code
const body = document.querySelector("body");
const bgHexCodeSpanElement = document.querySelector("#bg-hex-code");

function changeBackgroundColor() {
  const color = darkColorsArr[getRandomIndex()];

  bgHexCodeSpanElement.innerText = color;
  body.style.backgroundColor = color;
}

const btn = document.querySelector("#btn");
btn.onclick = changeBackgroundColor;
changeBackgroundColor() grabs a random color, updates the <span> text, and changes the body background.

The button’s onclick handler triggers this function on each click.

How to Run
Clone the repo:

bash
Copy code
git clone https://github.com/SharpSanders/random-background-changer.git
cd random-background-changer
Open the app:

Double-click index.html
or

Use VS Code’s Live Server extension.

That’s it—no build step or backend needed.

Project Structure
text
Copy code
random-background-changer/
├── index.html   # Markup for heading, hex display, and button
├── styles.css   # Color variables, button styling, basic layout
└── script.js    # Color array, random selection, DOM updates
What I Practiced
Creating and using a color palette array.

Using Math.random() and Math.floor() for random indices.

Selecting DOM elements and updating innerText and styles.

Using CSS custom properties (:root variables) for colors.

Simple UI feedback from user interaction.

Future Improvements
Show a small history of recently used colors.

Add a “Copy Hex” button to copy the current color to clipboard.

Display RGB/HSL equivalents alongside the hex code.

Add smooth transitions for background color changes.

Author
Created by Trevyn Sanders.