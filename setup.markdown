---
layout: page
title: Setup
permalink: /setup/
---

Before we start the workshop component of how to build a static website with Jekyll and GitHub for digital research there is some preliminary setup we have to complete on your computer. There are several ways to install the different components we need to create a static Jekyll website on GitHub. We will approach setup through the command line. Depending on which operating system you use, setup can be straightforward or the most time consuming aspect of learning how to build a Jekyll website on GitHub pages. Below are installation instructions for Linux, Windows, and OS X users. Once Jekyll is installed on each system, the instructions will be the same for every user participating in the workshop.

## Linux Instructions

## Windows Instructions


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

