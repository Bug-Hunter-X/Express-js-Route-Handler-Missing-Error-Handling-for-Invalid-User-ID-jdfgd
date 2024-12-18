# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  the lack of proper error handling when dealing with user inputs.  The example shows a route that retrieves a user by ID.  If the ID is not a valid number, the application will likely throw an error, resulting in an unexpected server response.

## Bug

The `bug.js` file contains the problematic code.  It attempts to access a user using `parseInt(userId)`, but doesn't handle the scenario where `userId` is not a valid integer. This can lead to runtime errors.

## Solution

The `bugSolution.js` file provides a corrected version. It includes error handling to check if `userId` is a valid number and returns an appropriate error response if not.