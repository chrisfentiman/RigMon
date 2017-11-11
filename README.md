# RigMon #


### What is RigMon? ###

RigMon is a quick way to monitor your mining rigs using Telegram bot.

It currently supports:
* Claymore miners (Eth, Equihash, CryptoNight)
* EWBF miner

You can also check balance and transaction history in:
* Bittrex
* Poloniex

### How do I get set up? ###

* Download and install Node.js

https://nodejs.org/en/download/

* Clone or download this repository
* With a command line go to the repository folder and run

`npm install`

When you are finished with the config.json, you can run

`npm start`

### config.json ###
* Configuration

Open `config.json` with your favorite text editor

Specify your currency and symbol here:

`"currency": "usd"`

`"currency_symbol": "$"`

You can use any currency you see on https://coinmarketcap.com, you have to use lowercase letters.

Specify your power cost per kW (for example, 0.09 is 9 cents for 1 kilowatthour)

`"electricity": 0.09`

Replace your Telegram Bot token with TELEGRAMBOT_TOKEN here:

`"token": "TELEGRAMBOT_TOKEN"`

* How to get Telegram Token

Talk to the BotFather https://telegram.me/botfather

Write /newbot and follow the instructions

You should get your token like this:
`Use this token to access the HTTP API:
488814350:AAFxmfas0zOKSmDaAgAierd90-v8h_LKeF8`

* Configuring your mining rigs

Use `"clay":` for rigs using Claymore miner

Use `"ewbf":` for rigs using EWBF miner

Change host and port address to what you set up as your miners API.

`"host": "127.0.0.1"`

`"port": 3333`

Default values for Claymore is port 3333, EWBF is port 42000.

Use IP 127.0.0.1 if you are mining on the computer you are running RigMon.

You can reference your rig with any comments you like, I put my remote login and password here.

`"comments": "comment"`

Put your power from the wall here in watts, for profit calculation:

`"power": 820`

Put the coin shortname and algorithm you are mining with this rig here:

`"coin": "ETH"`

`"algo": "eth"`

Currently available algos are: 

eth - Ethereum

eq - Equihash

cn - CryptoNight

* First time run

After running your bot for the first time, you have to use the command /id

You will receive your chat id which you will have to put to the config file here:

`"chatid": 123456`

You can also add your bot to a group and get an /id there.