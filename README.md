## Unhandled Promise Rejections in Express.js

This repository demonstrates a common error in Express.js applications: unhandled promise rejections.  The `bug.js` file shows an Express server with an asynchronous operation that might fail.  Crucially, it lacks proper error handling, leading to silent failures.  The `bugSolution.js` file provides a corrected version with robust error handling.

**Problem:**

The original code performs an asynchronous operation using `Promise`. However, it omits the `.catch()` block to handle potential rejections. If the asynchronous operation fails, the error is silently swallowed, potentially causing the application to malfunction or return unexpected responses to clients.

**Solution:**

The solution incorporates a `.catch()` block to explicitly handle rejection. This allows for logging the error, sending appropriate error responses to the client, or implementing alternative actions to maintain application stability.

This example highlights the importance of consistent error handling, especially when dealing with asynchronous operations in Node.js and Express.js applications.