# Simple Repo

*For the sake of clarity, whenever I say repo (short for repository) or directory it just means a folder. Also, I am assuming you already have a github account and if not go create one for free!*

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

2.5. I just realized we should probably download a nicer text editor than Notpad or textEdit. Go ahead and install **Sublime Text 3** via Chocolatey! `choco install sublimetext3 -y`. Aren't you glad we can install software way faster!? and if you enter `choco list` you will be able to track all the software you've installed. *\*There isn't a simple way to effectively uninstall software natively with choco but if the package allows, sometimes you can uninstall via `choco uninstall nameOfSoftware` but I highly recommend you read up on it beforehand.*

    
3. Supposing that the CLI is now pointing to `firstRepo` and we have Sublime Text 3 installed, we should be ready to go.

I suggest that you mirror your setup like the one below because I want you to see real-time changes:
**Windows:**
![alt text](https://cldup.com/66yVgRD1hm.PNG)
**Mac:**
![alt text](https://cldup.com/4CiuNkH2Wx.png)

Ok let's make some magic!

1. Input into the CLI `git init` and you will notice a new `.git` directory appear in your `firstRepo` folder--do not mess with it because this folder will hold all the fancy Git stuff. 
    - Notice the results you get when entering in `git status` and `git log`.
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
    Two things. First, the `git status` is notifying you that Git has noticed some file(s) changes but has not been told to `add` that file version(s) to the "tracking" system. Once you `add` file changes to the "tracking" system you must then save them into the git repo with `git commit`... and add a message to remember what you've saved, with `-m` (for message), and quotes for the message. It should look like this: `git commit -m "short message here"`.
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
    We just added the untracked file `firstGit.html` to the "tracking" system but still haven't added it to the Git repo nor added a tiny informative message. ([Here](https://chris.beams.io/posts/git-commit/) you will find an article on git messages)
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
    Your files have been added to the Git repo and now live as your first saved version with the message "initial commit". To see your saved version(s) we enter `git log`.
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
`git push` uploads the copy on your machine to the server.
    
4. Go back to your Github repository page at https://github.com/yourUserName/firstProject. Your project should now be on Github the cetralized version control system (CVCS).

5. Remember, whenever changes are made to the CVCS those changes will not magically apear on your system (unless you made them yourself and then `git push` them locally). Before you make any local changes remember to do a `git pull`(pulls from the server) so that you edit the most up-to-date version of the CVCS repo.
    - Suppose someone in Japan made changes to your CVCS repo. Your CVCS repo is now updated. And lets say you made changes without first downloading them via `git pull`, but instead you `git push` those changes. Your upload/push will essentially override the changes the person in Japan made and your version will live in the CVCS and their changes will basically be non-existent since you never pulled them unto your computer in the fist place. NOT WHAT YOU WANT TO BE DOING--ALWAYS PULL.

We are good to go!. You now have the power to collaborate with anyone from anywhere and make something revolutionary :) It is a very common practice to make an .md file that will hold valuable information for the team and world-at-large. *This will be the extent of our intro with Git and Github. If you need extra knowledge, please go watch a video. If you're doing ok but have lots of questions you can always keep learning as you go.*

**Next, go build something!**

---
[NEXT: Your First Website](../WD101.3-YourFirstWebsite)
