<p align="center">
  <img src='https://nightofcode.com/github/night-of-code/twitch-chat-sub-responder/twitch-chat-sub-responder.jpg' />
</p>


## Subscription Responder for Twitch Chat
When someone subscribes to a Twitch channel, auto respond with a custom message of appreciation.

Supports multiple channels and custom messages for both new and returning subs.

## About
Created for the Twitch community. Please do not use this tool to send unwanted messages. If in doubt, check with the broadcaster.

This repository is in no way affiliated with Twitch.

## Instructions
##### 1. Run make to build everything

##### 2. Update config files
You must update both files found in the **config** folder.

    **channels.txt**
    Contains channels and response messages. 1 channel per line. The file uses the following format:
    channel_name, response_message_new_subscriber, response_message_returning_subscriber

    Response messages may contain the following place-holders: ##months##, ##username##

    Example:
    ```
    Welcome back @##username## You are a ##months## month subscriber
    // output:  Welcome back @username You are a 15 month subscriber
    ```

    **settings.txt**
    Contains connection settings for Twitch IRC. You must update your username and oauth. You can generate your oauth token here:
    [https://twitchapps.com/tmi/](https://twitchapps.com/tmi/)

##### 3. Run
```
$ twitch-chat-sub-responder.exe
```

To end the program running in the terminal, press Ctrl+c twice.
Designed to run locally or be deployed to Heroku.

## Author
Craig Sherlock [@nightofcode](https://twitter.com/nightofcode)

## License
twitch-chat-sub-responder is licensed under the GNU General Public License v2.0. See the LICENSE file for more info.