# Simple Windows Forms Calculator
<img src="https://github.com/user-attachments/assets/3ac14f99-f8f5-41e7-9bd5-f578db91cc0e" width="500" />

## Description
This project is a simple calculator application built using C# and Windows Forms. It allows users to perform basic arithmetic operations such as addition, subtraction, multiplication, and division. The calculator interface consists of buttons for digits, operations, and the "Equal" button to calculate the result.

## Features
- Basic arithmetic operations: addition, subtraction, multiplication, and division.
- Supports decimal point input.
- Displays the calculation in a readable format.
- Clear button to reset the calculation.

## Getting Started

### Prerequisites
To run this project, you need to have:
- Visual Studio installed with support for Windows Forms applications.
- .NET Framework (recommended version: 4.7.2 or above).

### How to Run the Project
1. Open the project in Visual Studio.
2. Build the solution (Press `Ctrl + Shift + B`).
3. Run the application by pressing `F5` or clicking the `Start` button.

### Code Structure

- `calculator.cs` - The main form for the calculator. Contains event handlers for the buttons and logic for performing calculations.

### Button Click Events

#### `ButtonDigit_Click`
Handles the input of digits and decimal points. If the user starts a new calculation, the text box is cleared before entering the digit.

#### `ButtonClear_Click`
Clears the `caTextBox` and resets the calculation. It also clears the operation label.

#### `ButtonOpenration_Click`
Stores the current value (`x`) and the selected operation in `pendingOperation`. The textbox is cleared to allow entering the second value.

#### `ButtonEqual_Click`
Performs the calculation based on the selected operation and displays the result in the `caTextBox`. It updates the display label with the full equation and result.

## How It Works

The calculator works by:
1. Storing the first number (`x`) when an operation button is clicked.
2. Allowing the user to input the second number (`y`).
3. Using the `ButtonEqual_Click` event to perform the operation and display the result.

### Example Usage
- Click `5`, then `+`, then `3`, and finally `=`. The result `8` will be displayed.
- Click `7`, then `/`, then `0`, and finally `=`. The display will show an error message indicating "Cannot divide by zero".

## Enhancements
- Error handling for division by zero.
- Option to handle negative numbers.
- Option to use keyboard input for digits and operators.
