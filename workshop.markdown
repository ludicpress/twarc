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

Visit GitHub.com and click on the “Sign up” button on the upper right. Write your desired username. This will be visible to others, identify you on GitHub, and also be part of your site’s URL; for example, this author’s GitHub username is ludcipress and hia demo statis site’s URL is http://ludicpress.github.io/jekylldemo/. (Note you can also purchase your own domain name and use it for this site, but that won’t be covered in this workshop). Also write your desired email address and password, then click “Create an account”.

On the next page, click the “Choose” button next to the “Free” plan option, ignore the “Help me set up an organization next” checkbox, and click “Finish sign up”.

Optional: Visit https://github.com/settings/profile to add a full name (can be your real name, GitHub user name, or something else) and other public profile information, if desired.

Now that you have a GitHub account we can upload your website folder to GitHub using Git in the command line. However, we first need to create a new repository in GitHub so we have somewhere to send our website folder. While still logged in to GitHub you can add a new repository by clicking on the ```+``` icon in the top right-hand side of the page. Select the option ```new repository```. In the new repository, use the same name as the project folder and select the option ```Public``` before clicking the ```Create repository``` button. This ensures your site will be live when you upload the website folder. Keep the next page open as you'll need it for the next step.

## Git
Now that we have a repository we need to use Git to upload our website folder. On the GitHub page after you created the repository there should be a link that looks something like this:

```https://github.com/ludicpress/jekylldemo.git```

This is the web address that your website folder will use to push its contents to the repository on GitHub. Copy this link and go back into your command line interface.

Next we need to go into the folder using the ```cd``` command:

```cd jekylldemo/

In your command line, type and enter:

```git config --global user.email "you@example.com"
```git config --global user.name "your name"

We need to track our files:

```git add .```

This tracks all files in folder:

```git remote add origin [your copied URL]```

Mine looks like this:

```git remote add origin https://github.com/ludipress/jekylldemo.git```

You will then need to initialize your first commit:

```git push -u origin master```

You will be prompted to sign in with your username and password

Wait a few moments for the task to be complete. Once your command prompt reappears go back into your GitHub repository and refresh your webpage. The website folder with all your files should now be there.

But wait, you have one last step to complete before your site is live. In GitHub, click on branch and type in a new branch labelled ```gh-pages``` in the name field and then click ```Create branch```. Make sure this branch is your default branch so any changes you make are made to your website and not the original master file you uploaded. 

You can now visit your static site. The URL of your website will look like the following:

```username.github.io/websitefolder/```

My site looks like:
```ludicpress.github.io/jekylldemo/```

## Edit your Static Site
Congratulations, your static site is live! But wait, there is so much more you can do! It also may not look much like a website if some of the settings are missing from the ```_config.yml``` file. In this next section I will give an overview of how to navigate your website folder files and edit those files which represent your web pages, posts, and templates.

From now on all edits you make can be done in the GitHub interface. The first thing we need to go is edit the ```_config.yml``` file and make sure some of our build settings are good. Open up the file and click on the little pencil icon to edit the file. Here you can edit your ```Site Settings``` and ```Build Settings```. In the site settings you can edit the fields, but in the build settings we need to make sure your site is working properly.

You should see the following information in the build settings:


If not, copy and paste the above and put it just below the build settings heading.



## Final Thoughts
As you become increasingly comfortable with the command line, you will find wget a helpful addition to your digital research toolkit. If there is an entire set of archival documents that you want to download for text mining, if they’re arranged in a directory and are all together (which is not as common as one might think), a quick wget command will be quicker than scraping the links with Python. Similarly, you can then begin downloading things directly from your command line: programs, files, backups, etc. You will soon find that wget may be a first option for you to research all kinds of web content!
