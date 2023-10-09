# Solution 1 - Brute Force

This solution involves iterating through the input linked lists, converting their values to integers, adding them together, and then creating a new linked list with the resulting digits.


## Time Complexity: O(n)
## Space Complexity: O(n)



## Code

```java
public static ListNode addTwoNumbers(ListNode l1, ListNode l2) {
    // Create a dummy node with a value of 0 to be the head of the result list
    ListNode dummy = new ListNode(0);

    // Set the current node to the dummy node
    ListNode curr = dummy;

    // Initialize a carry variable to 0
    int carry = 0;

    // Loop through both input linked lists until they both are null
    while (l1 != null || l2 != null) {
        // If either list is null, set its value to 0
        int x = (l1 != null) ? l1.val : 0;
        int y = (l2 != null) ? l2.val : 0;

        // Add the values of the two nodes and the carry value
        int sum = carry + x + y;

        // Update the carry value
        carry = sum / 10;

        // Create a new node with the ones digit of the sum and set it as the next node of the current node
        curr.next = new ListNode(sum % 10);

        // Move the current node to the next node
        curr = curr.next;

        // Move the pointers to the next nodes of the input lists if they are not null
        if (l1 != null) l1 = l1.next;
        if (l2 != null) l2 = l2.next;
    }

    // If there is a carry after the loop, create a new node with its value and set it as the next node of the current node
    if (carry > 0) {
        curr.next = new ListNode(carry);
    }

    // Return the next node of the dummy node, which is the head of the result list
    return dummy.next;
}


```

# Solution 2 - Recursion

This solution adds the values of the nodes of the two linked lists along with the carry value recursively. The sum is computed as (l1.val + l2.val + carry) % 10 and the carry is updated as (l1.val + l2.val + carry) / 10. The new node is created with the sum as its value and its next pointer is set to the result of calling the function recursively on the next nodes of the input lists. The base case is when both input lists are null and the carry is 0, in which case null is returned. The head of the result list is returned as the result of calling the function on the head nodes of the input lists with an initial carry of 0.


## Time Complexity: O(n)
## Space Complexity O(n)

## Code

```java
public static ListNode addTwoNumbers(ListNode l1, ListNode l2) {
    // Call the helper function with an initial carry of 0
    return addTwoNumbersHelper(l1, l2, 0);
}

private static ListNode addTwoNumbersHelper(ListNode l1, ListNode l2, int carry) {
    // Base case: if both input lists and the carry value are null, return null
    if (l1 == null && l2 == null && carry == 0) {
        return null;
    }
    
    // Get the value of the current node in each input list, or 0 if the list is null
    int x = (l1 != null) ? l1.val : 0;
    int y = (l2 != null) ? l2.val : 0;
    
    // Add the values of the current nodes and the carry value
    int sum = carry + x + y;
    
    // Create a new node with the ones digit of the sum
    ListNode node = new ListNode(sum % 10);
    
    // Recursively call the helper function with the next nodes of the input lists and the carry value
    node.next = addTwoNumbersHelper((l1 != null) ? l1.next : null,
                                    (l2 != null) ? l2.next : null,
                                    sum / 10);
                                    
    // Return the new node
    return node;
}
```

# Solution 3 - Iterative

The code adds two numbers represented by linked lists, digit by digit. It iterates through each node in both linked lists, adds the corresponding values, and keeps track of any carry. A new node is created for the result and the carry is carried over to the next iteration. If there is still a carry after iterating through both linked lists, a new node is created with the value of the carry. The final result is the linked list that starts with the second node of the dummy node.

## Time Complexity: O(n)
## Space Complexity: O(n)

## Code

```java
public ListNode addTwoNumbers(ListNode l1, ListNode l2) {
    // Create a dummy node to be the head of the result list
    ListNode dummy = new ListNode(0);
    // Set the current node to the dummy node
    ListNode curr = dummy;
    // Initialize a carry variable to 0
    int carry = 0;
    
    // Loop through both input linked lists until they both are null
    while (l1 != null || l2 != null) {
        // If either list is null, set its value to 0
        int val1 = (l1 != null) ? l1.val : 0;
        int val2 = (l2 != null) ? l2.val : 0;
        // Add the values of the two nodes and the carry value
        int sum = val1 + val2 + carry;
        // Update the carry value
        carry = sum / 10;
        // Create a new node with the ones digit of the sum and set it as the next node of the current node
        curr.next = new ListNode(sum % 10);
        // Move the current node to the next node
        curr = curr.next;
        // Move the pointers to the next nodes of the input lists if they are not null
        if (l1 != null) l1 = l1.next;
        if (l2 != null) l2 = l2.next;
    }
    
    // If there is a carry after the loop, create a new node with its value and set it as the next node of the current node
    if (carry > 0) {
        curr.next = new ListNode(carry);
    }
    
    // Return the next node of the dummy node, which is the head of the result list
    return dummy.next;
}



```