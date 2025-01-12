# React useEffect Infinite Render Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook causing an infinite render loop.  The problem arises from omitting the dependency array in `useEffect`, leading to the effect running after every render, triggering a cycle of re-renders.

## Bug Description
The provided `MyComponent` uses `useEffect` to log a message on every render. Without a dependency array, the effect runs repeatedly, causing the component to re-render endlessly. This leads to performance problems and potentially crashes the application.

## Solution
The solution involves adding a dependency array to the `useEffect` hook. This ensures the effect only runs when the specified dependencies change.

## How to reproduce the bug
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`. Observe the console log and browser performance.

## How to fix the bug
1. Replace the buggy `useEffect` with the corrected version in `bugSolution.js`.
2. Rerun `npm start` and observe the improved behavior. 