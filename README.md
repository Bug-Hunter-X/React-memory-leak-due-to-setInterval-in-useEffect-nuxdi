# React Memory Leak with setInterval in useEffect

This repository demonstrates a common React memory leak that occurs when using `setInterval` within the `useEffect` hook without proper cleanup.  The example shows a simple counter that increments every second.  However, because the `setInterval` is not cleared when the component unmounts, the counter continues to run, leading to a memory leak.  The solution demonstrates the correct way to use `setInterval` within `useEffect` to avoid this issue.

## Bug
The `bug.js` file contains the buggy code which uses `setInterval` without a cleanup function.  This will result in a memory leak in the React application.

## Solution
The `bugSolution.js` file presents the corrected implementation.  It uses the return value of `useEffect` to add a cleanup function that clears the `setInterval` when the component unmounts.