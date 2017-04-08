# Simple Repo

*For the sake of clarity, whenever I say repo(short for repository) or directory it just means a folder. Also, I am assuming you already have a github account and if not go create one for free!*

In this section we are going to:
1. Make a directory on your desktop (named `firstRepo`) and create an .html (`firstGit.html`) file with the following code.
    ```
    <!DOCTYPE html>
    <html lang="en">
    <head>
    	<meta charset="UTF-8">
    	<title>My First Git File</title>
    </head>
    <body>
    	This just happend.
    </body>
    </html>
    ```
    *If it's not already inside, place `firstGit.html` inside the `firstRepo` directory.*
2. Open your CLI (Command Promp[Windows]/Terminal[Mac]) and make sure the path points to the firstRepo directory.
    **Windows** 
    Location: C:\Users\yourUserNameHere\Desktop\firstRepo
    Example: 
    ```
    C:\Users\Bryant Ruelas\Desktop\firstRepo>
    ```
    **Macintosh** 
    Location: /Users/yourUserNameHere/Desktop/firstRepo
    Example:
    ```
    firstRepo 🚀  bruest >
    ```
    2.5. I just realized we should probably download a nicer text editor than Notpad or textEdit. Go ahead and install **Sublime Text 3** via Chocolatey! `choco install sublimetext3 -y`. Aren't you glad we can install software way faster! and if you enter `choco list` you will be able to track all the software you've installed. *\*There isn't a simple way to effectively uninstall software natively with choco but if the package allows sometimes you can uninstall via `choco uninstall nameOfSoftware` but I recomend you read up on it beforehand.*
    
3. Supposing that the CLI is now pointing to `firstRepo` and we have Sublime Text 3 installed, we should be ready to go.

I suggest that you mirror your setup like the one below because I want you to see real-time changes:
**Windows:**
![alt text](https://cldup.com/66yVgRD1hm.PNG)
**Mac:**
![alt text](https://cldup.com/4CiuNkH2Wx.png)

Ok let's make some magic!

1. Input into the CLI `git init` and you will notice a new `.git` directory appear in your `firstRepo` folder. 
    - Notice the result you get when entering in `git status` and `git log`. 
        - git status should return: 
            ```
            Untracked Files:
                firstGit.html
            nothing added to commit but untracked files present
            ```
        - git log should return:
            ```
            your current branch 'master' does not have any commits yet
            ```
    - In the CLI enter `git add .` and check `git status` and `git log` again.
        - git status should return: <--- **\*changes occured.**
            ```
            Changes to be committed:
                new file: firstGit.html
            nothing added to commit but untracked files present
            ```
        - git log should return: <--- **\*no changes occured.**
            ```
            your current branch 'master' does not have any commits yet
            ```
    - Enter in `git commit -m "initial commit"` -- you may be prompted to edit your `git config --global` info.
     After making the commit you should see: 
         ```
         [master (root-commit) someRandomNumber123] initial commit
        1 file changed, 1 insertion(+)
        create mode 100644 firstGit.html
         ```
        - git status should return: 
            ```
            On branch master 
            nothing to commit, working tree clean
            ```
        - git log should return:
            ```
           initial commit
            ```
2. In Sublime Text 3 change firstGit.html (to example below) and save:
    ```
    <!DOCTYPE html>
    <html lang="en">
    <head>
    	<meta charset="UTF-8">
    	<title>My First Git File</title>
    </head>
    <body>
    	And this just happened!!!
    </body>
    </html>

    ```
    - Notice `git status` & `git log` again.
    - Now enter `git commit -am "body edit"` which is short for `git add .` + `git commig -m 'someMessage'`. The short command only works if you have previously commited the current file before.
    - And again, look at `git status` and  `git log`.
         - git status should return: 
            ```
            On branch master 
            nothing to commit, working tree clean
            ```
        - git log should return:
            ```
            commit [some weird string called a shaw]
            Author: [info]
            Date: [info]
            
            body edit
            
            commit [some weird string called a shaw]
            Author: [info]
            Date: [info]
            
            initial commit
            ```   
            
3. We will now put our project on the server at Github. Go over to github.com and create a new repository.
    Fill out the form like the one below and click Create repository.
    ![alt text](https://cldup.com/bnEx0fmKhe.png)
    
    Now copy the script that looks similar to this one and put it in your CLI.
    ```
    git remote add origin https://github.com/yourUserName/firstProject.git
    git push -u origin master
    ```
    
4. Go back to your Github repository page and your project should now be on Github the cetralized version control system (CVCS).

5. Remember, whenever changes are made to the CVCS those changes will not magically apear on your system (unless you made them yourself and then `git push` them locally)therefore, whenever you are going to make local changes remember to do a `git pull` so that you edit the most up-to-date version of the CVCS repo.
    - Suppose someone in Japan made changes to your CVCS repo. Your CVCS repo is now updated. And lets say you made changes without first downloading them via `git pull`, then you `git push` those changes then you will essentially override the changes the person in Japan made and your version will live in the CVCS and their changes will basically be non-existent. 

We are good to go!. You now have the power to collaborate with anyone from anywhere and make something revolutionary :) It is a very common practice to make an .md file that will hold valuable information for the team and world-at-large. 

Next, go build something!
---
[NEXT: Your First Website](../WD101.3-YourFirstWebsite)