**THIS GUIDE IS FOR INSTALLING THE `review` BRANCH OF THE MUSIC BOT.**

# Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
  - [Step 1: Preperation](#step-1-preparation)
  - [Step 2: Installation](#step-2-installation)
  - [Step 3: Configuration](#step-3-configuration)

# Introduction

Docker is a way to virtualize the Musicbot. By using Docker you do not have to worry about any dependencies or whether it may run on your platform or not. Simply use the docker image and run the music bot.

# Installation

## Step 1: Preparation

The only requirement is that you have [Docker](https://docs.docker.com/mac/) installed. You do not require anything else. You do not need to build the image yourself as it is available on [Docker Hub](https://hub.docker.com/r/sidesplitter/musicbot/)!

## Step 2: Installation

To pull the latest version of the musicbot image, run the following:

    docker pull sidesplitter/musicbot

To initialize your music bot and setup the file tree, you must run it once:

    docker run --name musicbot sidesplitter/musicbot

After letting this command run, you will probably find an error about not having a configuration file. Let's fix that!

## Step 3: Configuration

Get the [default configuration](https://raw.githubusercontent.com/SexualRhinoceros/MusicBot/review/config/example_options.ini) and save it somewhere. When you're finished with editing it, you can copy it to your docker container by using the following command:

    docker cp /path/to/options.ini musicbot:/musicBot/config/options.ini

In order for the configuration to take effect, you need to restart your docker container.

    docker restart musicbot

Everything should now run smoothly. If you want to change the permissions you can do the same thing only with the [permissions file](https://raw.githubusercontent.com/SexualRhinoceros/MusicBot/review/config/example_permissions.ini).

***

That's everything! Check out the [wiki article](https://github.com/SexualRhinoceros/MusicBot/wiki/Commands-list "Commands list") on how to use your bot.