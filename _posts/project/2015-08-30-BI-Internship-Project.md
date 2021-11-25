---
layout: post
bigtitle:  '[Internship] BI Engineer Internship Project: ELK Stack for Self-Reporting Service and Search Engine'
subtitle:   
categories:
    - project
    - internship
tags:
    - internship
related_posts:
    - _posts/project/2015_Intern_PJT.md
published: true
---

# [Internship] BI Engineer Internship Project: ELK Stack for Self-Reporting Service and Search Engine

---

I had an opportunity to do a summer internship at a 3PL (3rd Party Logistics) company before my junior year. Another summer intern and I joined the Business Intelligence (BI) team, and we were assigned an 11-week project to build a web application providing the following functions:

1. Fast and accurate search engine for SSRS reports and Tableau dashboards on the same UI

Unless the clients knew the exact directory of the report and dashboard, it was time consuming to find SSRS reports and Tableau dashboards living two separate web pages. A fast search and display of two reports on the same UI would facilitate easier tracking of reports and therefore reduce redundant emails and phone calls from clients asking BI analysts for the directory of reports.

2. Self-reporting tool for non-technical users

Clients had to specify detailed requirements and write a ticket to the BI team in order to request a new Tableau dashboard. Enabling the clients to build their own reports (that are not too complex for BI analysts to be involved) would reduce the number of tickets to the BI team and avoid the hassle for the clients to write a ticket and wait in line.

---

Since another intern and I were in charge of the whole project, we agreed to divide the work. He was in charge of building a framework for Web Application using MVC ASP .NET, and I delved into providing the two key functions mentioned above by using ELK stack (Elasticsearch, Logstash, Kibana).


Below is the architecture of the project:

![1](/assets/img/project/2015_Intern_PJT/1.jpg)
