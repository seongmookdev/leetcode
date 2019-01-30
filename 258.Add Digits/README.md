URL: [https://leetcode.com/problems/add-digits/](https://leetcode.com/problems/add-digits/)

# Problem

Given a non-negative integer `num`, repeatedly add all its digits until the result has only one digit.

**Example:**

    Input: 38
    Output: 2 
    Explanation: The process is like: 3 + 8 = 11, 1 + 1 = 2. 
                 Since 2 has only one digit, return it.

**Follow up:**Could you do it without any loop/recursion in O(1) runtime?

---

# Solution

    class Solution:
        def addDigits(self,num):
            """
            :type num: int
            :rtype: int
            """
            if num == 0:
                return 0
			else:
                return (num-1)%9 + 1
            
    if __name__ == '__main__':
        s = Solution()
        num = 38
        print(s.addDigits(num))

---

# Reference

URL: [https://en.wikipedia.org/wiki/Digital_root](https://en.wikipedia.org/wiki/Digital_root)
