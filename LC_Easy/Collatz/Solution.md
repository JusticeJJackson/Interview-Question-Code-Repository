# Note: Time and Space complexity are not required for possible to compute for this problem as the collatz conjecture is not proven to be bounded by any polynomial function. still, it is a good exercise to think about the possible time and space complexity of your solution.

# Collatz Iteraive

This solution iteratively applies the Collatz Conjecture to reduce the input number to 1, counting the steps taken. 

## Code

```java
public static int collatzConjecture(int n) {
        int steps = 0;
        while (n != 1) {
            if (n % 2 == 0) {
                n /= 2;  // If n is even, divide by 2
            } else {
                n = 3 * n + 1;  // If n is odd, multiply by 3 and add 1
            }
            steps++;  // Count the number of steps
        }
        return steps;
    }

```

# Collatz Recursive

Utilizing recursion, this solution calculates the steps needed to reach 1 by dividing the input number by 2 for even numbers and applying 3n+1 for odd numbers. 

## Code

```java
if (n == 1) {
            return 0;  // Base case: If n is 1, no steps needed
        } else if (n % 2 == 0) {
            return 1 + collatzConjectureRecursive(n / 2);  // If n is even, recurse with n/2
        } else {
            return 1 + collatzConjectureRecursive(3 * n + 1);  // If n is odd, recurse with 3n+1
        }
```

# Collatz Memorization

Building upon the recursive solution, this version incorporates memorization to store intermediate results, reducing redundant calculations and improving efficiency. It does this by creating a map to store the number of steps needed to reach 1 for each number. If the number is already in the map, the number of steps is returned. Otherwise, the number of steps is calculated and stored in the map. this reduces the runtime for multiple calls to the same number from O(n) to O(1).

## Code

```java
private static Map<Integer, Integer> memo = new HashMap<>();

public static int collatzConjectureMemorization(int n, Map<Integer, Integer> memo) {
        if (memo.containsKey(n)) {
            return memo.get(n);  // If result for n is already memoized, return it
        }

        if (n == 1) {
            return 0;  // Base case: If n is 1, no steps needed
        } else if (n % 2 == 0) {
            int steps = 1 + collatzConjectureMemorization(n / 2, memo);  // If n is even, recurse with n/2
            memo.put(n, steps);  // Memoize the result for n
            return steps;
        } else {
            int steps = 1 + collatzConjectureMemorization(3 * n + 1, memo);  // If n is odd, recurse with 3n+1
            memo.put(n, steps);  // Memoize the result for n
            return steps;
        }
    }

```

# Collatz Max

 This solution iteratively applies the Collatz Conjecture to find the maximum number encountered in the sequence. 

## Code

```java
public static int collatzConjectureMax(int n) {
        int maxNum = n;
        while (n != 1) {
            if (n % 2 == 0) {
                n /= 2;  // If n is even, divide by 2
            } else {
                n = 3 * n + 1;  // If n is odd, multiply by 3 and add 1
            }
            maxNum = Math.max(maxNum, n);  // Update maxNum with the maximum value encountered
        }
        return maxNum;
    }
```

# Collatz Max Recursive

Utilizing recursion, this solution calculates the maximum number encountered in the sequence by dividing the input number by 2 for even numbers and applying 3n+1 for odd numbers. It then calculates the max value by comparing the current number with the result of the recursive call.

## Code

```java
public static int collatzConjectureMax(int n) {
if (n == 1) {
            return n;  // Base case: If n is 1, return n
        } else if (n % 2 == 0) {
            return Math.max(n, collatzConjectureMax(n / 2));  // If n is even, recurse with n/2
        } else {
            return Math.max(n, collatzConjectureMax(3 * n + 1));  // If n is odd, recurse with 3n+1
        }
}
```