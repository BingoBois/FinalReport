<p style="color: red; font-weight: bold">>>>>>  gd2md-html alert:  ERRORs: 0; WARNINGs: 1; ALERTS: 30.</p>
<ul style="color: red; font-weight: bold"><li>See top comment block for details on ERRORs and WARNINGs. <li>In the converted Markdown or HTML, search for inline alerts that start with >>>>>  gd2md-html alert:  for specific instances that need correction.</ul>

<p style="color: red; font-weight: bold">Links to alert messages:</p><a href="#gdcalert1">alert1</a>
<a href="#gdcalert2">alert2</a>
<a href="#gdcalert3">alert3</a>
<a href="#gdcalert4">alert4</a>
<a href="#gdcalert5">alert5</a>
<a href="#gdcalert6">alert6</a>
<a href="#gdcalert7">alert7</a>
<a href="#gdcalert8">alert8</a>
<a href="#gdcalert9">alert9</a>
<a href="#gdcalert10">alert10</a>
<a href="#gdcalert11">alert11</a>
<a href="#gdcalert12">alert12</a>
<a href="#gdcalert13">alert13</a>
<a href="#gdcalert14">alert14</a>
<a href="#gdcalert15">alert15</a>
<a href="#gdcalert16">alert16</a>
<a href="#gdcalert17">alert17</a>
<a href="#gdcalert18">alert18</a>
<a href="#gdcalert19">alert19</a>
<a href="#gdcalert20">alert20</a>
<a href="#gdcalert21">alert21</a>
<a href="#gdcalert22">alert22</a>
<a href="#gdcalert23">alert23</a>
<a href="#gdcalert24">alert24</a>
<a href="#gdcalert25">alert25</a>
<a href="#gdcalert26">alert26</a>
<a href="#gdcalert27">alert27</a>
<a href="#gdcalert28">alert28</a>
<a href="#gdcalert29">alert29</a>
<a href="#gdcalert30">alert30</a>

<p style="color: red; font-weight: bold">>>>>> PLEASE check and correct alert issues and delete this message and the inline alerts.<hr></p>




<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report0.jpg). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report0.jpg "image_tooltip")



# Dolphin News


## A Hacker News Clone

Large System Development

By Christian, Christoffer, Viktor, William og Zaeem

Fall 2018

Copenhagen Business Academy




# Introduction

"_Dolphin News_" is based on the "_[Hacker News Clone](https://github.com/datsoftlyngby/soft2018fall-lsd-teaching-material/blob/master/assignments/01-HN%20Clone%20Task%20Description.ipynb)_"-project, which is a small light version of popular websites such as Reddit. The user is able to create post, which can be up- and down-voted, as well as commented by other users and the comments can be up- and down-voted as well. The point of the site, is that the popular post (and comments within the post) gets pushed to the top of the site through the use of the voting system, and thus subsequently pushing the least popular post and topics down.



<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report1.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report1.png "image_tooltip")


