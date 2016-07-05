## Help
**Basic troubleshooting**

1. Make sure you are using the [latest](https://github.com/SexualRhinoceros/MusicBot/releases/tag/1.9.5) **stable release** (currently `1.9.5`).
2. Make sure your **dependencies are updated**. This will solve most issues.
If you have issues
3. Make sure your **configuration file is correct**. Double-check it.
4. After making any changes, or updating dependencies, **restart the bot**.

If none of these solve your issue, read below for common problems and how to fix them. If none fix your issue, join the [Rhino Help Server](http://discord.me/rhinohelp).

### `Owner not found, bot is not on any servers.`

Your bot isn't on any servers. You should accept an invite link to a server while logged into the account, or join via OAuth for bot accounts ([documentation here](https://discordapp.com/developers/docs/intro)).

### `discord.errors.Forbidden: FORBIDDEN (status code: 403)`

Your bot **does not have permission** to perform the action required. As a rule of thumb, make sure it has most, if not all, permissions on the server (except `Administrator`).

### `'pip' is not recognized as an internal or external command`

You probably **installed Python wrong**. When installing Python 3.5+ on Windows, you should tick the box during the installation prompts that states "Install pip". See [this question](http://stackoverflow.com/questions/23708898/pip-is-not-recognized-as-an-internal-or-external-command) on StackOverflow for more help.

### `AttributeError: module 'discord' has no attribute 'opus'`

Legacy versions of `discord.py` **do not support** voice connections. Update your dependencies using the provided `requirements.txt` (on Linux, OSX), or run the `update_deps.bat` script on Windows.

### `You don't have permission to use that command.`

**You do not have permission** to use a specific bot command. Ask the bot owner to edit `permissions.ini` in the config folder to give you permission. There are various video tutorials:

* Adding users to groups: https://www.youtube.com/watch?v=DC1FifOv9eU
* Adding roles to groups: https://www.youtube.com/watch?v=nWH2priWQcg

### `[s16le @ 0x2c50f80] Application provided invalid(...)`

This is `ffmpeg` complaining about various issues that shouldn't impact how the bot runs and how the music plays. You can **safely ignore warnings like this**.

### `AttributeError: 'WebSocketClientProtocol' object has no attribute 'wait_for'`

This is because `discord.py` is **not up to date**. Update your dependencies using the provided `requirements.txt` (on Linux, OSX), or run the `update_deps.bat` script on Windows.

### `[WinError 10038] An operation was attempted on something that is not socket`

This error occurs when the websocket is closed. It is a known issue, and something that we are trying hard to develop solutions for. To fix manually, just `!restart` the bot, run `!disconnect` then `!summon`, or switch voice regions.