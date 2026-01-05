# LeetCode 2665 — Counter II  
## Step-by-Step Solution Logic and Reasoning

---

## Step 1: Understand the Required Output

The function `createCounter(init)` must return **an object**, not a single value.  
This object must expose exactly **three methods**:

- `increment()`
- `decrement()`
- `reset()`

Each method must:
- Update the counter value
- Return the updated value immediately

---

## Step 2: Identify the State That Must Be Preserved

Two pieces of data must persist across multiple method calls:

- `init` → the original starting value
- `current` → the changing counter value

These values must:
- Be accessible to all three methods
- Not be directly accessible from outside the counter

---

## Step 3: Choose a Mechanism to Preserve State

To preserve state between calls, the solution uses a **closure**.

- `current` is declared inside `createCounter`
- The returned methods are defined inside the same scope
- The methods retain access to `current` and `init` even after `createCounter` finishes executing

---

## Step 4: Initialize the Counter State

Inside `createCounter`:

- Assign `current = init`
- This ensures the counter starts at the correct value

```js
let current = init;
