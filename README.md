# React Native Error: Cannot read properties of undefined (reading '...')

This repository demonstrates a common React Native error where you attempt to access component state or props before the component has fully mounted.  This leads to a runtime error: `Cannot read properties of undefined (reading '...')`.

## Problem

Accessing `this.props` or `this.state` within the constructor or before the component's initial render results in undefined values.

## Solution

The solution involves accessing these properties after the component mounts, usually within the `componentDidMount` lifecycle method.  Alternatively, default values should be set for state in the constructor to prevent this error.