# Number of Good Pairs

## Problem Statement

Given an array of integers `nums`. A pair `(i,j)` is called good if `nums[i] == nums[j]` and `i < j`. Return the number of good pairs. 

## Example 1:

Input:

`nums` = `[1,2,3,1,1,3]`

Output:

`4`

> Explanation: There are 4 good pairs `(0,3)`, `(0,4)`, `(3,4)`, `(2,5)` 0-indexed.

## Example 2:

Input:

`nums` = `[1,1,1,1]`

Output:

`6`

> Explanation: Each pair in the array are good.

## Example 3:

Input:

`nums` = `[1,2,3]`

Output:

`0`

> Explanation: There are no good pairs in the array

## Java Starter Code

```java
import java.util.*;

public class Solution {

    static class PlaylistRandomizer {
        private List<String> songs;
        private int k;
        private List<String> playedSongs;

        /**
         * Constructor for PlaylistRandomizer.
         *
         * @param songs an array of songs represented as strings
         * @param k     an integer representing the constraint on repeated songs
         */
        public PlaylistRandomizer(String[] songs, int k) {
            this.songs = new ArrayList<>(Arrays.asList(songs));
            this.k = k;
            this.playedSongs = new ArrayList<>();
        }

        /**
         * Plays a random song from the playlist, ensuring it hasn't been played in the last k songs.
         *
         * @return the name of the currently played song
         */
        public String playSong() {
            if (songs.isEmpty()) {
                System.out.println("No more songs in the playlist.");
                return null;
            }

            Random random = new Random();
            int randomIndex = random.nextInt(songs.size());
            String currentSong = songs.remove(randomIndex);
            playedSongs.add(currentSong);

            if (playedSongs.size() > k) {
                String removedSong = playedSongs.remove(0);
                songs.add(removedSong);
            }

            System.out.printf("Playing song: %s, Available songs: %s\n", currentSong, songs);
            return currentSong;
        }
    }

    /**
     * Tests the PlaylistRandomizer class with some example inputs.
     *
     * @param args the command line arguments (unused)
     */
    public static void main(String[] args) {
        String[] playlist = {"A", "B", "C", "D", "E"};
        PlaylistRandomizer playlistRandomizer = new PlaylistRandomizer(playlist, 3);

        for (int i = 0; i < 7; i++) {
            playlistRandomizer.playSong();
        }
    }
}

```

## Python Starter Code

```python
"""
Given an array of integers `nums`. A pair `(i,j)` is called good if `nums[i] == nums[j]` and `i < j`.
Return the number of good pairs.

Example 1:

Input: nums = [1,2,3,1,1,3]
Output: 4
Explanation: There are 4 good pairs (0,3), (0,4), (3,4), (2,5) 0-indexed.

Example 2:

Input: nums = [1,1,1,1]
Output: 6
Explanation: Each pair in the array are good.

Example 3:

Input: nums = [1,2,3]
Output: 0
Explanation: There are no good pairs in the array
"""


def numIdenticalPairs(nums):
    # Implement solution here
    return 0

def test():
    nums_inputs = [[1, 2, 3, 1, 1, 3], [1, 1, 1, 1], [1, 2, 3]]
    expected_outputs = [4, 6, 0]

    for nums_input, expected_output in zip(nums_inputs, expected_outputs):
        output = numIdenticalPairs(nums_input)
        if output == expected_output:
            print('PASS: numIdenticalPairs({}) = {}'.format(nums_input, output))
        else:
            print('FAIL: numIdenticalPairs({}) = {} (expected {})'.format(nums_input, output, expected_output))

test()

```


# [Link to Solution](Solution.md)


