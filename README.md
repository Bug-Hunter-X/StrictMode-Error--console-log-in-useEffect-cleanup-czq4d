# React 19 StrictMode useEffect Cleanup Error

This repository demonstrates a common error encountered when using `console.log` within the cleanup function of a `useEffect` hook in React 19 StrictMode.  StrictMode enforces stricter rules and can reveal subtle issues that might not be apparent in a regular environment.

The `bug.js` file contains the problematic code.  The `bugSolution.js` file provides a solution.

## Problem

Using `console.log` (or other side effects) inside the cleanup function of `useEffect` can trigger warnings or errors in StrictMode.  This is because the cleanup function is intended for resource management and not for side effects.

## Solution

The solution involves removing the side effects (like `console.log`) from the cleanup function. If logging is required, perform it before the return statement of the `useEffect`.