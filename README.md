# Sudoku Solver in C

This project is a simple Sudoku solver implemented in C. The program takes a partially filled 9x9 grid of Sudoku and attempts to solve it using a backtracking algorithm.

## How It Works

The Sudoku solver works by:
1. Checking each empty cell in the grid.
2. Trying all possible numbers from 1 to 9.
3. Checking if placing a number in the cell is valid using the `isSafe` function, which ensures the number doesn't violate the Sudoku rules:
   - The number isn't already in the current row.
   - The number isn't already in the current column.
   - The number isn't already in the current 3x3 subgrid.
4. Recursively attempting to solve the grid with the current placement.
5. Backtracking if no valid number can be placed in a cell.

The algorithm continues until the entire grid is filled or no solution is found.

## Files

- `sudoku_solver.c`: Contains the implementation of the Sudoku solver.
- `README.md`: This file, providing an overview of the project.

## How to Run

1. Compile the code using a C compiler, for example:
    ```sh
    gcc -o sudoku_solver sudoku_solver.c
    ```
2. Run the executable:
    ```sh
    ./sudoku_solver
    ```

The program will print the solved Sudoku grid if a solution exists, or indicate that no solution exists.

## Example

Given the following grid:
