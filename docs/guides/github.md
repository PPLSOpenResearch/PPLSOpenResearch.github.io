---
layout: default
title: Github Tutorial
parent: Guides
nav_order: 4
---

# Github Tutorial for Beginners
{: .no_toc }

*Created by Bonan Zhao on Aug 1, 2021*

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

---

## Introduction

### What is GIT?

[GIT](https://git-scm.com) is a piece of software that allows you to save your work at any given moment in time. It's typically called a `version control system`, which essentially means that it allows you to create versions of your workspace and makes possible to switch between older and newer states.

<details markdown="block">
<summary>More</summary>
You can think of it like a video game. You get to a certain point in the game, after hours of struggle. You're really proud of how far you've come, and don't want to do it over again in case you die. So you decide to save your game. If something bad happens after that point you can always reload your game and start from that point on.

This is exactly what happens with GIT: however, instead of calling it saving your game we call it committing your changes. A "change" is a code modification you made within a working day.

If you ever would want to go back to a previous game save you can make GIT help you do so by checking out to that commit. You will learn more about that in the next sections.

Check out the following short clip to learn about the essentials of GIT:

* [GIT explained in 100 seconds](https://www.youtube.com/watch?v=hwP7WQkmECE)
</details>

### What is Github

[GitHub](https://github.com) is an online software development platform that allows you to store a copy of your code online.
GitHub allows us to freely store code online (or remote, as most developers call it), and work together with others using one central (and remote) repository.

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

After you installed GIT you can use it through the your terminal (MacOS & Linux users) or Git Bash (Windows users). To verify that it worked, enter the command:

  `git --version`

It should say that the version is 2.32.0 (or up if you've installed a new version).

Now that you have GIT installed, it's important to make a basic configuration. Inside your CLI, type in the following (Replace "Your name" and "your.email@youremailserver.com" with your own name and email address, respectively):

  ```
  git config --global user.name "Your name"
  git config --global user.email "your.email@yourmailserver.com"
  ```

This makes sure GIT is able to identify you as the person that uses it to save your files and folders.

Some basic GIT commands you will learn later include: `git init`, `git add`, `git commit`, and `git push`. For self-learners, here is a list of helpful materials:

* [GIT Tutorial for beginners (Youtube)](https://www.youtube.com/watch?v=HVsySz-h9r4)
* [Introduction to GIT - Core Concepts (Youtube)](https://www.youtube.com/watch?v=uR6G2v_WsRA)
* [GIT & GitHub Crash Course (Youtube)](https://www.youtube.com/watch?v=SWYqp7iY_Tc)
* [Git Playground](https://git-school.github.io/visualizing-git/)

## Safe connection

When working with online (remote) code repositories, you might be dealing with unsecure connections. In order to make the connection more secure, you can use SSH - short for `Secure Shell`.

The concept of secure networking through use of identifiers (eg., a SSH key) is also known as "authentication": are you who you say you are? Authentication is a central idea within programming and you should keep it in mind.

Check the following resources for more information:

* [Beginners Guide To SSH](https://www.youtube.com/watch?v=qWKK_PNHnnA)
* [How SSH works](https://www.youtube.com/watch?v=zlv9dI-9g1U)

To connect your computer with your online Github project, follow this [official instruction](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh).

## Create your first Github repository

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

Whenever you want to update your repository, repeat steps 2, 3 and 5. You can think about these three steps as if you were sending a package:

* Command `git add .` is like adding everything into a delivery box
* Command `git commit -m "note"` is like writing the sending information for the delivery box
* Command `git push` is like the act of sending out the delivery box

Note that Github also has a desktop app that helps you manage repository update without command line: <https://desktop.github.com>.

One of my favorite meme about Github:

![]({{ site.baseurl }}{% link assets/images/github_meme.png %})

## Advanced topics

Collaboration on Github is usually done via `branch`, `fork`, and `pull request`.

## Acknowledgement

Most of the content in this tutorial is adapted from [HackYourFuture](https://github.com/HackYourFuture)'s [teaching material](https://github.com/HackYourFuture/HTML-CSS/blob/master/Week2/README.md), maintained by their awesome volunteers.

---

<!-- [Next: Six pillars of open research]({{ site.baseurl }}{% link docs/guides/six_pillars_of_open_research.md %}) -->
