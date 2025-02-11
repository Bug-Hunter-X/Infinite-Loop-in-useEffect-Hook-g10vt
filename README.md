# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook. The bug arises from an incorrectly configured dependency array, leading to an infinite render loop.

## Bug Description

The `useEffect` hook is used to perform side effects after a component renders. In this example, the effect logs the current `count` to the console. However, if the dependency array is missing or incorrect, the effect will run on every render, creating an infinite loop.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console output, and you'll see the infinite loop.

## Solution

The solution is to properly specify the dependencies in the dependency array.  By only including `count` the effect only runs when the `count` variable changes.  This fixes the infinite loop.