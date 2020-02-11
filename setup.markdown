---
layout: page
title: Setup
permalink: /setup/
---

Before we start the workshop component of how to build an archive of Twitter data with the command line tool twarc, there is some there is some preliminary setup we have to complete on your computer and with Twitter. Since twarc is used through the command line, we have to install packages onto your computer for it work. Depending on which operating system you use, setup can be straightforward or the most time consuming aspect of learning how to use twarc. Below are installation instructions for Linux, Windows, and OS X users. Once wget is installed on each system, the instructions will be the same for every user participating in the workshop.

Before we install twarc we need to register an application at [developer.twitter.com](https://developer.twitter.com/en/apps). To do this you will need a Twitter account and then register as a developer. Once these steps are completed you can register an application by clicking the ```create an app``` icon. The app is required to generate the API keys we need to interact with twarc to build an archive of data. To create the app there are a series of required fields which need to be filled out, including: App name, Application Description, Website URL, and Tell us how this app will be used. There is no magic recipe to filling out the form. However, it is important that you emphasize the app is for research purposes only as you are not using the app for commercial or government purposes. I used the following information when I created the application:

```App name: twarc research profile 1```  
```Application description: To be used to gather research data in the twarc command line tool.```  
```Website URL: [enter your url]```  
```Tell us how this app will be used: The app will be used to communicate with twarc to archive tweets for analysis in research projects on social media.```  

When prompted, be sure to read the [Developer Agreement and Policy](https://developer.twitter.com/en/developer-terms/agreement-and-policy) and Twitter's list of [restricted use cases](https://developer.twitter.com/en/developer-terms/more-on-restricted-use-cases).

You may receive a follow up from Twitter about your app, but it is a relatively straightforward process you can complete in a few minutes. You may need to wait a day or two to receive your confirmation, which is why it is important to complete this step first.

## Linux Instructions
Ubuntu ships with Python 3, as the default Python installation. Complete the following steps to install pip (pip3) for Python 3. Start by updating the package list using the following command in the command line:

```sudo apt update```

Once the package list is updated, use the following command to install pip for Python 3:

```sudo apt install python3-pip```

When prompted to select ```yes``` or to type ```y```, please do so to install the package. The command above will also install the dependencies required for building Python modules.

Once the installation is complete, verify the installation by checking the pip version:

```pip3 --version```

The output version my vary, but it will look something like this:

```pip 9.0.1. from /usr/lib/python3/dist-packages (python 3.6)```

Now that pip is installed, we can use it to install twarc. Type and enter the following command into the command line:

```pip3 install twarc```

It will proceed to download the most recent version of twarc, which is wget 1.75. After the script stops running, and you are back to your main window, enter the following command into the terminal:

```twarc```

If twarc has installed, you will see almost a dozen lines of commands that end with the following statement:

```twarc: error: the following arguments are required: command```

This means twarc has installed and you need to use an argument after twarc. If twarc is not installed on your system it will respond with:

```$ command not found.```

At this point, however, twarc should be installed successfully. If it is not installed, go through each of the steps above to make sure you did not make a mistake installing pip.

## Windows Instructions
To install twarc we have to activate the Windows Subsystem for Linux (WSL) and install a Linux distro (i.e., command line). For this workshop we will use the Ubuntu application on Windows, but first we have to activite the WSL.

To activate the WSL, open Powershell as an Administrator. To do this, type in Powershell in the Windows search bar in the bottom left corner of your screen. The application Windows Powershell Ise will appear. On the right-hand side of the window will be the option 'Run as administrator'. Select Run as administrator and enter your administrative login credentials if prompted. If you do not run Powershell as an administrator the next step will not work.

In the Powershell terminal that opens up, copy and paste the following command and hit enter:

```Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux```

Restart your computer when prompted to do so.

Once your computer has restarted, open the Microsoft Store. You can access the Microsoft Store by typing Microsoft Store in the Windows search bar and select open from the right-hand side of the window. When the Microsoft Store opens, type 'Ubuntu' into the search bar. Several Ubuntu applications will appear in the search results. Select the app that is only titled 'Ubuntu' and developed by Canonical Group Limited.

Click install and wait for the Ubuntu application for Windows to install. Once the application has installed, type Ubuntu in the Windows search bar and open the application. Note, you do not need to Run as administrator for this application. The Ubuntu application will take approximately 5 to 10 minutes to install, so do not worry if it does not open right away.

When Ubuntu opens for the first time you will be propted to create a username and password. Create your username and hit enter. Create your password and hit enter. A re-enter password prompt will appear and you re-enter your password. Your username and password should now be created. Whenever you open Ubuntu and try to install software you will be prompted for your username and password.

Now that Ubuntu is installed and you have created a username and password we can go ahead and install Pip. Pip is a package management system that simplifies installation and management of software packages written in Python, such as twarc. Pip is not installed by default on Ubuntu 18.04, but the installation is pretty straightforward.

Ubuntu 18.04 ships with Python 3, as the default Python installation. Complete the following steps to install pip (pip3) for Python 3. Start by updating the package list using the following command:

```sudo apt update```

Once the package list is updated, use the following command to install pip for Python 3:

```sudo apt install python3-pip```

When prompted to select ```yes``` or to type ```y```, please do so to install the package. The command above will also install the dependencies required for building Python modules.

Once the installation is complete, verify the installation by checking the pip version:

```pip3 --version```

The output version my vary, but it will look something like this:

```pip 9.0.1. from /usr/lib/python3/dist-packages (python 3.6)```

Now that pip is installed, we can use it to install twarc. Type and enter the following command into the command line:

```pip3 install twarc```

It will proceed to download the most recent version of twarc, which is wget 1.75. After the script stops running, and you are back to your main window, enter the following command into the terminal:

```twarc```

If twarc has installed, you will see almost a dozen lines of commands that end with the following statement:

```twarc: error: the following arguments are required: command```

This means twarc has installed and you need to use an argument after twarc. If twarc is not installed on your system it will respond with:

```$ command not found.```

At this point, however, twarc should be installed successfully. If it is not installed, go through each of the steps above to make sure you did not make a mistake installing pip.

## OS X Instructions
To install twarc on OS X there are several dependencies we need to install, including Apple's Command Line Tools and Homebrew. This requires downloading XCode. If you have the App Store, you should be able to just download XCode.  If not, the following instructions will work.

To download this, go to the Apple Developer website, register as a developer, and then in the downloads for Apple developers section you will need to find the correct version. If not, you will need to click on the link: “Looking for additional developer tools? View Downloads.”

After logging in with your free developer credentials, you will see a long list. Type ```xcode``` in the search bar and find a version that is compatible with your operating system version. This may take some clicking around to find the right version for you. For example, Xcode 3.2 is the version for OS X 10.6 Snow Leopard, 3.0 is the version for OS X 10.5 Leopard, etc.

It is a big download, and will take some time. Once you have the file, install it (when I timed the download it took almost 15 minutes!).

You will need to install the ‘Command Line Tools’ kit in XCode. Open up the ‘Preferences’ tab, click on ‘Downloads,’ and then click ‘Install’ next to Command Line Tools. We are now ready to install a package manager.

The easiest package manager to install is Homebrew. Go to https://brew.sh and review the instructions. There are many important commands, like Jekyll, that are not included by default in OS X. This program facilitates the downloading and installation of all required files.

To install Homebrew, open up your terminal window and type the following:

```/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"```

This uses the ruby programming language, built into OS X, to install Homebrew. If prompted to press ```RETURN``` hit returnTo see if the installation worked, type the following into your terminal window:

```brew```

A list of documentation options should appear if it has been installed. We have one more command to run to make sure everything is working, which is:

```brew doctor```

With Homebrew installed, we now have to install twarc. This is now an easy step.

```brew install twarc```

It will proceed to download the most recent version of twarc, which is wget 1.75. After the script stops running, and you are back to your main window, enter the following command into the terminal:

```twarc```

If twarc has installed, you will see almost a dozen lines of commands that end with the following statement:

```twarc: error: the following arguments are required: command```

This means twarc has installed and you need to use an argument after twarc. If twarc is not installed on your system it will respond with:

```$ command not found.```

At this point, however, twarc should be installed successfully. If it is not installed, go through each of the steps above to make sure you did not make a mistake installing Homebrew.
