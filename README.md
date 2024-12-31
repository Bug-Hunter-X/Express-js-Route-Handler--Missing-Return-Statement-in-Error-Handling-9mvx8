# Express.js Route Handler: Missing Return Statement

This repository demonstrates a common error in Express.js route handlers: a missing `return` statement within an error-handling `if` block.

## Bug Description

The `bug.js` file contains a route handler that fetches user data based on an ID. If the user is not found, it sends a 'User not found' message with a 404 status. However, the `if` statement handling the not-found case is missing a `return` statement. This means that even if the user is not found, the code continues to execute, potentially sending an additional response or causing unexpected behavior.

## Bug Solution

The `bugSolution.js` file demonstrates the corrected code. The addition of the `return` keyword ensures that if the user is not found, no further code in the handler is executed, and only the 404 response is sent.