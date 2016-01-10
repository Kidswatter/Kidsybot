# FAQ

Q:`'pip' is not recognized as an internal or external command`

A: http://stackoverflow.com/questions/23708898/pip-is-not-recognized-as-an-internal-or-external-command


Q:`Bot prints 'no, not whitelisted and new' when I try to play something`

A: Add yourself to the whitelist! By typing !whitelist @username


Q:`I'm getting this error! http://puu.sh/m6hkf/40eec0910c.png`

A: The bot needs permission to delete messages. An option to toggle this behavior.


Q:`What is my (owner)ID?`

A: Type !id in a discord server with the bot online.


Q:`I'm having an issue with the Discord installation!`

A: Open up the command prompt and type `pip install --upgrade git+https://github.com/Rapptz/discord.py@async` into it.


Q:`I'm having other errors with the bot, it has to be broken`

A: If Rhinobot is running in my discord, the bot isn't broken. I keep everything as updated as possible!

Q: `AttributeError: module 'discord' has no attribute 'opus'`

A:A: Whatever you did, you did something wrong.  The old version of discord.py (which you get by running pip install discord.py) doesn't support voice; only the async branch does.  You need git to install that one, which is why we have you install git.