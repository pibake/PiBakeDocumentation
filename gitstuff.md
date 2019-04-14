# How to operate `git` and GitHub
Written by Wyatt J. Miller, 2019

This file is for internal documentation only. To my teammates, please use this as a reference guide on how to operate `git` and how to interface with GitHub. I'm assuming that you have some basic file commands. 

## Installation

First, you have to install [git](https://git-scm.com/). This is essential. If you do not have this, you will git errors (see what I did there?).

Once you have installed `git`, press the Super (Windows) key, type git and you'll see Git Bash as an option, if you have Windows of course.

If you're on Ubuntu Linux, type the following:<br>
`sudo apt install git`

If you're on macOS, install the Homebrew package manager and install git that way. This is needed for automatic updates to `git` without having to go grab it from the website.

If the installation had no errors, type:<br>
`git --version` to see the version and check if `git` is installed.

## Cloning all the things

To clone a repo, type the following:<br>
`git clone https://web/address/to/git/repo`

This will clone the `master` branch of the repository you entered to your local machine. This repository is your working directory for your repository. Remeber this because the phrase will come up later in the documentation. If you want to clone a different brach to your local machine, type the following:<br>
`git clone https://web/address/to/git/repo -b branch_name`

Note that `branch_name` can be whatever your branch name is.

If you haven't already, change your current directory to the directory you just cloned.

## Craft your own branch (optional)

To create your own branch on your local machine, type the following:<br>
`git checkout -b branch_name`

Note that `branch_name` can be whatever your branch name is.

## Staging your files

You have added and/or modified some files in your working directory. Awesome! Now, it is time to stage your files. To see your status of yoour files, type:<br>
`git status`

To stage all of your files, type:<br>
`git add .`

To stage a particular file, type:<br>
`git add path/to/file`

## Commiting stuffs

Once you have staged your files, you can now commit your changes! Type:<br>
`git commit -m "I'm a commit! Woo!"`
to commit on your local machine.

## Pushing to GitHub

Once your ready to push your commits onto GitHub, type:<br>
`git push origin master`

Replace `master` with the branch you'd like to push.

If you have a branch that you have created yourself, type the following instead:<br>
`git push -u origin branch_name`

Note that `branch_name` can be whatever your branch name is.

## Back to the Future

If you have to go back commits, it's really simple! To go back to only fiddle around with previous commits, type:<br>
`git checkout commit`

Better yet, if you have to go back, create a branch. That way, you'll always a place to go back to whenever you made a breaking change. Type:<br>
`git checkout -b commit`

Note that `commit` is the the alphanumeric string of characters that's on your commit. You can find these by typing:<br>
`git log` or `git log -n 5` to check the five latest commits on your current branch.
