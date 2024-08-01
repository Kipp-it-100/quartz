---
title: 
tags:
  - tutorial
icon: 
aliases:
---
When you think your connection may be running slow, you probably know that you can check you speed at speedtest.net.  However, this browser site is chock full of ads and itself can be a little heavy on system resources.  Here's how to download and run Ookla's lightweight CLI (Command Line Interface) speed test on Mac, PC, and Linux.
## On Mac
For installing on macOS will be using Homebrew, a popular macOS package manager to install the command line speed test.  If you do not already have Homebrew installed, simply open Terminal.app and run the following command: 

```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Once Homebrew is installed, leave Terminal open.  Next, we will be running the command which will tell Homebrew to install the package for the command line speed test.  
```shell
brew install speedtest-cli
```
Voila! Once homebrew is finished, you will be able to run your speed test directly from the command line.  Do so by typing:
```shell
speedtest-cli
```
Then, hit enter and enjoy the quick analysis of your connection speed without having to open a browser window, skipping the slowdown that can come from Ookla's bombarding of ads!
## On Windows
Installing the speedtest cli on PC is exceedingly simple.  First, navigate to the following link: https://www.speedtest.net/apps/cli.  Scroll down and you'll see an option to download the app for Windows.  Note that the Speedtest command line interface app is only available for 64-bit installations of Windows.

Click the button labeled "Download for Windows."  Once you extract (unzip) the resulting download, you'll be left with a file called "speedtest.exe."  Place this file wherever you would like, keeping in mind that its specific file path will need to be referenced when running.  I suggest placing it at C:\Program Files\speedtest.exe as it is easy to remember and is accessible by all user accounts on your PC.  For easy deployment, consider making a desktop shortcut or pinning speedtest.exe to you Window's taskbar

To run the application from the command line itself, or if you want to include it in a bigger script, simply input the full file path to the application in Command Prompt, Powershell, or Terminal and press enter.
```
"C:\Program Files\speedtest.exe"
```
## On Linux
Instructions for installing on Linux may vary as there are so many different Linux distributions that may use default package managers specific to specific distros.  With that in mind, we are going to go over how to install the Speedtest CLI on one of the most common flavors of Linux: Debian/Ubuntu.

First, open a trusty terminal window.  Now, before we run the actual command to install the speed test, we need to update the repsitory for  our package manager.  To do this we will be using a "curl" command.  If you don't have curl installed, or if your are unsure, first run the following command:
```shell
sudo apt-get install curl
```

Once curl is installed, then proceed to run the following command that points apt to the correct, most current repository for the Speedtest CLI Linux app:
```shell
curl -s https://packagecloud.io/install/repositories/ookla/speedtest-cli/script.deb.sh | sudo bash
```

Now that apt is set to use the correct package repository, we can finally run the final command which will actually install app, after which it will be ready for use:
```shell
sudo apt-get install speedtest
```

There you have it! From there, you can run your speedtest from within anywhere in your Linux filesystem by simply typing "speedtest" and hitting enter.

