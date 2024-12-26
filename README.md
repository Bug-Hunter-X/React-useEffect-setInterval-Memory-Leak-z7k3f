# React useEffect setInterval Memory Leak

This repository demonstrates a common React bug involving memory leaks caused by the improper use of `setInterval` within the `useEffect` hook.  The provided code shows the faulty implementation and its solution.

## Bug
The `bug.js` file contains a React component that uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component unmounts, resulting in a memory leak.  Each render adds a new interval, leading to exponential resource consumption.

## Solution
The `bugSolution.js` file corrects this issue by incorporating a cleanup function within the `useEffect` hook. This function clears the interval when the component unmounts, preventing the memory leak.

## How to run

1. Clone this repo
2. Navigate to the directory in your terminal
3. Run `npm install`
4. Run `npm start` to view both versions in a React development server