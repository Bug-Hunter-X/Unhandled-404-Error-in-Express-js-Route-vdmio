# Unhandled 404 Error in Express.js Route

This repository demonstrates a common error in Express.js applications: failing to handle the case where a requested resource (in this case, a user) is not found.  The bug.js file shows the problematic code, and the bugSolution.js file provides a corrected version.

## Bug Description

The original code attempts to fetch a user from a database based on an ID passed as a route parameter.  However, it lacks proper error handling when a user with the specified ID does not exist.  This results in an unhandled 404 error, which is not ideal for a production application.

## Solution

The solution adds a check to see if the user is found before attempting to send the response. If the user is not found, it returns a 404 status code with an appropriate message.