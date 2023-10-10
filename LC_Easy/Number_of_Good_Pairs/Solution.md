# Solution 1 - Brute Force

This solution iterates over all pairs of elements in the array, checking if each pair is a good pair.

## Time Complexity: O(n^2)
## Space Complexity: O(1)

## Code

```java
public class Solution1 {
    public static int numIdenticalPairs(int[] nums) {
        int count = 0;

        for (int i = 0; i < nums.length - 1; i++) {
            for (int j = i + 1; j < nums.length; j++) {
                if (nums[i] == nums[j]) {
                    count++;
                }
            }
        }

        return count;
    }
}
```

# Solution 2 - HashMap

Utilizing a HashMap to store the frequency of each number, this solution counts the number of good pairs by considering the combinations of frequencies. It has a time complexity of O(n) and a space complexity of O(n).

## Time Complexity: O(n)
## Space Complexity: O(n)

## Code

```java
import java.util.HashMap;
import java.util.Map;

public class Solution {
    public static int numIdenticalPairs(int[] nums) {
        int count = 0;
        Map<Integer, Integer> frequencyMap = new HashMap<>();

        for (int num : nums) {
            frequencyMap.put(num, frequencyMap.getOrDefault(num, 0) + 1);
        }

        for (int frequency : frequencyMap.values()) {
            count += frequency * (frequency - 1) / 2;
        }

        return count;
    }
}
```

# Solution 3 - Sorting

By sorting the array, this solution groups identical numbers together. It then calculates the count of good pairs based on the runs of identical numbers. 

## Time Complexity: O(nlog(n))
## Space Complexity: O(1)

## Code

```java
import java.util.Arrays;

public class Solution {
    public static int numIdenticalPairs(int[] nums) {
        Arrays.sort(nums);
        int count = 0;
        int currentRun = 1;

        for (int i = 1; i < nums.length; i++) {
            if (nums[i] == nums[i - 1]) {
                currentRun++;
            } else {
                count += currentRun * (currentRun - 1) / 2;
                currentRun = 1;
            }
        }

        count += currentRun * (currentRun - 1) / 2;

        return count;
    }
}

```