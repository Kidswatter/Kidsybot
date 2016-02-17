# Configuration file for `develop` branch

## Default file

    [Credentials]
    Username = my@email
    Password = your_password
    
    [Permissions]
    OwnerID = 000000000000000000
    
    [Chat]
    CommandPrefix = !
    
    [MusicBot]
    WhiteListCheck = no
    SkipsRequired = 4
    SkipRatio = 0.5
    SaveVideos = yes
    NowPlayingMentions = no
    AutoSummon = yes
    UseAutoPlaylist = yes

## Explanations for each setting

### `[Credentials]` section

- `Username`: Discord email address to login with.
- `Password`: Discord password to login with.

### `[Permissions]` section

- `OwnerID`: The Discord user ID to use as the owner (full permissions on bot). To find your Discord user ID, type `\@username` and your ID is the numbers in the message that is highlighted like a mention in the following format `<@00000000>`.

### `[Chat]` section

- `CommandPrefix`: Text needed before commands to be registered as a command (i.e setting this to `bot.` changes all commands to `bot.commandname`).

### `[MusicBot]` section

- `WhiteListCheck`: Enables / disables the whitelist.
- `SkipsRequired`: The amount of skips required to skip the song (owners of the bot can override this command).
- `SkipRatio`: The amount of skips required in percent (0.5 = 50%) to skip the song.
- `SaveVideos`: Saves all the played songs into the cache. When disabled, the bot will delete songs after it has played them to save disk space.
- `NowPlayingMentions`: The bot will announce and mention the requester when a requested song is played.
- `AutoSummon`: On start up, if the owner is in a voice channel, join that channel.
- `UseAutoPlaylist`: Play a random songs when nothing is en-queued.