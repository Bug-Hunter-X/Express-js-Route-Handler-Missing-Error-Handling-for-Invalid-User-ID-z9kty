# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling for invalid input.  Specifically, the route `/users/:id` fails to handle cases where `:id` is not a valid integer.

## Bug

The `bug.js` file contains an Express.js route handler that fetches a user based on their ID.  It attempts to parse the ID as an integer using `parseInt()`, but doesn't handle potential errors if the ID is not a valid number. This can lead to unexpected behavior or crashes.

## Solution

The `bugSolution.js` file shows the corrected version of the route handler.  It includes checks to ensure the ID is a valid integer before attempting to find the user.  If the ID is invalid, it returns an appropriate error response.