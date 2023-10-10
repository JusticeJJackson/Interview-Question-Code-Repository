# Fizz Buzz

## Problem Statement

Write a program that outputs the string representation of numbers from `1` to `n`. But for multiples of three it should output `"Fizz"` instead of the number and for the multiples of five output `"Buzz"`. For numbers which are multiples of both three and five output `"FizzBuzz"`.

## Example 1:

Input:

`n = 15`

Output:

`1`
`2`
`Fizz`
`4`
`Buzz`
`Fizz`
`7`
`8`
`Fizz`
`Buzz`
11
`Fizz`
`13`
`14`
`FizzBuzz`

## Example 2:

Input: 

`n = 6`

Output:

`1`
`2`
`Fizz`
`4`
`Buzz`
`Fizz`



## Java Starter Code

```java
import java.util.List;
import java.util.ArrayList;

public class Solution {
  
    /**
     * Returns a list of strings representing the numbers from 1 to n, 
     * where multiples of three are replaced by "Fizz", multiples of five are replaced by "Buzz", 
     * and multiples of both three and five are replaced by "FizzBuzz".
     * 
     * @param n the maximum number in the list
     * @return the list of strings
     */
    public static List<String> fizzBuzz(int n) {
        // Implement your solution here
        return null;
    }

    /**
     * Tests the fizzBuzz method with some example inputs.
     * 
     * @param args the command line arguments (unused)
     */
    public static void main(String[] args) {
        int n = 15;
        List<String> output = fizzBuzz(n);
        System.out.println(output);
    }
}
```

## Python Starter Code

```python
"""
FizzBuzz problem: Print numbers from 1 to n. But for multiples of three print "Fizz" instead of the number and for 
the multiples of five print "Buzz". For numbers which are multiples of both three and five print "FizzBuzz".

Example:
Input: 15
Output: "1","2","Fizz","4","Buzz","Fizz","7","8","Fizz","Buzz","11","Fizz","13","14","FizzBuzz"
"""
def fizzBuzz(n: int):
    # Implement your solution here

print(fizzBuzz(15))

```

# [Link to Solution](Solution.md)



