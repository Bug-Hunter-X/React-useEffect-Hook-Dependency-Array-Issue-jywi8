# React useEffect Hook Dependency Array Issue
This repository demonstrates a common issue with the React `useEffect` hook: forgetting to include all variables used within the effect in its dependency array.  This can lead to unexpected behavior, such as infinite loops or stale closures.

The `bug.js` file shows the problematic code, where the `count` variable is accessed within the effect but not listed in the dependency array. This causes the effect to run on every render, potentially leading to performance issues or unexpected side effects. 

The `bugSolution.js` file provides the corrected code, where `count` is correctly added to the dependency array.  The effect now only runs when the `count` value changes.

This example highlights the importance of carefully managing dependencies in the `useEffect` hook to ensure predictable and efficient React components.