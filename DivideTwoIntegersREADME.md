# leet-day5

**DivideTwoIntegers**


**Problem Description**

Given two integers, dividend and divisor, this problem requires dividing the dividend by the divisor without using multiplication, division, and mod operators. The goal is to return the quotient after dividing the dividend by the divisor, following the truncation-towards-zero rule.


**Approach**

The problem can be approached by repeatedly subtracting the divisor from the dividend until the dividend becomes less than the divisor. The number of subtractions performed will give us the quotient. We need to handle special cases like dividing by zero and overflow.


**Handle special cases:**

Check if the divisor is zero or if the dividend is equal to INT_MIN (-2^31) and the divisor is -1. Return INT_MAX (2^31 - 1) in these cases to handle divide by zero and overflow scenarios.

Get the sign of the result: Determine whether the result should be positive or negative based on the signs of the dividend and divisor.

Convert dividend and divisor to positive: Take the absolute values of the dividend and divisor to perform the division.

Perform division: Start a loop while the absolute value of the dividend is greater than or equal to the absolute value of the divisor. Within the loop, subtract the absolute value of the divisor from the absolute value of the dividend and increment a quotient variable by 1.

Apply the sign and handle overflow: Multiply the quotient by the sign obtained in step 2. If the quotient exceeds INT_MAX, return INT_MAX. Otherwise, return the quotient as the result.


_**Complexity Analysis**_

**Time complexity: **O(log(dividend)). In each iteration, we reduce the dividend by at least half.

**Space complexity:** O(1). We use constant extra space.


**Conclusion**

The "Divide Two Integers" problem can be solved efficiently using the repeated subtraction approach. By carefully handling special cases and applying truncation rules, we can obtain the correct quotient. This solution offers a time complexity of O(log(dividend)) and a space complexity of O(1).
