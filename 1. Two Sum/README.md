URL: https://leetcode.com/explore/featured/card/top-interview-questions-easy/92/array/546/


# Probole
    Given an array of integers, return indices of the two numbers such that they add up to a specific target.
    You may assume that each input would have exactly one solution, and you may not use the same element twice.


**Example:**

    Given nums = [2, 7, 11, 15], target = 9,
    
    Because nums[0] + nums[1] = 2 + 7 = 9,
    return [0, 1].


----------
# Solution
    class Solution:
        def twoSum(self, nums, target):
            table = {}
            for i, v in enumerate(nums):
                if target-v in table:
                    return table[target-v], i
                else:
                    table[v] = i
    
    if __name__ == '__main__':
        s = Solution()
        nums = [2,11,13,7]
        target = 9
        print(s.twoSum(nums, target))
