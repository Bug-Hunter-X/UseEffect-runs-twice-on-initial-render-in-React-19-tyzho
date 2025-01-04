# React 19 useEffect Double-Run Bug

This repository demonstrates a bug in React 19 where the `useEffect` hook runs twice during the initial render.  This can lead to unexpected behavior and performance issues, especially when performing side effects like API calls.

## Bug Description

The `useEffect` hook, when used without dependencies, is supposed to run only once after the initial render. However, in this example, it runs twice. This is likely due to an issue with React's internal state management or optimization strategies.

## Solution

The issue is resolved by adding the dependency array in useEffect. When useEffect has an empty dependency array ([]), it's triggered only once after the initial render.