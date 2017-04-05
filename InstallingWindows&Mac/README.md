# Installing Software: Windows/Mac
---
Web development is constantly growing and we will need to keep up with the latest software. Downloading software also means you will need to keep track of each one and make sure they are up to date with the newest releases--this can be a huge pain. Fortunately, there is software for that too! Software to install software and keep track of all software installations. 

To get started with Git we will need to download some software and we will do it with the command line interface(CLI). I highly encourage you to learn how to use the CLI as a tool to speed up productivity. 
 ###### `WARNING:`

`The CLI is a very powerful tool and you can literally ruin your computer. I advise you to take proper percaution and be sure you know what you are doing. I do not take any responsibility.`

So lets begin :)

### Windows
Open the default CLI as an administrator--Windows calls it Command Prompt. 
Make sure you right click and **run as administrator**.
\**Your current path does NOT have to look exactly like the image below C:WINDOWS\system32 it could be C:WHATEVER\YOU\WANT*
![alt text](https://cldup.com/mqr22_MuZm.PNG)
Quick commands that you may find helpful:
 - Clear the screen
    ```
    C:\WINDOWS\system32> cls
    ```
- Move to a different folder (directory). \*Sample takes you to desktop
    ```
    C:\WINDOWS\system32> cd "C:\Users\Bryant Ruelas"
    ```
- List all files and directories inside current path.
    ```
    C:\Users\Bryant Ruelas> dir
    ```
- Move back. I am currently at `C:\Users\Bryant Ruelas` but if I enter `cd ..` or `cd ..\` or `cd ../`...
    ```
    C:\Users\Bryant Ruelas> cd ..\
    **I will get moved out to**
    C:\Users\>
    ```
 - To move into any specific file quickly, you can always enter `cd ` (with a white space after it) and then drag and drop whatever file you want into the CLI. This will be handy when you have to deal with a long path or file/folder name(s) that have a space like `C:\Users\Bryant Ruelas`.
 
A package manager (PM) is an awesome tool to download and manage software with ease. Chocolatey is the most popular PM for windows as of the creation of this lesson so we will download Chocolatey. 
1. Go to [Chocolatey.](https://chocolatey.org/) 
2. Install with cmd.exe.
The cmd.exe command you will paste will look similar to the one below. Please do not copy and paste the sample below. 
Visit the Chocolatey site to download the most recent version.
`@powershell -NoProfile -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"`
3. After past press enter and wait for the software to download. If you are having trouble please refer to the choco site. 

Now we can install Git! And all kinds of other software(aka packages) without having to go to different sites everytime you need to downlaod the latest version. It is all possible with a simple command like `choco install nameofsoftware` just look them up [here.](https://chocolatey.org/packages)

To install Git with the CLI enter `choco install git.install -y`. The -y is just a short command(the dash is also refered to as a flag) or flag to notify the software that yes you agree to terms, conditions, and all other requirements. You can choose to leave the -y flag out but you will still need to confirm requirements eventually to proceed with the download.

After you've downloaded software you must restart the Command Prompt. Close the CLI and re-open it as an **Administrator**.

To make sure it worked enter `git --version` and you should see the following(probably with a more recent version).
![alt text](https://cldup.com/qnaso7P-tZ.PNG)

### Mac
Open the default CLI called Terminal.
*Your Terminal will not look exactly like mine and the path may be different but don't worry. You're doing fine!
![alt text](https://cldup.com/kuQOnpphqe.png)
Quick commands that you may find helpful:
 - Clear the screen
    ```
    ~ 🚀  bruest > clear
    ```
- Move to a different folder (directory). \*Sample takes you to /Desktop/newFolder but you can enter any path.
    ```
    ~ 🚀  bruest > cd ~/Desktop/newFolder
    ```
- List all files and directories inside current path.
    ```
    newFolder 🚀  bruest > ls 
    ```
- Move back. I am currently at `/Users/Bruest/Desktop/newFolder` but if I enter `cd ..` or  `cd ../`...
    ```
    newFolder 🚀  bruest > cd ..\
    **I will get moved back, out of newFolder**
    Desktop 🚀  bruest >
    ```
 - To move into any specific file quickly, you can always enter `cd ` (with a white space after it) and then drag and drop whatever file you want into the CLI. This will be handy when you have to deal with a long path or file/folder name(s) that have a space like `C:\Users\Bryant Ruelas`.

A package manager (PM) is an awesome tool to download and manage software with ease. Homebrew is the most popular PM for Mac as of the creation of this lesson so we will download Homebrew. 

1. Go to [Homebrew.](https://brew.sh/) 
2. Install with Terminal.
The Terminal script command you will paste will look similar to the one below. Please do not copy and paste the sample below. 
Visit the Homebrew site to download the most recent version.
`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
3. After past press enter and wait for the software to download. If you are having trouble please refer to the Homebrew site. 

Now we can install Git! And all kinds of other software/packages(Homebrew calles them formulas) without having to go to different sites everytime you need to downlaod the latest version. It is all possible with a simple command like `brew install nameofsoftware` just look them up [here](http://braumeister.org/) or type `brew search nameofsoftwareyouarelookingfor`.

To install Git with the CLI enter `brew install git`.
\**NOTE: If you are the administrator of the computer and have been restricted to download software try entering `sudo` before the script and make sure you are writing the correct script!**

After you have downloaded software you may need to restart the Terminal. Close the CLI and re-open it.
To make sure it worked enter `git --version` and you should see the following(probably with a more recent version).
![alt text](https://cldup.com/OCjbbRcif0.png)

---
[Next: Making a Repository](./makingARepo/)

