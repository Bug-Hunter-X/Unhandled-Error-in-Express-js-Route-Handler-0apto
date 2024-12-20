# Unhandled Error in Express.js Route Handler

This repository demonstrates a common error in Express.js route handlers:  lack of proper error handling for invalid input.  The `bug.js` file shows the problematic code, while `bugSolution.js` provides a corrected version.

## Problem

The original code attempts to access a user based on an ID passed as a route parameter.  However, it fails to handle cases where the ID is not a valid integer, leading to potential errors (e.g., `NaN` comparisons).  This can cause crashes or unexpected behavior in the application.

## Solution

The improved code includes comprehensive error handling:

1. **Type checking:** It verifies that the `userId` is a valid integer before attempting to use it.
2. **Error handling:** If the `userId` is invalid or the user is not found, it returns an appropriate HTTP error response with a clear message.

This ensures robustness and prevents unexpected crashes.