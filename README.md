# Unexpected Null Handling in JavaScript Addition Function

This repository demonstrates a common, yet subtle, bug in JavaScript related to null value handling during addition. The `foo` function is intended to add two numbers, but its handling of null inputs leads to unexpected behavior.  The bug is in how null values are handled when either 'a' or 'b' is null; it returns null instead of potentially handling those nulls as zeros.

## How to Reproduce

1. Clone the repository.
2. Open `bug.js` and examine the code.
3. Run the script using Node.js (or your preferred JavaScript runtime).
4. Observe the unexpected results of `foo(null,2)`, `foo(1,null)` and `foo(null,null)`

## Solution

The `bugSolution.js` file contains corrected code.  The solution involves explicitly checking for and handling null values before attempting the addition, converting them to 0 if necessary.

## Lessons Learned

This example highlights the importance of carefully handling null or undefined values in your JavaScript code, to avoid unexpected behaviors and potential errors in your application. Always consider the edge cases and potential inputs for your functions and handle them gracefully.