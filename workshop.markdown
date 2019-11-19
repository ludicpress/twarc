---
layout: page
title: Workshop
permalink: /workshop/
---

Does your research require you to build a static website to document your project or disseminate information as part of a knowledge mobilization requirement? In this workshop you will learn how to build a Jekyll static website using GitHub pages. You will learn some command line fundamentals and be introduced to Jekyll, Ruby, Git and GitHub. By the end of the workshop you will have your own Jekyll website hosted on GitHub pages.

For this workshop we are going to build your Jekyll site and then upload it to GitHub using Git commands in your command line interface. Once the Jekyll website repository is uploaded to GitHub, we will configure your Jekyll repository to GitHub pages, which will make your project a live website.

## Build a Jekyll Site
Before we begin the workshop you need to make sure Jekyll is installed on your machine. Make sure to consult the [Setup page](https://ludicpress.github.io/staticsites/setup/) if you have not installed Jekyll on your Linux, Windows or OS X machines.

The first thing we will do is create a Jekyll website based on its default template. At the command line, type in the following and hit enter. Note, where I have typed in ```jekylldemo``` you can type anything, but keep in mind this will be the name of your Jekyll website repository:

```jekyll new jekylldemo```

This command told Jekyll to create a new site by installing all the necessary files in a folder names ```jekylldemo```. This folder will be referred to as the website folder for the rest of the workshop. 

You have created your first static site, congratulations! Obviously, there is still a lot more work to do in terms of adding content, but now we can move onto the next stage and add the site to GitHub using Git.

## GitHub
Before we can use Git to upload our website folder to GitHub, we need to create a GitHub user account. A GitHub user account will let you host your website for free on GitHub. In addition, GitHub will also let you keep track of versions of the website and its writing as it grows or changes over time.

Visit GitHub.com and click on the “Sign up” button on the upper right. Write your desired username. This will be visible to others, identify you on GitHub, and also be part of your site’s URL; for example, this author’s GitHub username is ludcipress and hia demo statis site’s URL is http://ludicpress.github.io/statissites/. (Note you can also purchase your own domain name and use it for this site, but that won’t be covered in this workshop). Also write your desired email address and password, then click “Create an account”.

On the next page, click the “Choose” button next to the “Free” plan option, ignore the “Help me set up an organization next” checkbox, and click “Finish sign up”.

Optional: Visit https://github.com/settings/profile to add a full name (can be your real name, GitHub user name, or something else) and other public profile information, if desired.

Now that you have a GitHub account we can upload your website folder to GitHub using Git in the command line. However, we first need to create a new repository in GitHub so we have somewhere to send our website folder. While still logged in to GitHub you can add a new repository by clicking on the ```+``` icon in the top right-hand side of the page. Select the option ```new repository```. In the new repository, use the same name as the project folder and select the option ```Public``` before clicking the ```Create repository``` button. This ensures your site will be live when you upload the website folder. Keep the next page open as you'll need it for the next step.

## Git
Now that we have a repository for our website folder to go into we need to use Git to make sure 

## Markdown


## Final Thoughts
As you become increasingly comfortable with the command line, you will find wget a helpful addition to your digital research toolkit. If there is an entire set of archival documents that you want to download for text mining, if they’re arranged in a directory and are all together (which is not as common as one might think), a quick wget command will be quicker than scraping the links with Python. Similarly, you can then begin downloading things directly from your command line: programs, files, backups, etc. You will soon find that wget may be a first option for you to research all kinds of web content!
