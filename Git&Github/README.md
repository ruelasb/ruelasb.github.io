# Git and Github
---
The most important part of this project will be to get you started with a version control software/system (VCS)--in this case Git--and a centralized version control system (CVCS) on a server--in this case Github. I have decided to tackle this monster first because not only will it be a great complimentary tool for this and many other projects but essential to your journey as a software developer. Unfortunately, because this will be a "learn as you go" type of lesson and since we want to cover as much ground as possible, you will need to study git on your own for a more in-depth understanding.

#### Git
What is a version control system and why does it exist?
 - It allows you to save different versions of a file.
 - It allows you to compare those past versions to the current version.
 - It allows you to revert back to old versions or creat multiple versions based on the old ones.
>Version control is a system that records changes to a file or set of files over time so that you can recall specific versions later...It allows you to revert files back to a previous state, revert the entire project back to a previous state, compare changes over time, see who last modified something that might be causing a problem, who introduced an issue and when, and more. Using a VCS also generally means that if you screw things up or lose files, you can easily recover. In addition, you get all this for very little overhead. 
[-Official Git Documentation](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)

This is the basic structure on your computer.
![alt text][gitImg1]

Git on its own is a very powerful tool and may seem confusing at first but trust me it will click. While Git allows you to make changes to your project/repo (files, folders, etc...) it does not provide an easy way for you to collaborate with co-workers, friends or the world at large. And that it where Github comes in.

#### Github
What is a centralized version control system and why does it exist?
 - It allows your repo to live in a server space where other collaborators may have access to it.
 - If your repo is on the server others will (with your permission) make changes to it.
 - If it is someone elses repo you will be able to submit and make changes with their permission.

This is the basic structure on the server--in our case the Github server.  
![alt text][gitImg2] 

How it works: 
   1. They *clone*(download) your server repo to their local machine.
   2. Then they *add & commit*(save) changes and save those changes to their local version.
   3. Then they *push*(upload) those files to your server repo but not without your permission.
   
Enough reading. Let's get started.

[Installing: Windows/Mac](../InstallingWindows&Mac)

[gitImg1]: https://git-scm.com/book/en/v2/images/local.png
[gitImg2]: https://git-scm.com/book/en/v2/images/centralized.png

   