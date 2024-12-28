# React setInterval Memory Leak
This repository demonstrates a common memory leak in React components that use `setInterval` without proper cleanup in the `useEffect` hook.  The `bug.js` file contains the buggy code, while `bugSolution.js` provides the corrected version.

## Problem
The `setInterval` function, if not handled correctly, creates a memory leak because it continues running even after the component unmounts.  This leads to unnecessary resource consumption and potential performance issues.

## Solution
The solution involves returning a cleanup function from the `useEffect` hook. This function clears the interval before the component unmounts, preventing the memory leak.
