# Solution 1 - Modulo and Integer Division

One possible solution is to convert the integer to a string and check if the string is a palindrome. Another possible solution is to reverse the integer and compare it with the original integer. Here is an example implementation of the second solution:

## Time Complexity:  O(log10(x)) or O(n)
## Space Complexity:  O(1)
> The time complexity is O(log10(x)) because the number of digits in x is given by log10(x). This can also be written as O(n) where n is the number of digits inputted


## Code

```java
public boolean isPalindrome(int x) {
    if (x < 0) { // check if integer is negative
        return false; // return false if integer is negative
    }
    int reverse = 0; // initialize reversed integer
    int original = x; // store original integer
    while (x != 0) { // loop until all digits have been extracted
        int digit = x % 10; // extract rightmost digit
        reverse = reverse * 10 + digit; // add extracted digit to reversed integer
        x /= 10; // remove rightmost digit from original integer
    }
    return original == reverse; // check if original integer equals reversed integer
}
```
> This solution first checks if the input integer is negative, in which case it cannot be a palindrome. Then it initializes two variables: reverse to 0 (which will store the reverse of the integer) and original to x (which is the original input integer). It then loops through the digits of the input integer, extracting the last digit using the modulo operator and adding it to reverse after multiplying it by 10 to shift the digits one place to the left. Finally, it compares original with reverse to check if they are equal, which indicates that the input integer is a palindrome.

# Solution 2 - Convert to String

One Solution would be converting the integer to a string and then using two pointers to create a “sliding window” to see if the left and right pointers are equal, slowly moving in towards the middle. 

## Time Complexity: O(log10(x)) or O(n)
## Space Complexity: O(log10(x)) or O(n)
> The time and space complexity is O(log10(x)) because the number of digits in x is given by log10(x). This can also be written as O(n) where n is the number of digits inputted

## Code

```java
public boolean isPalindrome(int x) {
    String str = Integer.toString(x); // convert integer to string
    int left = 0; // initialize left pointer
    int right = str.length() - 1; // initialize right pointer
    while (left < right) { // loop while left is less than right
        if (str.charAt(left) != str.charAt(right)) { // check for mismatch
            return false; // return false if mismatch found
        }
        left++; // move left pointer forward
        right--; // move right pointer backward
    }
    return true; // return true if string is palindrome
}
```

# Solution 3 - Convert to string and use string methods to reverse


## Time Complexity: O(log10(x)) or O(n)
## Space Complexity: O(log10(x)) or O(n)
> The time and space complexity is O(log10(x)) because the number of digits in x is given by log10(x). This can also be written as O(n) where n is the number of digits inputted

## Code

```java
public boolean isPalindrome(int x) {
    String str = Integer.toString(x); // convert integer to string
    int len = str.length(); // get length of string
    String reverse = ""; // initialize reversed string
    for (int i = len - 1; i >= 0; i--) {
        reverse = reverse + str.charAt(i); // build reversed string
    }
    return str.equals(reverse); // check if original string equals reversed string
}

```