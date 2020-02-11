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

To view the jsonl file you've created you can open the file with a text editor, such as [BBEdit](https://apps.apple.com/us/app/bbedit/id404009241?mt=12) on OSX or [notepad ++](https://notepad-plus-plus.org/downloads/) on Windows.

## Exercise 1: Gather by Term and Hashtag
Let's say you want to gather Twitter data on users around a given topic that is encapsulated by a hashtage or a series of terms. As noted in the warm up section, you can gather tweets as they happen using the ```filter``` query and the past week's tweets using the ```search```.

For this exercise, we want to gather tweets on the coronavirus, which are differentiated here for search and filter:

```twarc search coronavirus,corona virus > coronavirussearch.jsonl```  
or  
```twarc filter coronavirus,corona virus > coronavirussearch.jsonl```

Note, we are using two different spellings of the coronavirus to capture the term as it's been used on Twitter.

Using either of these commands will gather all tweets on Twitter using the term. However, we will want to delmit this information either by geolocation and/or language.

As noted in the warm up section, you could use ```geocode``` to limit tweets by a geolocation, like Toronto:

```twarc filter coronavirus --geocode 43.653226,-79.383184,10mi > coronavirustweetsastheyhappen.jsonl```  
or  
```twarc search coronavirus --geocode 43.653226,-79.383184,10mi > coronavirustweetspreviousweek.jsonl```  

You can also use language as Twitter attempts to code the language of a Tweet (note, this is not 100% accurate). You can limite your search to a particular language using an [ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) code:

```twarc filter coronavirus --geocode 45.501689,-73.567256,10mi --lang fr > coronavirustweetsastheyhappen.jsonl```  
or  
```twarc search coronavirus --geocode 45.501689,-73.567256,10mi --lang fr > coronavirustweetspreviousweek.jsonl```  

As you can see from this example, we differentiated the search and filter commands by the location of Montreal and the language French. This type of filter can be useful when you're trying to get a sense of how a specific community in a geolocation tweets about a topic.

## Exercise 2: Gather by Twitter Account
Another strategy to gather Twitter data is by selecting specific Twitter accounts. As noted in the warm section, you can gather tweets as they happen using the ```filter``` query and the past week's tweets using the ```search```.

For this exercise, we want to gather tweets sent out by specific organizations on the coronavirus, which are differentiated here for search and filter. Note, we use the ```follow``` command followed by the userid of the Twitter account. To get the userid of an account, [GetTwitterID](http://gettwitterid.com/) can generate a userid using the twitter handle as input. In the case of this example, we are gathering all tweets from the World Health Organization on the coronavirus:

```twarc filter coronavirus --follow 14499829 > coronavirustweetsbyorganizationlive.jsonl```  
or  
```twarc search coronavirus --follow 14499829 > coronavirustweetsbyorganizationpast```

As you can see, it will only scrape tweets sent by this organization when they tweet the term coronavirus. Some researchers may want to develop a list of accounts they want to follow on a topic and these can added to the ```follow``` function by adding a comma (```,```) with no spaces after each each userid.

## Final Thoughts
As you become increasingly comfortable with the command line, you will find twarc a helpful addition to your digital research toolkit. If there is a selection of twitter data that you want to download for text mining and analysis, a quick twarc command will be quicker than scraping the links manually. While this workshop focuses on a few of the commands, a fuller list with quick examples can be found at the [twarc GitHub project](https://github.com/DocNow/twarc).
