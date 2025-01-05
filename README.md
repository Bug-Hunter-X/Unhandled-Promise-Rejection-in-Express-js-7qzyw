# Unhandled Promise Rejection in Express.js

This repository demonstrates a common error in Node.js Express.js applications: unhandled promise rejections.  The `bug.js` file contains code with a missing error handler, leading to a silent failure. The solution (`bugSolution.js`) shows how to properly handle promise rejections.

## Problem
Asynchronous operations frequently cause errors that aren't always immediately obvious. When a promise rejects without a catch block to handle it, Node.js emits a warning to the console, but the server might not gracefully shut down. This can lead to unexpected behavior and difficult debugging.

## Solution
Always include `.catch()` blocks to handle potential errors within your promises.  Use a centralized error handler for better error logging and response management.