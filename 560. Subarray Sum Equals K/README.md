URL: [https://leetcode.com/problems/subarray-sum-equals-k/](https://leetcode.com/problems/subarray-sum-equals-k/)

---

# Problem

Given an array of integers and an integer **k**, you need to find the total number of continuous subarrays whose sum equals to **k**.

**Example 1:**

    Input:nums = [1,1,1], k = 2
    Output: 2

**Note:**

1. The length of the array is in range [1, 20,000].
2. The range of numbers in the array is [-1000, 1000] and the range of the integer **k** is [-1e7, 1e7].

---

# Solution

    class Solution:
        def subarraySum(self, nums: 'List[int]', k: 'int') -> 'int':
            count, cur, res = {0:1}, 0, 0
            for v in nums:
                cur += v
                res += count.get(cur-k, 0)
                count[cur] = count.get(cur,0)+1
            return res
        
    if __name__ == '__main__':
        s = Solution()
        print(s.subarraySum([1,2,1,2,1],3))
