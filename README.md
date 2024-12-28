# React Native AsyncStorage: Accessing Value Before Retrieval

This repository demonstrates a common error when working with AsyncStorage in React Native: attempting to access a value before it has been fully retrieved from storage. This often leads to cryptic errors like `undefined is not an object` (evaluating '_this2.state.someValue') or similar.

## Problem

The issue stems from the asynchronous nature of AsyncStorage.  Getting a value takes time, and if you try to use it immediately after calling `getItem`, the value might still be undefined, leading to the error.

## Solution

The solution is to properly handle the asynchronous operation using `async/await` or promises, ensuring that you access the value only after it has been successfully retrieved.  Error handling is also crucial to gracefully manage potential issues.

## Usage

Clone this repository and run the example projects (`AsyncStorageBug.js` and `AsyncStorageSolution.js`) to see the problem and the solution in action.  You'll need to have a React Native development environment set up.