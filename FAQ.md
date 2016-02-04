# FAQ

#### 'pip' is not recognized as an internal or external command
You probably installed python wrong.  See: http://stackoverflow.com/questions/23708898/pip-is-not-recognized-as-an-internal-or-external-command

#### I'm getting this error! http://puu.sh/m6hkf/40eec0910c.png
The bot needs permission to delete messages. An option to toggle this behavior will be added in the future.

#### What is my (Owner)ID?
Type !id in the help server.  The link is in the readme.

#### AttributeError: module 'discord' has no attribute 'opus'
The old version of discord.py (which you get by running pip install discord.py) doesn't support voice; only the async branch does.  You need git to install that one, which is why we have you install git.

#### I'm getting this error! http://i.imgur.com/SkIWWBJ.png
You have entered the wrong login details in the options file. Open the file and edit it.

#### Is/will spotify supported?
No, and it probably never will be.

#### Can I have the bot play a radio stream?
No.  The bot downloads the song before playing it, so it won't work with streams of indefinite length.  That means twitch.tv too, since youtube-dl supports that.

#### Is [some other website or service] supported?
The bot uses [youtube-dl](https://github.com/rg3/youtube-dl) to handle getting information on whatever links you throw at it.  It supports over 600 sites, so the answer is probably yes, except for streams, but you already know that.  See: [youtube-dl supported sites](https://rg3.github.io/youtube-dl/supportedsites.html "Yes, it supports various porn sites, but you probably don't want to be banned from whatever server you try it on.")