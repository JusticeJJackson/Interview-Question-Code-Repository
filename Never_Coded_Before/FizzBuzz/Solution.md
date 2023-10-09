# Solution 1 - Naive Approach

This approach checks every number from 1 to n and prints out "Fizz" for multiples of 3, "Buzz" for multiples of 5, "FizzBuzz" for multiples of both 3 and 5, and the number itself for all other cases.

## Time Complexity: O(n)
## Space Complexity: O(1)



## Code

```java
public static void fizzBuzz(int n) {
    for (int i = 1; i <= n; i++) {
        if (i % 3 == 0 && i % 5 == 0) {
            System.out.println("FizzBuzz");
        } else if (i % 3 == 0) {
            System.out.println("Fizz");
        } else if (i % 5 == 0) {
            System.out.println("Buzz");
        } else {
            System.out.println(i);
        }
    }
}
```

# Solution 2 - String Concatenation

This approach uses string concatenation to build the output for each number, and then prints out the resulting string.

## Time Complexity: O(n)
## Space Complexity O(1)

## Code

```java
public static void fizzBuzz(int n) {
    for (int i = 1; i <= n; i++) {
        String output = ""; // initialize output string
        if (i % 3 == 0) {
            output += "Fizz"; // append "Fizz" if divisible by 3
        }
        if (i % 5 == 0) {
            output += "Buzz"; // append "Buzz" if divisible by 5
        }
        if (output.equals("")) { // if output string is empty
            output += Integer.toString(i); // append the number as a string
        }
        System.out.println(output); // print the output string for each number
    }
}
```

# Solution 3 - String Concatenation with StringBuilder

This approach is similar to the previous one, but uses a StringBuilder to improve performance when building the output string.

## Time Complexity: O(n)
## Space Complexity: O(n)

## Code

```java
public static void fizzBuzz(int n) {
    for (int i = 1; i <= n; i++) {
        StringBuilder output = new StringBuilder(); // initialize a new StringBuilder to store the output
        if (i % 3 == 0) {
            output.append("Fizz"); // Append "Fizz" if divisible by 3
        }
        if (i % 5 == 0) {
            output.append("Buzz"); // Append "Buzz" if divisible by 5
        }
        if (output.length() == 0) {
            output.append(i); // If not divisible by 3 or 5, append the number itself
        }
        System.out.println(output.toString()); // Print the output string for each number
    }
}
```