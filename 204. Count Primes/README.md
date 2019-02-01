# Problem

URL: [https://leetcode.com/problems/count-primes/](https://leetcode.com/problems/count-primes/)

Count the number of prime numbers less than a non-negative number, **n**.

**Example:**

    Input: 10
    Output: 4
    Explanation: There are 4 prime numbers less than 10, they are 2, 3, 5, 7.

---

# Solution

    class Solution:
        def countPrime(self, n):
            """
            :type n: int
            :rtype: int
            """
            a = [False, False] + [True]*(n-1)
            primes = []           
            for i in range(2,n):
                if a[i]:
                    primes.append(i)
                for j in range(2*i, n+1, i):
                    a[j] = False
            return len(primes)
            
    if __name__ == '__main__':
        s = Solution()
        n = 10
        print(s.countPrime(n))
