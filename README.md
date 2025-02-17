# JavaScript Function: Unexpected Behavior with Undefined Values

This repository demonstrates a common JavaScript code error:  unhandled undefined values.  The `foo` function correctly handles `null` values, returning `null` if either input `a` or `b` is `null`. However, it lacks explicit handling for `undefined` values, leading to potential issues.

The `bug.js` file contains the buggy code. The `bugSolution.js` file provides a corrected version.

## Bug Description

The original code doesn't check for `undefined` values. Passing undefined values into the function will lead to addition of undefined with number which will result in NaN.

## Solution

The solution adds a check for `undefined` values, using the loose equality operator (`==`) to handle both `null` and `undefined` in a single condition.  This makes the function more robust and prevents unexpected results.