# 2634. Filter Elements from Array

## 📌 Problem Overview

This problem requires implementing a custom version of JavaScript’s `Array.filter()` method **without using the built-in `filter` function**.

You are given:
- An integer array `arr`
- A function `fn` that returns a **truthy or falsy value**

Your task is to return a new array containing **only the elements** for which `fn(arr[i], i)` evaluates to `true`.

---

## ✅ Key Rules

- Do **not** use `Array.filter`
- `fn` can take:
  - One argument → the element
  - Two arguments → the element and its index
- Only values where `Boolean(fn(...)) === true` should be kept

---

## 🧠 Approach & Logic

We solve this problem by **manually iterating** through the array and applying the filtering logic ourselves.

### Step-by-Step Breakdown

1. **Create an empty array**
   - This will store elements that pass the filter condition.

2. **Loop through the input array**
   - Use a `for` loop to access each element and its index.

3. **Apply the filtering function**
   - Call `fn(arr[i], i)` for each element.

4. **Check for truthy values**
   - If the function returns a truthy value, include the element.

5. **Push valid elements**
   - Add the element to the result array.

6. **Return the filtered array**
   - Once iteration is complete, return the new array.

---

## 🧪 Implementation

```js
/**
 * @param {number[]} arr
 * @param {Function} fn
 * @return {number[]}
 */
var filter = function(arr, fn) {
    const filteredArr = [];

    for (let i = 0; i < arr.length; i++) {
        if (fn(arr[i], i)) {
            filteredArr.push(arr[i]);
        }
    }

    return filteredArr;
};
