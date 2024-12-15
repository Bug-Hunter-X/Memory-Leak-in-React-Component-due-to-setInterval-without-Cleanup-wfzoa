# React setInterval Memory Leak
This repository demonstrates a common React bug: memory leaks caused by the improper use of `setInterval` within the `useEffect` hook without proper cleanup.

## The Bug
The `bug.js` file contains a React component that uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component unmounts, resulting in a memory leak.

## The Solution
The `bugSolution.js` file provides the corrected version.  It uses the return function of `useEffect` to clear the interval when the component unmounts, preventing memory leaks.

## How to Reproduce
1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the counter in the browser.  Notice that even after navigating away from the component, the counter continues to increase (in `bug.js`). The corrected version in `bugSolution.js` will correctly stop updating.