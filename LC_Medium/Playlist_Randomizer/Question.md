# Playlist Randomizer

## Problem Statement

You are tasked with creating a class, `PlaylistRandomizer`, to manage the playback of songs in a playlist. The constructor of this class takes two inputs: an array of songs, represented as strings (e.g., `["A", "B", "C", "D", "E"]`), and an integer k. The class has one method, playSong, which plays a random song from the array. However, there's a catch—the randomly selected song cannot have been played in the last k songs.

# Exmaple:

Create an instance of `PlaylistRandomizer` with songs `["A", "B", "C", "D", "E"]` and `k = 3`

`playlist = PlaylistRandomizer(["A", "B", "C", "D", "E"], 3)`

> Play a random song (let's assume it's "B")

`print(playlist.playSong())  # Prints: B, Available songs: A, C, D, E`

> Play another random song (let's assume it's "D")

`print(playlist.playSong())  # Prints: D, Available songs: A, C, E`

> Play another random song (let's assume it's "A")

`print(playlist.playSong())  # Prints: A, Available songs: C, E`

> Play another random song (let's assume it's "E")

`print(playlist.playSong())  # Prints: E, Available songs: B, C`

> Play another random song (let's assume it's "C")

`print(playlist.playSong())  # Prints: C, Available songs: B, D, E`

## Java Starter Code

```java
import java.util.ArrayList;
import java.util.List;
import java.util.Random;

/**
 * Playlist Randomizer
 *
 * Problem Statement:
 * You are tasked with creating a class, PlaylistRandomizer, to manage the playback of songs in a playlist.
 * The constructor of this class takes two inputs: an ArrayList of songs represented as strings
 * (e.g., ["A", "B", "C", "D", "E"]), and an integer k.
 * The class has one method, playSong, which plays a random song from the array.
 * However, there's a catch—the randomly selected song cannot have been played in the last k songs.
 *
 * Example:
 *
 * Create an instance of PlaylistRandomizer with songs ["A", "B", "C", "D", "E"] and k = 3
 *
 * PlaylistRandomizer playlist = new PlaylistRandomizer(["A", "B", "C", "D", "E"], 3);
 *
 * // Play a random song (let's assume it's "B")
 * System.out.println(playlist.playSong());  // Prints: B, Available songs: A, C, D, E
 *
 * // Play another random song (let's assume it's "D")
 * System.out.println(playlist.playSong());  // Prints: D, Available songs: A, C, E
 *
 * // Play another random song (let's assume it's "A")
 * System.out.println(playlist.playSong());  // Prints: A, Available songs: C, E
 *
 * // Play another random song (let's assume it's "E")
 * System.out.println(playlist.playSong());  // Prints: E, Available songs: B, C
 *
 * // Play another random song (let's assume it's "C")
 * System.out.println(playlist.playSong());  // Prints: C, Available songs: B, D, E
 */
public class Solution {

    static class PlaylistRandomizer {

        /**
         * Constructor for PlaylistRandomizer.
         *
         * @param songs an ArrayList of songs represented as strings
         * @param k     an integer representing the constraint on repeated songs
         */
        public PlaylistRandomizer(ArrayList<String> songs, int k) {
            // Implementation of constructor
        }

        /**
         * Plays a random song from the playlist, ensuring it hasn't been played in the last k songs.
         *
         * @return the name of the currently played song
         */
        public String playSong() {
            // Implementation of playSong method
            return null;
        }
    }

    /**
     * Tests the PlaylistRandomizer class with some example inputs.
     *
     * @param args the command line arguments (unused)
     */
    public static void main(String[] args) {
        ArrayList<String> playlist = new ArrayList<>(List.of("A", "B", "C", "D", "E"));
        PlaylistRandomizer playlistRandomizer = new PlaylistRandomizer(playlist, 3);

        for (int i = 0; i < 7; i++) {
            playlistRandomizer.playSong();
        }
    }
}


```

## Python Starter Code

```python
import random

class Solution:

    """
    Playlist Randomizer
    
    Problem Statement:
    You are tasked with creating a class, PlaylistRandomizer, to manage the playback of songs in a playlist.
    The constructor of this class takes two inputs: an ArrayList of songs represented as strings
    (e.g., ["A", "B", "C", "D", "E"]), and an integer k.
    The class has one method, playSong, which plays a random song from the array.
    However, there's a catch—the randomly selected song cannot have been played in the last k songs.
    
    Example:
    
    Create an instance of PlaylistRandomizer with songs ["A", "B", "C", "D", "E"] and k = 3
    
    playlist = PlaylistRandomizer(["A", "B", "C", "D", "E"], 3)
    
    # Play a random song (let's assume it's "B")
    print(playlist.playSong())  # Prints: B, Available songs: A, C, D, E
    
    # Play another random song (let's assume it's "D")
    print(playlist.playSong())  # Prints: D, Available songs: A, C, E
    
    # Play another random song (let's assume it's "A")
    print(playlist.playSong())  # Prints: A, Available songs: C, E
    
    # Play another random song (let's assume it's "E")
    print(playlist.playSong())  # Prints: E, Available songs: B, C
    
    # Play another random song (let's assume it's "C")
    print(playlist.playSong())  # Prints: C, Available songs: B, D, E
    """

    class PlaylistRandomizer:

        def __init__(self, songs, k):
            """
            Constructor for PlaylistRandomizer.

            :param songs: an array of songs represented as strings
            :param k: an integer representing the constraint on repeated songs
            """
            pass

        def play_song(self):
            """
            Plays a random song from the playlist, ensuring it hasn't been played in the last k songs.

            :return: the name of the currently played song
            """
            pass

    def test_playlist_randomizer(self):
        """
        Tests the PlaylistRandomizer class with some example inputs.
        """
        playlist = ["A", "B", "C", "D", "E"]
        playlist_randomizer = self.PlaylistRandomizer(playlist, 3)

        for _ in range(7):
            result = playlist_randomizer.play_song()
            print('Current Song: {}, Available Songs: {}'.format(result, ', '.join(playlist_randomizer.songs)))


solution = Solution()
solution.test_playlist_randomizer()
```


# [Link to Solution](Solution.md)


