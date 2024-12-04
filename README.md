# JavaScript Null vs Undefined Check Error

This repository demonstrates a subtle but common error in JavaScript related to checking for null and undefined values. The example shows how using loose equality (`==`) can lead to unexpected behavior and `TypeError` exceptions when dealing with potentially undefined objects.

The `bug.js` file contains the erroneous code, while `bugSolution.js` provides the corrected implementation.

## Bug
The `foo` function attempts to handle null and undefined input. However, using `x == null` only correctly handles `null`.  When `undefined` is passed, attempting to access `x.length` results in a `TypeError` because `undefined` does not have a `length` property.

## Solution
The solution involves using strict equality (`===`) or explicitly checking for both null and undefined using the `||` operator to avoid the type error.