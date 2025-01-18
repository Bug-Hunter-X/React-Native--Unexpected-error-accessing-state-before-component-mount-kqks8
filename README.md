# React Native: Unexpected Error Accessing State Before Component Mount

This repository demonstrates a common error in React Native: attempting to access component state or props before the component has fully mounted.  This often occurs when using data fetched asynchronously within `componentDidMount` inside the render method.

## Problem

The provided `bug.js` example shows how this error manifests.  Attempting to access `this.state.data` within the `render` method before `componentDidMount` has completed the data fetch results in an error because `this.state.data` is initially `null`.

## Solution

The `bugSolution.js` file provides a solution using conditional rendering.  This approach checks if the data is available before rendering the component to avoid errors.  Alternatively, you might use a loading indicator.