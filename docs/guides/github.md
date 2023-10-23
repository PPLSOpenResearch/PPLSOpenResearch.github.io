---
layout: default
title: Github tutorial
parent: Guides
nav_order: 3
---

# Github Tutorial for Beginners
{: .no_toc }

*Created by Bonan Zhao on Aug 1, 2021*

*Updated by Georgia Carter on Nov 10, 2022*

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>


## Introduction

### What is GIT?

[GIT](https://git-scm.com) is a piece of software that allows you to save your work at any given moment in time. It's typically called a `version control system`, which essentially means that it allows you to create versions of your workspace and makes it possible to switch between older and newer states.

<details markdown="block">
<summary>More</summary>
You can think of it like a video game. After hours of struggle, you get to a certain level in the game. You're really proud of how far you've come, and don't want to do it over again in case you die. So you decide to save your game. If something bad happens after that point you can always reload your game and start from that point onwards.

This is exactly what happens with GIT: however, instead of calling it saving your game, we call it committing your changes. A "change" is a file modification you have made.

Check out the following short clip to learn about the essentials of GIT:

* [GIT explained in 100 seconds](https://www.youtube.com/watch?v=hwP7WQkmECE)
</details>

### What is Github

[GitHub](https://github.com) is an online software development platform that allows you to store a copy of your code online.
GitHub allows us to freely store code online (or remotely, as most developers call it), and work together with others using one central (remote) repository.

<details markdown="block">
<summary>More</summary>

* To learn more about Github: [What is GitHub? on Youtube](https://www.youtube.com/watch?v=w3jLJU7DT5E)
* [GIT Good: A Practical Introduction to GIT and GitHub I](https://codeburst.io/git-good-part-a-e0d826286a2a)
* [GIT Good: A Practical Introduction to GIT and GitHub II](https://codeburst.io/git-good-a-practical-introduction-to-git-and-github-in-git-we-trust-f18fa263ec48)
</details>


## Installation

1. Install Git
    * For Windows, install [Git Bash](https://git-scm.com/download/win)
    * For MacOS, install [GIT](https://git-scm.com/download/mac)
    * For Linux, install [GIT](https://git-scm.com/download/linux)

2. Create a Github account at <https://github.com>

## Basic GIT commands

After you've installed GIT you can use it through the your terminal (MacOS & Linux users) or Git Bash (Windows users). To verify that it worked, enter the command:

  `git --version`

It should say that the version is 2.32.0 (or higher if you've installed a newer version).

Now that you have GIT installed, it's important to make a basic configuration. Inside your command line interface, type in the following (Replace "Your name" and "your.email@youremailserver.com" with your own name and email address, respectively):

  ```
  git config --global user.name "Your name"
  git config --global user.email "your.email@yourmailserver.com"
  ```

This makes sure GIT is able to identify you when saving your files and folders.

Some basic GIT commands you will learn later include: `git init`, `git add`, `git commit`, and `git push`. For self-learners, here is a list of helpful materials:

* [GIT Tutorial for beginners (Youtube)](https://www.youtube.com/watch?v=HVsySz-h9r4)
* [Introduction to GIT - Core Concepts (Youtube)](https://www.youtube.com/watch?v=uR6G2v_WsRA)
* [GIT & GitHub Crash Course (Youtube)](https://www.youtube.com/watch?v=SWYqp7iY_Tc)
* [GIT Playground](https://git-school.github.io/visualizing-git/)

## Authentication 

In order to securely connect the device that you are using with your GitHub account, GitHub requires authentication to check that you are who you say you are. Think of this as 'logging in' to your GitHub account on a particular device.

One way to do this is through SSH - short for `Secure Shell`. One of the good things about SSH is that you can authenticate a device (say your personal laptop) once, and store the key so that you do not need to redo this process. 
GitHub provides [useful documentation](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) to help walk you through the process of first setting up SSH on your device. But we'll also discuss the most important steps here. 

### Check for existing SSH keys
The first thing to do is check whether you already have existing SSH keys. This page of the documentation has the instructions in detail, along with the code commands you will want to use in either Git Bash or your terminal. 
[Checking for existing SSH keys](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys). 
You can toggle the instructions for your particular operating system (Mac, Windows or Linux). Also, you do not need to navigate to the folder with your local git repo in it just yet.

If you do not have an existing SSH key with one of the three filenames GitHub assigns by default; these are one of: 
* id_rsa.pub
* id_ecdsa.pub
* id_ed25519.pub

### Generate a new SSH key
Here are the instructions in full [Generating a new SSH key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).

There's a little section about passphrases for your SSH key. It's essentially a password for the SSH key. For example, if someone got ahold of your device where you did not have a passphrase for your SSH key, then they'd have access to everything that required previous authentication. Passphrases act as a barrier against this. The downside is that you'll have to enter it every time you want to use the SSH key to connect to GitHub. However, you can add the passphrase to something called an SSH agent, which will remember the passphrases for each SSH key you've set up. 
Whether or not you want to set up a passphrase is up to you. 

### Adding the SSH key to ssh-agent 
For Mac and Linux, this can all be done from the Terminal. For Windows users, you will have to take an extra step to run the ssh-agent. You will need to auto-launch the ssh-agent for Git on Windows. The details for this can be found here [Auto-launching ssh-agent on Windows](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/working-with-ssh-key-passphrases#auto-launching-ssh-agent-on-git-for-windows). 

### Adding the SSH key to your GitHub account
We can then move on to adding the SSH key to your GitHub account as we'll ignore the hardware security key section. You will find the full details here [Adding a new SSH key to your GitHub account](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account). 
**Note:** Where the documtation mentions the Git CLI, it is either your Terminal or Git Bash 

Further, if you already have a local repo connection set up (with personal access tokens, for example), you can find the details on how to switch over to SSH here [Switching remote URLs from HTTPS to SSH](https://docs.github.com/en/get-started/getting-started-with-git/managing-remote-repositories#switching-remote-urls-from-https-to-ssh)

### Test the connection
This is the last step of setting up SSH. The instructions are comparatively straightforward for this (no huge differences for Windows thankfully) [Testing your SSH connection](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/testing-your-ssh-connection)

## Personal Access Tokens

Another way to authenticate your connection is by using personal access tokens (PATs). This is because GitHub recently removed authenatication with usernames and passwords. This means that when you are prompted to enter your username and password, you may receive an error if you enter your GitHub account password as is. 

To fix this, you will need to create a PAT and use this token as the password when prompted. 

You can find more information about this here:
* [Github Personal Access Tokens](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)

## Creating your first Github repository

Once you have sorted GIT, Github, and your SSH authentication, you are now ready to start sharing code on Github!

On Github, people use the word "repository" (or "repo", for short) to stand for a single project (think about one folder than contains all of your code for a project). Repositories can contain folders and files, images, videos, spreadsheets, and data sets – anything your project needs.

To create a new repository:

* Login to Github, and in the upper right corner, next to your avatar or identicon, click `+` and then select `New repository`.
* Name your repository `demo` (use your own project name instead of "example" here)

Once you created this new repo, Github will automatically show you how to update it. Usually you want to link an existing local folder to this Github repo. In this case:

1. In your local folder, type (in terminal or Git bash, see earlier note):
  ```
  git init
  ```
2. To add your stuff into the "uploads", type
  ```
  git add .
  ```
  Note the dot symbol `.`, it stands for "everything". Therefore, this command will add everything into the upload.
3. Then type
  ```
  git commit -m "initial commit"
  ```
  Replace `initial commit` with whatever descriptive comment you want to use. Here `-m` simply stands for "message".
4. Now, following what Github has suggested you:
  ```
  git remote add origin git@github.com:PplsOpenResearch/demo.git
  ```
  Similarly, replace `git@github.com:PplsOpenResearch/demo.git` with whatever yours is.
5. Finally, do
  ```
  git push -u origin main
  ```
  You need to use this command only for the first time pushing to a repository. After that, you just need to use the shorter version: `git push`.
  
6. Now refresh your repo's Github webpage, and you should be seeing everything online there.

**Note:** "main" is the default branch name for some users, while others may have "master" - you can check which yours is here
  
  ![]({{ site.baseurl }}{% link assets/images/github_branchname.png %})
  
  If you would like to change the name of the default branch, you can do so by navigating to Settings > Repositories
  
  ![]({{ site.baseurl }}{% link assets/images/github_defaultbranch.png %})

Whenever you want to update your repository, repeat steps 2, 3 and 5. You can think about these three steps as if you were sending a package:

* Command `git add .` is like adding everything into a delivery box
* Command `git commit -m "note"` is like writing the sending information for the delivery box
* Command `git push` is like the act of sending out the delivery box

Note that Github also has a desktop app that helps you manage repository update without command line: <https://desktop.github.com>. Another popular alternative is GitKraken <https://www.gitkraken.com/>.
If you're interested in learning more about git on the command line, you can find helpful info here: <https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html>.

## Going back in time 

If you accidentally make a mistake, and want to go back in time, you're able to reload your last save point (the game analogy strikes again!).

If you want a previous version of a file, there are a few steps you'll want to do: 

1. In your local folder, type (in terminal or Git bash, see earlier note):
  ```
  git log --oneline
  ```
  This allows us to see all of our previous commits, with their IDs. It is this ID that you want when trying to move back in time to a previous file version. 
  
2. Once you've got the commit ID, type:
  ```
  git checkout [commit ID] [filename]
  ```
  If you did not push the latest changes, you can also use ```HEAD``` instead of the commit ID; if you have pushed the faulty change, then you will need the commit ID.
  
Check out the following resources for more info: 

* [Restoring files](https://opensource.com/life/16/7/how-restore-older-file-versions-git)
* [Going back to a previous commit](https://www.atlassian.com/git/tutorials/undoing-changes/git-reset)

  
## Advanced topics

You can work on a different "version" of your project with `branches`.

* [Git Tutorial: Branches](https://www.youtube.com/watch?v=sgzkY5vFKQQ)
* [Introduction to GIT - Branching and Merging](https://www.youtube.com/watch?v=FyAAIHHClqI)

If you want to develop a project based on someone else's existing code, you can use `forks`.

* [About forks](https://docs.github.com/en/github/collaborating-with-pull-requests/working-with-forks/about-forks)

As a sum-up, try this [GitHub 'Hello World' Project](https://guides.github.com/activities/hello-world/).

## Acknowledgement

Most of the content in this tutorial is adapted from [HackYourFuture](https://github.com/HackYourFuture)'s [teaching material](https://github.com/HackYourFuture/HTML-CSS/blob/master/Week2/README.md), maintained by their awesome volunteers.

---

<!-- [Next: Open research data and materials]({{ site.baseurl }}{% link docs/guides/open_data.md %}) -->
