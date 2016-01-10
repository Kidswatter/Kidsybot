# Configuration file for `develop` branch

## Default file

    [Credentials]
    Username = my@email.com
    Password = rhino_is_a_numpty
    
    [Permissions]
    OwnerID = 112233445566778899
    
    [Chat]
    CommandPrefix = !
    
    [MusicBot]
    DaysActive = 0
    WhiteListCheck = no
    SkipsRequired = 7
    SkipRatio = 0.5
    SaveVideos = yes
    NowPlayingMentions = no

## Explanations for each setting

### `[Credentials]` section

- `Username`: Discord email address to login with.
- `Password`: Discord password to login with.

### `[Permissions]` section

- `OwnerID`: The Discord user ID to use as the owner (full permissions on bot). To find your Discord user ID, type `\@your_username` and your ID is the numbers in the message that is highlighted like a mention.

### `[Chat]` section

- `CommandPrefix`: Text needed before commands to be registered as a command (i.e setting this to `bot.` changes all commands to `bot.commandname`).

### `[MusicBot]`

- `DaysActive`: This is the amount of days they should be active to be added in the whitelist automaticly.
- `WhiteListCheck`: Enables / disables the whitelist.
- `SkipsRequired`: The amount of skips required to skip the song. (owners of the bot can override this command)
- `SaveVideos`: If enabled it saves all the played songs.
- `NowPlayingMentions`: If enabled the bot will announce when a new song comes up.
