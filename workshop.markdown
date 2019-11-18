---
layout: page
title: Workshop
permalink: /workshop/
---

Does your research require you to build an archive of data from public websites? In this workshop attendees will learn how to automatically download webpages with the wget program in your command line interface without going through the tedious process of manually downloading webpages. Attendees will also be guided through the process of cleaning up data once it’s downloaded.

For this workshop we are going to walk through a few exercises using wget in your operating system's command line interface: terminal for Linux and OS X and Ubuntu for Windows. If you have followed the setup instructions to install wget on your Linux, Windows, or OS X machines then you are ready to begin the workshop. 

## Warm-Up

Before we begin there are a couple of exercises we need to go through before we can start the workshop. The first exercise is to make sure wget is installed. In the command prompt type in the following command and hit enter:

```wget --version```

Alternatively, you can type an abbreviated command and hit enter:

```wget -V```

Note that the uppercase ```-V``` is important. If you type ```-v``` you will receive an error message. Upper case and lower case characters are important with wget, like most programs in the command line.

After you type the command and hit enter you should receive a version message followed by information about your installation of wget, including copyright, license, and developer information:

```GNU Wget 1.19.4 build on linux gnu.```

At the time of writing the documentaton for this workshop the version of wget on my computer was 1.19.4. If you want to see if wget is up-to-date you can enter the following commands for Linux, OS X, and Windows:

Linux  
```sudo apt-get upgrade wget```

OS X (Homebrew)  
```brew upgrade wget```

Windows (Ubuntu)  
```sudo apt-get upgrade wget```

Depending on whether wget is up-to-date you will receive a message stating wget has been upgraded or wget is already the newest version.

Now that we know wget is installed and ready to go on your computer for some digital research we can try a few other commands. Another command that is really useful if you need instructions to help you craft your command is the help function. In the command prompt type in the following command and hit enter:

```wget --help```

Alernatively, you can type an abbreviated command and hit enter

```wget -h```

Note that the lowercase ```-h``` is important. If you type ```-H``` you will invoke the 'go to foreign hosts when recrusive' command and retrieve an error code because you have completed your command string. 

After you type in the command and hit enter you should receive a version message followed by a list of commands you can invoke using wget:

```GNU Wget 1.19.4, a non interactive network retriever.```  
```Usage: wget [OPTION]... [URL]...```  

You will notice this second line starting with ```Usage``` shows you how to use wget. You begin with the command ```wget``` followed by your options and ends with the URL where you want to retrieve web data. The options are listed in the command printout after you enter ```wget --help``` or ```wget -h```, which includes commands for:

Startup  
Logging and input file  
Download  
Directories  
HTTP options  
HTTPS (SLS/TLS) options  
HSTS options  
FTP options  
FTPS options  
WARC options  
Recursive download  
Recursive accept/reject  

You will observe that there are several command options, sometimes dozens, under each category. The list of commands might seem overwhelming, but rest assured we will only be using a handful in this workshop. It is important, however, to take note of the range of options available to you in wget because there is likely an option or string of options that will enable you to complete your digital research.

## Exercise 1: Retrieve a Webpage or File
Let's take an example file from the web. Say you want to download a news article hosted on *The Medium* website, UTM's student newspaper. First though, we need to create a folder for you to deposit your data. In your working directory, make a new directory. Let's call it wget-medium. To make sure you are in your home directory, type in and enter the following command:

```cd```

The command ```cd``` is the 'change directory' command. You use this command to navigate through your folders. When you type in ```cd``` you are automatically redirected to your home directory. When you type ```cd ..``` you navigate backwards one directory. 

To create a new folder in your home directory with the folder name wget-medium, type in and enter the following command:

```mkdir wget-medium```

The command ```mkdir``` is the 'make directory' command. You have probably noticed that many commands are just abbreviations of actions. If you ever need a list of commands for your terminal simply type and enter:

```help```

And a list of commands will print out followed by the version of your terminal. At the time of writing this workshop my version was 3.2.57 on a 64 bit Apple desktop:

```$ GNU bash, version 3.2.57(1)-release (x86_64-apple-darwin19)```

Now that you have created the directory, let's navigate to the director. Type in and enter the following command:

```cd wget-medium/```

The ```cd``` command also can navigate you to a folder from the folder you currently reside. Next we want to retrieve a news article from UTM news. First you need to get the url and then type in and enter the following command:

```wget https://themedium.ca/news/mississauga-asks-students-for-feedback-on-living-green/```

After some initial messages, you should see the following (however, some figures, dates, and some details will be different):

```--2019-10-09 13:14:35--  https://themedium.ca/news/mississauga-asks-students-for-feedback-on-living-green/```  
```Resolving themedium.ca (themedium.ca)... 104.28.7.47, 104.28.6.47```  
```Connecting to themedium.ca (themedium.ca)|104.28.7.47|:443... connected.```  
```HTTP request sent, awaiting response... 200 OK```  
```Length: unspecified [text/html]```  
```Saving to: ‘index.html’```  
```index.html              [ <=>                ] 113.03K  --.-KB/s    in 0.04s```  
```2019-10-09 13:14:58 (2.85 MB/s) - ‘index.html’ saved [115746]```

