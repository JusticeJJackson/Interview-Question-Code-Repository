# Solution 1 - Naive Approach

This approach compares the frequency of characters between the two strings to determine the difference.

## Time Complexity: `O(n)`
## Space Complexity: `O(1)`


## Code

```java
public char findTheDifference(String s, String t) {
    int[] freq = new int[26]; // initialize an array to store frequency of characters
    
    // count the frequency of characters in s
    for (char c : s.toCharArray()) {
        freq[c - 'a']++; // increment the count of the character in the frequency array
    }
    
    // check the frequency of characters in t and find the extra character
    for (char c : t.toCharArray()) {
        if (--freq[c - 'a'] < 0) { // decrement the count of the character in the frequency array
            return c; // return the character that is not in s
        }
    }
    
    return ' '; // default return value if no extra character is found
}
```

# Solution 2 - HashMap

This approach uses a HashMap to store the frequency of characters in string s, and then iterates through string t to check if the character is present in the HashMap and has a non-zero frequency. If so, it decrements the frequency, otherwise it returns the character.

## Time Complexity: `O(n)`
## Space Complexity: `O(n)`

## Code

```java
public char findTheDifference(String s, String t) {
    // initialize a frequency map for characters in s
    Map<Character, Integer> freq = new HashMap<>();
    for (char c : s.toCharArray()) {
        freq.put(c, freq.getOrDefault(c, 0) + 1);
    }
    // iterate through characters in t
    for (char c : t.toCharArray()) {
        if (!freq.containsKey(c) || freq.get(c) == 0) {
            return c; // return the character that is not in s
        }
        freq.put(c, freq.get(c) - 1); // update the frequency of c in s
    }
    return ' '; // default return value
}
```

# Solution 3 - Bit Manipulation

This approach XORs the ASCII values of all characters in both strings. The resulting value is the ASCII value of the added character.

## Time Complexity: `O(n)`
## Space Complexity: `O(1)`

## Code

```java
public char findTheDifference(String s, String t) {
    int result = 0; // initialize the XOR result
    for (char c : s.toCharArray()) {
        result ^= c; // XOR each character in s
    }
    for (char c : t.toCharArray()) {
        result ^= c; // XOR each character in t
    }
    return (char) result; // cast the result back to a character and return it
}

```