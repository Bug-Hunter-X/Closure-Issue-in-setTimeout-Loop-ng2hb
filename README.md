# Closure Issue in setTimeout Loop

This repository demonstrates a common closure issue in JavaScript when using `setTimeout` within a loop.  The expected behavior is to print numbers 0 through 9 with a one-second delay between each. However, due to the way closures work in JavaScript, the loop completes before the `setTimeout` callbacks execute, resulting in the same value of `i` (10) being printed repeatedly.

## Bug
The `bug.js` file contains the problematic code.  Run this file to see the unexpected output.

## Solution
The `bugSolution.js` file demonstrates the solution which involves using an immediately invoked function expression (IIFE) to create a new scope for each iteration of the loop, ensuring each `setTimeout` callback captures the correct value of `i`.

This example highlights the importance of understanding how closures and asynchronous operations interact in JavaScript.