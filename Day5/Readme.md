# LeetCode 2635 — Apply Transform Over Each Element in Array  
## Step-by-Step Solution Logic and Reasoning

---

## Step 1: Understand the Goal of the Problem

The task is to implement a custom version of the array transformation behavior similar to `Array.map`, but **without using the built-in `map` method**.

We are given:
- An integer array `arr`
- A function `fn`

We must return a **new array** where each element is produced by applying `fn` to:
- the element value `arr[i]`
- the element index `i`

Formally:

```js
returnedArray[i] = fn(arr[i], i)
