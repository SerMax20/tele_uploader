# tele_uploader
Telegram bot able to upload large file, also on Dropbox!

## Installation

tele_uploader requires [PHP](http://php.net/downloads.php) >= 5.6.0 and [Composer](https://getcomposer.org/) to run.

### Dependencies installation

To be able to run tele_uploader, you **must** install all the dependencies listed in [composer.json](/composer.json); to do that, type:

```sh
$ composer install
```

This process can take a while...

## Configuration

After all dependencies are satisfied, you can start to configure the environment variables.

For convenience, I've listed them inside the [env.sh](/env.sh) file so that the only thing you have to do is open it and fill with your keys.

### Keys meaning

We have just four keys:

- BOT_TOKEN: the unique token generated by [@BotFather](https://t.me/BotFather)
- DB_ID: the unique dropbox app key
- DB_SECRET: the unique dropbox app secret
- DB_TOKEN: the unique dropbox app instance token

For the Dropbox keys, you have to create a new Dropbox application [here](https://www.dropbox.com/developers/apps).

In the following picture, I'll show you where to find each key.
![pic_db](/pics/pic_db.png)

## Run!

Now we're ready to execute the bot!

Let's import the environment variable, with:

```sh
$ source env.sh
```

and then...run!

```sh
$ php bot.php
```

## Commands

When you send to the bot a direct download link or a media message, it will download it in it's personal directory.
After that, you can use the following commands:

- **/telegram**: will upload the file to your Telegram chat
- **/dropbox**: will upload the file to the Dropbox registered application directory

These actions can be also used with the command **/upload**, that offer to you the ability to navigate your file system to choose what to upload.  

## Credits

A special thanks to [Daniil Gentili](https://daniil.it/) aka [danog](https://github.com/danog) that created [MadelineProto](https://github.com/danog/MadelineProto).