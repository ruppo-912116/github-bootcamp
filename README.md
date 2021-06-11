# github-bootcamp
Github bootcamp practise repo

## Introducing Git!
Git is a version control system which tracks teh change in a file over a time.

## installation and setup
pwd(print working directory) command prints out the path where you currently are. On windows, use start . to view the file location.

## Commits in details (and related topics)
The contents of your project folder are represented by the working directory. It is like a workbench. .git folder represents the repository. Within the .git folder, there are two "places" that should be mentioned, the staging area (represented by the index file) and the commit history (represented by the objects folder).
The staging area is sort of like a rough draft space. Whenever ypu are done working on a file or files in your working directory, you want to copy them to the staging area (using the git add command).
Once you have all the files that you want to update in the next version of your project in the staging area, you are ready to save them in the next version of your project called a commit. You do this using the git commit command.
A commit is basically a version of your project and each commit has a 40 character hash (40 letters and numbers) and this hash acts like a name for the commit, its a way to refer to it.

## Working with Branches 
HEAD is simply a pointer that refers to the current location in your repository. It points to a particular branch reference.

## Working with Branches 
HEAD points to a particular references.
/HEAD
/ref/heads

## The Ins and Outs of Stashing
git stash pop removes the content from the stash. git stash apply does not remove the content from the stash thus the unstaged and the staged content or change in the stash can be applied to the different files.
git stash apply stash@{1}----> used for referencing a specific stashed content from the stash stack (here stash@{1})


## Centralized workflows
The simplest collaborative workflow is to have everyone work on the master branch.
