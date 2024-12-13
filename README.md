# React Native useCallback Stale Closures

This repository demonstrates a common, yet subtle, bug in React Native when using the `useCallback` hook. The issue arises from incorrect dependency handling, resulting in stale closures and unexpected behavior.  The bug involves a counter that fails to increment correctly due to a new memoized function being created with each state update, rather than re-using an existing function.

The `bug.js` file shows the buggy implementation. The `bugSolution.js` demonstrates how to resolve this by removing the state variable from the dependency array.