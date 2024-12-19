# Unnecessary Re-renders in React useEffect Hook

This repository demonstrates a common React bug involving the `useEffect` hook. The example shows how an improperly configured `useEffect` hook can lead to unnecessary re-renders and potential performance issues.

## Bug Description

The `useEffect` hook is used to perform side effects in functional components. However, if the dependency array is missing or incorrect, the effect will run on every render, causing performance problems and potentially unexpected behavior.

## Bug Solution

To fix this issue, we must correctly specify the dependency array. In this case, the effect only needs to run when the `count` state variable changes, so we add `[count]` as the dependency array.