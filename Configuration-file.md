## Credentials

The bot needs its own account to run on (not your own.)  
Username is the email you registered the bot's discord account with.

    [Credentials]
    Username = your_bots_email@foo.com
    Password = bots_pass

## Permissions

You need your id, not the bot's id.  The bot does not own the bot, you do.
If you don't know how to get this, join the help server (link in the readme) *with the owner's account* and type !id in chat. You should get something along the lines of: 
> OwnerName's ID is 12300000000000789

    [Permissions]
    OwnerID = 123...789

## Chat

Change this if you don't want commands to trigger another bot on the same server. Ex: One bot uses ~play, ~skip, etc and you want your bot to use !play, !skip, etc.  
    
    [Chat]
    CommandPrefix = !
   
This means you would type !play, !skip, etc.  
This explanation exists because it seems no one knows what **pre**-fix means.  
  
You can restrict the bot to only listen to certain text channels. By default, it will listen on all channels in the server its in.  
To find the text channel(s) you want you bot to listen on, go to the server and simply right click on the text channel and copy link. It should look like:
> discordapp.com/channels/129488835553334912/143335558889992656  

Copy and paste the **second** set of numbers, and separate multiple text channels with single spaces.  
*Uncomment (remove the ; at the start of the line) and add channel IDs to enable.*  

    ;BindToChannels = 

## MusicBot

    [MusicBot]
    DefaultVolume = 0.45  

The starting volume of the bot. Scale of .01 to 1.0, 1.0 being 100% volume. 

    WhiteListCheck = no

**Deprecated in favor of permissions**

    SkipsRequired = 4
    SkipRatio = 0.5

If no, deletes videos after they have been played. If the video is still in the queue after playing, the bot will avoid redownloading.  

    SaveVideos = yes

Mentions the user who queued a song when the song plays
  
    NowPlayingMentions = no

On startup, if the owner is in a voice channel, join that channel. Auto joining a server without the owner being on is currently being worked on. 

    AutoSummon = yes

Play random songs out of included playlist when nothing is queued  

    UseAutoPlaylist = yes

Prints extra output in the console and some errors to chat.  
This option is a work in progress, don't expect much.  You might as well just leave it on for now.  

    DebugMode = no