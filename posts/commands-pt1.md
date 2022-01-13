---
title: Root to Linux, Hands-on Commands Part 1
description: In part 1 of this guide, you will learn and use some of the basic Linux commands to see your working directory, list directories and files, make new directories, and create text files.
date: 2021-12-17
tags:
  - posts
layout: layouts/post.njk
---

## Introduction
One of the most intimidating parts of learning Linux is working with the Linux shell. The shell is a command line interpreter and gives a user the ability to execute programs which are also called commands. 

In part 1 of this guide, you will learn and use some of the basic Linux commands to see your working directory, list directories and files, make new directories, and create text files.

## Prerequisites
You will need a Linux shell to work with to try these commands in this tutorial. If you do not have a [Linux distro](https://en.wikipedia.org/wiki/Linux_distribution) set up, you can use an online command shell to practice these commands. For this tutorial I used [JSLinux](https://bellard.org/jslinux/).

## Checking Current Directory
In Linux, a directory is a location on your computer that stores files. They are set up in a hierarchical system on your computer. 

To see what directory you are currently in you can use the `pwd` command.

```bash
pwd
```
While using JSLinux you will be in the `root` directory. 

If you are using the Linux shell on your own computer you will likely be in the `home` directory. 

![pwd command to show current working directory](https://cdn.glitch.global/3f55f8f2-9d21-4ff4-aad8-49272d37c68b/pwd.png?v=1642098577846)

## Creating Directories
Now that you know what directory you are in, you can start creating new directories and set up your own hierarchical structure. 

In the image below. you will see several directories and files that are set up in a hierachy. These directories are named after the author Jane Austen, some of her books, and a few of the characters in those books. 

In this section of the tutorial you will learn the commands to create each directory, change directories and list the directories that have been created.

![Directory hierarchy](https://cdn.glitch.global/3f55f8f2-9d21-4ff4-aad8-49272d37c68b/directory.png?v=1642098754325)

The first directory you will create is `austen`. 
To create this directory you will use the `mkdir` command which stands for make directory. 
In the Linux shell type:
```bash
mkdir austen
``` 
> **Note:** If you type `Austen` it will be different from `austen`. The Linux shell sees these as two different directories. Be sure to pay attention to your capitalization and any spelling errors while creating directories or files. 

To see if the directory was created you can use the `ls` command. 
This command is short for **list** and will list out any directories or files that are in the current working directory.  
In the image below you can see the `austen` directory is listed along with a few default directories that come with JSLinux. 

![austen directory listed with ls command](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/lvqp0drzpwq8o4i5t16i.png)

### Creating Directories Under `austen`
Now you can create the next directories in the hierarchy. You will create the `Emma`, `Persuasion`, and `Pride_prejudice` directories. 
You can create each directory one at a time with the `mkdir` command like you did when creating the `austen` directory.

![created the Emma directory](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/elsetoxvkiexlkcci9tc.png)

or you can create several directories at a time like the image below.

Use the `mkdir` command and separate each directory you would like to create. Here we create the `Persuasion` and `Pride_prejudice` directories all at once. 

Once you are done creating the directories you can use the `cd` command, which stands for change directory, to move from the `root` or `home` directory to the `austen` directory. 
From there you can use the `ls` command to list all of your new directories and confirm they were successfully created.

![Creating multiple directories with mkdir](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/bwoh0c4rijwi38jo711o.png)

To create the next directories in the hierarchy you will use the same `mkdir` command. In the image below you will see an example of changing directories to the austen directory and creating the character name directories. 

You must add them to the correct file path. For example, Knightly will go under the Emma directory so you will create it by including Emma in the file path like: 
`mkdir Emma/Knightly`

Repeat the same pattern with the other directories that need to be added. 

> **Note:** In the Linux shell you can press the tab key on your keyboard after you start a file path to auto-complete it. For example, if you type `Pr` then hit the `tab` key it will auto complete to `Pride_prejudice` for you. This will save time as you create more directories.

![Creating more directories](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/m9gm1duga1tjtk4kp44b.png)

### Creating a Text File
In the directory hierarchy image you can see that there are two `partner.txt` files. 
`.txt` stands for a text file. To create text files you use the `touch` command. 

Navigate to the Churchill directory with the `cd` command. 
Then type: 
```bash
touch partner.txt
```
Use the `ls` command to see if you were successful in creating a text file.

![Creating a text file](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/crh1huydxpdsqq7bcq2i.png)

Follow the same steps to create a `partner.txt` file under the `Persuasion/Wentworth` directory.

Once you have created both text files you should now have all of the directories and files from the first image. 

## Conclusion
In part 1 of this hands-on guide you learned the following basic commands:
- `pwd` to see your current working directory
- `ls` to list directories and files
- `mkdir` to create a new directory
- `cd` to change directories
- `touch` to create a text file

In part 2 of this hands-on guide you will learn the commands to move a directory, copy a file, delete a file, and edit a file. 

Take the time to go back through the commands you just learned before moving on to part 2. 
