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

###Making a change and commiting the changes
Once you have a local copy of this repo all set up, now is when you can finally make a change! the simplest change to make would be to simply open the *index.html* file and add this line of code above the comment in the *index.html* file (replace 'Your Name!' with your real name)

```
<div class="nameBlock">
  <h2>Your Name!</h2>
</div>
```
and save *index.html*. if you open *index.html* You'll see that your name is now added to the page!

Now you'll want to 'commit' that change to the git repo. to commit the changes you make, simply run these commands

```
git add .
git commit -m "Type a Commit Message Here!"
```

These Commands will *stage* your changes to be *committed*, and the commit will permanently save your changes to the local git repo. If you want to keep making more changed and committing them, feel free to do so!

###uploading your changes to your fork
Now, we need to upload your new changes to the files to your fork located on github, if you remember from earlier, you will have Two remotes, *origin* which should be your fork, and *upstream* which should be the main codebase for RMIT-HealthTech.

before uploading your changes, we should check to see if there are any new changes tot he RMIT-HealthTech repo, to download any new changes, commit any changes you have made and then run
```
git pull upstream master
```
this will grab all the latest changes, and merge them with your changes to the code. Once that is complete, upload your changes to your fork on github!
```
git push origin master
```
Just a warning, never, ever force push your commits to a remote, as force pushing can cause a lot of headache when using features of git that allow you to see old code and revert changes.

###Finally, merging your changes into the RMIT-HealthTech repo
Now that you have uploaded your changes, You will want to merge your changes into main RMIT-HealthTech repo. in order to do so, you will need to open a *Pull Request* to merge your changes into RMIT-HealthTech/master. In order to do that, please refer to this [documentation on opening Pull Requests](https://help.github.com/articles/creating-a-pull-request/)

Once someone merges your Pull Request, your changes should be available for everyone to pull down!
