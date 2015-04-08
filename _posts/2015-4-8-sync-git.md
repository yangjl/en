---
layout: post
title: "Git version control between laptop and local linux server with Github"
description: "Git version control"
category: notes
tags: [tutorial, github]
---
{% include JB/setup %}

I have a Mac laptop with multiple git-repositories. But my computational works are mostly carried out on a linux server. From/To there I push and pull changes via SSH. I would like to sync codes and data analysis results between the two systems. Here is what I learned from others experience via a post from [stackoverflow](http://stackoverflow.com/questions/4948190/git-repository-sync-between-computers-when-moving-around).

Below, I modified a little bit from above post. Lets say my netbook is called "Macbook". I create a repository there

```
$ cd ~/git
$ mkdir newThing
$ cd newThing
$ git init --bare
```

On the Linux server I will then create a clone of it. Maybe I will add some files also

```
$ git clone username@0.0.0.1:/home/username/git/newThing
$ git add .
$ git commit -m "Initial"
$ git push origin master
```

On my Mac, I will also add the Linux address.

```
$ git remote add externalName username@address:/home/username/git/newThing
$ git pull externalName master
```

Something to read: [http://progit.org/](http://progit.org/).
