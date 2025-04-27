# 📊 Count Subarrays of Length Three With a Condition

## 🧩 Problem Statement

Given an integer array `nums`, return the **number of subarrays of length 3** such that:

> **The sum of the first and third elements equals exactly half of the middle element.**

---

## ✍️ Examples

### ✅ Example 1

- **Input:** `nums = [1, 2, 1, 4, 1]`  
- **Output:** `1`  
- **Explanation:** Only the subarray `[1, 4, 1]` satisfies the condition:
  - `1 + 1 = 2`
  - `4 / 2 = 2`  
  ✅ Valid!

---

### ❌ Example 2

- **Input:** `nums = [1, 1, 1]`  
- **Output:** `0`  
- **Explanation:** Subarray `[1, 1, 1]` does **not** satisfy the condition:
  - `1 + 1 = 2`
  - `1 / 2 = 0.5`  
  ❌ Invalid

---

## 🧠 Key Points

- We're looking for **subarrays of exactly 3 elements**.
- For each subarray `[a, b, c]`, check if:

  ```js
  a + c === b / 2


/**
 * Count subarrays of length 3 where the sum of the first and third element
 * equals exactly half of the middle element.
 * 
 * @param {number[]} nums - The input array of integers
 * @return {number} - The count of valid subarrays

 */


   ```js
var countSubarrays = function(nums) {
    let count = 0;
    
    // Loop through the array, stopping 2 elements before the end
    for (let i = 0; i < nums.length - 2; i++) {
        const first = nums[i];
        const middle = nums[i + 1];
        const third = nums[i + 2];

        // Check the condition
        if (first + third === middle / 2) {
            count++;
        }
    }

    return count;
};
  ```js
