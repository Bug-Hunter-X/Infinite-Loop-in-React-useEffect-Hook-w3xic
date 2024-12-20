# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The `useEffect` hook, without a proper dependency array, leads to an infinite loop, causing performance issues and application crashes. This example showcases the problem and provides a solution.

## Bug Description

The `MyComponent` uses `useEffect` to log the current count.  However, the dependency array is missing. As a result, the effect runs after every render because `count` changes on every click.  This creates an infinite loop where the component renders, the effect runs, triggering a re-render, and so on.

## Solution

The solution involves adding the `count` variable to the dependency array. Now, the effect runs only when the `count` value changes.