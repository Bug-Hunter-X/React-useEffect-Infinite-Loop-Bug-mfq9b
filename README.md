# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The example shows an infinite loop caused by the absence of a dependency array in `useEffect`, leading to unnecessary re-renders and potential performance issues or unintended side-effects.

## Bug Description

The `useEffect` hook is designed to perform side effects after render. However, if it's called without a dependency array ([]), it runs after every render, creating an infinite loop. In this case, the `console.log` statement will repeatedly execute.

## How to reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs and notice the continuous output of "Effect running".

## Solution

The solution involves providing a dependency array to the `useEffect` hook. This array lists the variables that trigger the effect. In this case, we want the effect to run only when the `count` changes, thus, the dependency array is `[count]`. Refer to `bugSolution.js` for the corrected code.