What you have done is downloaded just the raw text file of the UTM News article. If you open the HTML file it will appear in your browser. You now have a copy of the UTM news article that you can add to your research data.

## Exercise 2: Retrieve Multiple Files from a Website
Let's say you want to download copies of all The Medium's news articles. To do this we will need to enter in a few options to our wget script.

Wget operates on the following general basis:

```wget [OPTIONS] [URL]```

In the previous exercise we learned about the ```[URL]``` component of wget. ```[OPTIONS]```, however, give the program a bit more information about what exactly we want to do. the program knows that an option is an option by the presence of a dash before the variable. This lets wget know the difference between the URL and the options.

So let's now learn a few other commands to write a wget script to download all The Medium's news articles.

```-r```

Recursive retrieval is the most important part of wget. What this means is the program begins to follow links from the URL you provide and downloads them too. You will notice the URL we used is part of the ```/news/``` folder of the UTM website. So, if we use ```-r``` on the ```/news/``` folder it will download all the news articles in that folder. However, it will also follow any other links in the news articles that point to other websites. By default, ```-r``` sends wget to a depth of five sites after the first URL. This means it follows links, to a limit of five clocks after the first URL. At this point, your wget script could capture a lot of data you do not want. So, we need a few more commands.

```-np```

The command  ```-np``` is the 'no parent' command which can also be written as ```--no-parent```. This is an important command as it tells wget to follow links, but not beyond the last parent directory. In the case of this exercise, that means it won't go anywhere that is not part of the https://themedium.ca/news/ hierarchy. The no parent command is crtitical for delineating your search.

Finally, it is important to add in a few commands that slow down your wget script. Web servers handle a lot of traffic and the wget program will download everything you command it too immediately unless you tell it to wait. There are two commands you can use to slow downloads:

```-w [SECONDS]```  
and  
```--limit-rate=[KB/S]```  

The command ```-w``` is the 'wait' command and delays the download of each link by seconds. A good wait time is 2 seconds (```-w 2```) as it roughly represents how long it would take you to click from link to link. On rare occasions, you may come across a site that blocks automated downloading altogether. The website’s terms of service, which you should consult, may not mention a policy on automated downloading, but steps to prohibit it may be built into their website’s architecture nonetheless. In such rare cases, you can use the command ```--random-wait [SECONDS]``` which will vary the wait by 0.5 and 1.5 times the value of seconds you provide.

The command ```--limit-rate``` is the 'limit rate' of download speed for wget. You don't want to use up too much of the servers' bandwidth. The 'limit rate' command will limit the maximum downalod speed in kb/s. A good rate is around 200 kb/s for small files, but it's up to your discretion when setting a download speed limit. For this workshop, however, we are going to set our limit rate to 20 kb/s in case there are several people completing this exercise at the same time.

So, we are now ready to download news articles from The Medium. Note, the trailing slash on the URL is critical as it tells wget we are accessing news articles in a directory. If you omit the slash wget will think you are wanting to download a file. The order of the options does not matter, but here is a command you type in and enter:

```wget -r -np -w 2 --limit-rate=20k https://themedium.ca/news/```

The download will be much slower than before, but your terminal will being downloading all the news articles on *The Medium* website. When it is done you should have a directory labelled ```themedium.ca``` that contains the ```/news/``` sub-directory. This directory will appear in the location that you ran the command from your command line, so likely is in your ```USER``` directory. Links will be replaced with internal links to the other pages you have downloaded, so you can have a fully working themedium.ca site of news articles on your computer.

If for whatever reason you want to cancel the search you simply hit ```CTRL``` and ```C```together.

## Exercise 3: Mirror a Website
Let's say you want to copy an entire website, you would use the mirror function by using the command:

```-m```

The ```-m``` command mirrors an entire URL, and is especially useful for backing up an entire website. For digital research, this can be quite useful if you're doing historical research of social groups whose online presence is known to disappear, or who frequently change and update their web content. Mirror introduces the following set of commands: time-stamping, which looks at the date of the site and doesn’t replace it if you already have that version on your system (useful for repeated downloads), as well as infinite recursion (it will go as many layers into the site as necessary).

The command for mirroring *The Medium* website is:

```wget -m -w 2 --limit-rate=20k https://themedium.ca/```

As in the previous exercise, the download will be very slow, but The Medium website will be perfectly mirrored when complete showing all of the sub-directories. It is difficult to gauge how long this will take, but mirroring websites can sometimes take hours, even days depending on how much web content is on the website. This is especially the case for websites with audio-visual material.

## Final Thoughts
As you become increasingly comfortable with the command line, you will find wget a helpful addition to your digital research toolkit. If there is an entire set of archival documents that you want to download for text mining, if they’re arranged in a directory and are all together (which is not as common as one might think), a quick wget command will be quicker than scraping the links with Python. Similarly, you can then begin downloading things directly from your command line: programs, files, backups, etc. You will soon find that wget may be a first option for you to research all kinds of web content!
