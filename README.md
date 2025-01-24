# Express.js Route Handler Bug: Missing Error Handling

This repository demonstrates a common bug in Express.js route handlers: missing error handling for invalid input.  Specifically, the `/users/:id` route attempts to parse the `id` parameter as an integer without checking for potential errors (e.g., if the ID is not a number or is not found).  This can result in unexpected behavior or even crashes.

The `bug.js` file contains the buggy code.  The `bugSolution.js` file provides a corrected version with proper error handling.

## How to Reproduce

1. Clone this repository.
2. Run `npm install express` to install the necessary dependencies.
3. Run `node bug.js`.
4. Make requests to `/users/:id` with various values of `id` (including non-numeric values) to observe the behavior.  Then compare with the solution.

## Solution

The solution involves adding error handling to check if the `id` parameter is a valid integer and to handle the case where the user is not found.