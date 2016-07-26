#HealthTech git tutorial!

Welcome to RMIT-HealthTech, This is a quick little tutorial that will help you get all set up and ready to use git and github!

##Getting ready

Before learning how to use git, Here are a few things that will make life easier while using git

###Downloading some git tools
If you need some tools to help get started with git, I highly recommend these tools!

* [SourceTree - a GUI Git Client](https://www.sourcetreeapp.com/)

   To use this, you'll have to create a free account with Atlassian, but this is a completly free tool

* [cmder - a console emulator for Windows](http://cmder.net/)

   This is a console emulator that I mostly use because you can open up new terminals in tabs (Like an internet browser), so you can have cmd, powershell and git bash all open at the same time! If you download the full package, you'll have access to git within the terminal without having to install anything else.

* [Atom - open source IDE made by github](https://atom.io/)

   A fantastic IDE that has a ton of community packages, although we may not be using this IDE for this project for any Back End Development as Visual Studio will be more appropriate, but for this tutorial and for Front End Development, Atom is one of the best tools out there.

###Setting up an SSH key to use on github

To make it so that you don't have to keep typing your username and password to push/pull to a remote git repo on github, Follow this guide to setup a SSH key for your system to automatically allow you to read and write to and from github.

[SSH Key setup Guide](https://help.github.com/articles/generating-an-ssh-key/)

##Git Tutotial!

###Forking and setting up a local repo
After you have got all your git tools installed, the first thing you will need to do is to fork this repo. The repo hosted by RMIT-HealthTech will be the 'single source of truth' and should never be used for active development, instead, you should fork this repo and start making changes to your copy of this repo!

To do that, simply click on the *fork* button at the top-right hand corner of the repo screen, github will fork you a copy of this repo and you will be able to start making changes!

Once you have created your fork, you will need to get a copy of your fork down onto your machine, to do this, you simply need to run this command (replace <your-username> with your github username)

```
git clone git@github.com:<your-username>/git-funtimes.git
```
and this will download a copy of your fork to your machine.

The only thing left to do is to add a reference to the RMIT-HealthTech repo of this git tutorial, and to do that, you need to run this command
```
git remote add upstream git@github.com:RMIT-HealthTech/git-funtimes.git
```
If you type *git remote -v* into a command line, you will see that you'll have two references to remotes, *origin* which is your fork, and *upstream* which is RMIT-HealthTech's fork.
