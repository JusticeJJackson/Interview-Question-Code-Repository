# Solution 1

The playSong method randomly selects a song from the playlist by generating a random index (randomPos). It then removes the selected song from the playlist, which is an O(n) operation since it requires shifting elements to fill the gap. The selected song is enqueued in the lastPlayed queue. If the size of the lastPlayed queue exceeds k, it dequeues the oldest song from the queue and adds it back to the playlist. The method finally returns the randomly selected song. This approach ensures that the selected song has not been played in the last k songs, but the time complexity is O(n) due to the removal operation.

## Time Complexity: `O(n)`
## Space Complexity: `O(n)`

## Code

```java
import java.util.ArrayList;
import java.util.LinkedList;
import java.util.Queue;
import java.util.Random;

public class PlaylistRandomizer {
    private ArrayList<String> songs;
    private int k;
    private Queue<String> lastPlayed;

    public PlaylistRandomizer(ArrayList<String> songs, int k) {
        this.songs = songs;
        this.k = k;
        this.lastPlayed = new LinkedList<>();
    }

    public String playSong() {
        Random random = new Random();
        int randomPos = random.nextInt(songs.size());



        // Pop the randomly song from the array
        // O(n) because we are removing from the middle of the array
        String selectedSong = songs.remove(randomPos);

        // Enqueue the selected song
        lastPlayed.offer(selectedSong);

        // Check if the lastPlayed queue size exceeds k, dequeue if necessary
        if (lastPlayed.size() > k) {
            songs.add(lastPlayed.poll());
        }

        return selectedSong;
    }
}
```

# Solution 2 - Optiminzed

The playSong method randomly selects a song from the playlist by generating a random index (randomPos). It then swaps the selected song with the last song in the playlist using a temporary variable. After that, it removes the last song from the playlist and enqueues it in the lastPlayed queue. If the size of the lastPlayed queue exceeds k, it dequeues the oldest song from the queue and adds it back to the playlist. The method finally returns the randomly selected song. This process ensures that the selected song has not been played in the last k songs, and the time complexity is O(1).

## Time Complexity: `O(1)`
## Space Complexity: `O(n)`


## Code

```java
import java.util.ArrayList;
import java.util.LinkedList;
import java.util.Queue;
import java.util.Random;

public class PlaylistRandomizer {
    private ArrayList<String> songs;
    private int k;
    private Queue<String> lastPlayed;

    public PlaylistRandomizer(ArrayList<String> songs, int k) {
        this.songs = songs;
        this.k = k;
        this.lastPlayed = new LinkedList<>();
    }

    public String playSong() {
        Random random = new Random();
        int randomPos = random.nextInt(songs.size());

        // Swap the randomly selected song with the last song
        String temp = songs.get(randomPos);
        songs.set(randomPos, songs.get(songs.size() - 1));
        songs.set(songs.size() - 1, temp);

        // Pop the last song from the array
        // O(1) because we are removing from the end of the array
        String selectedSong = songs.remove(songs.size() - 1);

        // Enqueue the selected song
        lastPlayed.offer(selectedSong);

        // Check if the lastPlayed queue size exceeds k, dequeue if necessary
        if (lastPlayed.size() > k) {
            songs.add(lastPlayed.poll());
        }

        return selectedSong;
    }
}

```