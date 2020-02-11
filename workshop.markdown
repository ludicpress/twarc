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


## Exercise 1:


## Exercise 2:


## Exercise 3:


## Final Thoughts
There is still plenty more to learn with Jekyll and GitHub pages. There are also dozens, if not hundreds, of themes available to use instead of the Minima theme that comes with this tutorial. In addition, there are many digital research groups creating static page themes in Jekyll, such as the [Minimal Computing](https://github.com/minicomp) for digital editions, digital exhibits, and a range of other static sites for humanities and social science projects. If this is your first time with static sites, don't be dismayed by the learning curve or the simplicity. The payoff can be great depending on your digital research goals and projects.
