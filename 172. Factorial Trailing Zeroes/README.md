URL: [https://leetcode.com/problems/factorial-trailing-zeroes/](https://leetcode.com/problems/factorial-trailing-zeroes/)

# Problem

Given an integer n, return the number of trailing zeroes in n!.

**Example 1:**

    Input: 3
    Output: 0
    Explanation: 3! = 6, no trailing zero.

**Example 2:**

    Input: 5
    Output: 1
    Explanation: 5! = 120, one trailing zero.

---

# Solution

    class Solution:
        def trailingZeroes(self, n):
            """
            :type n: int
            :rtype: int
            """
            if n == 0:
                return 0
            else:
                return n//5 + self.trailingZeroes(n//5)
            #return 0 if n == 0 else n/5 + s.trailingZeroes(n/5)
        
    if __name__ == '__main__':
        s = Solution()
        n = 10
        print(s.trailingZeroes(n))

---

# Reference

URL: [https://brilliant.org/wiki/trailing-number-of-zeros/](https://brilliant.org/wiki/trailing-number-of-zeros/)
