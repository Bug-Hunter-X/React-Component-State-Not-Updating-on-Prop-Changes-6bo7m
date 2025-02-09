# React Component State Not Updating on Prop Changes

This repository demonstrates a common error in React where a component's state fails to update correctly when props change. The issue arises from using the wrong lifecycle method to handle prop updates.

## Problem
The `MyComponent` component attempts to update its state based on the `data` prop. However, it uses `componentDidMount`, which only runs once after the initial render.  As a result, changes to the `data` prop after the initial render are not reflected in the component's state.

## Solution
The solution involves using the `componentDidUpdate` lifecycle method. This method is called after every update to the component, including prop changes. It receives the previous props as an argument, enabling a comparison to determine if an update is needed.