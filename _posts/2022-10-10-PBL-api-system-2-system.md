---
toc: true
title: System to System APIs
layout: post
description: 
categories: []
tags: [api, javascript, python]
type: pbl
week: 8
---

## API Frontend to Backend Overview
> This blog expects an understanding of RapdiAPI and using Python for request and response to obtain data.  Additionally, it is shows that access to data can occur across Web Applications. Here are highlights of this article.
1. JavaScript to Flask/Python to RapidAPI interface.
2. Flask/Python to provide API to simplify access for JavaScript Frontend developer.  
    - API credentials are hidden
    - Cache and calling RapidAPI or other APIs less
    - Access Control, firewall issues in Backend
3. FastPages/JavaScript handles formatting of data.

[Review API Terms](https://www.techfunnel.com/information-technology/application-programming-interface/)

![]({{site.baseurl}}/images/api.webp)

### [Flask/Python Code](https://github.com/nighthawkcoders/flask_portfolio/blob/main/api/covid.py)
> The Flask/Python Code has been heavily commented.  Additionally, the file can be run, tested, and debugged.  The lecture that goes with this will required students to step through debugging session as they review the code.
- VSCode Project: flask_portfolio
- Python File: api/covid.py

> The biggest learnings in Backend, in this code, versus Jupyter Notebook...
- Blueprint for covid.py, the interaction and registration with main.py
- The use of updateTime(), to only call API every 24 hours
- A main tester method that help with development and debugging
![]({{site.baseurl}}/images/debug_tester.png)
- Understanding the API resources and how they are run as a service through the Web Application
    - Run server, select to right of play button an pick Debug
    ![]({{site.baseurl}}/images/debug_server.png)
    - Debug Python Covid API, set a breakpoint in covid.py file and run server through browser
    ![]({{site.baseurl}}/images/debug_python_api.png)



### [Fastpages/JavaScript Code](https://raw.githubusercontent.com/nighthawkcoders/APCSP/master/_posts/2022-07-10-PBL-rapidapi.md)
> The JavaScript Code has been documented and featured in the Fastpages site.  The lecture that goes with this document will share how to debug the JavaScript using the Chrome Browser.
- VSCode Project: APCSP
- JavaScript/Markdown File: 2022-07-10-PBL-rapidapi.md

> The biggest learning in Frontend, in this code, will be the interaction between HTML and the JavaScript.  This is called the <mark>Document Object Model (DOM)</mark>. 
- In this example. an HTML table is setup and JavaScript is used to Create and Update Element IDs in the Table.  This is similar to the JavaScript table made in the Python Jupyter notebook, the big difference is the DOM syntax.
- The concept of for loop is the same, though the syntax ```for (const row of data.countries_stat)``` and keywords are different.   
- Visual showing Inspect on a Chrome Browser

![]({{site.baseurl}}/images/inspect.png)


## Hacks
> The big focus on of this hack is for students to adapt the project(s) to something that is helpful to the Scrum Teams final project.  
- Requirements System to System.  Your team project needs to have a Frontend and Backend that are distinct projects.
- Distribution of Development between Frontend and Backend developers.  As you divide work and systems, I would suggest Scrum Master and Devops Engineer join either Frontend or Backend.
- A Teacher suggestion is to start by using these files very closely!  Make very small changes while incorporating API specific to the team.