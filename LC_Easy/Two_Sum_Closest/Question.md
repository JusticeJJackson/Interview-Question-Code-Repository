# Two Numbers Closest to Target

## Problem Statement

Given an array of integers `nums` and an integer `target`, find two numbers in the array such that their sum is closest to the `target`, but does not exceed it. Return the indices of the two numbers.

You may assume that each input would have exactly one solution and you may not use the same element twice.


## Example 1:

Input:
`nums = [1, 2, 3, 4, 5]`
`target = 8`

Output:
`(2, 3)`
> Explanation: The sum of numbers at indices 2 and 3 is 7, which is the closest sum to the target (8) without exceeding it.

## Example 2:

Input:
`nums = [10, 20, 30, 40, 50]`
`target = 45`

Output:
`(1, 2)`
> Explanation: The sum of numbers at indices 1 and 2 is 50, which is the closest sum to the target (45) without exceeding it.

## Example 3:

Input:
`nums = [5, 10, 15, 20, 25]`
`target = 23`

Output:
`(1, 2)`
> Explanation: The sum of numbers at indices 1 and 2 is 25, which is the closest sum to the target (23) without exceeding it.



## Java Starter Code

```java
import java.util.Arrays;

/**
 * Problem: Closest Two Sum Without Exceeding Target
 *
 * Given an array of integers `nums` and an integer `target`, find a pair of
 * distinct indices (i, j) such that:
 * - The sum of nums[i] + nums[j] is the closest possible to the target,
 * - Without exceeding the target.
 *
 * Return the pair of indices that achieves this. If multiple pairs yield the same sum,
 * any valid pair can be returned.
 *
 * Examples:
 *
 * Example 1:
 * Input:
 * nums = [1, 2, 3, 4, 5]
 * target = 8
 *
 * Output:
 * (2, 4)
 * Explanation: nums[2] + nums[4] = 3 + 5 = 8, which is exactly the target and the best possible sum.
 *
 * Example 2:
 * Input:
 * nums = [10, 20, 30, 40, 50]
 * target = 45
 *
 * Output:
 * (0, 1)
 * Explanation: nums[0] + nums[1] = 10 + 20 = 30, which is the closest sum to 45 without exceeding it.
 *
 * Example 3:
 * Input:
 * nums = [5, 10, 15, 20, 25]
 * target = 23
 *
 * Output:
 * (0, 2)
 * Explanation: nums[0] + nums[2] = 5 + 15 = 20, which is the closest valid sum under 23.
 */
public class Solution {
    /**
     * Finds a pair of indices (i, j) such that the sum of nums[i] and nums[j] is closest to the target,
     * but does not exceed it.
     *
     * @param nums   the input array of integers
     * @param target the target sum
     * @return an array containing the indices of the pair (i, j)
     */
    public static int[] closestTwoSumIndices(int[] nums, int target) {
        // Implementation here
        return new int[]{0, 0};
    }

    /**
     * Tests the closestTwoSumIndices method with some example inputs.
     *
     * @param args the command line arguments (unused)
     */
    public static void main(String[] args) {
        int[][] inputs = {{1, 2, 3, 4, 5}, {10, 20, 30, 40, 50}, {5, 10, 15, 20, 25}};
        int[] targets = {8, 45, 23};
        int[][] expectedOutputs = {{2, 3}, {1, 2}, {1, 2}};

        for (int i = 0; i < inputs.length; i++) {
            int[] input = inputs[i];
            int target = targets[i];
            int[] expectedOutput = expectedOutputs[i];
            int[] output = closestTwoSumIndices(input, target);

            if (Arrays.equals(output, expectedOutput)) {
                System.out.printf("PASS: closestTwoSumIndices(%s, %d) = %s\n",
                        Arrays.toString(input), target, Arrays.toString(output));
            } else {
                System.out.printf("FAIL: closestTwoSumIndices(%s, %d) = %s (expected %s)\n",
                        Arrays.toString(input), target, Arrays.toString(output), Arrays.toString(expectedOutput));
            }
        }
    }
}

```

## Python Starter Code

```python
"""
Problem: Closest Two Sum Without Exceeding Target

Given an array of integers `nums` and an integer `target`, find a pair of **distinct indices** `(i, j)` such that:
- The sum of `nums[i] + nums[j]` is the **closest possible to the target**, 
- **Without exceeding** the target.

Return the pair of indices that achieves this. If multiple pairs yield the same sum, any valid pair can be returned.

Examples:

Example 1:
Input:
nums = [1, 2, 3, 4, 5]
target = 8

Output:
(2, 4)
Explanation: nums[2] + nums[4] = 3 + 5 = 8, which is exactly the target and the best possible sum.

Example 2:
Input:
nums = [10, 20, 30, 40, 50]
target = 45

Output:
(0, 1)
Explanation: nums[0] + nums[1] = 10 + 20 = 30, which is the closest sum to 45 without exceeding it.

Example 3:
Input:
nums = [5, 10, 15, 20, 25]
target = 23

Output:
(0, 2)
Explanation: nums[0] + nums[2] = 5 + 15 = 20, which is the closest valid sum under 23.
"""

def closest_two_sum_indices(nums, target):
    # Implementation here
    return [0, 0]

# Tests the closest_two_sum_indices function with some example inputs.
def main():
    inputs = [[1, 2, 3, 4, 5], [10, 20, 30, 40, 50], [5, 10, 15, 20, 25]]
    targets = [8, 45, 23]
    expected_outputs = [[2, 3], [1, 2], [1, 2]]

    for i in range(len(inputs)):
        input_list = inputs[i]
        target = targets[i]
        expected_output = expected_outputs[i]
        output = closest_two_sum_indices(input_list, target)

        if output == expected_output:
            print(f"PASS: closest_two_sum_indices({input_list}, {target}) = {output}")
        else:
            print(f"FAIL: closest_two_sum_indices({input_list}, {target}) = {output} (expected {expected_output})")

if __name__ == "__main__":
    main()

```


# [Link to Solution](Solution.md)


