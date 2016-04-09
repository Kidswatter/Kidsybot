## What do these errors mean?

![](http://i.imgur.com/SkIWWBJ.png)

You have entered the wrong login details in the options file. Open the file and edit it *and remember to save*.  Yes, people have forgotten to save.

![](http://puu.sh/m6hkf/40eec0910c.png)

The bot needs permission to delete messages (besides its own). An option to toggle this behavior will be added in the future.

### `'pip' is not recognized as an internal or external command`
You probably installed python wrong.  See: http://stackoverflow.com/questions/23708898/pip-is-not-recognized-as-an-internal-or-external-command

### `AttributeError: module 'discord' has no attribute 'opus'`
The old version of discord.py (which you get by running `pip install discord.py`) doesn't support voice; only the async branch does.  You need git to install the async branch, which is why we have you install git.

### `You don't have permission to use that command. Reason: This command is not whitelisted for your group (Default).`
The command that you are trying to use is not whitelisted for your group. Most of the time this comes from `!volume`.  If you want your users to be able to use different commands, you need to edit `permissions.ini` and add the command to the `CommandWhitelist`

### I edited `permissions.ini` and nobody can use commands!!
You need to make sure you uncommented the line. remove the `;` in front of any line you are using.  If you edited `GrantToRoles` or `UserList` be sure you added a role ID or a user ID not their names. 

### Wtf is this?
##### `[s16le @ 0x2c50f80] Application provided invalid, non monotonically increasing dts to muxer in stream 0: 2216 >= 2191`

This isn't an error, just ffmpeg complaining about something in the audio data.  You can ignore this.

## What is my (Owner)ID?
Mention yourself, but but a backslash before it, like so: `\@mynamehere`. Alternatively, just type !id in the help server.  The link is in the readme.

## How do I update the bot?
Currently, you just download it and change the config again.  Eventually some sort of system will be added to either alert you that there's an update, or do it for you.  The topic in the #musicbothelp channel in the help server is always updated with when the bot has been updated.

## How do I play a youtube playlist?
Just use the playlist link.  You need to use the actual playlist url though, not a song from the playlist.
- Good: `!play https://www.youtube.com/playlist?list=PLC0A615438E62547A`
- Bad: `!play https://www.youtube.com/watch?v=gbv-yqqmLH0&list=PLC0A615438E62547A`

## Is/will spotify be supported?
No, and it probably never will be.

## Can I have the bot play a stream?
No.  The bot downloads the song before playing it, so it won't work with streams of indefinite length.  That means twitch.tv too, since youtube-dl supports that.

## Is [some other website or service] supported?
The bot uses [youtube-dl](https://github.com/rg3/youtube-dl) to handle getting information on whatever links you throw at it.  It supports over 600 sites, so the answer is probably yes, except for streams, but you already know that.  See: [youtube-dl supported sites](https://rg3.github.io/youtube-dl/supportedsites.html "Yes, it supports various porn sites, but you probably don't want to be banned from whatever server you try it on.")

## Can the bot be in multiple voice channels?

Not currently. Soon :tm:.  This requires `Bot` accounts, which aren't finished yet.

