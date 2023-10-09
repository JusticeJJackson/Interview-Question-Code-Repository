# Jewels and Stones

## Problem Statement

You're given strings **J** representing the types of stones that are jewels, and **S** representing the stones you have. Each character in **S** is a type of stone you have. You want to know how many of the stones you have are also jewels.

The letters in **J** are guaranteed distinct, and all characters in **J** and **S** are letters. Letters are case sensitive, so "a" is considered a different type of stone from "A".


## Example 1:

Input:

**J** = "aA"

**S** = "aAAbbbb"

Output:
3


## Example 2:

Input: 

**J** = "z"

**S** = "ZZ"

Output: 
0


```java
 * 
 * Example 1:
 * Input: J = "aA", S = "aAAbbbb"
 * Output: 3
 * 
 * Example 2:
 * Input: J = "z", S = "ZZ"
 * Output: 0
 * 
 * Note:
 * S and J will consist of letters and have length at most 50.
 * The characters in J are distinct.
 */
public class Solution {
    
    /**
     * Determines how many stones you have are also jewels.
     * 
     * @param J the types of stones that are jewels
     * @param S the stones you have
     * @return the number of stones you have that are also jewels
     */
    public static int numJewelsInStones(String J, String S) {
        // implementation here
    }

    /**
     * Tests the numJewelsInStones method with some example inputs.
     * 
     * @param args the command line arguments (unused)
     */
    public static void main(String[] args) {
        String[] jInputs = {"aA", "z"};
        String[] sInputs = {"aAAbbbb", "ZZ"};
        int[] expectedOutputs = {3, 0};
        for (int i = 0; i < jInputs.length; i++) {
            String jInput = jInputs[i];
            String sInput = sInputs[i];
            int expectedOutput = expectedOutputs[i];
            int output = numJewelsInStones(jInput, sInput);
            if (output == expectedOutput) {
                System.out.printf("PASS: numJewelsInStones(%s, %s) = %d\n", jInput, sInput, output);
            } else {
                System.out.printf("FAIL: numJewelsInStones(%s, %s) = %d (expected %d)\n", jInput, sInput, output, expectedOutput);
            }
        }
    }
}
```

```python
"""
Problem: Jewels and Stones

You're given strings J representing the types of stones that are jewels, and S representing the stones you have.  
Each character in S is a type of stone you have.  You want to know how many of the stones you have are also jewels.

The letters in J are guaranteed distinct, and all characters in J and S are letters. Letters are case sensitive, 
so "a" is considered a different type of stone from "A".

Example 1:
Input: J = "aA", S = "aAAbbbb"
Output: 3

Example 2:
Input: J = "z", S = "ZZ"
Output: 0

Note:
S and J will consist of letters and have length at most 50.
The characters in J are distinct.
"""

def num_jewels_in_stones(J: str, S: str) -> int:
    # implementation here
    pass

def test_num_jewels_in_stones():
    j_inputs = ["aA", "z"]
    s_inputs = ["aAAbbbb", "ZZ"]
    expected_outputs = [3, 0]
    for j, s, expected in zip(j_inputs, s_inputs, expected_outputs):
        result = num_jewels_in_stones(j, s)
        if result == expected:
            print(f"PASSED: num_jewels_in_stones({j}, {s}) = {result}")
        else:
            print(f"FAILED: num_jewels_in_stones({j}, {s}) = {result}; expected = {expected}")

test_num_jewels_in_stones()


```



