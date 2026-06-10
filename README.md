# LeetCode 217 - Contains Duplicate

## Problem

Given an integer array `nums`, return `true` if any value appears at least twice in the array, and return `false` if every element is distinct.

### Example 1

**Input**
```text
nums = [1,2,3,1]
```

**Output**
```text
true
```

### Example 2

**Input**
```text
nums = [1,2,3,4]
```

**Output**
```text
false
```

---

## Approach

We use an `unordered_set` to store the elements encountered while traversing the array.

- If an element is already present in the set, a duplicate exists.
- Return `true` immediately.
- Otherwise, insert the element into the set.
- If the traversal finishes without finding duplicates, return `false`.

This approach provides efficient lookup and insertion operations.

---

## C++ Solution

```cpp
class Solution {
public:
    bool containsDuplicate(vector<int>& nums) {
        unordered_set<int> st;

        for (int num : nums) {
            if (st.find(num) != st.end()) {
                return true;
            }
            st.insert(num);
        }

        return false;
    }
};
```

---

## Complexity Analysis

| Complexity | Value |
|------------|--------|
| Time Complexity | O(n) |
| Space Complexity | O(n) |

---

## Key Concepts

- Array Traversal
- Hashing
- Unordered Set
- Duplicate Detection

---

## Repository Structure

```text
leetcode-217-contains-duplicate/
│
├── README.md
└── solution.cpp
```

---

## Author

Ranjith

Solved as part of the LeetCode problem-solving journey.
