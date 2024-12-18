# React 18 useEffect Dependency Array Warning

This repository demonstrates a common warning encountered when upgrading to React 18 (and later) related to the `useEffect` hook's dependency array.

## The Problem

In previous React versions, omitting dependencies from the `useEffect` hook's second argument (the dependency array) might not have immediately caused issues. However, React 18 enforces stricter rules leading to warnings (and potentially unexpected behavior) if dependencies are missing.

The provided `bug.js` file showcases an example of this warning. The effect function logs the current count; however, the `count` variable isn't included in the dependency array, so the effect doesn't re-run when the count updates.