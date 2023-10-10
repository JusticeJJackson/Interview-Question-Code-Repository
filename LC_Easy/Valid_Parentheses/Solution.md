# Solution 1 - Brute Force

This approach repeatedly removes matched pairs of parentheses from the string until no more replacements can be made. If the resulting string is empty, it means all parentheses have been matched, and the original string is valid. 

## Time Complexity: O(n^2)
## Space Complexity: O(1)

## Code

```java

public static boolean isValid(String s) {
    // Iterate through each possible pair of parentheses
    while (s.contains("()") || s.contains("[]") || s.contains("{}")) {
        s = s.replace("()", "");  // Replace matched pairs of parentheses with an empty string
        s = s.replace("[]", "");
        s = s.replace("{}", "");
    }

    // If the string becomes empty after removing all matched pairs, it is valid
    return s.isEmpty();
}

```

# Solution 2- Stack

This solution uses a stack to keep track of the opening parentheses encountered. Whenever a closing parentheses is encountered, it is compared to the top of the stack to see if they match. If they do, the opening parentheses are popped off the stack. If they don't, the string is not valid.


## Time Complexity: O(n)
## Space Complexity: O(n)


## Code

```java
public static boolean isValid(String s) {
    // instantiate a stack to keep track of opening parentheses
    Stack<Character> stack = new Stack<>();

    // iterate through each character in the string
    for (char c : s.toCharArray()) {
        // if the character is an opening parentheses, push it onto the stack
        if (c == '(' || c == '[' || c == '{') {
            stack.push(c);
        }
        // if the character is a closing parentheses, check if it matches the top of the stack
        else if (c == ')' && !stack.isEmpty() && stack.peek() == '(') {
            stack.pop();
        } else if (c == ']' && !stack.isEmpty() && stack.peek() == '[') {
            stack.pop();
        } else if (c == '}' && !stack.isEmpty() && stack.peek() == '{') {
            stack.pop();
        }
        // if the character is not a parentheses, return false (string is invalid)
        else {
            return false;
        }
    }

    // if the stack is empty, all parentheses have been matched and the string is valid
    return stack.isEmpty();
}
```