# Solution 1 - Brute Force

This solution employs a brute-force approach by iterating over all pairs of elements in the array, calculating the sum for each pair, and keeping track of the pair with the closest sum to the target. 

## Time Complexity: `O(n^2)`
## Space Complexity: `O(1)`


## Code

```java
public static int[] twoSumClosestBruteForce(int[] nums, int target) {
    int[] result = new int[2];
    int minDiff = Integer.MAX_VALUE;

    for (int i = 0; i < nums.length - 1; i++) {
        for (int j = i + 1; j < nums.length; j++) {
            int sum = nums[i] + nums[j];
            int diff = Math.abs(sum - target);
            if (diff < minDiff) {
                minDiff = diff;
                result[0] = i;
                result[1] = j;
            }
        }
    }

    return result;
}
```

# Solution 2 - Sorting with Two Pointers

This approach first sorts the input array and then uses two pointers to explore pairs. By moving the pointers based on the sum of the current pair, the algorithm efficiently converges towards the closest sum to the target

## Time Complexity: `O(nlog(n))`
## Space Complexity: `O(1)`

## Code

```java
public static int[] twoSumClosestSorting(int[] nums, int target) {
    int[] result = new int[2];
    int minDiff = Integer.MAX_VALUE;

    Arrays.sort(nums);

    int left = 0;
    int right = nums.length - 1;

    while (left < right) {
        int sum = nums[left] + nums[right];
        int diff = Math.abs(sum - target);

        if (diff < minDiff) {
            minDiff = diff;
            result[0] = left;
            result[1] = right;
        }

        if (sum < target) {
            left++;
        } else {
            right--;
        }
    }

    return result;
}

```

# Solution 3 - HashMap for Complements

This solution utilizes a HashMap to store complements for each element in the array as it iterates through. When a complement is found, the algorithm checks if it forms a pair with a closer sum to the target. 

## Time Complexity: O(n)
## Space Complexity: {INSERT SPACE COMPLEXITY}

## Code

```java
public static int[] twoSumClosestHashMap(int[] nums, int target) {
    Map<Integer, Integer> complementMap = new HashMap<>();
    int[] result = new int[2];
    int minDiff = Integer.MAX_VALUE;

    for (int i = 0; i < nums.length; i++) {
        int complement = target - nums[i];
        if (complementMap.containsKey(complement)) {
            int diff = Math.abs(nums[i] - complement);
            if (diff < minDiff) {
                minDiff = diff;
                result[0] = complementMap.get(complement);
                result[1] = i;
            }
        }

        complementMap.put(nums[i], i);
    }

    return result;
}
```