# LeetCode Problem 120 - Triangle

## 📝 Problem Description

Given a triangle array, return the minimum path sum from top to bottom.

For each step, you may move to an **adjacent number** of the row below. More formally, if you are on index `i` on the current row, you may move to either index `i` or `i + 1` on the next row.

---

### 🔍 Example 1

**Input:**
```python
triangle = [
     [2],
    [3,4],
   [6,5,7],
  [4,1,8,3]
]
Output: 11
Explanation: The path 2 → 3 → 5 → 1 gives the minimum total = 11.

🔍 Example 2
Input: triangle = [[-10]]
Output: -10

✅ Constraints
1 <= triangle.length <= 200

triangle[0].length == 1

triangle[i].length == triangle[i - 1].length + 1

-10⁴ <= triangle[i][j] <= 10⁴

💡 Approach
This problem is typically solved using Dynamic Programming (Bottom-Up):

Start from the second-last row of the triangle.

For each element, choose the minimum path from the row below.

Update the current element with the sum of its value and the minimum of its two adjacent numbers from the row below.

Continue until the top of the triangle is reached.

The result will be at triangle[0][0].

🧠 Complexity
Time Complexity: O(n²)

Space Complexity: O(1) if done in-place, or O(n) if using extra space
