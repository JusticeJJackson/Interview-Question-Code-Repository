# Solution 1 - Backtracking

This solution utilizes a backtracking algorithm to explore all possible combinations of a binary string with '?' wildcards. 

## Time Complexity: `O(2^n)`
## Space Complexity: `O(n))`


## Code

```java
public static List<String> generateCombinations(String inputStr) {
        List<String> result = new ArrayList<>();
        backtrack(inputStr.toCharArray(), 0, result);
        return result;
    }

    private static void backtrack(char[] chars, int index, List<String> result) {
        if (index == chars.length) {
            result.add(new String(chars));
            return;
        }

        if (chars[index] == '?') {
            chars[index] = '0';
            backtrack(chars, index + 1, result);
            chars[index] = '1';
            backtrack(chars, index + 1, result);
            chars[index] = '?'; // Backtrack
        } else {
            backtrack(chars, index + 1, result);
        }
    }
```

# Solution 2 - Recursive String Builder

The second approach employs a recursive method to build all possible combinations of the binary string. 

## Time Complexity: `O(2^n)`
## Space Complexity: `O(n)`

## Code

```java

    public static List<String> generateCombinations(String inputStr) {
        List<String> result = new ArrayList<>();
        buildString(inputStr.toCharArray(), 0, new StringBuilder(), result);
        return result;
    }

    private static void buildString(char[] chars, int index, StringBuilder current, List<String> result) {
        if (index == chars.length) {
            result.add(current.toString());
            return;
        }

        if (chars[index] == '?') {
            current.append('0');
            buildString(chars, index + 1, current, result);
            current.setLength(current.length() - 1);
            
            current.append('1');
            buildString(chars, index + 1, current, result);
            current.setLength(current.length() - 1);
        } else {
            current.append(chars[index]);
            buildString(chars, index + 1, current, result);
            current.setLength(current.length() - 1);
        }
    }

```

# Solution 3 - Iterative Masking

This solution uses an iterative approach, applying bitwise masking to generate all combinations efficiently.

## Time Complexity: `O(2^n)`
## Space Complexity: `O(n)`

## Code

```java
    public static List<String> generateCombinations(String inputStr) {
        List<String> result = new ArrayList<>();
        int count = 1 << countWildcards(inputStr);
        
        for (int i = 0; i < count; i++) {
            result.add(applyMask(inputStr, i));
        }

        return result;
    }

    private static int countWildcards(String str) {
        int count = 0;
        for (char c : str.toCharArray()) {
            if (c == '?') {
                count++;
            }
        }
        return count;
    }

    private static String applyMask(String str, int mask) {
        StringBuilder result = new StringBuilder();
        int maskIndex = 0;

        for (char c : str.toCharArray()) {
            if (c == '?') {
                result.append((mask & (1 << maskIndex++)) == 0 ? '0' : '1');
            } else {
                result.append(c);
            }
        }

        return result.toString();
    }
}

```