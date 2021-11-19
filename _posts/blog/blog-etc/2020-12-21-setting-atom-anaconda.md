---
layout: post
bigtitle: Syncing Atom on Anaconda
subtitle: 'Settung up Atom on Anaconda (base)'
categories:
    - blog
    - blog-etc
tags:
    - atom
comments: true
date: '2020-12-21 14:45:51 +0900'
related_posts:
  - category/_posts/etc/2020-12-21-markdown-tutorial.md
  - category/_posts/etc/2020-12-21-markdown-tutorial2.md
published: true
---

# Syncing Atom on Anaconda

## Intro

1. Set up a terminal on Atom
2. ync it to Anaconda, so that we see (base) on the terminal

## Atom platformio-ide-terminal package installation
---

[File] - [Settings] (Ctrl + ,) - [Install]

Search "platformio-ide-terminal" and install.



## Syncing Anaconda to Atom platformio-ide-terminal
---
Let's try syncing Anaconda to Atom platformio-ide-terminal

![그림1](/assets/img/Blog/Etc/setting/atom-conda1.png)

If you install "platformio-ide-terminal" and press <code>Ctrl+\`</code>, you will see a screen like the one above.

Of course, if you type in <code>conda</code> in the command, you will get an error.

Go to Setting by typing <code>Ctrl+,</code>

Find the platformio-ide-terminal package at [Settings] - [Packages], then click "Settings"

In **Core** section, insert your directory of Anaconda activate under **Auto run Command**

>>C:/Anaconda3/Scripts/activate

![그림2](/assets/img/Blog/Etc/setting/atom-conda2.png)

\+ I also changed the Shell Override

C:\WINDOWS\System32\cmd.exe

![그림3](/assets/img/Blog/Etc/setting/atom-conda3.png)

**Hooray~**

### Reference
-  [https://stackoverflow.com/questions/43207427/using-anaconda-environment-in-atom](https://stackoverflow.com/questions/43207427/using-anaconda-environment-in-atom)
