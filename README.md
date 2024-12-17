# React useEffect Hook Missing Cleanup Function

This repository demonstrates a common error in React applications: forgetting to include a cleanup function within the `useEffect` hook.  This can lead to memory leaks and unexpected behavior when components unmount.

## The Bug

The `bug.js` file shows an example of an `useEffect` hook without a return statement. When the component unmounts, any cleanup actions (such as event listeners, subscriptions, or timers) associated with the effect will not be properly cleaned up, potentially leading to resource leaks.

## The Solution

The `bugSolution.js` file demonstrates the corrected version, including a return statement to define the cleanup function. This ensures that the effect is properly cleaned up when the component unmounts.

## How to reproduce
1. Clone this repository.
2. Open the `bug.js` file.
3. Observe that the component does not clean up properly.
4. Open the `bugSolution.js` file. Notice the added `return` statement and how this handles unmounting correctly.
