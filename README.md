# React Router v6 Catch-All Route Issue

This repository demonstrates a subtle issue with catch-all routes (`*`) in React Router v6 when they are nested within other routes.  The issue arises when a catch-all route is placed after a more specific route.  This can lead to unexpected routing behavior, as the catch-all route may not always correctly handle URLs that do not match any previous routes.

## Reproduction Steps
1. Clone the repository.
2. Run `npm install`.
3. Run `npm start`.
4. Navigate to the `/` route. This works correctly. 
5. Navigate to the `/about` route. This also works correctly. 
6. Navigate to a non-existent route like `/random`. This might not work as expected, showcasing the bug. 
7. Run the bugSolution.js file to see the correct implementation

## Solution
The solution involves placing the catch-all route as the first route. This ensures that it handles any unmatched URLs correctly.