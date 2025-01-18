# React 19 useEffect Cleanup Issue

This repository demonstrates a common issue with the `useEffect` hook in React 19: the cleanup function might not always be called when expected, leading to potential memory leaks or unexpected behavior.

## Problem Description

The provided `bug.js` file shows a simple counter component.  The `useEffect` hook logs the current count and includes a cleanup function. However, under certain conditions (such as rapid component unmounting), the cleanup function might not be executed, resulting in unintended side effects.

## Solution

The `bugSolution.js` file offers a corrected version of the component. The solution addresses the issue by ensuring that the cleanup function is always called properly, even when the component unmounts before the effect has a chance to complete. This might involve more robust dependency management or improved asynchronous handling to avoid race conditions.