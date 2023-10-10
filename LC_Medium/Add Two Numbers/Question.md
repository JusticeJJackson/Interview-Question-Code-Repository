# Add Two Numbers

## Problem Statement

You are given two non-empty linked lists, `l1` and `l2`, representing two non-negative integers. The digits are stored in reverse order, and each of their nodes contains a single digit. Add the two numbers and return the sum as a linked list.

You may assume the two numbers do not contain any leading zero, except the number 0 itself.

## Example 1:

Input:

`l1 = [2, 4, 3], l2 = [5, 6, 4]`

Output:

`[7, 0, 8]`

## Example 2:

Input: 

`l1 = [0], l2 = [0]`

Output:

`[0]`

## Example 3:

Input: 

`l1 = [9,9,9,9,9,9,9], l2 = [9,9,9,9]`

Output: 

`[8,9,9,9,0,0,0,1]`

## Java Starter Code

```java
import java.util.Collections;
import java.util.List;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.*;

/*
 * This code contains a ListNode class that represents a singly-linked list, with each node containing a value (val) 
 * and a reference to the next node in the list (next). To create a new node, you can use the constructor ListNode(val).
 * 
 * Example usage:
 * 
 * // create a new node with value 2 and next reference set to null
 * ListNode node = new ListNode(2);
 * 
 * // create a new node with value 4 and next reference set to the node above
 * ListNode nextNode = new ListNode(4);
 * node.next = nextNode;
 * 
 * // get the value and next reference of a node
 * int val = node.val;
 * ListNode next = node.next;
 *
 * To access the next and val objects in the ListNode class, you can use the dot notation as shown above.
 */
public class Solution {
    
    /**
     * Definition for singly-linked list.
     */
    public static class ListNode {
        int val;
        ListNode next;
        ListNode(int val) {
            this.val = val;
        }
    }
    /**

    Problem Statement:

    You are given two non-empty linked lists representing two non-negative integers. The digits are stored in
    reverse order, and each of their nodes contains a single digit. Add the two numbers and return the sum as a
    linked list. You may assume the two numbers do not contain any leading zero, except the number 0 itself.
    
    Example 1:
    
    Input: l1 = [2,4,3], l2 = [5,6,4]
    Output: [7,0,8]
    
    Explanation: 342 + 465 = 807.
    
    Example 2:
    
    Input: l1 = [0], l2 = [0]
    Output: [0]
    Explanation: 0 + 0 = 0.
    
    Example 3:
    
    Input: l1 = [9,9,9,9,9,9,9], l2 = [9,9,9,9]
    Output: [8,9,9,9,0,0,0,1]
    Explanation: 9999999 + 9999 = 89990001.

    
    Constraints:
    The number of nodes in each linked list is in the range [1, 100].
    0 <= Node.val <= 9
    It is guaranteed that the list represents a number that does not have leading zeros.
    
    */
    public static ListNode addTwoNumbers(ListNode l1, ListNode l2) {
        //implement code here
        return null;
    }

    public static void main(String[] args) {
        // create input linked lists
        ListNode l1 = new ListNode(2);
        l1.next = new ListNode(4);
        l1.next.next = new ListNode(3);
        
        ListNode l2 = new ListNode(5);
        l2.next = new ListNode(6);
        l2.next.next = new ListNode(4);
        
        // expected output linked list
        ListNode expectedOutput = new ListNode(7);
        expectedOutput.next = new ListNode(0);
        expectedOutput.next.next = new ListNode(8);
        
        // test function
        ListNode output = addTwoNumbers(l1, l2);
        
        // compare results
        while (expectedOutput != null && output != null) {
            if (expectedOutput.val != output.val) {
                System.out.println("FAILED: expected " + expectedOutput.val + ", but got " + output.val);
                return;
            }
            expectedOutput = expectedOutput.next;
            output = output.next;
        }
        
        if (expectedOutput != null || output != null) {
            System.out.println("FAILED: output linked list does not have the same length as the expected output");
            return;
        }
        
        System.out.println("PASSED: all tests passed");
    }
}
```

## Python Starter Code

```python
'''
This code contains a ListNode class that represents a singly-linked list, with
each node containing a value (val)
and a reference to the next node in the list (next). To create a new node, you can
use the constructor ListNode(val).

Example usage:

# create a new node with value 2 and next reference set to null
    node = ListNode(2)

# create a new node with value 4 and next reference set to the node above
    next_node = ListNode(4)
    node.next = next_node

# get the value and next reference of a node
    val = node.val
    next = node.next

To access the next and val objects in the ListNode class, you can use the
dot notation as shown above.
'''
class ListNode:
    def __init__(self, val=0, next=None):
        self.val = val
        self.next = next

"""

Problem Statement:

You are given two non-empty linked lists representing two non-negative integers
The digits are stored in reverse order, and each of their nodes contains a single
digit. Add the two numbers and return the sum as a linked list. You may assume the
two numbers do not contain any leading zero, except the number 0 itself.

Example 1:

Input: l1 = [2,4,3], l2 = [5,6,4]
Output: [7,0,8]
Explanation: 342 + 465 = 807.

Example 2:

Input: l1 = [0], l2 = [0]
Output: [0]
Explanation: 0 + 0 = 0.

Example 3:

Input: l1 = [9,9,9,9,9,9,9], l2 = [9,9,9,9]
Output: [8,9,9,9,0,0,0,1]

Constraints:

The number of nodes in each linked list is in the range [1, 100].
0 <= Node.val <= 9
It is guaranteed that the list represents a number that does not have leading zeros.
"""
def addTwoNumbers(l1: ListNode, l2: ListNode) -> ListNode:
    # implementation here
    return None

def run_tests():
    # create input linked lists
    l1 = ListNode(2)
    l1.next = ListNode(4)
    l1.next.next = ListNode(3)
    l2 = ListNode(5)
    l2.next = ListNode(6)
    l2.next.next = ListNode(4)
    # expected output linked list
    expected_output = ListNode(7)
    expected_output.next = ListNode(0)
    expected_output.next.next = ListNode(8)
    # test function
    output = addTwoNumbers(l1, l2)
    # compare results
    while expected_output is not None and output is not None:
        if expected_output.val != output.val:
            print(f"FAILED: expected {expected_output.val}, but got {output.val}")
            return
        expected_output = expected_output.next
        output = output.next
    if expected_output is not None or output is not None:
        print("FAILED: output linked list does not have the same length as the expected output")
        return
    print("PASSED: all tests passed")

run_tests()
```

# [Link to Solution](Solution.md)


