Monitors what is currently playing in your
[Clementine](http://www.clementine-player.org/) music player, by hooking into
the relevant dbus signals to detect state change.

(This is the first python script I've ever written.)

Whenever the state of the player changes, this script outputs a single line of
pipe (|) delimited fields indicating the state and song info.

When the player is stopped, it will write the single field:

    stopped

If a song is currently playing, it will write the following fields:

1. State, which is either `playing` or `paused`.
2. The track number.
3. The title of the song.
4. The artist for the song.
5. The album for the song.
6. The duration of the song in minutes and seconds (`m:ss`).
7. The full path and file name.
8. File containing the current cover image (if available).

e.g. `playing|20|So Was Red|Thomas Newman|The Shawshank Redemption|2:46|/path/to/music/Thomas Newman/The Shawshank Redemption/20 So Was Red.mp3|/tmp/clementine-art-l10931.jpg`

(MIT License)
