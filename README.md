# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook causing an infinite render loop. The bug occurs when the `useEffect` hook doesn't specify a dependency array correctly, causing the effect to run after every render.

## Bug Description

The `MyComponent` component uses the `useEffect` hook to log the current count to the console. However, because the dependency array is omitted, the effect runs after every render, leading to an infinite loop of logging and re-renders. The solution is to include the `count` state variable in the dependency array to prevent this unwanted behavior.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Open your browser and observe the infinite console logging.

## Solution

The `bugSolution.js` file shows the corrected code where `count` is included in the dependency array of `useEffect`. This ensures that the effect only runs when the `count` variable changes. This prevents the infinite render loop, addressing the bug.
