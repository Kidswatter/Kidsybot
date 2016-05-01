# Table of Contents

[Introduction](#introduction)

1. [Step 1: Preparation](#step-1-preparation)
    - [1.a: Install a TextEditor Homebrew and Python](#1a-install-a-texteditor-homebrew-and-python)
    - [1.b: Installing dependencies](#1b-installing-dependencies)
2. [Step 2: Download and setup MusicBot](#2-download-and-setup-musicbot)
    - [2.a: Install python dependencies](#2a-install-python-dependencies)
    - [2.b: Change configuration file](#2b-change-configuration-files)
3. [Step 3: Start the bot](#3-start-the-bot)
    - [3.a: Test the bot (non permanent)](#3a-test-the-bot-non-permanent)
    - [3.b: Start the bot (permanent with screen)](#3b-start-the-bot-permanent-with-screen)

# Introduction

Installing the bot on OSX requires the downloading of several libraries. These libraries are best managed with [Homebrew](http://brew.sh/). Homebrew and a basic text editor are required for this MusicBot to function.

# Step 1: Preparation

Let's get everything ready to install.

### 1.a: Install a TextEditor Homebrew and Python

If you do not have a text editor, download a basic text editor from the Apple App Store (TextWrangler, XCode, or equivalent) or download an outside editor such as [Atom](https://atom.io/). Following that, go to [Homebrew](http://brew.sh/) and download Homebrew by running the command line on their website through Terminal (mac's version of cmd). Run `brew update` to fetch the latest package data.

Next, you need to install Python3.5 or later. You can either navigate to Python's [Download](https://www.python.org/downloads) page and `Download Python 3.5.1` or [ClickHere](https://www.python.org/ftp/python/3.5.1/python-3.5.1-macosx10.6.pkg) to start the download automatically.

### 1.b: Installing dependencies

To install dependencies, enter the following commands **without sudo**

    brew install git
    brew install ffmpeg
    brew install opus
    brew install libffi
    brew install libsodium

## 2: Download and setup MusicBot

To download the latest version of the music bot use the following URL and download it to your desktop:

    https://github.com/SexualRhinoceros/MusicBot/archive/review.zip

**NOTE: Do NOT change the folder name or move this folder from the desktop, this will mess up the future commands you need to type. (this will be updated in the near future to allow placement of the MusicBot folder wherever you want it)**

### 2.a: Install python dependencies

This next step is somewhat optional, as MusicBot will attempt to do this for you if you haven't. On OSX, you should run these commands **without root**, since Homebrew does not clobber your system Python.

    pip3.5 install --upgrade -r requirements.txt
    
This installs the various python dependencies used by the bot.

### 2.b: Change configuration files

**If you haven't already done so, create a COMPLETELY NEW Discord account for your bot.** You cannot share accounts with your bot - Discord doesn't allow multiple voice connections from one account (you won't be able to listen to your own bot :cry:).

The configuration files are located in the `config/` folder. There are two files, `example_options.ini` and `example_permissions.ini` that tell you how to configure the bot. You should copy and rename these files to `options.ini` and `permissions.ini` respectively, then edit them. **Your bots login credentials and YOUR OwnerID will go in the `options.ini` file!**

## 3: Start the bot 

Log into the bot's account on your Discord client and join the server you want your bot to live on. Then, log out of the bot's account and log back into your Main Account. *This only needs to be performed once.*
If you are using a `BOT` account and put your bot's token in the `options.ini` file you don't need to do this.

With terminal open type the following to access the MusicBot folder:

    cd desktop
    cd MusicBot-review

### 3.a Test the bot (non permanent)
Make sure you're still in the `MusicBot` folder (you should see `Name-MacBook-Pro:MusicBot-review Username$` or something similar in front of the cursor). If you don't see that repeat, type `cd` followed by `return` and repeat the above steps.

Run this:

    python3.5 run.py

If you see this:

    Connected!

    Username: [Bot Username]
    ID: [Bot User ID]
    --Server List--
    [Server Name(s)]

that means everything is good and running correctly!

### 3.b: Start the bot (permanent with screen)

Close the test bot first by hitting `Ctrl+C` in the Terminal window while the bot is running.  You may need to press it a few times.

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
**NOTE: You can close the terminal without the bot disconnection, however if you shut down your computer, close the lid, or let it sleep you will have to restart the bot again.**

You don't need to do anything else! :smile: You can check out the [wiki articles](https://github.com/SexualRhinoceros/MusicBot/wiki/Commands-list "Commands list") to find out how to use your bot. :grin: