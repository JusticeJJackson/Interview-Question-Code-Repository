# Solution 1 - Brute Force

The brute force approach involves generating all possible substrings of the given string and checking if each substring contains unique characters.


## Time Complexity: `O(n^3)`
## Space Complexity: `O(n)`



## Code

```java
public int lengthOfLongestSubstring(String s) {
    int n = s.length(); // get the length of the input string
    int ans = 0; // initialize a variable to store the length of the longest substring
    // iterate over every possible substring
    for (int i = 0; i < n; i++) {
        for (int j = i + 1; j <= n; j++) {
            // check if the current substring contains all unique characters
            if (allUnique(s, i, j)) {
                ans = Math.max(ans, j - i); // update ans if the current substring is longer
            }
        }
    }
    return ans; // return the length of the longest substring
}

// helper function to check if a substring has all unique characters
public boolean allUnique(String s, int start, int end) {
    Set<Character> set = new HashSet<>(); // create a hash set to store the characters
    for (int i = start; i < end; i++) { // iterate over the substring
        char ch = s.charAt(i); // get the current character
        if (set.contains(ch)) { // check if the character is already in the hash set
            return false; // return false if it is not unique
        }
        set.add(ch); // add the character to the hash set
    }
    return true; // return true if all characters are unique
}


```

# Solution 2 - Sliding Window

This solution involves using a sliding window approach with a HashSet to keep track of unique characters. The algorithm iterates through the string, updating the window boundaries based on character occurrences, and returns the length of the longest non-repeating substring.

## Time Complexity: `O(n)`
## Space Complexity: `O(n)`

## Code

```python
class Solution {
    public int lengthOfLongestSubstring(String s) {
        int n = s.length();
        Set<Character> set = new HashSet<>();
        int ans = 0, i = 0, j = 0;
        
        while (i < n && j < n) {
            if (!set.contains(s.charAt(j))) {
                set.add(s.charAt(j++));
                ans = Math.max(ans, j - i);
            } else {
                set.remove(s.charAt(i++));
            }
        }
        return ans;
    }
}



```