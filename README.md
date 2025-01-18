# React useEffect Closure Bug

This repository demonstrates a common error in React's `useEffect` hook: creating a closure that captures stale state values.

## The Bug

The `bug.js` file contains a component that attempts to log the current count value every second using `setInterval`. However, the `setInterval` callback function creates a closure over the `count` variable's initial value, meaning that it will always log '0', even as the count changes.  This is because the closure captures the value of `count` at the time the `useEffect` hook is initially called, not at the time the callback executes.

## The Solution

The `bugSolution.js` file shows how to fix this by using a functional update or referencing `count` from the current state. 

## How to run

1. Clone this repo.
2. Navigate to the directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the React app.
5. Observe the console output to see the bug and its solution in action.