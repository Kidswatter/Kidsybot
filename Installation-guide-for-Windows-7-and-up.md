# Table of Contents

2. [Step 1: Installing Python](#step-1-installing-python-351)
    - [1.a Download Python installer](#1a-downloading-python-installer)
    - [1.b: Install Python](#1b-install-python-351)
    - [1.c: Install Git](#1c-install-git)
3. [Step 2: Install and configure MusicBot](#step-2-install-and-configure-musicbot)
    - [2.a: Download MusicBot](#2a-download-musicbot)
    - [2.b: Change configuration file](#2b-change-configuration-file)
    - [2.c: Start the bot!](#2c-start-the-bot)

## Step 1: Installing Python 3.5.1

Python 3.5+ is required to run MusicBot.

### 1.a: Downloading Python installer

You can download the Windows installer for your appropriate system architecture here:

* 32-bit: https://www.python.org/ftp/python/3.5.1/python-3.5.1.exe
* 64-bit: https://www.python.org/ftp/python/3.5.1/python-3.5.1-amd64.exe

### 1.b: Install Python 3.5.1

Open the installer you downloaded in step 1.a. When the installer opens, ensure that the checkboxes *'Install launcher for all users (recommended)'* and '*Add Python 3.5 to PATH*' are both **checked** and then click the big *Install Now* button.

![Python installer initial screen](http://i.imgur.com/48qmRJ0.png)

**If a UAC prompt appears, click *'yes'* to start installation.**

Python should begin to install and you should see the progress bar slowly fill as the installation takes place.

![Python installer progress bar](http://i.imgur.com/bSUIO10.png)

Once that is done, click the button labeled *Close* to finish installation.

![Python installer completion screen](http://i.imgur.com/zb9s0gA.png)

You have now successfully installed Python onto your machine! :smile:

### 1.c: Install Git

If you don't already have it, you need to install Git for Windows (Git Bash). [Download it here](https://git-for-windows.github.io/).

During the installation, select these options (which should be selected by default):
* Use Git from Git Bash only
* Checkout Windows-style, commit Unix-style endings
* Use MinTTY (the default terminal MSYS2)

To open Git Bash, open Windows Explorer in your designated folder and right-click. You will get the option `Git Bash` on the context menu. Click it to open a new shell.

![Git Bash context menu](http://i.imgur.com/ptlggmn.png) 

## Step 2: Install and configure MusicBot

### 2.a: Download MusicBot

With Git Bash open, run the following command to download MusicBot:

    git clone https://github.com/SexualRhinoceros/MusicBot.git MusicBot -b master

### 2.b: Change configuration file

When you have cloned using Git, you will get the MusicBot folder inside the directory. Open it.

![MusicBot contents](http://i.imgur.com/Tm0NEoW.png)

In the `config` folder, if there isn't a file called `options.ini`, copy `example_options.ini` and rename the copy to `options.ini`.  Then, open `options.ini` in a text editor OTHER than Windows Notepad, otherwise you'll see a single line full of stuff. I suggest [Notepad++](https://notepad-plus-plus.org "Notepad++").  Editing the options file with windows notepad will mangle the content and the bot won't be able to read it.

Configure the file however you want, it should explain everything you need.  The three things you MUST change are the bot's email, password and your OwnerID. If you have any further questions, you can ask on the help server.

### 2.c: Start the bot!

**If you haven't already done so, create a COMPLETELY NEW Discord account for your bot.** You cannot share accounts with your bot.  Discord doesn't allow multiple voice connections from one account (you won't be able to listen to your own bot :cry:).

Log into the bot's account in your browser (you can use a private tab so you don't need to log out of yours) and join the server you want your bot to live on. Then, log out of the bot's account (or just close the tab if its a private tab).

Go back to the main MusicBot directory and double click `runbot.bat`. If you don't see any errors, that means everything is good and running correctly! You don't need to do anything else! :smile: You can check out the [wiki articles](https://github.com/SexualRhinoceros/MusicBot/wiki/Commands-list "Commands list") to find out how to use your bot.  If you see an error and you don't know what it means, ask about it on the help server.

**NOTE:** By default, the `AutoSummon` option is enabled.  This means the bot will automatically join the owner's voice channel. If the owner isn't in a voice channel, join one and use the command `!summon` to bring the bot into your channel.

If you close the console, turn off your computer or put it to sleep the bot will go away. To keep this bot running 24/7 you must have it running on a computer or server. 