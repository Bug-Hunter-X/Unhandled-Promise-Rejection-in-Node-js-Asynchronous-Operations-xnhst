# Unhandled Promise Rejection in Node.js Asynchronous Operations

This repository demonstrates a common issue in Node.js: unhandled promise rejections or uncaught exceptions within asynchronous operations.  The `bug.js` file showcases the problem, where an error in an asynchronous callback isn't caught, causing the server to crash without proper error handling.  `bugSolution.js` provides the corrected version with appropriate error handling.

## Problem

In asynchronous JavaScript, errors that occur within promises or callbacks can easily be missed, leading to cryptic crashes. The example uses `setTimeout` to mimic an asynchronous task that may fail.  If the random number generated is greater than 0.5, an error is thrown, but it's not handled, resulting in an unhandled promise rejection.

## Solution

Proper error handling is crucial.  The solution utilizes a `try...catch` block within the asynchronous operation to gracefully handle errors.  Alternatively, you could utilize `.catch()` on a Promise if applicable.  This prevents crashes and allows for logging or other appropriate actions in case of failure.