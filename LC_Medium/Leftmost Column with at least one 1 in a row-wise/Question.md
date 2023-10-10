# Leftmost Column with at least one 1 in a row-wise 

## Problem Statement

Given a 2D Sorted Binary Square Array consisting solely of integers `1` and `0` sorted such that all `0`s in a row come before all `1`s. Find the first column that contains any instance of `1`.

## Example 1:

Input = 

`[`  
 `[0,0,0,0,0,1,1,1]`,   
 `[0,0,0,0,0,0,0,0]`,    
 `[0,0,1,1,1,1,1,1]`,    
 `[0,0,0,0,1,1,1,1]`,    
 `[0,0,0,1,1,1,1,1]`    
`]`

Output = 

`3`

Explanation: 

The column of the first `1` that appears in any row is `3`, as `input[2][2] = 1`

## Example 2:

Input = 

`[`  
 `[0,0,0,0,0,1,1,1]`,  
 `[0,1,1,1,1,1,1,1]`,  
 `[1,1,1,1,1,1,1,1]`,  
 `[1,1,1,1,1,1,1,1]`,  
 `[0,0,0,0,0,0,0,0]`  
`]`  

Output =

 `1`

Explanation: 

The column of the first `1` that appears in any row is `1`, as `input[2][0] = 1`


## Example 3:

Input = 

`[`  
 `[0,0,0,0,0,0,0,0]`,  
 `[0,0,0,0,0,0,0,0]`,  
 `[0,0,0,0,0,0,0,0]`,  
 `[0,0,0,0,0,0,0,0]`,  
 `[0,0,0,0,0,0,0,0]`  
`]`  

Output = 

`-1`

Explanation: 

There are no instances of `1`, hence we return an invalid column value `-1`.

## Java Starter Code

```java
import java.util.Collections;
import java.util.List;
import java.util.ArrayList;
import java.util.Arrays;
/*
Given a 2D Sorted Binary Square Array consisting solely of integers '1' and '0' sorted such that 
all '0's in a row come before all '1's. Find the first column that contains any instance of '1'.
*/


public class Solution{
    
        /*
    searchColumns - function that takes in a 2D Sorted Binary Square Array and returns the
    column index of the first instance of a '1' in the array. If there are no '1's in the array,
    return -1.

    Given a 2D Sorted Binary Square Array consisting solely of integers '1' and '0' sorted such that all '0's in a row come before all '1's. Find the first column that contains any instance of '1'.

    Example 1:

    Input = [
    [0,0,0,0,0,1,1,1],
    [0,0,0,0,0,0,0,0],
    [0,0,1,1,1,1,1,1],
    [0,0,0,0,1,1,1,1],
    [0,0,0,1,1,1,1,1]
    ]
    Output = 3

    Explanation: The column of the first '1' that appears in any row is 3, as input[2][2] = 1

    Example 2:

    Input = [
    [0,0,0,0,0,1,1,1],
    [0,1,1,1,1,1,1,1],
    [1,1,1,1,1,1,1,1],
    [1,1,1,1,1,1,1,1],
    [0,0,0,0,0,0,0,0]
    ]
    Output = 1

    Explanation: The column of the first '1' that appears in any row is 1, as input[2][0] = 1

    Example 3:

    Input = [
    [0,0,0,0,0,0,0,0],
    [0,0,0,0,0,0,0,0],
    [0,0,0,0,0,0,0,0],
    [0,0,0,0,0,0,0,0],
    [0,0,0,0,0,0,0,0]
    ]
    Output = -1

    Explanation: There are no instances of '1', hence we return an invalid column value '-1'.
    */
    public static int searchColumns(int[][] arr) {
        // TODO: Implement solution
        return -1;
    }

    public static void main(String[] args) {
    // Define test cases
    int[][] input1 = {
        {0,0,0,0,0,1,1,1},
        {0,0,0,0,0,0,0,0},
        {0,0,1,1,1,1,1,1},
        {0,0,0,0,1,1,1,1},
        {0,0,0,1,1,1,1,1}
    };
    int expectedOutput1 = 3;

    int[][] input2 = {
        {0,0,0,0,0,1,1,1},
        {0,1,1,1,1,1,1,1},
        {1,1,1,1,1,1,1,1},
        {1,1,1,1,1,1,1,1},
        {0,0,0,0,0,0,0,0}
    };
    int expectedOutput2 = 1;

    int[][] input3 = {
        {0,0,0,0,0,0,0,0},
        {0,0,0,0,0,0,0,0},
        {0,0,0,0,0,0,0,0},
        {0,0,0,0,0,0,0,0},
        {0,0,0,0,0,0,0,0}
    };
    int expectedOutput3 = -1;

    // Call the function and store the result in a variable
    int actualOutput1 = searchColumns(input1);
    int actualOutput2 = searchColumns(input2);
    int actualOutput3 = searchColumns(input3);

    // Compare the actual output with the expected output and print the result
    if (actualOutput1 == expectedOutput1) {
        System.out.println("Test 1 passed.");
    } else {
        System.out.println("Test 1 failed. Expected output: " + expectedOutput1 + ". Actual output: " + actualOutput1);
    }

    if (actualOutput2 == expectedOutput2) {
        System.out.println("Test 2 passed.");
    } else {
        System.out.println("Test 2 failed. Expected output: " + expectedOutput2 + ". Actual output: " + actualOutput2);
    }

    if (actualOutput3 == expectedOutput3) {
        System.out.println("Test 3 passed.");
    } else {
        System.out.println("Test 3 failed. Expected output: " + expectedOutput3 + ". Actual output: " + actualOutput3);
    }
}

}

```

