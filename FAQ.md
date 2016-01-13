# FAQ

#### 'pip' is not recognized as an internal or external command
See: http://stackoverflow.com/questions/23708898/pip-is-not-recognized-as-an-internal-or-external-command

#### Bot prints 'no, not whitelisted and new' when I try to play something
Add yourself to the whitelist! By typing !whitelist @username

#### I'm getting this error! http://puu.sh/m6hkf/40eec0910c.png
The bot needs permission to delete messages. An option to toggle this behavior.

#### What is my (owner)ID?
Type !id in a discord server with the bot online.

#### I'm having an issue with the Discord installation!
Open up the command prompt and type `pip install --upgrade git+https://github.com/Rapptz/discord.py@async` into it.

#### I'm having other errors with the bot, it has to be broken
If Rhinobot is running in my discord, the bot isn't broken. I keep everything as updated as possible!

#### AttributeError: module 'discord' has no attribute 'opus'
Whatever you did, you did something wrong.  The old version of discord.py (which you get by running pip install discord.py) doesn't support voice; only the async branch does.  You need git to install that one, which is why we have you install git.

#### I'm getting this error! http://i.imgur.com/SkIWWBJ.png
You have entered the wrong login details in the options file. Open the file and edit it.