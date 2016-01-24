# RhinoBot's commands

### `!summon`
Summon the music bot into your current voice channel. The bot should auto-summon itself into the owner's current voice channel when joining if the owner is in a voice channel.

**Note**: RhinoBot cannot move voice channels by itself yet.  You will have to either drag RhinoBot to a different voice channel in Discord, or restart RhinoBot and summon it to a different channel.

##### Permissions: Owner only
##### Typical output: None
##### Arguments: None

---

### `!id`
This will print out your Discord user ID into the chat. This command cannot print IDs for other users.

##### Permissions: Everyone
##### Typical output: `@yournamehere, your id is <ID>`
##### Arguments: None

---

### `!whitelist <status> <user>`
This command will add or remove the specified user from the whitelist.

##### Permissions: Owner only
##### Typical output: None
##### Arguments:
* `<status>`: Status to set the user as in the whitelist. Accepts `+`, `-`, `add` or `remove`.
* `<user>`: User to add or remove from the whitelist as an @mention.

---

### `!blacklist <status> <user>`
This command will add or remove the specified user from the blacklist.

##### Permissions: Owner only
##### Typical output: None
##### Arguments:
* `<status>`: Status to set the user as in the backlist. Accepts `+`, `-`, `add` or `remove`.
* `<user>`: User to add or remove from the blacklist as an @mention.

---

### `!play [url]`
Add a song to the queue!

##### Permissions: Everyone
##### Typical output:
* For standalone songs: `@yournamehere, Enqueued <song title> to be played. Position in queue: <position in queue> - estimated time until playing: <ETA>`
* For YouTube playlists: `Gathering playlist information for <song count> songs.` + default output for standalone songs for first song (after fetching playlist is complete)

##### Arguments:
* `[url]`: URL to play. This can be from a wide variety of sites, many sites supported by `youtube_dl` are supported by RhinoBot. [youtube_dl supported songs list](https://rg3.github.io/youtube-dl/supportedsites.html). Will output help if omitted.

---

### `!pause`
Pause the bot.

##### Permissions: Everyone
##### Typical output: None
##### Arguments: None

---

### `!resume`
Undo `!pause` and resume playback.

##### Permissions: Everyone
##### Typical output: None
##### Arguments: None

---

### `!queue`
Output the current queue of songs.

##### Permissions: Everyone
##### Typical output:
```
Now Playing: <song title> added by <user who added song> [<current song play times>]

1. <song title> added by <user who added song>
```
##### Arguments: None

---

### `!volume [amount]`
Change the current volume for all users of the bot. **NOT RECCOMMENDED.** Users can adjust RhinoBot's volume for themselves.

##### Permissions: Everyone
##### Typical output:
* `[amount]` not included: `@yournamehere, Current volume: <current volume>`
* `[amount]`: `@yournamehere, updated volume from <old value> to <new value>`
##### Arguments:
* `[amount]`: Amount to change volume by/to. Accepts `1 - 100`, `+n` or `-n` where `n` is amount to change volume by.

---

### `!skip`
Vote to skip the current song. When owners use this, it instantly skips the song.

##### Permissions: Everyone/Owner only
##### Typical output:
```
@yourname, your skip for <song name here> was acknowledged.
<amount of votes left> more people are required to vote to skip this song.
```
##### Arguments: None

---

### `!shuffle`
Shuffle the queue.

##### Permissions: Everyone
##### Typical output: `*shuffleshuffleshuffle*`
##### Arguments: None

---

### `!clear`
Empty the queue.

##### Permissions: Owner only
##### Typical output: None
##### Arguments: None

---

### `!joinserver <Discord join URL>`
Instructs the bot to join a server

##### Permissions: Owner only
##### Typical output: None
##### Arguments:
* `<Discord join URL>`: Server join URL for the bot to join.