---
layout: post
bigtitle:  '[Internship] QA Data Analyst Internship Project: Using Text Mining to Find Similar Bugs in the Past'
subtitle:   
categories:
    - project
    - internship
tags:
    - internship
related_posts:
    - _posts/project/2015_Intern_PJT.md
    - _posts/project/2016_Intern_PJT.md
published: true
---


# [Internship] QA Data Analyst Internship Project: Using Text Mining to Find Similar Bugs in the Past

---
## Introduction

I had an opportunity to work as a data analyst intern for a game-making company this summer. I worked in the Quality Assurance team, which was relatively larger than QA teams in other industries because of the nature of the game-making company.

In this post, I would like to share how I came up with the idea for the project and how text mining could help solve the existing inefficiencies in the bug process.

---

## Background
![1](/assets/img/project/2021_Intern_PJT/1.png)

Currently, a bug goes through a series of processes from the occurrence of a bug and its closing.
1.	**QA Tester**: Enters bug information
2.	**QD**: Enters/Examines bug information
3.	**SE Lead**: Assigns an SE to the bug
4.  **SE**: Fixes the bug
5.	**QA Tester**: Final review of the bug and Closes the ticket

---

## Issues with the Current Process

In the bug process above, QA Tester and SE Lead do pre-investigations


<div class="me">
    <div><img src= "/assets/img/project/2021_Intern_PJT/2.png"></div>
    <div><img src= "/assets/img/project/2021_Intern_PJT/3.png"></div>
</div>

  <script>
    $(document).ready(function(){
      $('.me').slick();
    });
  </script>


<!-- ![2](/assets/img/project/2021_Intern_PJT/2.png)
![3](/assets/img/project/2021_Intern_PJT/3.png) -->
-	**QA Tester**: try different filters and type in different keywords to find if there have been any similar bugs in the past which is time consuming.
-	**SE Lead**: checks capacity and competency of SE and assigns the bug to the SE who is available and seems most suitable.

---

## Project Goal
<!-- ![6](/assets/img/project/2021_Intern_PJT/6.png)


![7](/assets/img/project/2021_Intern_PJT/7.png) -->

<div class="me">
    <div><img src= "/assets/img/project/2021_Intern_PJT/6.png"></div>
    <div><img src= "/assets/img/project/2021_Intern_PJT/7.png"></div>
</div>

  <script>
    $(document).ready(function(){
      $('.me').slick();
    });
  </script>


Our goal was to build a web application that finds similarities between a new and bugs in the past which will bring about the following benefits:

1.	**QA Testers** can determine whether or not to create a ticket for a new bug based on its similarities to bugs in history
    - Find bugs in order of its similarities to the new bug
    - Reduces bug comparison time
    -	Avoids duplicate bug tickets.


2.	**SE Lead** can assign the bug to an SE who has solved similar bugs in the past which
    - Saves SE Lead’s time thinking about which SE to assign
    - Increase Bug Fix Rate by assigning to an SE who has solved similar bugs in the past
    - Reduce bug fixing time by assigning to an SE who has solved similar bugs in the past

---

## Web Application

Technologies used:
- R shiny
- Text mining (KoNLP, dplyr, tidytext, stringr)
- JavaScript

#### Full screen shot

![4](/assets/img/project/2021_Intern_PJT/4.png)

---

#### Key functions:
>**Auto-compmlete search: This is where a user enters a bug keyword or BugID**
![8](/assets/img/project/2021_Intern_PJT/8.png)


****

>**Color Scheme: Coloring bugs with the same characteristics (Feature, TypeofBug,) make it easy to find similar bugs**
![10](/assets/img/project/2021_Intern_PJT/10.png)

>**Second Search Box: A search box for the dataframe allows users to narrow down to find a specific bug with certain key words. Note that it can search through the comments**
![5](/assets/img/project/2021_Intern_PJT/5.png)



---

## Improvements

-	The app does not handle typos well currently. For example, Google can handle typos like“unifomr” and automatically generate results for “uniform”. Since the bug descriptions are written in Korean, I was not able to find libraries that would enable such settings. If we can accumulate enough data about which words users are likely to make typos, we would expect to solve this issue to some extent.

---

## In Retrospect

-	Through the experience of leading a project from scratch to the end, I realized the high standards a product must meet to be published in a industry setting and the importance of earning buy-ins from stakeholders.
- It was fun having informational interviews with potential users from diverse backgrounds to get feedbacks and incorporating those feedback into the application.
-	I enjoyed learning about the process of how bugs are generated, reported to our system, fixed and finally closed by collaborative efforts of professionals across the teams.
- I really appreciate my manager, colleagues, and intern friends who helped me throughout the journey. My mentor was always there for me to ask questions like where to locate resources or who to ask for questions I had. I would like to thank my manager as well for granting me permission to explore a variety of data, attend virtual meetings at other studios, and lead projects that I proposed. Everyone was very willing to take time to answer my questions and put up with my curiosity. I not only learned and practiced the technical skills to become a good data analyst, but I also learn how important it is to build a good relationship with my colleagues with whom I spend 1/3 of my day! Not that I had a bad relationship with anyone, it's just really fun working with people with whom you can trust.
