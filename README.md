# Jason Bot

Python - bot to retrieve posts from specific subreddit and post to Twitter. Specifically to post markov chain engine (SSim) output to Jason, a bot account on Twitter.

Uses script from CorbinDavenport

## Disclaimer

No liabilities. Probably don't use this as it breaks Twitter API terms of use. 

## Dependencies

Needs Python 3, [tweepy](https://github.com/tweepy/tweepy), [PRAW](https://praw.readthedocs.org/en/), and [py-gfycat](https://github.com/ankeshanand/py-gfycat) libraries:

    pip install tweepy
    pip install praw
    pip install gfycat

## Setting up the bot

All settings found in the `config.ini` file. 

1. Under the [BotSettings] section, add the username of the Twitter account you will use to `TwitterUsername` (do not include the @ symbol)
2. Under the [BotSettings] section, add the name of the subreddit to `SubredditToMonitor` (do not include /r/ prefix)
3. By default, the bot will wait at least 600 seconds between tweets to prevent rate limiting detection, you can change this by editing the `DelayBetweenTweets` setting in the [BotSettings] section

Add Twitter API auth details to config:

1. (https://dev.twitter.com/apps) 
2. 'Create New App' 
3. Fill out the Name, Description, and Website fields with anything you want (you can leave the callback field blank)
4. Set 'Access level' to 'Read and write'
5. Click the 'Keys and Access Tokens' tab
6. Click the 'Create my access token' button
7. Fill out the [PrimaryTwitterKeys] section in the config file with the info

In addition, you will have to create an application on Reddit:

1. Sign in with your Reddit account
2. Go to your [app preferences](https://www.reddit.com/prefs/apps) and create a new application at the bottom
3. Select the application type as 'script'
4. Add the token (seen below the name of the bot after it's generated) and the secret to the [Reddit] section of the config file

## Usage

Once you edit the bot script to provide the necessary API keys and the subreddit you want to tweet from, execute

    python memebot.py
