## Pyramid Generator (Console Application)

This JavaScript code generates a pyramid pattern using a specified character and count. The output is displayed in the console.

### Table of Contents

- [Project Description](#project-description)
- [Features](#features)
- [How to Use](#how-to-use)
- [Technologies Used](#technologies-used)
- [Customization](#customization)

### Project Description

This JavaScript code generates a pyramid pattern using a predefined character ("!") and a fixed height (10 rows). The output is displayed directly in the browser's console. This project demonstrates fundamental JavaScript concepts like loops and string manipulation.

### Features

- Generates a pyramid pattern using the "!" character.
- The pyramid's height is determined by the `count` variable (currently set to 10).
- The output is displayed in the console.
- The pyramid is generated in a normal or inverted state, determined by the `inverted` variable.

### How to Use

1. Open your browser's developer console (usually by pressing F12 or right-clicking and selecting "Inspect").
2. Paste the code into the console.
3. Press Enter.
4. The pyramid pattern will be displayed in the console.

### Technologies Used

- JavaScript

### Customization

* To change the character used in the pyramid, modify the `character` variable.
* To change the height of the pyramid, modify the `count` variable.
* To invert the pyramid, set the `inverted` variable to `true`.

### Code

```javascript
const character = "!";
const count = 10;
const rows = [];
let inverted = false;

function padRow(rowNumber, rowCount) {
  return " ".repeat(rowCount - rowNumber) + character.repeat(2 * rowNumber - 1) + " ".repeat(rowCount - rowNumber);
}

for (let i = 1; i <= count; i++) {
  if (inverted) {
    rows.unshift(padRow(i, count));
  } else {
    rows.push(padRow(i, count));
  }
}

let result = "";

for (const row of rows) {
  result = result + row + "\n";
}

console.log(result);