# Unix Command Cheat Sheet

## Unix Operating System (OS)

UNIX is an operating system created by AT&T's Bell Laboratories and allows multi-tasking and multi-user. Operating systems like Mac OS, Linux, Android OS, iOS and Chrome OS are examples that are based on Unix. 
Unix consists of three parts: the kernel, the shell and the code. The kernel is responsible for the communication with the computer hardware and therefore manages CPU and RAM. 
The shell is an command line interpreter (CLI) and is placed between the user and the kernel. It interprets the inputs the user does and forwards the commands to the kernel for execution. 
The code itself are the commands the user enters into the CLI. 

The following cheat sheet should help get an overview of the most important commands.

## Git and GitHub

Git is an open-source version control tool created by developers working on the Linux operating system in 2005. On the other hand, GitHub is a 2008-based company that provide the interface to make the usage of Git easier.
Using Git and GitHub simplifies shared projects with different users. The following figure shows a collaboration project with three users working on the same project with the help of GitHub. 

![Simplified workflow of Git and Github](http://github.com/majimaken/unix-cheatsheet/Figures/git-flow.png)

## Commands
### CLI Basics 

First, we want to introduce you to the basic commands that are required for the usage of Git and GitHub. This is of importance as you will be working locally on your project before you commit it to the remote repository (GitHub cloud). 
The following commands allow us to get to the desired project folder.

|Command|Description|
|---|---|
|dir|Show the current directory you are working in|
|cd Documents/Projects/Time-Series|Change directory to folder Time-Series|
|cd ..|Change directory to one level higher (back to Projects)|
|mkdir test-project|Make new directory called test-project|
|touch readme.me|Create file called readme.md|

### Getting Started  

Now as you know where you want to store your project data, there are two ways to get started. Either, an existing project on GitHub can be cloned or a completely new project can be started. Before we discuss these two approaches, we need to set identity in order to get Git and GitHub working.

|Command|Description|
|---|---|
|git config --global user.name "your.name"|Set the name shown for commits|
|git config --global user.email "your.email@your.email.com"|Set e-mail address|

#### Cloning an Existing Repository

Cloning an existing repository from GitHub can be practical and should be done every time one before continuing working on a project. After getting to the desired directors using the commands above, the remote repository can be cloned. For this process, the HTTPS URL is required as shown in the figure below. After cloning the project, the user can work on these files locally in order to commit changes later on.

|Command|Description|
|---|---|
|git clone https://github.com/majimaken/unix-cheatsheet.git|Cloning remote repository to current (local) directory|

![Simplified workflow of Git and Github](http://github.com/majimaken/unix-cheatsheet/Figures/clone.jpg)

#### Initializing a New Repository

If we want to start working on your own project, we can simply create files in the project directory we determined earlier. To get Git and its version control working, we need to initialize it. After this, we manually create files in this directory.

|Command|Description|
|---|---|
|git init|Initializing git in the current directory|


### Working on a Project

If we want to continue working on an existing repository, we should pull all changes from the remote repository before working. 

|Command|Description|
|---|---|
|git remote add origin https://github.com/majimaken/unix-cheatsheet.git|Defining remote repository and name it "origin"|
|git pull origin main|Pulling everything from main branch of the remote repository|

The changes made in the files need to committed to the main branch. After the last command, the login screen of GitHub should appear. 

|Command|Description|
|---|---|
|git add .|Add all files to future commit|
|git add README.md|Adding only README.md to future commit|
|git commit -m "Brief Changelog"|Committing to main branch with brief comment|
|git remote add origin https://github.com/majimaken/unix-cheatsheet.git|Adding remote repository and name it "origin"|
|git push -u origin main|Pushing local commits to the remote repository "origin" and push it to the main branch|

### Branches

Sometimes if a user works on new features and does not want to risk ruining the already existing code, creating branches can be useful. The changes should not be visible on the main branch, even after committing them. 

|Command|Description|
|---|---|
|git status|Checking information about current branch and pending changes|
|git checkout main|Going back to main branch|
|git checkout -b new|Creating new branch and call it "new"| 
|git add .|Add all files to future commit (to new branch)|
|git add README.md|Adding only README.md to future commit (to new branch)|
|git commit -m "Brief Changelog for Branch"|Committing to branch "new" with brief comment|

Before we continue working on an existing branch, we need to pull the current version of the main branch.

|Command|Description|
|---|---|
|git checkout new|Changing to branch "new"|
|git merge main|Pulling everything from master and merging it with branch "new"|