## Python Starter Code

```python
"""
searchColumns - function that takes in a 2D Sorted Binary Square Array and returns the
column index of the first instance of a '1' in the array. If there are no '1's in the array,
return -1.

Given a 2D Sorted Binary Square Array consisting solely of integers '1' and '0' sorted such that all '0's in a row come before all '1's. Find the first column that contains any instance of '1'.

Example 1:

Input = [
[0,0,0,0,0,1,1,1],
[0,0,0,0,0,0,0,0],
[0,0,1,1,1,1,1,1],
[0,0,0,0,1,1,1,1],
[0,0,0,1,1,1,1,1]
]
Output = 3

Explanation: The column of the first '1' that appears in any row is 3, as input[2][2] = 1

Example 2:

Input = [
[0,0,0,0,0,1,1,1],
[0,1,1,1,1,1,1,1],
[1,1,1,1,1,1,1,1],
[1,1,1,1,1,1,1,1],
[0,0,0,0,0,0,0,0]
]
Output = 1

Explanation: The column of the first '1' that appears in any row is 1, as input[2][0] = 1

Example 3:

Input = [
[0,0,0,0,0,0,0,0],
[0,0,0,0,0,0,0,0],
[0,0,0,0,0,0,0,0],
[0,0,0,0,0,0,0,0],
[0,0,0,0,0,0,0,0]
]
Output = -1

Explanation: There are no instances of '1', hence we return an invalid column value '-1'.
"""
def searchColumns(n):
    #Implement Here
    return -1;



def testSearch():
    # Define test cases
    input1 = [
        [0,0,0,0,0,1,1,1],
        [0,0,0,0,0,0,0,0],
        [0,0,1,1,1,1,1,1],
        [0,0,0,0,1,1,1,1],
        [0,0,0,1,1,1,1,1]
    ]
    expectedOutput1 = 3

    input2 = [
        [0,0,0,0,0,1,1,1],
        [0,1,1,1,1,1,1,1],
        [1,1,1,1,1,1,1,1],
        [1,1,1,1,1,1,1,1],
        [0,0,0,0,0,0,0,0]
    ]
    expectedOutput2 = 1

    input3 = [
        [0,0,0,0,0,0,0,0],
        [0,0,0,0,0,0,0,0],
        [0,0,0,0,0,0,0,0],
        [0,0,0,0,0,0,0,0],
        [0,0,0,0,0,0,0,0]
    ]
    expectedOutput3 = -1

    # Call the function and store the result in a variable
    actualOutput1 = searchColumns(input1)
    actualOutput2 = searchColumns(input2)
    actualOutput3 = searchColumns(input3)

    # Compare the actual output with the expected output and print the result
    if actualOutput1 == expectedOutput1:
        print("Test 1 passed.")
    else:
        print("Test 1 failed. Expected output: " + str(expectedOutput1) + ". Actual output: " + str(actualOutput1))

    if actualOutput2 == expectedOutput2:
        print("Test 2 passed.")
    else:
        print("Test 2 failed. Expected output: " + str(expectedOutput2) + ". Actual output: " + str(actualOutput2))

    if actualOutput3 == expectedOutput3:
        print("Test 3 passed.")
    else:
        print("Test 3 failed. Expected output: " + str(expectedOutput3) + ". Actual output: " + str(actualOutput3))

testSearch()






```



