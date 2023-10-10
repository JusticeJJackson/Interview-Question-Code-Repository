# Number of Good Pairs

## Problem Statement

Given an array of integers `nums`. A pair `(i,j)` is called good if `nums[i] == nums[j]` and `i < j`. Return the number of good pairs. 

## Example 1:

Input:

`nums` = `[1,2,3,1,1,3]`

Output:

`4`

> Explanation: There are 4 good pairs `(0,3)`, `(0,4)`, `(3,4)`, `(2,5)` 0-indexed.

## Example 2:

Input:

`nums` = `[1,1,1,1]`

Output:

`6`

> Explanation: Each pair in the array are good.

## Example 3:

Input:

`nums` = `[1,2,3]`

Output:

`0`

> Explanation: There are no good pairs in the array

## Java Starter Code

```java
import java.util.*;

public class Solution {
    /**
     * Given an array of integers `nums`. A pair `(i,j)` is called good if `nums[i] == nums[j]` and `i < j`.
     * Return the number of good pairs.
     *
     * @param nums the input array of integers
     * @return the number of good pairs
     */
    public static int numIdenticalPairs(int[] nums) {
       
    }

    /**
     * Tests the numIdenticalPairs method with some example inputs.
     *
     * @param args the command line arguments (unused)
     */
    public static void main(String[] args) {
        int[][] numsInputs = {{1, 2, 3, 1, 1, 3}, {1, 1, 1, 1}, {1, 2, 3}};
        int[] expectedOutputs = {4, 6, 0};

        for (int i = 0; i < numsInputs.length; i++) {
            int[] numsInput = numsInputs[i];
            int expectedOutput = expectedOutputs[i];
            int output = numIdenticalPairs(numsInput);
            if (output == expectedOutput) {
                System.out.printf("PASS: numIdenticalPairs(%s) = %d\n", Arrays.toString(numsInput), output);
            } else {
                System.out.printf("FAIL: numIdenticalPairs(%s) = %d (expected %d)\n", Arrays.toString(numsInput), output, expectedOutput);
            }
        }
    }
}
```

## Python Starter Code

```python
"""
Given an array of integers `nums`. A pair `(i,j)` is called good if `nums[i] == nums[j]` and `i < j`.
Return the number of good pairs.

Example 1:

Input: nums = [1,2,3,1,1,3]
Output: 4
Explanation: There are 4 good pairs (0,3), (0,4), (3,4), (2,5) 0-indexed.

Example 2:

Input: nums = [1,1,1,1]
Output: 6
Explanation: Each pair in the array are good.

Example 3:

Input: nums = [1,2,3]
Output: 0
Explanation: There are no good pairs in the array
"""


def numIdenticalPairs(nums):
    # Implement solution here
    return 0

def test():
    nums_inputs = [[1, 2, 3, 1, 1, 3], [1, 1, 1, 1], [1, 2, 3]]
    expected_outputs = [4, 6, 0]

    for nums_input, expected_output in zip(nums_inputs, expected_outputs):
        output = numIdenticalPairs(nums_input)
        if output == expected_output:
            print('PASS: numIdenticalPairs({}) = {}'.format(nums_input, output))
        else:
            print('FAIL: numIdenticalPairs({}) = {} (expected {})'.format(nums_input, output, expected_output))

test()

```


# [Link to Solution](Solution.md)


