# LEETCODE-Arrays-717
---

# 🧪 **Dry Runs**

---

## **Example 1**

### Input:

```
bits = [1, 0, 0]
```

### Step-by-step:

* n = 3
* Start at index **1** (`n-2`):

| i | bits[i] | condition (i>=0 && bits[i]==1)? | count1 |
| - | ------- | ------------------------------- | ------ |
| 1 | 0       | NO → loop stops                 | 0      |

* count1 = 0 → even
  **Return true**

---

## **Example 2**

### Input:

```
bits = [1, 1, 0]
```

### Step-by-step:

Start at index **1**:

| i | bits[i] | condition met? | count1 |
| - | ------- | -------------- | ------ |
| 1 | 1       | YES            | 1      |
| 0 | 1       | YES            | 2      |
| - | stop    | loop ends      |        |

* count1 = 2 → even
  **Return true**

---

## **Example 3**

### Input:

```
bits = [1, 1, 1, 0]
```

### Step-by-step:

Start at index **2**:

| i | bits[i] | condition? | count1 |
| - | ------- | ---------- | ------ |
| 2 | 1       | YES        | 1      |
| 1 | 1       | YES        | 2      |
| 0 | 1       | YES        | 3      |
| - | stop    |            |        |

* count1 = 3 → odd
  **Return false**

---

## **Example 4** (Edge case)

### Input:

```
bits = [1, 0]
```

Start at index **0**:

| i | bits[i]   | condition? | count1 |
| - | --------- | ---------- | ------ |
| 0 | 1         | YES        | 1      |
| - | loop ends |            |        |

* count1 = 1 → odd
  **Return false**

(Correct: `[1,0]` represents a 2-bit char, not a single 0 at end)

---

# 🎯 Final Understanding

Your logic checks how many **trailing 1s** appear before the final 0.

* **Even number of trailing 1s → last is 1-bit**
* **Odd number of trailing 1s → last is part of a 2-bit character**

The dry run matches the intended logic of the problem.

---
