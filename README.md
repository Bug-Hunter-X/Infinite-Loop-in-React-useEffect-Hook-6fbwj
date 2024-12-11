# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications: an infinite loop caused by an incorrectly used `useEffect` hook.  The `useEffect` hook, while powerful, requires careful consideration of its dependencies.  Failure to include relevant state variables in the dependency array can lead to unintended and infinite re-renders.

## Bug Description

The provided `bug.js` file contains a `MyComponent` that uses `useEffect` to log the current count. However, the dependency array is missing `count`.  This leads to an infinite loop because the effect triggers after every render, causing a continuous update cycle.

## Solution

The `bugSolution.js` provides the corrected component.  By adding `count` to the dependency array, `useEffect` only runs when the `count` value changes.