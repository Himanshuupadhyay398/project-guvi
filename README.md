# Sudoku Solver

This project is a browser-based Sudoku solver that dynamically generates a 9x9 grid where users can input a Sudoku puzzle. It uses a backtracking algorithm implemented in JavaScript to solve the puzzle and display the solution.

---

## Features
- **Dynamic Sudoku Grid**: A 9x9 grid is dynamically created using JavaScript.
- **Input Validation**: Accepts numbers (1-9) as input, leaving blank cells as zeros in the backend.
- **Backtracking Solver**: Uses a recursive algorithm to solve the Sudoku puzzle.
- **User Interaction**: Allows users to input their puzzle, solve it with a button click, and displays the result.

---

## File Structure
1. **index.html**: 
   - Contains the structure of the webpage and the "Solve" button to trigger the solving process.
2. **style.css**:
   - Styles the Sudoku grid and input fields.
3. **script.js**:
   - Implements the logic for grid generation, validation, and solving.

---

## How to Use
1. Clone the repository or download the files.
2. Open `index.html` in any modern browser.
3. Enter the Sudoku puzzle row by row:
   - Use numbers `1-9` for filled cells.
   - Leave empty cells blank.
4. Click the **Solve** button to solve the puzzle.
5. If the solution exists, it will populate the grid. Otherwise, you'll see an alert indicating that no solution exists.

---

## Code Overview

### 1. **Grid Initialization**
The grid is generated dynamically with JavaScript:
```javascript
document.addEventListener("DOMContentLoaded", () => {
    const grid = document.getElementById("sudoku-grid");
    for (let i = 0; i < 81; i++) {
        const input = document.createElement("input");
        input.type = "text";
        input.maxLength = 1;
        grid.appendChild(input);
    }
});
