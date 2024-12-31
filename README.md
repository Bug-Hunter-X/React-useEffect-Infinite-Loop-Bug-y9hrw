# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug arises from incorrectly specifying the dependency array, leading to an infinite render loop.

## Bug Description
The `useEffect` hook in the provided `MyComponent` component is missing the `count` variable in its dependency array. This causes the effect to run on every render, regardless of whether the `count` value has changed. The effect then updates the `count` variable, triggering another render, creating an infinite loop.  This leads to a poor user experience and potential application crashes.

## Bug Solution
The solution involves adding `count` to the dependency array. This ensures the effect only runs when the `count` value changes.

## How to reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the infinite loop in the console and the rapidly updating counter on the screen.