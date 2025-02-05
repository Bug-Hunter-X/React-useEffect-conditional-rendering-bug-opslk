# React useEffect Conditional Rendering Bug

This repository demonstrates a common bug in React applications involving conditional rendering within the `useEffect` hook.  The issue arises when attempting to conditionally update the document title based on component state, leading to an unexpected behavior where the title updates only when the count is incremented, but not on initial render.

## Bug Description

The `MyComponent` component uses the `useState` hook to manage a count.  A `useEffect` hook is used to update the document title whenever the count changes. However, due to an incorrect condition (`if (count > 0)`), the title update is skipped on the initial render (when the count is 0).  The title correctly updates only after the count is incremented.

## Solution

The solution involves ensuring that the title update happens even when the count is 0, by removing the unnecessary condition. This enables the immediate reflection of the count in the document title. 