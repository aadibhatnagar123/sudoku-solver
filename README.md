Sudoku Solver using Dancing Links and Algorithm X
This project is a high-performance C++ implementation designed to solve complex Sudoku puzzles. Unlike standard recursive solvers that can be slow on difficult grids, this application utilizes a specialized mathematical approach known as the Exact Cover problem to find solutions with maximum efficiency.

Core Logic and Methodology
The solver is built around Donald Knuth's Algorithm X, implemented through the Dancing Links (DLX) technique. This method is highly effective for Sudoku because it treats the game as a series of constraints rather than just a grid of numbers.

The program manages four specific constraints for every puzzle:

Cell Constraint: Each of the 81 cells must contain exactly one digit.

Row Constraint: Each row must contain the digits 1 through 9 exactly once.

Column Constraint: Each column must contain the digits 1 through 9 exactly once.

Block Constraint: Each 3x3 sub-grid must contain the digits 1 through 9 exactly once.

By converting these rules into a sparse matrix, the solver can quickly eliminate impossible options, reaching the correct solution much faster than a standard "guess-and-check" method.

Technical Implementation
Language: C++

Data Structure: The project uses a toroidal (donut-shaped) doubly linked list. This allows the program to "cover" and "uncover" rows and columns in the data matrix in constant time, which is the secret to its speed.

Memory Management: This implementation avoids the C++ Standard Template Library (STL) in favor of manual pointer manipulation. This reduces memory overhead and ensures the solver can run on systems with limited resources.

Usage Instructions
Compilation

To build the application from the source code, use a C++ compiler such as g++: g++ -o sudoku_solver sudoku.cpp

Execution

Run the compiled program using the following command: ./sudoku_solver

Input Format

The program expects a 9x9 grid where empty cells are represented by the digit 0. Once the input is provided, the solver will display the completed grid or notify the user if the puzzle is mathematically unsolvable.

Author
Aditya Bhatnagar 
Software Developer interested in Algorithmic Optimization and Data Structures.