_Original Hackernews as seen [here](https://news.ycombinator.com/ )  \
_

For development of this project, the team used familiar technologies such as NodeJS, React, MobX, Continuous Integration and MySQL, but the team also challenged them self by use new and different options. The team chose to write the project in TypeScript, use Kubernetes very early in the project to support scaling, and Grafana, Prometheus and Kibana for error-logging and monitoring.

This report will give a bit of insight into the mentioned technology choices, as well as topics such as the development process the team agreed upon, how the team operated another teams project and many more.

The teams original documentation for the project can be found [here](https://docs.google.com/document/d/1js5Vx5Y_EBHAWZZGPYC5kW4LwCBrb_e1Qx2xlP_ZxnI/edit#heading=h.r5cdkdv2gccu)




# 1. Requirements, architecture, design and process


## Project Structure

The project has been divided up into three different repos, to provide a better project structure and easier overview: 



*   Frontend: [https://github.com/BingoBois/DolphinNewsFrontend](https://github.com/BingoBois/DolphinNewsFrontend) 
*   Backend: [https://github.com/BingoBois/DolphinNewsNode](https://github.com/BingoBois/DolphinNewsNode) 
*   DevOps: [https://github.com/BingoBois/DolphinNewsDevOps](https://github.com/BingoBois/DolphinNewsDevOps)  


## 1.1. System requirements

**This section should contain an elaborate description of the requirements for the project. This includes the scope of the Hackernews clone (what should it be able to do / what should it not be able to do).**



<p id="gdcalert3" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report2.gif). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert4">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report2.gif "image_tooltip")


Picture [source](https://blog.capterra.com/wp-content/uploads/2015/12/dt940517dhc0-720x218.gif ) \


The project was developed in stages over a period of 3 months. The first stage consisted of a 8 week period, in which the team had to create a backlog, project board, as well as develop and deliver a system that fulfilled a [set minimum requirements](https://github.com/datsoftlyngby/soft2018fall-lsd-teaching-material/blob/master/assignments/03-Minimum_Requirements_and_API_Description.md) and that subsequently would be handed-over to a operating team for monitoring. 

After 8 weeks, the system had to:



*   Display a set of stories on your system's front page.
*   Display a set of comments on stories.
*   Stories or comments are posted by users, which have to be registered to and logged into the system to be able to post.
*   Users login to the system via a separate page.
*   Users are identified by a user name and a password.
*   New users can register to the system, via a separate page.

    

*   The complete HTTP API, as defined below.
    *   Accept posted stories/comments/etc.
        *   Through a specific API-path: _http://<your_host>:<your_port>/post_
    *   Provide the id of the latest digested post.
        *   Through a specific API-path: _http://<your_host>:<your_port>/status_
    *   Provide status information.
        *   Through a specific API-path: _http://<your_host>:<your_port>/status  \
_

During the next stages of development, the team usually had 1-2 weeks to develop and deliver the next parts of the system, while also acting as operators on another teams system and provide them with feedback. 

For the next stages of development the team had to implement _Continuous Integration_, followed by sitting down with the team that was operating and monitoring our system and agree on a _Service-Level Agreement_ (SLA), which included:



*   An uptime metric (Agreed to 95%)
*   A metric on "lost" posts from the simulator (Agreed to 5%)
*   A metric on serving speed of the landing page (Agreed to a maximum of 3 seconds)
*   At least one other metric (preferably more) that is/are relevant for measuring the performance of your system. (Agreed to a maximum of 3 seconds of response time)

To monitor that the _SLA_ was being upheld, the team was tasked to implement Grafana and Prometheus into the project.



*   An URL to your Grafana dashboard
*   Your Grafana dashboard must contain:
    *   At least one widget per SLA metric (KPI)
    *   The SLA itself or a link to the SLA document

The next assignment tasked the team to implement _logging_ and _alarms_ in _grafana_, to warn the team and the operators when or if our system crashed, and to have access to a _log_ that could explain what had happened at the time of the system crash or failure.

Finally, the team was tasked to add _scalability_ to our system, by creating a _Docker Swarm_ (or similar alternative technology) _cluster_ for your Hacker News Clone in which all components run as services.


## 


## 1.2. Development process

**In this part you should show off by telling us all you know about software development processes and describe which concepts you used to structure your development.**

At the beginning of the project, the team spent some time on setting up features for each of the three repos, such as auto-deployment with Kubernetes, Continuous Integration, as well as rules and settings for pushing new code to the master branch of the repos. 



<p id="gdcalert4" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report3.jpg). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert5">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report3.jpg "image_tooltip")


_Picture [source](https://about.gitlab.com/images/blogimages/ci-deployment-and-environments/queue.jpg) _



*   When working on a new feature or fixing errors, members would create a new branch and work on it there.
*   Members were not allowed to work on the master branch directly
*   Settings were set in place, making it impossible to push directly to the master branch
*   When merging a branch into master, a new Pull Request had to be created.
*   The new Pull Request could not be approved by the creator
*   Because of _Continuous Integration_, any test in code has to pass in order to be approved
*   Another team member had to go through the submitted Pull Request (as thorough as possible), point out any errors or flaws and give their most honest opinion regarding the code
*   If the team member was satisfied with the submitted code and potential requested changes to the code have been fixed, the team member could approve the Pull Request to be merged with the master branch.
*   The master branch would always contain the latest and approved version

While team members often worked from home, pair-programming was also used a lot during development, especially with the help of screen sharing tools such as Zoom, and voice tools as TeamSpeak.

In terms of methodology, the team went with a _agile development_ approach, which resulted in a lot of features and functions often undergoing multiple iterations during development. \
However, the team did not stick to a traditional _SCRUM_ approach to development of the project.

Despite using this iterative approach to development and while the team initially had create a _SCRUM_-board/_backlog_ with user stories, the team failed to assign roles such as _Scrum Master_, _Product owner_ etc., which resulted in all team members more or less only being assigned "_Scrum developers_" roles. 

This also meant that the team would discuss what to work on next on the project, either by face-to-face discussions in class, teamspeak or messenger, resulting in members often having to ask "_What should I work on?_" a lot. Failing to use and maintain the _SCRUM-board/Backlog_ also meant, that usually only 1 or 2 members of the team had an idea or overview of the projects status and what needed to be done. 

The team also failed to perform consistent _sprints_ and instead developed and deployed a lot of features at the last moment, which can be seen in the graphs below.     \




<p id="gdcalert5" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report4.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert6">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report4.png "image_tooltip")


_Graph of the contributions to the Backend_



<p id="gdcalert6" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report5.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert7">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report5.png "image_tooltip")


_Graph of the contributions to the Frontend_



<p id="gdcalert7" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report6.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert8">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report6.png "image_tooltip")


_Graph of the contributions to the DevOps_

So while the team was successful with the setup, settings and actual development of the project, the team dropped the ball hard when it came to oversight, sprints and operation of the project. 


## 


## 1.3. Software architecture


### Bare Metal Kubernetes Setup



<p id="gdcalert8" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report7.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert9">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report7.png "image_tooltip")


The team ran a very simple _Kubernetes _setup. The main goal was to learn the inner workings of _Kubernetes_, and to have a "_continuous deployment_" setup from the beginning, where we could rollback.

Since we were cheap, and wanted to do it as cost-efficient as possible, our Master machine had many roles; building, load balancing, and managing the cluster.

The cluster consisted of 1 slave pc, which also took care of logging, and the database.

It is actually a really bad example of a Kubernetes setup, but for us it was sufficient (most of the time), and was a nice learning experience.


### Continuous Deployment Setup


### 

<p id="gdcalert9" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report8.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert10">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report8.png "image_tooltip")


Our original plan was to have continuous deployment to a staging area, and then with the push of a button being able to push to a production environment. We ended up just deploying everything to master because we thought it was a good idea (it wasn't).

We blocked the master branch so the only way of getting commits in, is through pull requests. Then we have a nodejs/bash application listening on the Kubernetes master machine, which then builds, pushes and updates the kubernetes deployments.

Turned out we had to rollback a bunch of times, and our homebrew software could have been less hacky, but it worked nonetheless and served us well during development.




### MySQL Database Design

The setup for the MySQL database can be seen here: \
[https://github.com/BingoBois/DolphinNewsNode/blob/master/vandfaldemodele.sql](https://github.com/BingoBois/DolphinNewsNode/blob/master/vandfaldemodele.sql)

The database consists of 5 tables



*   comment
*   post
*   user
*   vote_comment
*   vote_post

Before showing the schemas of the tables, please note that the team decided to rename the requirements original _hanesst_id_ to _helge_id_. While other variables might also have been slightly renamed, they still look very similar to the requirements original naming.

The schemas of each of the tables are as follows:


#### comment-schema



<p id="gdcalert10" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report9.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert11">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report9.png "image_tooltip")



#### post-schema



<p id="gdcalert11" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report10.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert12">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report10.png "image_tooltip")



#### user-schema



<p id="gdcalert12" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report11.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert13">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report11.png "image_tooltip")



#### vote_comment-schema



<p id="gdcalert13" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report12.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert14">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report12.png "image_tooltip")



#### vote_post-schema


## 

<p id="gdcalert14" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report13.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert15">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report13.png "image_tooltip")



## 


## 1.4. Software design

The requirements for this project weren't as many, although there were some implications that would have the design changed. We were told to have an HTTP API ready, as well as a website for normal users to interact with, that would copy the functionality of a known techforum called "Hacker-News". 

A few requirements were put as well, on the data that it would receive. The data would be sent in by a stream of bots, hosted by the teacher. 


```
{
  "username": "<string>", 
  "post_type": "<string>", 
  "pwd_hash": "<string>", 
  "post_title": "<string>",
  "post_url": "<string>", 
  "post_parent": <int>, 
  "hanesst_id": <int>, 
  "post_text": "<string>"
}
```


There were also design requirements for the frontend, that we would have to follow, as such: \


<p id="gdcalert15" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report14.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert16">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report14.png "image_tooltip")




Immediately, we thought we would utilize some form of 3 layer architecture. The layers being:



*   Website
*   Backend
*   Persistence (Database)

The website we chose to make in React, as we've had experience with it, and it's a famous framework to use for web development. It's simple, and would allow us to create prototypes rather fast, as well as inheriting the NPM ecosystem. The website would be used to only display thing sent from the backend, and to be used as a messenger in general for the client. 

The backend would be written in NodeJS, utilizing TypeScript and Express to gain most proficiency, as we were quite a few people to operate each of the platforms. Static checking would allow us to avoid runtime errors, and gain control like we would have with other statically typed language (C# and Java).

The major concern and requirement here, would be **uptime. **A strong sense of pressure was put on that topic, and that our uptime would have to be at a acceptable level. At first, we assumed that smaller scalable solutions like message queues, or even docker swarm would fit the project and would allow us to fulfill that criteria. After further inspection, we came to the conclusion that kubernetes was a more sturdy choice, as it's used more often in the industry. The fact that it was made by google made it more credible as well, and the fact that they rely on it themselves gives assurance. 

Although these scaling tools come with more known cloud providers, we chose to go the manual way of doing things, and decided to try and setup our own kubernetes clusters as a learning experience. 

One last technical concern we had, would be the fact that the database wasn't as scalable, and that we would have to optimize our queries to ensure that there wasn't as much latency when it comes to selecting and updating / inserting info into the database.


## 


## 1.5. Software implementation

**This section should describe your actual implementation. Mainly how well you followed the requirements, process and software design you began with. If your system changed during this phase you should summarise the unexpected events/problems and explain how you solved them.**

The transition to Typescript proved to be a hassle sometimes, as the team used Frameworks that have their own types and needs to be followed, as the team no longer used dynamic typing. The learning curve was trying to get used to the new workflow that came with Typescript and it's quirks. The team persisted and stuck with Typescript, as the team wanted to learn something new rather than creating yet another typical CRUD Application. 

During our early development stages, there was quite the confusion in regards to the correlation with the data being sent to the system, by the bots. The team started creating MySQL schemes, to fit the data being sent to us, and modelled all of the systems tables accordingly, so the team would adapt all around that. One of these issues came apparent very early into the start of the project. Getting the application hosted, as well as making the website was rather easy, although two issues came along during the test phase. 

The team had mistaken the data received from the bots, and which was supplied to us. The website that was given to the team shows the latest post id. This post id could either be coming from a comment or a post. The team mistaked the hannest_id to be the latest post, although supposedly it's the latest of either comments or posts. This meant that the team were showing lower stats than most groups. 

Another concern that appeared, was the fact that the teams VPS were running rather slow. One thing that became apparent, was the fact that the teams clusters were being split on already low resource VPS machines. Each machine had around 1 gb of ram, and had 1 core to work on. The team searched vividly after a new host, to see if there was a alternative to offer, rather than paying for more expensive machines. 

The team discovered a private cloud provider called Contabo. They were offering way more substantial servers, that really helped a bunch in terms of getting the project running smoother in terms of response times. The transition to Contabo proved it's worth and the teams latency issues were decreased. 


# 


# 2. Maintenance and SLA status

We were assigned to operate the project developed by group 6/F, which repo can be found here: 

[https://github.com/edipetres/HackerNews-GroupF](https://github.com/edipetres/HackerNews-GroupF)

From the beginning of our assignment we kept a "_Operators Log_", documenting our entire operating assignment. From our internal thoughts on the project, to manually testing the backend and frontend, finding bugs, going through the latest updates to the repo, writing feedback, raising issues, documenting through screenshots, everything is documented in this log. 

The entire log can be read here: \
[https://docs.google.com/document/d/1fXdrMdLmUNE5lHgF4kbxaj-muuOK5JDSLDGCxRFu3Kw/edit#heading=h.xlty5i677mx2](https://docs.google.com/document/d/1fXdrMdLmUNE5lHgF4kbxaj-muuOK5JDSLDGCxRFu3Kw/edit#heading=h.xlty5i677mx2)

 \
In this chapter, we will try to distill and present the most important findings from our operating assignment.

 


## 2.1. Hand-over

Documentation from the developers felt like the minimum required information, compared to what the operators [delivered to the operators of their project](https://docs.google.com/document/d/1js5Vx5Y_EBHAWZZGPYC5kW4LwCBrb_e1Qx2xlP_ZxnI/edit#). The documentation provided the operators with information on how to run the project locally, details regarding some of the technologies being used and database schema design. The operators really missed a overview of the projects API's, as well as access to some of the services that the developers used, like AWS and Mlab. 

Combined with the fact that the developers had opted to keep the entire project within one repo and not split it up into multiple ones, made it difficult and confusing in the beginning to get a grasp of the projects structure.

The operators ended up spending a lot of time in the first few days manually testing the backend and frontend, as well as going through all the code that had been committed to the repository. This was done to help the operators get an complete overview and deeper insight into the projects current state and what needed to be done. To the developers credit, they had written a couple of issues on the Github repo, which helped the operators getting an overview of the projects status and maintaining it. 


## 


## 2.2. Service-level agreement

For the Service-level agreement (SLA), the operators suggested the following:



*   95% Uptime
*   Max 5% data Loss
*   Max 3 seconds response time

The developers had no objection to the proposed SLA, an so an agreement was quickly agreed upon.


## 2.3. Maintenance and reliability

When the operators started operating on the project, the frontend only displayed the layout of the page, no data was being loaded in or shown and gave a an error, stating that the frontend had "failed to load articles". Also, all of the selections in the navbar did not work either. \




<p id="gdcalert16" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report15.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert17">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report15.png "image_tooltip")


_Picture of the Frontend at hand-over_



In addition, the backend also had a lot of problems in the beginning, including being able able to create a user, but not to verify the newly created user through Postman.



<p id="gdcalert17" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report16.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert18">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report16.png "image_tooltip")


_Picture of a successfully created user through postman_



<p id="gdcalert18" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report17.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert19">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report17.png "image_tooltip")



    _Picture of failing to login with the newly created user._



Despite a lot of technical errors, a mess of a Github Repo and a lot of github issues raised by the operators, the developers responded quickly, by updating the project and fixing the most critical errors and adding missing features.

To monitor the system, the operators (almost) daily checked the github, to see if issues that had been raised had been addressed and fixed. 

The operators manually tested the backend and frontend, once new features or fixes had been added, as well as also going through the various commits, to see what had been added, changed or fixed under the hood, and finally documented the days work in the log. The manually testing proved that the developers had kept their promise of max 3 seconds of response time, based on the fact that both the frontend and backend responded incredible fast everytime the operators tested.

<p id="gdcalert19" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report18.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert20">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report18.png "image_tooltip")



    _Picture: The operators used the above graph provided by Helge, to quickly see if anything critical had happened. The developers graph-line is the light-purple one, group f_

As can be seen on the graph above, the project by group_f (the developers) successfully consumed over 14 mio. comments or post to its database, and successfully reported the latest 'hanesst_ids' back, making only one of two projects to achieve this.     



<p id="gdcalert20" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report19.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert21">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report19.png "image_tooltip")


_Picture of Helge's graph, showing various errors reported by projects_

In terms of error-messages, the developers also achieved the seconds lowest errors, among all the projects.

The developers sadly relied to much on the AWS tools, meaning they never setup tools such as Grafana, Prometheus or Kibana, to help the operators monitor if the SLA agreement was being uphold.



<p id="gdcalert21" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report20.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert22">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report20.png "image_tooltip")


_Picture from the developers AWS Monitoring of the project _ \


Looking through the AWS tools, the operators could see that the average latency was kept to about 334.9 microseconds.

The developers also setup an alarm, for if the system was unresponsive for more than 15 minutes.



<p id="gdcalert22" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report21.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert23">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report21.png "image_tooltip")
_Picture of the projects alarm setup_

At the end of the project, the operators have generally been very pleased by the progress made by the developers. All though some features were missing or did not function as expected in the beginning, the developers addressed the issues raised, all while the system maintained incredible stability. 

The operators do have a few minor issues that needs to be improved:



*   Implement Grafana, Prometheus or Kibana for easier SLA monitoring
    *   Operators had no real way of checking if the SLA agreement was upheld
*   Slow response
    *   According to Helge, developers should respond to issues raised to the operators within 48 hours of posting and preferable with a fix to address the issue.
*   Did not finish or adress all Github issues (as of 18/12-2018)
    *   54 issues was raised during development
    *   36 was closed 
    *   Of the 54 issue, 29 of them (or 53.70%) was raised by the operators
*   Lack of feedback
    *   Communication and feedback between operators and developers was mostly done through Github issues, which worked great.
    *    A lot of the issues that we raised in the project repo was never commented. The operators would have liked to see the developers (at minimum) write a comment stating "Ok, we'll look into it", just to show that they've seen the issue and are aware of it. 
    *   The operators would also have liked to see the developers linking to commits fixing or addressing issues raised when closing or responding to an issue.

    

<p id="gdcalert23" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report22.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert24">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report22.png "image_tooltip")



    _Picture of a great example, of communication between the operators and the developers._


    

<p id="gdcalert24" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report23.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert25">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report23.png "image_tooltip")



    _Picture of an example of what the operators considered "bad feedback". Issue just got closed by a developer, but no feedback/comments or  link to commits that addressed and fixed the issue_



# 3. Discussion


## 3.1. Technical discussion



<p id="gdcalert25" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report24.jpg). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert26">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report24.jpg "image_tooltip")


_Picture [source](https://www.vectorstock.com/royalty-free-vector/positive-and-negative-thinking-vector-18958626) _

In general the project itself was really interesting and challenging, but the team have some mixed feelings about the final result.  \
 \
On the positive side



*   The team was happy with the successful implementation and learning experience of technologies such as Kubernetes
*   How the team successfully wrote the project using TypeScript. 
*   The setup of settings and rules regarding the development process of the project also proved to be a positive experience for the team, despite the extra steps. 
*   The team felt very good about the work done to operate team E's project, in which the team not only created over 53.70% of the issues raised and provided them with feedback, but also managed to heavily documented its findings and thoughts in a separate document.



On the negative side:



*   The team spent a lot of time and resources on trying to learn and apply new technologies. 
*   The team did not follow the _SCRUM _structure and practices
*   Failed to maintain and update the backlog, making it easy for the developers to lose track and overview of development. 
*   Development could have benefitted for some more models to help keep the team on the same page and the right course. 
*   The team failed to deliver on a few the required feature 
*   Still some bugs in the current system
*   As the system grew it got very slow and had a horrible response time. 
*   The system only managed to consume about ⅓ of the total data, compared to other teams. 
*   Not enough written test for the backend and frontend
*   Team failed to maintain data for grafana, prometheus and kibana, making it difficult for our operators to see if we managed to fulfill our SLA goals. 
*   The team should have pushed team E and demand that grafana and prometheus getting implemented into the system or at least prove to us, that the AWS tools could provide us with the data to make sure that the SLA was fulfilled. 
*   Because the team had structured the project into three different repos, the team should also have made it easier to share the various _types_ that was required for working with TypeScript. 
*   The team also feels that the group (group 4) that was supposed to operate our system and provide us feedback, failed to accomplish this task.


## 


## 3.2. Group work reflection & Lessons learned



<p id="gdcalert26" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report25.jpg). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert27">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report25.jpg "image_tooltip")


_Picture [source](https://pjp-eu.coe.int/documents/1017981/1667839/reflection-group.jpg/3df1d356-c8c0-4a16-9c22-e98edac0b0a8?t=1404492688000)_



<p id="gdcalert27" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report26.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert28">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report26.png "image_tooltip")


_Picture [source ](https://kubernetes.io/images/kubernetes-horizontal-color.png)_


### Kubernetes



*   The team opted to integrate Kubernetes from the beginning of the project, saving the team time when the project down the line required us to integrate some form of scalability to the system. 
*   Kubernetes helped the team develop a stabile and as crash-proof system (as possible).
*   While it saved the team time further down the development line, it took quite some time to get a grip of it and a lot of trial and error, but the time was well spent.
*   Because of the attempt to integrate Kubernetes so early in development, had the team not being able to accomplish it, the team would have had time to choose a different approach.


### 

<p id="gdcalert28" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report27.jpg). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert29">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report27.jpg "image_tooltip")


_Picture [source](https://cdn-images-1.medium.com/max/2000/1*D8Wwwce8wS3auLAiM3BQKA.jpeg ) _


### TypeScript



*   Exciting new language for most of the developers 
*   Gave the team access to _ES5_ and _ES6_ features, and support for future versions
*   Built in transpiler for older ES-versions, giving the project great compatibility with older browser.
*   Built on top of JavaScript, meaning 
*   Turned out to be a tough transition from JavaScript for some of the developers, due to features such as _Static Typing_, _Strict Null Checking_ and _interfaces_, which while being features being used in _Java_ and _C#_, was difficult to adjust to in a _JavaScript _environment.



<p id="gdcalert29" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report28.jpg). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert30">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report28.jpg "image_tooltip")


_Picture [source](http://vertassets.blob.core.windows.net/image/11a1feb2/11a1feb2-44e4-4c97-97e5-195e729fa67f/450x300people_holding_gears.jpg ) _


### Development Process



*   Required some additional settings and setup
*   More work to get code up on the master branch
*   Worked great for quality control of the developers work  
*   Minor fixes and adjustments required the same process, as major features and functions, which sometimes could be tedious

For even more reflections regarding the project, the team members wrote two different blogs (due to limited team sizes) for a different exam project in "_Udforskning & Formidling_" ( "_Discovery & Research_") regarding topics related to the project:



*   "_[How TypeScript and Static Typing can improve your JavaScript](https://github.com/radeonxray/UFO-Exam#intro-to-typescript)_", by Christian & Zaeem
*   "_[Does the choice of Kubernetes & Docker Swarm matter?](https://github.com/2joocy/UFOBlog)_", by Chris, Viktor and William


# 


# Conclusion



<p id="gdcalert30" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/Dolphin-Final-Report29.png). Store image on your image server and adjust path/filename if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert31">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/Dolphin-Final-Report29.png "image_tooltip")


Picture [Source](http://www.evidentlycochrane.net/wp-content/uploads/2014/07/Screen-Shot-2014-07-23-at-14.41.59.png )

The team could have spent more time (and pages) on going even deeper into our project and development, but only had a maximum of 10 pages. The team could also have spent some more time on sketches, drawings and perhaps even a UML diagram of the system, to better visualize the vision for the project, its design and architecture.

Overall though, while the team was not satisfied with all the parts the final system, some parts worked great, like the choice of TypeScript, Kubernetes and the way the development process was set up. The team was also very happy and satisfied with the work put into the operator assignment.
