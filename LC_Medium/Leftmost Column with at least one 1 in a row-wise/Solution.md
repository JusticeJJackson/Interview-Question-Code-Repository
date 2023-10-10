# Solution 1 - Brute Force

This method finds the leftmost column index with a 1 in a given 2D matrix of integers, where each row is sorted in ascending order. It first initializes the leftmost column to a very large number to ensure that any leftmost column found will be smaller, then iterates over all rows and columns of the matrix to find the first 1 in each row, updating the leftmost column index accordingly. Finally, it returns the leftmost column index if found, otherwise returns -1.

## Time Complexity: O(n^2)
## Space Complexity: O(n)

## Code

```java
// This method takes a 2D matrix of integers as input and returns the leftmost column index with a 1 in it.
public int searchColumns(int[][] matrix) {
    // Get the number of rows and columns in the matrix.
    int rows = matrix.length;
    int cols = matrix[0].length;
    // Set the leftmost column to a very large number to ensure that any leftmost column found will be smaller.
    int leftmost = Integer.MAX_VALUE;

    // Iterate over all rows of the matrix.
    for (int i = 0; i < rows; i++) {
        // Iterate over all columns of the matrix.
        for (int j = 0; j < cols; j++) {
            // If a 1 is found at the current position, update the leftmost column and exit the inner loop.
            if (matrix[i][j] == 1) {
                leftmost = Math.min(leftmost, j);
                break;
            }
        }
    }

    // If a leftmost column was not found, return -1. Otherwise, return the leftmost column index.
    return leftmost == Integer.MAX_VALUE ? -1 : leftmost;
}


```

# Solution 2 - Binary Search

This implementation uses binary search to search for the leftmost 1 in each row. For each row, it initializes the binary search range to be the entire row, and then repeatedly halves the range until it finds the leftmost 1 (if there is one). Once it finds the leftmost 1 in the row, it updates the leftmost variable to be the column index of the leftmost 1 (if it's smaller than the current value of leftmost). If a leftmost 1 is not found in any row, leftmost remains equal to cols, so the function returns -1.



## Time Complexity: O(n log(n))
## Space Complexity O(n)

## Code

```java
public int leftMostColumnWithOne(int[][] matrix) {
    int rows = matrix.length;
    int cols = matrix[0].length;
    int leftmost = cols;

    for (int i = 0; i < rows; i++) {
        int lo = 0;
        int hi = cols - 1;

        // Binary search for the leftmost 1 in the current row.
        while (lo <= hi) {
            int mid = lo + (hi - lo) / 2;
            if (matrix[i][mid] == 1) {
                leftmost = mid;
                hi = mid - 1;
            } else {
                lo = mid + 1;
            }
        }
    }

    return leftmost == cols ? -1 : leftmost;
}


'''