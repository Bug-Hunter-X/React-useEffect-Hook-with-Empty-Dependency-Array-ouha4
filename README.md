# React useEffect Hook with Empty Dependency Array

This repository demonstrates a common mistake when using the `useEffect` hook in React: using an empty dependency array (`[]`) when you actually need the component to re-render on state changes. This can lead to unexpected behavior, where side effects only run once, even when the state changes.

## Problem

The `MyComponent` function uses `useEffect` with an empty dependency array.  The `console.log` statement only runs once on the initial render.  It won't run again when the button is clicked and the `count` state updates.

## Solution

The solution is to include the relevant state variable(s) in the dependency array. In this case, `count` should be included so the effect runs after each update of `count`.

## How to reproduce the bug

1. Clone the repository
2. Run `npm install`
3. Run `npm start`
4. Click the button multiple times. Observe that the console only logs the message once.
