# Git and Github

The most important part of this project will be to get you started with a version control software/system (VCS)--in this case Git--and a centralized version control system (CVCS) on a server--in this case Github. I have decided to tackle this monster first because not only will it be a great complimentary tool for this and many other projects but essential to your journey as a software developer. Unfortunately, because this will be a "learn as you go" type-of lesson and we want to cover as much ground as possible, you will need to study Git on your own for a more in-depth understanding of the system. If you don't already know Git we will do a brief and basic overview below. If you do, feel free to go [here](../InstallingWindows&Mac). 

#### Git
What is a version control system and why does it exist? 

>Version control is a system that records changes to a file or set of files over time so that you can recall specific versions later...It allows you to revert files back to a previous state, revert the entire project back to a previous state, compare changes over time, see who last modified something that might be causing a problem, who introduced an issue and when, and more. Using a VCS also generally means that if you screw things up or lose files, you can easily recover. In addition, you get all this for very little overhead. 
[--Official Git Documentation](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)

A VCS allows you to:
 - Save different versions of a file.
 - Compare those past versions to the current version.
 - Revert back to old versions or creat multiple versions based on the old ones.

This is the basic structure on your computer.
![alt text][gitImg1]

Git on its own is a very powerful tool and may seem confusing at first but trust me it will click. While Git allows you to make, track, and compare changes to your project(s)/repo(s) (files, folders, etc...) it does not --by itself-- provide an simple way for you to collaborate with co-workers, friends or the world at large. And that it where Github comes in--it serves as a hub to hold the master copy of your project. Git deals primarily with the local repo (the project on your local computer) and github deals with "housing"/"serving" a master repo where anyone can collaborate. *Don't get it? Don't worry. You can either keep going and pick it up as we go or do some side reasearch on the topic.*

#### Github
What is a centralized version control system and why does it exist?

It is basically the server/software that holds the "main" copy of a project and can communicate with the VCS on any computer and:

 - It allows your repo to live in a server space where other collaborators may have access to it.
 - If your repo is on the server others will (with your permission) make changes to it.
 - If it is someone elses repo you will be able to submit and make changes with their permission.

This is the basic structure on the server--in our case the Github server.  
![alt text][gitImg2] 

How it works: 
When you or some other user comes accross a project to collaborate on you simply:
   1. **_Clone_**(download) the repo from the server to their local machine.
   2. **_Add & commit_**(save) those changes to their local machine.
   3. **_Push_**(upload) the recently saved files to the repo on the server.
Lastly, if you come back again to make further changes:
	 4. **_Pull_**(update) the repo again into your computer so that you can edit the most recent version.
   
Enough reading. Let's get started.

[Installing: Windows/Mac](./InstallingWindows&Mac.md)

[gitImg1]: https://git-scm.com/book/en/v2/images/local.png
[gitImg2]: https://git-scm.com/book/en/v2/images/centralized.png

   
