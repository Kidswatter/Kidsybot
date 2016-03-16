Interacting with MusicBot is done via chat commands.  The bot does not take commands via DMs, with the exception of the `joinserver` command from the owner of the bot.  The owner may have changed the bot's command prefix from the default `!` to something else, as to not interfere with another bot that uses `!` for commands.  Most messages are deleted after some time, as not to fill up the chat with stale information.

## Command format
### `!command [optional argument] [multiple | choice | argument] <required argument>`
Basic description of what the command does.  Additional information may be provided.

If a command has a second set of usage text, that means there's another way to use the command.

When using arguments, **do not include the brackets** (**[ ]** or **< >**).  These are for indicating the type of argument.  If an argument starts with an `@`, i.e. **`[@user]`**, this indicates that the argument should be a user mention, not just the name of the user.  Discord names are not unique, any user can change their name to anything at any time, including the name of other users.

**Note**: Possible exception or caveat that the user should take note of when using the command.  For example: `!command` is not a real command, just a place holder to demonstrate the command format.

## Commands

### `!play <song link>`
### `!play <song text to search for>`
Add a song to the queue, or add the first youtube result for the provided search text.

**Note**: In the `develop` version of the bot, to search for a song, you use `!play ytsearch:my_search_query`
##### Arguments:
- `<song link>` A link to some song.  **Links are not limited to youtube**, see [this FAQ entry](https://github.com/SexualRhinoceros/MusicBot/wiki/FAQ#is-some-other-website-or-service-supported).
  - Example: `!play https://www.youtube.com/watch?v=gbv-yqqmLH0`
- *or...*
- `<song text to search for>` Some search query you want the bot to look up on youtube.
  - Example: `!play I ran seagulls` will play *I Ran* by *A Flock of Seagulls*.

---

### `!queue`
Prints the bot's current queue in chat.

---

### `!np`
Prints the currently playing song in the chat.

---

### `!skip`
Vote to skip the current song, or if you're the owner, skip the current song.

Skip settings may vary, but the two conditions are either a static number of votes required, or a percent of undefeaned users in voice chat.  These values are set by the owner, and the bot will announce how many votes are required to skip when the command is used.  As previously stated, the owner can skip at any time.

---

### `!search [service] [number] <query>`
Interactively search for a video to add to the queue.  The bot will look up `number` videos and prompts the user to accept or deny each video.  This command times out after 30 seconds, and has a hard limit of 10 max search items.

##### Arguments:
- `[service]` Optionally specify a service to search for videos on.  The default is youtube, but it can be any of the following (the short ones are abbreviations):
  - `youtube`, `soundcloud`, `yahoo`, or `yt`, `sc`, `yh` if you don't want to type the whole thing.
- `[number]` Optionally specify a number of video results to prompt.  The default is 1 and is limited to 10, althought this may be increased in the future.

---

### `!shuffle`
Shuffles the queue.

---

### `!clear`
Clears the queue.

---

### `!pause`
Pauses the playback of the current song.

---

### `!resume`
Resumes playback of a paused song.

---

### `!volume [amount]`
Changes the volume of the current song, or prints the current volume if an `amount` is not specified.  This affects all users.

##### Arguments:
- `[amount]` If specified, set the volume to the given level (a number between `1` and `100`), or a relative amount to the current level (`+5` or `-10`, etc).

---

### `!summon`
Call the bot to your voice channel.  Obviously, you must be in a voice channel to use this command.

The bot can move between voice channels on a server (that it has permission to join), but not across servers.  If the bot lacks permissions to join, either grant the bot permission or just drag the bot into the channel.

**Note:** Typically, you don't need to use this command if you enable the `AutoSummon` option.  That makes the bot attempt to join the owner's voice channel on startup.

---

### `!clean <amount>`
Search through `amount` of messages and remove any sent by the bot.  If the bot has **Manage Messages** permission in the channel, the bot will also remove message that invoked bot commands (messages that were commands for the bot, `!play`, `!np`, etc).

**Note:** `amount` is not how many messages to remove, it's how many messages to *search through* to remove.

##### Arguments:
- `<amount>` Number of messages to search through to remove the bots own messages (and messages invoking the bot if the bot has **Manage Messages** permissions).

---

### `!blacklist <status> <@user>`
Add or remove a user from the bot blacklist.  Blacklisted users cannot use any bot commands.  This overrides any permissions settings set in `permissions.ini`.  The owner cannot be blacklisted.  Listing multiple users is not supported, but may be in a future update.

**Note:** Remember to @mention the user when using this command.

##### Arguments:
- `<status>` Whether to add or remove a user.  Accepted values are `+`, `-`, `add`, and `remove`.
- `<@user>` Target user.  Must be a mention.

---

### `!whitelist <status> <@user>`
Add or remove a user from the bot whitelist.  Similar to the blacklist option, however the whitelist must be enabled for this to have any effect.  Permissions settings in `permissions.ini` **do not** override this.

**Note:** Remember to @mention the user when using this command, and to enable the `WhiteListCheck` option in `options.ini` for this command to have any effect.

##### Arguments:
- `<status>` Whether to add or remove a user.  Accepted values are `+`, `-`, `add`, and `remove`.
- `<@user>` Target user.  Must be a mention.

---

### `!help`
Prints a basic list of commands.  This command is more or less a place holder until a nice, dynamic command is created.  At least it links to this nicely documented page though.

---

### `!id [@user]`
Prints the user's id in chat, or prints the id of the specified user.

##### Arguments:
- `[@user]` Optionally specify to print another user's id.  Must be a mention.

---

### `!listroles`
DMs the user a list of roles and ids on the server.  This command is used to assist in setting up permissions, specifically the `GrantToRole` option.

---

### `!perms`
DMs the user their permissions on the server.  Helpful for figuring out what they can and can't do *without spamming every command to see if it works*.

---

### `!joinserver <server invite link>`
Asks the bot to join a server.  This is the one command that can be invoked by DMing the bot.

**Note:** Only the owner can use this command.  This cannot be changed through permissions.

##### Arguments:
- `<server invite link>` An invite link for a server, usually looks something like `http://discord.gg/somerandomtexthere`.
