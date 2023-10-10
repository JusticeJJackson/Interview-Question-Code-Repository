# Longest Substring Without Repeating Characters

## Problem Statement

Given a string `s`, find the length of the longest substring without repeating characters.

## Example 1:

Input: 

`s = "abcabcbb"`

Output: 

`3`

> Explanation: The answer is `"abc"`, with the length of `3`.

## Example 2:

Input: 

`s = "bbbbb"`

Output: 

`1`

> Explanation: The answer is `"b"`, with the length of `1`.

## Example 3:

Input: 

`s = "pwwkew"`

Output: 

`3`

> Explanation: The answer is `"wke"`, with the length of `3`.
Notice that the answer must be a substring, "pwke" is a subsequence and not a substring.

# Constraints:

`0` <= `s.lengt`h <= `5 * 104`
`s `consists of English letters, digits, symbols and spaces.

## Java Starter Code

```java
import java.util.Collections;
import java.util.List;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.*;

/**
 * Given a string s, find the length of the longest substring without repeating characters.
 *
 * Example 1:
 * Input: s = "abcabcbb"
 * Output: 3
 * Explanation: The answer is "abc", with the length of 3.
 *
 * Example 2:
 * Input: s = "bbbbb"
 * Output: 1
 * Explanation: The answer is "b", with the length of 1.
 *
 * Example 3:
 * Input: s = "pwwkew"
 * Output: 3
 * Explanation: The answer is "wke", with the length of 3.
 * Notice that the answer must be a substring, "pwke" is a subsequence and not a substring.
 *
 * Constraints:
 * 0 <= s.length <= 5 * 104
 * s consists of English letters, digits, symbols and spaces.
 */
public class Solution {
    public static int lengthOfLongestSubstring(String s) {
        //implement code here
        return 0;
    }

    public static void main(String[] args) {
        String s1 = "abcabcbb";
        int expectedOutput1 = 3;
        int output1 = lengthOfLongestSubstring(s1);
        System.out.println("Test 1 Passed? " + (expectedOutput1 == output1));

        String s2 = "bbbbb";
        int expectedOutput2 = 1;
        int output2 = lengthOfLongestSubstring(s2);
        System.out.println("Test 2 Passed? " + (expectedOutput2 == output2));

        String s3 = "pwwkew";
        int expectedOutput3 = 3;
        int output3 = lengthOfLongestSubstring(s3);
        System.out.println("Test 3 Passed? " + (expectedOutput3 == output3));
    }
}


```

## Python Starter Code

```python
def lengthOfLongestSubstring(s):
    # implementation here
    return None


def runs_tests():
    # Example usage and additional test cases
    s1 = "abcabcbb"
    expected_output1 = 3
   
    output1 = lengthOfLongestSubstring(s1)
    if output1 == expected_output1:
        print("Test case 1 PASSED")
    else:
        print(f"Test case 1 FAILED: expected {expected_output1}, but got {output1}")

    s2 = "bbbbb"
    expected_output2 = 1
    output2 = lengthOfLongestSubstring(s2)
    if output2 == expected_output2:
        print("Test case 2 PASSED")
    else:
        print(f"Test case 2 FAILED: expected {expected_output2}, but got {output2}")
run_tests()





```



