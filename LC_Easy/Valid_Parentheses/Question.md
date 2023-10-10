# Valid Parentheses

## Problem Statement

Given a string `s` containing just the characters `'(', ')'`, `'{', '}'`, `'[' and ']'`, determine if the input string is valid.

An input string is valid if:
Open brackets must be closed by the same type of brackets.
Open brackets must be closed in the correct order.


## Example 1:

Input:

`s = "()"`

Output:

`True`

## Example 2:

Input:

`s = "()[]{}"`

Output:

`True`

## Example 3:

Input:

`s = "(]"`

Output:

`False`

## Example 4:

Input:

`s = "([)]"`

Output:

`False`

## Example 5:

Input:

`s = "{[]}"`

Output:

`True`


# Constraints:
 1 <= s.length <= 104
s consists of parentheses only '()[]{}'.


## Java Starter Code

```java
import java.util.Collections;
import java.util.List;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.*;

/**
 * Problem: Valid Parentheses
 *
 * Given a string s containing just the characters '(', ')', '{', '}', '[' and ']', determine if the input string is valid.
 * An input string is valid if:
 * - Open brackets must be closed by the same type of brackets.
 * - Open brackets must be closed in the correct order.
 *
 * Example 1:
 * Input: s = "()"
 * Output: true
 *
 * Example 2:
 * Input: s = "()[]{}"
 * Output: true
 *
 * Example 3:
 * Input: s = "(]"
 * Output: false
 *
 * Example 4:
 * Input: s = "([)]"
 * Output: false
 *
 * Example 5:
 * Input: s = "{[]}"
 * Output: true
 *
 * Constraints:
 * - 1 <= s.length <= 104
 * - s consists of parentheses only '()[]{}'.
 */
class Solution{
    /**
     * Determines whether the input string contains valid parentheses.
     * @param s the input string
     * @return true if the string contains valid parentheses, false otherwise
     */
    public static boolean isValid(String s) {
        // implementation here
        return false;
    }

    /**
     * Tests the isValid method with some example inputs.
     * @param args the command line arguments (unused)
     */
    public static void main(String[] args) {
        String[] inputs = {"()", "()[]{}", "(]", "([)]", "{[]}"};
        boolean[] expectedOutputs = {true, true, false, false, true};
        for (int i = 0; i < inputs.length; i++) {
            String input = inputs[i];
            boolean expectedOutput = expectedOutputs[i];
            boolean output = isValid(input);
            if (output == expectedOutput) {
                System.out.printf("PASS: isValid(%s) = %b\n", input, output);
            } else {
                System.out.printf("FAIL: isValid(%s) = %b (expected %b)\n", input, output, expectedOutput);
            }
        }
    }
}
```

## Python Starter Code

```python
"""
Problem: Valid Parentheses

Given a string s containing just the characters '(', ')', '{', '}', '[' and ']', determine if the input string is valid.
An input string is valid if:

Open brackets must be closed by the same type of brackets.
Open brackets must be closed in the correct order.
Example:
input: "()"
output: true

input: "()[]{}"
output: true

input: "(]"
output: false

input: "([)]"
output: false

input: "{[]}"
output: true

Constraints:

1 <= s.length <= 104
s consists of parentheses only '()[]{}'.
"""

def is_valid(s: str) -> bool:
    # implementation here
    return False


def test_is_valid():
    inputs = ["()", "()[]{}", "(]", "([)]", "{[]}"]
    expected_outputs = [True, True, False, False, True]
    for i, e in zip(inputs, expected_outputs):
        output = is_valid(i)
        if output == e:
            print(f"PASSED: is_valid({i}) = {output}")
        else:
            print(f"FAILED: is_valid({i}) = {output}; expected = {e}")

test_is_valid()
```


# [Link to Solution](Solution.md)


