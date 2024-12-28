# Infinite useEffect Loop in React

This repository demonstrates a common error in React applications involving the `useEffect` hook: creating an infinite loop.  The example shows how a seemingly simple counter component can cause performance problems if the dependency array is not correctly specified.

## The Problem

The provided `bug.js` file contains a functional component that uses `useState` and `useEffect` to track and display a click counter.  However, the `useEffect` hook is missing a crucial dependency array or has an incorrect one, resulting in an infinite render loop.

## The Solution

The solution, found in `bugSolution.js`, addresses this by correctly specifying the dependency array for the `useEffect` hook. By including `count` in the dependency array, the effect only runs when the value of `count` changes, preventing the infinite loop.