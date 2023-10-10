# Daily Temperatures

## Problem Statement

Given an array of daily temperatures T, return an array ans such that ans[i] is the number of days you have to wait until a warmer temperature for the ith day appears. If there is no future day for which this is possible, put 0 instead.

## Example 1:

Input: 

[73,74,75,71,69,72,76,73]

Output: 

[1,1,4,2,1,1,0,0]

Explanation:

For the first day, the only higher temperature is on day 2, resulting in a wait time of 1. Similarly, for the second day, the next higher temperature is on day 3. The third day, however, has a wait time of 4 as the next highest temperature is on day 7, and so on.

## Example 2:

Input:

[30,40,50,60]

Output:

[1,1,1,0]

Explanation: 

Every day has a higher temperature in the future except the last one, which has no higher temperature.

## Example 3:

Input: 

[30,60,90]

Output: 

[1,1,0]

Explanation: For the first day, the next higher temperature is on day 2, and similarly for the second day. There is no higher temperature for the third day.


## Java Starter Code

```java
import java.util.Collections;
import java.util.List;
import java.util.ArrayList;
import java.util.Arrays;


class Solution {
       /**
    * Problem: Daily Temperatures
    *
    * Given an array of integers temperatures represents the daily temperatures, return an array answer 
    * such that answer[i] is the number of days you have to wait after the ith day to get a warmer temperature. 
    * If there is no future day for which this is possible, answer[i] == 0.
    *
    * Example 1:
    * Input: [73,74,75,71,69,72,76,73]
    * Output: [1,1,4,2,1,1,0,0]

    * Explanation: The answer for every index is calculated as follows:
    * 1. For i = 0: You cannot find a day with a higher temperature to the right, so answer[0] = 1.
    * 2. For i = 1: There is only one day with a higher temperature to the right, so answer[1] = 1.
    * 3. For i = 2: There are four days with a higher temperature to the right, so answer[2] = 4.
    * 4. For i = 3: There is only one day with a higher temperature to the right, so answer[3] = 2.
    * 5. For i = 4: There is only one day with a higher temperature to the right, so answer[4] = 1.
    * 6. For i = 5: There is only one day with a higher temperature to the right, so answer[5] = 1.
    * 7. For i = 6: You cannot find a day with a higher temperature to the right, so answer[6] = 0.
    * 8. For i = 7: You cannot find a day with a higher temperature to the right, so answer[7] = 0.
    *
    * Example 2:
    * Input: [30,40,50,60]
    * Output: [1,1,1,0]
    * Explanation: Every day has a higher temperature in the future except the last one, which has no higher temperature.
    *
    * Example 3:
    * 
    * Input: [30,60,90]
    * Output: [1,1,0]

    * Explanation: For the first day, the next higher temperature is on day 2, and similarly for the second day. There is no
    * higher temperature for the third day.
    *
    * Constraints:
    * - 1 <= temperatures.length <= 105
    * - 30 <= temperatures[i] <= 100

     */
    public static int[] dailyTemperatures(int[] temperatures) {
      //implement here   
      return null;
    }

    public static void main(String[] args) {
    int[][] temperaturesList = {{73, 74, 75, 71, 69, 72, 76, 73}, {30, 40, 50, 60}, {30, 60, 90}};
    int[][] expectedOutputs = {{1, 1, 4, 2, 1, 1, 0, 0}, {1, 1, 1, 0}, {1, 1, 0}};

    for (int i = 0; i < temperaturesList.length; i++) {
        int[] temperatures = temperaturesList[i];
        int[] expectedOutput = expectedOutputs[i];
        int[] output = dailyTemperatures(temperatures);
        if (Arrays.equals(output, expectedOutput)) {
            System.out.printf("PASS: dailyTemperatures(%s) = %s\n", Arrays.toString(temperatures), Arrays.toString(output));
        } else {
            System.out.printf("FAIL: dailyTemperatures(%s) = %s (expected %s)\n", Arrays.toString(temperatures), Arrays.toString(output), Arrays.toString(expectedOutput));
        }
    }
}
}


```

## Python Starter Code

```python
"""
You are given n tasks to complete and two people to assign them to.
Each task i is associated with a reward point for the first person, reward_1[i],
and a reward point for the second person, reward_2[i].
Both people work as a team to complete all the tasks, with the first person
completing k tasks and the second completing the remaining tasks (n-k).
Your task is to find the maximum combined reward points that can be gained by both people together.

Example 1:

Input: n=5, reward_1=[5,4,3,2,1], reward_2=[1,2,3,4,5], k=3
Output: 21

Explanation: With 5 tasks, the first person completes 3 tasks and the second person completes 2 tasks.
The maximum combined reward points are 21, obtained by the first person completing tasks 1-3 and the second person completing
tasks 4-5.

Example 2:

Input: n=4, reward_1=[8,4,5,2], reward_2=[3,1,6,7], k=2
Output: 29

Explanation: With 4 tasks, the first person completes 2 tasks and the second person completes 2 tasks.
The maximum combined reward points are 29, obtained by the first person completing tasks 1-2 and the second person completing tasks 3-4.

Example 3:

Input: n=2, reward_1=[10,12], reward_2=[8,6], k=1
Output: 18

Explanation: There are two tasks with reward values of [10,12] and [8,6], and only one task can be completed. The optimal solution
is to complete the first task with a reward of 10.


"""

def taskCompletion(n, reward_1, reward_2, k):
    #Implement Here
    return None

def testMethod():
    reward_1 = [[5,4,3,2,1], [8,4,5,2], [10,12]]
    reward_2 = [[1,2,3,4,5], [3,1,6,7], [8,6]]
    n = [5, 4, 2]
    k = [3, 2, 1]
    expectedOutputs = [21, 29, 18]
    for i in range(len(n)):
        r1 = reward_1[i]
        r2 = reward_2[i]
        e = expectedOutputs[i]
        o = taskCompletion(n[i], r1, r2, k[i])
        if o == e:
            print(f"PASS: taskCompletion({n[i]}, {r1}, {r2}, {k[i]}) = {o}")
        else:
            print(f"FAIL: taskCompletion({n[i]}, {r1}, {r2}, {k[i]}) = {o} (expected {e})")

testMethod()




```



