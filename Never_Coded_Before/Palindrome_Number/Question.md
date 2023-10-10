# Palindrome Number

## Problem Statement

Determine whether an integer is a palindrome. An integer is a palindrome when it reads the same backward as forward.

## Example 1:

Input:

`n = 121`

Output:

`True`


## Example 2:

Input:

`n = -121`

Output:

`False`

> Explanation: From left to right, it reads -121. From right to left, it becomes 121-. Therefore it is not a palindrome.

## Example 3:

Input:

`n = 10`

Output:

`False`

> Explanation: Reads 01 from right to left. Therefore it is not a palindrome.

## Java Starter Code

```java
import java.util.Collections;
import java.util.List;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.*;

/**
 * Problem: Palindrome Number
 * 
 * Determine whether an integer is a palindrome. An integer is a palindrome when it reads the same backward as forward.
 * 
 * Example 1:
 * Input: x = 121
 * Output: true
 * 
 * Example 2:
 * Input: x = -121
 * Output: false
 * Explanation: From left to right, it reads -121. From right to left, it becomes 121-. Therefore it is not a palindrome.
 * 
 * Example 3:
 * Input: x = 10
 * Output: false
 * Explanation: Reads 01 from right to left. Therefore it is not a palindrome.
 */
public class Solution {
    
    /**
     * Determines whether an integer is a palindrome.
     * 
     * @param x the integer to check
     * @return true if x is a palindrome, false otherwise
     */
    public static boolean isPalindrome(int n) {
        // implementation here
    }

    /**
     * Tests the isPalindrome method with some example inputs.
     * 
     * @param args the command line arguments (unused)
     */
    public static void main(String[] args) {
        int[] inputs = {121, -121, 10};
        boolean[] expectedOutputs = {true, false, false};
        for (int i = 0; i < inputs.length; i++) {
            int input = inputs[i];
            boolean expectedOutput = expectedOutputs[i];
            boolean output = isPalindrome(input);
            if (output == expectedOutput) {
                System.out.printf("PASS: isPalindrome(%d) = %b\n", input, output);
            } else {
                System.out.printf("FAIL: isPalindrome(%d) = %b (expected %b)\n", input, output, expectedOutput);
            }
        }
    }
}

```

## Python Starter Code

```python
"""
Problem: Palindrome Number

Determine whether an integer is a palindrome. An integer is a palindrome when it reads the same backward as forward.

Example 1:
Input: n = 121
Output: true

Example 2:
Input: n = -121
Output: false
Explanation: From left to right, it reads -121. From right to left, it becomes 121-. Therefore it is not a palindrome.

Example 3:
Input: n = 10
Output: false
Explanation: Reads 01 from right to left. Therefore it is not a palindrome.
"""

def is_palindrome(n: int) -> bool:
    # implementation here
    pass

def test_is_palindrome():
    inputs = [121, -121, 10]
    expected_outputs = [True, False, False]
    for i in range(len(inputs)):
        input = inputs[i]
        expected_output = expected_outputs[i]
        output = is_palindrome(input)
        if output == expected_output:
            print(f"PASS: is_palindrome({input}) = {output}")
        else:
            print(f"FAIL: is_palindrome({input}) = {output} (expected {expected_output})")

if __name__ == "__main__":
    test_is_palindrome()

```


# [Link to Solution](Solution.md)




