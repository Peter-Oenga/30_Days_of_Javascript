# Counter Function Using Closures (JavaScript)

## Problem Overview

This project implements a solution to **LeetCode Problem 2620 – Counter**.

### Problem Statement

Given an integer `n`, return a **counter function**.  
Each time the counter function is called:

- The **first call** returns `n`
- Every **subsequent call** returns the previous value plus `1`

#### Example

```js
const counter = createCounter(10);
counter(); // 10
counter(); // 11
counter(); // 12
