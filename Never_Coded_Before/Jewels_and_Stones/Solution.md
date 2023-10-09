# Solution 1 - Brute Force
A simple solution is to iterate over each character in the S string and check if it's present in the J string. If it is, we increment the count. This solution has a time complexity of O(N*M), where N is the length of S and M is the length of J.


## Time Complexity: O(N*M) 
## Space Complexity: O(N*M)


## Code

```java
public int numJewelsInStones(String J, String S) {
    int count = 0; // Initialize a counter for the number of jewels found in S
    for (int i = 0; i < S.length(); i++) {
        if (J.indexOf(S.charAt(i)) != -1) { // Check if the character in S is in J
            count++; // Increment the count if the character is a jewel
        }
    }
    return count; // Return the final count of jewels found in S
}
```

# Solution 2 - Hash Set

This solution is to create a hash set of the characters in the J string and then iterate over each character in the S string and check if it's present in the hash set. If it is, we increment the count.

## Time Complexity: O(N+M)
## Space Complexity: O(N+M)


## Code

```java
public int numJewelsInStones(String J, String S) {
    int count = 0; // Initialize a counter for the number of jewels found in S
    Set<Character> jewelSet = new HashSet<>(); // Create a set to store the characters in J
    for (int i = 0; i < J.length(); i++) {
        jewelSet.add(J.charAt(i)); // Add each character in J to the set
    }
    for (int i = 0; i < S.length(); i++) {
        if (jewelSet.contains(S.charAt(i))) { // Check if each character in S is in the set
            count++; // If so, increment the counter
        }
    }
    return count; // Return the final count of jewels found in S
}
```

# Solution 3 - Array

This solution uses an array to keep track of the count of each character in the S string. Then we iterate over the characters in the J string and add the corresponding count to the total count.

## Code

## Time Complexity: O(n)
## Space Complexity: O(1)


```java
public int numJewelsInStones(String J, String S) {
    int count = 0; // Initialize a counter for the number of jewels found in S
    int[] stoneCount = new int[128]; // Create an array to store the count of each character in S
    for (int i = 0; i < S.length(); i++) {
        stoneCount[S.charAt(i)]++; // Increment the count of each character in S
    }
    for (int i = 0; i < J.length(); i++) {
        count += stoneCount[J.charAt(i)]; // Add the count of each character in J to the counter
    }
    return count; // Return the final count of jewels found in S
}
```