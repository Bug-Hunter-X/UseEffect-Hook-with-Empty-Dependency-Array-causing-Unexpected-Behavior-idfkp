# React useEffect Hook Issue

This repository demonstrates a common issue with the React `useEffect` hook: using an empty dependency array (`[]`) when you intend for the effect to run on every state change.  This results in the effect only executing once when the component mounts. The solution provides the correct way to handle this using the state variable as a dependency.

## Bug

The original `MyComponent`'s `useEffect` hook only logs the count once, when the component initially renders. Subsequent clicks to increment the count don't trigger the effect, resulting in incorrect behavior if the side effect requires updated state information.