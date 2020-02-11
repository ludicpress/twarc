---
layout: page
title: Workshop
permalink: /workshop/
---

Does your research require you to build an archive of Twitter data? In this workshop attendees will learn how to scrape tweets with the TWARC program in your command line interface without going through the tedious process of manually downloading tweets. Participants will also be guided through the process of cleaning up Twitter data once it’s downloaded.

For this workshop we are going to build an archive of Twitter data using the command line tool twarc. We are going to walk through a few exercises using twarc in your operating system’s command line interface: terminal for Linux and OS X and Ubuntu for Windows. If you have followed the setup instructions to install wget on your Linux, Windows, or OS X machines then you are ready to begin the workshop.

## Configuration
At this point you should have twarc installed and have created your app with Twitter. Now, we need to configure twarc with your app credentials. On the developer.twitter.com interface you will be able to view your app. When you open the app, you will need to view the ```keys and tokens```. Note, the ```Consumer API Keys```, whih includes a ```API key``` and ```API secret key```.

Returning to the command line, you are going to need to tell twarc about your application API keys and grant access to your Twitter account. Type and enter in the following command:

```twarc configure```

When prompted, you will be asked to enter your ```consumer key```. Copy and paste the ```API key``` from your app into the command line and hit enter.

You will then be prompted to enter your ```consumer secret```. Copy and paste the ```API secret key``` from your app into the command line and hit enter.

You will then be asked to authorize the application by entering a pin which will be provided by a URL printed in the command line. Go to the URL and type the pin into the command line. If all has gone well, you should receive a message stating ```Happy twarcing!```.

## Warm Up
All of the commands in twarc use the following logic when being used:

```twarc [query] [text] [--filter] [text] > [file output]```

Twarc has two main queries for gather tweets: ```search``` and ```filter```. The search query retrieves all tweets sent out over the past 7 days that meet your command's instructions. Twitter's search API imposes a 7 day cap which is why you cannot go further back in time. The filter query retrieves all tweets sent out as they happen. This means when you start the command you will need to leave it running on your computer until you have finished your study.

For example, you could use the following command to gather tweets on the coronavirus from accounts tweeting in Toronto as they happen, where the query is ```filter``` and the filter is ```geocode```:

```twarc filter coronavirus --geocode 43.653226,-79.383184,10mi > coronavirustweetsastheyhappen.jsonl```

If you want to gather tweets for a few days, a month, or a year, you let the command run in the terminal for the period of time you require. If you want to gather tweets from the previous week, can can swap out the ```filter``` query for ```search```, so you're command looks like this:

```twarc search coronavirus --geocode 43.653226,-79.383184,10mi > coronavirustweetspreviousweek.jsonl```

A good first exercise though to warm up with if you have never used twarc before is the ```sample``` query. The sample command listens to Twitter's [statuses/sample](https://developer.twitter.com/en/docs/tutorials/consuming-streaming-data) API for a "random" sample of recent public statuses. To use the command, type and enter in the following command:

```twarc sample > sampletweets.jsonl```

You only need to run the command for a few seconds so hit ```control``` or ```ctrl``` and ```c``` to stop the command. The sample command gathers tweets from all over the world, so a few seconds generates hundreds of tweets (if not thousands!).

To view the jsonl file you've created you can open the file with a text editor, such as [BBEdit](https://apps.apple.com/us/app/bbedit/id404009241?mt=12) on OSX or [notepad ++](https://notepad-plus-plus.org/downloads/) on Windows. When viewing the data 

## Exercise 1: Gather by Term and Hashtag


## Exercise 2: Gather by Twitter Account


## Exercise 3: Gather by Location


## Final Thoughts
There is still plenty more to learn with Jekyll and GitHub pages. There are also dozens, if not hundreds, of themes available to use instead of the Minima theme that comes with this tutorial. In addition, there are many digital research groups creating static page themes in Jekyll, such as the [Minimal Computing](https://github.com/minicomp) for digital editions, digital exhibits, and a range of other static sites for humanities and social science projects. If this is your first time with static sites, don't be dismayed by the learning curve or the simplicity. The payoff can be great depending on your digital research goals and projects.
