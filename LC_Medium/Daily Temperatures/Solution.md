# Solution 1 - Brute Force

This approach involves using two nested loops to iterate over each element in the array and compare it to the elements to its right, looking for the next highest temperature. If a higher temperature is found, the number of days until that temperature is reached is calculated and stored in the output array.


## Time Complexity: O(n^2)
## Space Complexity: O(n)



## Code

```java
public int[] dailyTemperatures(int[] temperatures) {
    int[] res = new int[temperatures.length]; // initialize output array with 0s
    for (int i = 0; i < temperatures.length; i++) { // loop through each element in the array
        for (int j = i + 1; j < temperatures.length; j++) { // loop through each element to the right of the current element
            if (temperatures[j] > temperatures[i]) { // if the temperature to the right is higher than the current temperature
                res[i] = j - i; // calculate the number of days until that temperature is reached and store it in the output array
                break; // exit the inner loop and move on to the next element in the outer loop
            }
        }
    }
    return res; // return the output array
}




```

# Solution 2 - Two Pointer

This solution uses a simple approach to solve the problem of finding the number of days until the next higher temperature in an array. It iterates over the array and for each element, it finds the next higher temperature by comparing it with all the elements to its right until a higher temperature is found. If a higher temperature is found, it calculates the number of days until that temperature is reached and stores it in the output array. If there is no next higher temperature, the output array is initialized with 0 for that element.


## Time Complexity: O(n^2)
## Space Complexity O(n)

## Code

```java
public int[] dailyTemperatures(int[] temperatures) {
    int n = temperatures.length; // Get the length of the input array
    int[] result = new int[n]; // Initialize the result array with the same length as the input
    
    for (int i = 0; i < n; i++) { // Iterate over the input array
        int j = i + 1; // Initialize the second pointer to point to the next element after the current one
        while (j < n && temperatures[j] <= temperatures[i]) { // Search for the next element with a higher temperature
            j++; // Move the second pointer to the next element
        }
        if (j < n) { // If a next higher temperature is found, calculate the number of days until that temperature is reached and store it in the result array
            result[i] = j - i;
        }
    }
    
    return result; // Return the result array
}


```

# Solution 3 - Stack

This approach involves using a stack to keep track of the indices of elements in the array that do not have a next higher temperature yet. We iterate over the array from right to left, and for each element, we pop all indices of elements with temperatures lower than or equal to the current element. The top of the stack now contains the index of the element with the next highest temperature. The number of days until that temperature is reached is calculated and stored in the output array. The current element's index is then pushed onto the stack.

## Time Complexity: O(n)
## Space Complexity: O(n)

## Code

```java
public int[] dailyTemperatures(int[] temperatures) {
    int n = temperatures.length; // Get the length of the input array
    int[] result = new int[n]; // Initialize the result array with the same length as the input
    Stack<Integer> stack = new Stack<>(); // Create a stack to keep track of indices of elements without next higher temperatures
    
    for (int i = n - 1; i >= 0; i--) { // Iterate over the input array backwards
        while (!stack.isEmpty() && temperatures[i] >= temperatures[stack.peek()]) { // Pop all indices of elements with lower or equal temperatures than the current element
            stack.pop();
        }
        if (stack.isEmpty()) { // If the stack is empty, there is no higher temperature for this element
            result[i] = 0;
        } else { // Otherwise, calculate the number of days until the next highest temperature is reached and store it in the result array
            result[i] = stack.peek() - i;
        }
        stack.push(i); // Push the current element's index onto the stack
    }
    
    return result; // Return the result array
}





```