# Table of Contents

[Introduction](#introduction)

1. [Step 1: Preparation](#step-1-preparation)
    - [1.a: Install a TextEditor Homebrew and Python](#1a-install-a-texteditor-homebrew-and-python)
    - [1.b: Installing dependencies](#1b-installing-dependencies)
2. [Step 2: Download and setup MusicBot](#2-download-and-setup-musicbot)
    - [2.a: Install python dependencies](#2a-install-python-dependencies)
    - [2.b: Change configuration file](#2b-change-configuration-files)
3. [Step 3: Start the bot](#3-start-the-bot)
4. [Step 4: Running the bot in a Screen (Optional)](#4-running-the-bot-in-a-screen-optional)

# Introduction

Installing the bot on OSX requires the downloading of several libraries. These libraries are best managed with [Homebrew](http://brew.sh/). Homebrew and a basic text editor are required for this MusicBot to function.

# Step 1: Preparation

Let's get everything ready to install.

### 1.a: Install a TextEditor Homebrew and Python

If you do not have a text editor, download a basic text editor from the Apple App Store (TextWrangler, XCode, or equivalent) or download an outside editor such as [Atom](https://atom.io/). Following that, go to [Homebrew](http://brew.sh/) and download Homebrew by running the command line on their website through Terminal (mac's version of cmd). Run `brew update` to fetch the latest package data.

Next, you need to install Python3.5 or later. You can either navigate to Python's [Download](https://www.python.org/downloads) page and `Download Python 3.5.1` or [ClickHere](https://www.python.org/ftp/python/3.5.1/python-3.5.1-macosx10.6.pkg) to start the download automatically.

**Installing Python3.5**
Navigate to and open the `python-3.5.1-macosx10.6.pkg` you downloaded.

This will be the first thing you see when it opens. 
**Click Continue.**
![Python installer initial screen](http://i.imgur.com/rNDbcMQ.png)

**Click Continue.**
![Python read me screen](http://i.imgur.com/BvWwg2a.png)

**Read the Software License Agreement then Click Continue**
![Python license screen](http://i.imgur.com/SUWJePm.png)

**Click Agree.**
![Python license accept screen](http://i.imgur.com/RuKTcG3.png)

**Choose your installation destination (Recommended: Downloads), then Click Install.**
![Python installation destination and type](http://i.imgur.com/tNHIehd.png)

**After the installation screen you will see this... Click Close.**
![Python install successful screen](http://i.imgur.com/pF7rBq8.png)

**Congratulations you have successfully installed Python3.5!!**

### 1.b: Installing dependencies

To install dependencies, enter the following commands **without sudo**

    brew install git
    brew install ffmpeg
    brew install opus
    brew install libffi
    brew install libsodium

## 2: Download and setup MusicBot

To get the latest version of MusicBot, run this command using Terminal:

    git clone https://github.com/SexualRhinoceros/MusicBot.git MusicBot -b master 

### 2.a: Install python dependencies

Run the following file that is located in your MusicBot's main folder.    
**Run this file:**    

    update_macdeps.command    

*You may have to right click the file, mouse over 'Open With' then select 'Terminal.app'*    
    
This installs the various python dependencies used by the bot.

### 2.b: Change configuration files

**If you haven't already done so, create a COMPLETELY NEW Discord account for your bot.** You cannot share accounts with your bot - Discord doesn't allow multiple voice connections from one account (you won't be able to listen to your own bot :cry:).

The configuration files are located in the `config` folder. There are two files, `example_options.ini` and `example_permissions.ini` that tell you how to configure the bot. You should copy and rename these files to `options.ini` and `permissions.ini` respectively, then edit them. 

![Music Bot Config Folder](http://i.imgur.com/GnzWRNG.png)

Open options.ini in a text editor of your choosing from the one you downloaded at the beginning of this guide. I suggest TextWrangler or Atom.

Configure the file however you want, it should explain everything you need. The three things you MUST change are the bot's email, password and your OwnerID. If you have any further questions, you can ask on the help server.

## 3: Start the bot 

Log into the bot's account on your Discord client and join the server you want your bot to live on. Then, log out of the bot's account and log back into your Main Account. *This only needs to be performed once.*
If you are using a `BOT` account and put your bot's token in the `options.ini` file you don't need to do this.

To start the bot navigate back to your MusicBot's main folder.    
**Run:**    

    runbot_mac.command    

*You may have to right click the file, mouse over 'Open With' then select 'Terminal.app'*    

If you see this:

    Connected!

    Username: [Bot Username]
    ID: [Bot User ID]
    --Server List--
    [Server Name(s)]

that means everything is good and running correctly!

You don't need to do anything else! :smile: You can check out the [wiki articles](https://github.com/SexualRhinoceros/MusicBot/wiki/Commands-list "Commands list") to find out how to use your bot. :grin:
    
    
    
    
### 4: Running the bot in a Screen (Optional)

Running the bot in a screen allows you to close Terminal without it shutting down the bot. If you don't run the bot in a screen, closing Terminal will cancel the bots operations and disconnect it from Discord. Screen simply allows you to close Terminal with out this happening.    
**(This is an optional step that is only for user preference. You don't have to do this.)**

To make your life easier, this is best performed by keeping your MusicBot's folder on the desktop.

If your bot is currently running cancel its operations by pressing `Ctrl+C` before continuing on to these steps.

If you aren't already in a the music bots folder through Terminal go ahead and perform these steps (if your Terminal line looks like this `Name-MacBook-Pro:MusicBot-1.9.7 Username$` or similar, skip to "Run this to make a `screen` console"):

    cd desktop
    cd MusicBot-1.9.7

Run this to make a `screen` console:

    screen -S bot

This creates a `screen` console with the name 'bot' so you can easily come back later if there are any problems. Don't be alarmed that the Terminal window became empty.

To start the bot in this screen, run:

    python3.5 run.py

Once that's online and good, press `Ctrl+a` then `d` separately to 'detach' from the screen. Your music bot should still be online on your server.

Now you can close your Terminal window and play with your bot!

If you ever want to have a look at the bot's console logs, SSH back into the machine and run:

    screen -r bot

That should bring everything back up.
**NOTE: You can close the terminal without the bot disconnecting, however if you shut down your computer, close the lid, or let it sleep you will have to restart the bot again.**