# HATB
havelock administator telegram bot

## Overview
HATB is a modular multi-group telegram administration helper

## Setup
### Dependencies
HATB needs [python-telegram-bot](https://github.com/python-telegram-bot/python-telegram-bot) to works properly:

`pip3 install python-telegram-bot`

## Installation
First you need to clone the repository

`git clone https://github.com/ExxonRsky/adminBot`

Now you have to [create a bot](https://core.telegram.org/bots#creating-a-new-bot) and paste the `APIKEY` inside the `TOKEN` variable inside `config.py` located in the same directory of `bot.py`

You have to create an `sqlite3` file called `buster.db` using this command

`sqlite3 busterdb < db.sql`

And finally you can run you personal istance of `HATB`

`chmod +x bot.py`

`./bot`

## Modules
HATB offers a modular system to integrate commands and actions to the bot

## There are 2 different kinds of modules:

### Commands modules
These modules contains only the single commands you can use with `/name-of-the-command`

### Current command modules:

- [x] `/ban` -  ban the user that wrote the quoted message
- [x] `/unban` - unban the user that wrote the quoted message
- [x] `/mode +o` - change the mode of the user quoted in the message to operator
- [x] `/mode -o` - change the mode of the user quoted in the message from operator to user
- [x] `/op` - if the user is an operator giving this command can became an administrator of the group
- [x] `/s0ng` - send a random song from [this YouTube Channel](https://www.youtube.com/user/bl4ckh4ts0ngs/)
- [x] `/ping` - just for fun, the bot will answer `pong`
- [x] `/help` - shows commands and controls info
- [ ] `/groupinfo` - show groups info
- [ ] `/info` - show info about the quoted user
 
### Onjoin modules
These are all the actions the bot will make every time a new user join

- [x] `nobots` - if a bot not in whitelist joins the group it will be banned
- [x] `not_ascii_name` - kick users with non-ascii char in first name
 
### OnMessage modules
These are all the actions the bot will do every time someone send a new message(it includes stickers, gifs, images, etc..)

- [ ] `antiflood` - integrates an algorithm to stop flooders inside the group
