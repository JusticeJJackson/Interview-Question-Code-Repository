# Collatz Conjecture

# Note, this is a mutli-part problem.  Please read the entire problem before starting.
Code it out, then do it recursively and iteratively, add memorization to prevent duplicated work

## Problem Statement

Given a positive integer `n`, the task is to find whether this number reaches `1` after performing the following two operations:

1. If `n` is even, then `n = n/2`.
2. If `n` is odd, then n = `3*n + 1`.
3. Repeat the above steps, until it becomes `1`.

## Example 1:

Input:

`n = 12`

Output:

`12, 6, 3, 10, 5, 16, 8, 4, 2, 1`

## Java Starter Code

```java

/**
 * Problem Statement:
 * Given a positive integer n, the task is to find whether this number reaches 1
 * after performing the following two operations:
 * - If n is even, then n = n/2.
 * - If n is odd, then n = 3*n + 1.
 * Repeat the above steps, until it becomes 1.
 *
 * Example:
 * Input:
 * n = 12
 * Output:
 * 12, 6, 3, 10, 5, 16, 8, 4, 2, 1
 */

public class Solution{

    // Method to calculate the number of steps required to reach 1
    // Iteratively
    public static int collatz1(int n) {
        // Implementation here
        return -1;
    }
    // Recursively
    public static int collatz2(int n) {
        // Implementation here
        return -1;
    }
    // With added memorization 
    public static int collatz3(int n) {
        // Implementation here
        return -1;
    }
    // find the maximum number in the collatz sequence recursively
    public static int collatz4(int n) {
        // Implementation here
        return -1;
    }

    public static void main(String[] args) {
        // Test cases
        int[][] testCases = {
            {6, 8, 16},
            {27, 111, 9232},
            {1, 0,1}
            // Add more test cases if needed
        };

        for (int i = 0; i < testCases.length; i++) {
            int inputNum = testCases[i][0];
            int expectedOutput = testCases[i][1];
            int maxOutput = testCases[i][2];

            // Testing collatz1
            int result1 = collatz1(inputNum);
            if (result1 == expectedOutput) {
                System.out.println("Test case " + (i + 1) + " for collatz1 PASSED");
            } else {
                System.out.println("Test case " + (i + 1) + " for collatz1 FAILED. Expected " + expectedOutput + ", but got " + result1);
            }

            // Testing collatz2
            int result2 = collatz2(inputNum);
            if (result2 == expectedOutput) {
                System.out.println("Test case " + (i + 1) + " for collatz2 PASSED");
            } else {
                System.out.println("Test case " + (i + 1) + " for collatz2 FAILED. Expected " + expectedOutput + ", but got " + result2);
            }

            // Testing collatz3
            int result3 = collatz3(inputNum);
            if (result3 == expectedOutput) {
                System.out.println("Test case " + (i + 1) + " for collatz3 PASSED");
            } else {
                System.out.println("Test case " + (i + 1) + " for collatz3 FAILED. Expected " + expectedOutput + ", but got " + result3);
            }

            // Testing collatz4
            int result4 = collatz4(inputNum);
            if (result4 == maxOutput) {
                System.out.println("Test case " + (i + 1) + " for collatz4 PASSED");
            } else {
                System.out.println("Test case " + (i + 1) + " for collatz4 FAILED. Expected " + expectedOutput + ", but got " + result4);
            }
        }
    }
}

```

## Python Starter Code

```python
"""
Problem Statement:
Given a positive integer n, the task is to find whether this number reaches 1
after performing the following two operations:
- If n is even, then n = n/2.
- If n is odd, then n = 3*n + 1.
Repeat the above steps, until it becomes 1.

Example:
Input:
n = 12
Output:
12, 6, 3, 10, 5, 16, 8, 4, 2, 1
"""

# Implement Collatz Conjecture here
def collatz_conjecture(n):
    """
    This function takes an integer n as input and applies the Collatz Conjecture
    until it reaches 1. The number of steps taken to reach 1 is returned.
    """
    return None
def collatz_conjecture_recursive(n):
    """
    This function takes an integer n as input and applies the Collatz Conjecture
    until it reaches 1. The number of steps taken to reach 1 is returned.
    """
    return None
def collatz_conjecture_memorization(n):
    """
    This function takes an integer n as input and applies the Collatz Conjecture
    until it reaches 1. The number of steps taken to reach 1 is returned.
    """
    return None
def collatz_conjecture_max(n):
    """
    This function takes an integer n as input and applies the Collatz Conjecture
    until it reaches 1. The maximum number in the sequence is returned.
    """
    return None


# Manual Test Cases
test_cases = [
    (1, 0),
    (2, 1),
    (3, 7),
    (4, 2),
    (5, 5),
    (10, 6),
    (15, 17),
    (27, 111),
    (40, 8),
    (50, 24)
    # Add more test cases if needed
]

max_test_cases = [
    (1, 1),
    (2, 2),
    (3, 8),
    (4, 3),
    (5, 16),
    (10, 16),
    (15, 16),
    (27, 9232),
    (40, 40),
    (50, 160)
    # Add more test cases if needed
]

for i, test_case in enumerate(test_cases):
    input_num, expected_output = test_case
    
    # Testing collatz_conjecture
    result = collatz_conjecture(input_num)
    if result != None:
        if result == expected_output:
            print(f"Test case {i+1} for collatz_conjecture PASSED")
        else:
            print(f"Test case {i+1} for collatz_conjecture FAILED. Expected {expected_output}, but got {result}.")

    # Testing collatz_conjecture_recursive
    result_recursive = collatz_conjecture_recursive(input_num)

    if result_recursive != None:
        if result_recursive == expected_output:
            print(f"Test case {i+1} for collatz_conjecture_recursive PASSED")
        else:
            print(f"Test case {i+1} for collatz_conjecture_recursive FAILED. Expected {expected_output}, but got {result_recursive}.")

    # Testing collatz_conjecture_memorization
    result_memorization = collatz_conjecture_memorization(input_num)

    if result_memorization != None:
        if result_memorization == expected_output:
            print(f"Test case {i+1} for collatz_conjecture_memorization PASSED")
        else:
            print(f"Test case {i+1} for collatz_conjecture_memorization FAILED. Expected {expected_output}, but got {result_memorization}.")

```


# [Link to Solution](Solution.md)


