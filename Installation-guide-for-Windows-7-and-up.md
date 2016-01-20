**THIS GUIDE IS FOR INSTALLING THE `develop` BRANCH ONTO A WINDOWS 7 AND UP MACHINE.** If you are not using Windows 7 or up, please use another article to install your RhinoBot.

# Table of Contents

1. [Step 1: Installing Git](#step-1-installing-git)
    - [1.a: Download Git installer](#1a-download-git-installer)
    - [1.b: Install Git](#1b-install-git)
2. [Step 2: Installing Python](#step-2-installing-python-351)
    - [2.a Download Python installer](#2a-downloading-python-installer)
    - [2.b: Install Python](#2b-install-python-351)
3. [Step 3: Install and configure RhinoBot](#step-3-install-and-configure-rhinobot)
    - [3.a: Download RhinoBot](#3a-download-rhinobot)
    - [3.b: Change configuration file](#3b-change-configuration-file)
    - [3.c: Start the bot!](#3c-start-the-bot)

# Step 1: Installing Git

First of all, we need to install Git. If you already have Git installed onto your machine, you can skip to Step 2.

### 1.a: Download Git installer

You can find the Windows installer for Git at [git-scm's website](https://git-scm.com/download/win "Download Git for windows"). Just open the page and let it download.

### 1.b: Install Git

Open the installer you downloaded in step 1.a. You should see something similar to the following:

![Git installer initial screen](http://i.imgur.com/mhdkclA.png)

Click *next* to proceed to the license screen. Read through the license and click *next* again to agree with it.

When you reach the *'Select Components'* screen, leave the default boxes checked and click *next*.

When you reach the *'Adjusting your PATH environment'* screen, you need to select *Use Git from the Windows Command Prompt*, just like in the screenshot below:

![Git installer adjusting PATH environment screen](http://i.imgur.com/RRZrucI.png)

Click *next* once again. On the *'Configuring the line ending conversions'*, leave it as the default setting and then click *next*.

On the *'Configuring the terminal emulator to use with Git Bash'* screen, leave it as the default setting and click *next* once again.

On the *'Configuring experimental performance tweaks'* screen, leave it as the default settings and click *next*.

Git should begin to install and you should see the progress bar slowly fill as the installation takes place.

![Git installer progress bar](http://i.imgur.com/GETzy0w.png)

Once that is done, uncheck *'View ReleaseNotes.html'* and click the button labeled *Finish*.

![Git installer completion screen](http://i.imgur.com/faa1jji.png)

You have now successfully installed Git onto your machine! :smile:

# Step 2: Installing Python 3.5.1

Now we have Git installed on this machine, we need to install Python.

### 2.a: Downloading Python installer

You can find the Windows installer for Python 3.5.1 at [Python's website](https://www.python.org/ftp/python/3.5.1/python-3.5.1.exe "Download Python 3.5.1 for windows"). Just open the page and let it download.

### 2.b: Install Python 3.5.1

Open the installer you downloaded in step 2.a. When the installer opens, ensure that the checkboxes *'Install launcher for all users (recommended)'* and '*Add Python 3.5 to PATH*' are both **checked** and then click the big *Install Now* button.

![Python installer initial screen](http://i.imgur.com/48qmRJ0.png)

**If a UAC prompt appears, click *'yes'* to start installation.**

Python should begin to install and you should see the progress bar slowly fill as the installation takes place.

![Python installer progress bar](http://i.imgur.com/bSUIO10.png)

Once that is done, click the button labeled *Close* to finish installation.

![Python installer completion screen](http://i.imgur.com/zb9s0gA.png)

You have now successfully installed Python onto your machine! :smile:

# Step 3: Install and configure RhinoBot

Let's get right into it, shall we?

### 3.a: Download RhinoBot

You can download the `develop` branch version of RhinoBot [here](https://github.com/SexualRhinoceros/MusicBot/archive/develop.zip "Download RhinoBot develop branch"). Once that is done, extract the .zip file into a convenient location (I suggest the Desktop).

![Extracting .zip file](http://i.imgur.com/PDTvnEu.png)

### 3.b: Change configuration file

When the extraction finishes, a new window should appear with the following contents:

![RhinoBot contents](http://i.imgur.com/Tm0NEoW.png)

Double click on the `config` folder to open it and then open `options.txt` in a text editor OTHER than Notepad, otherwise you'll see one big line full of stuff. I suggest [Notepad++](https://notepad-plus-plus.org "Notepad++").

Change the configuration settings to what you need according to [this wiki article](https://github.com/SexualRhinoceros/MusicBot/wiki/Configuration-file "develop branch configuration file").

### 3.c: Start the bot!

**If you haven't already done so, create a COMPLETELY NEW Discord account for your bot.** You cannot share accounts with your bot - Discord doesn't allow multiple voice connections from one account (you won't be able to listen to your own bot :cry:).

Log into the bot's account on your Discord client and join the server you want your bot to live on.

Go back to the main RhinoBot directory and double click `runbot.bat`. If you see:

    Connected!
    
    Username: [Bot Username]
    ID: [Bot User ID]
    --Server List--
    [Server Name(s)]

that means everything is good and running correctly! You don't need to do anything else! :smile: You can check out the [wiki articles](https://github.com/SexualRhinoceros/MusicBot/wiki/Commands-list "Commands list") to find out how to use your bot. :grin:

If you see an error, you might want to try installing dependencies by hand. You can do this by opening a command prompt in the MusicBot folder and executing the command `pip install -r requirements.txt`.

#### NOTE:
You need to use the `!summon` command to bring the bot into your voice channel now.  There will be an option for the bot to automatically join in a later release.
