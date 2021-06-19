# github-bootcamp
Github bootcamp practise repo

## Introducing Git!
Git is a version control system which tracks the change in a file over a time.

## installation and setup
pwd(print working directory) command prints out the path where you currently are. On windows, use start . to view the file location.

## Commits in details (and related topics)
<p>The contents of your project folder are represented by the working directory. It is like a workbench. .git folder represents the repository. Within the .git folder, there are two "places" that should be mentioned, **the staging area** (represented by the index file) and **the commit history** (represented by the objects folder).</p>

The staging area is sort of like a rough draft space. Whenever ypu are done working on a file or files in your working directory, you want to copy them to the staging area (using the `git add` command).

Once you have all the files that you want to update in the next version of your project in the staging area, you are ready to save them in the next version of your project called a commit. You do this using the ``` git commit ``` command.

<p>A commit is basically a version of your project and each commit has a 40 character hash (40 letters and numbers) and this hash acts like a name for the commit, its a way to refer to it.</p>

## Working with Branches 
HEAD is simply a pointer that refers to the current location in your repository. It points to a particular branch reference.

## Working with Branches 
HEAD points to a particular references.
/HEAD
/ref/heads

## The Ins and Outs of Stashing
git stash pop removes the content from the stash. git stash apply does not remove the content from the stash thus the unstaged and the staged content or change in the stash can be applied to the different files.
``` git stash apply stash@{1} ``` ----> used for referencing a specific stashed content from the stash stack (here stash@{1})


## Centralized workflows
The simplest collaborative workflow is to have everyone work on the master branch.

## Hashing and objects
Git stores the data in key value pairs. the key being the hash of the data. it is a key-value data store. we can insert any kind of content in the git repository and git will hand us back a unique key we can later use to retrieve that content.

```git hash-object <File>```
The git hash-object command takes some data, stores in out .git/objects directory and gives us back the unique SHA-1 hash that refers to that data object.
In the simplest for, git simply takes some content and returns the unique key that would be used to store our object. But it does not actually store anything.

```echo "hello" | git hash-object --stdin```
The --stdin option tells git hash-object to use the content from stdin rather than a file. In our example, it will hash the word "hello".
The echo command simply repeats whatever we tell it to repeat to the terminal. We pipe the output of echo to git hash-object.

```echo "hello" | git hash-object --stdin -w```
Rather than simply outputting the key that git would store our object under, we can use the -w option to tell git to actually write the object to the database. After running this command, check out the contents of .git/objects.

``` git cat-file -p <object-hash> ```
now that we have data stored in our git object database, we can try retrieving it using the git cat-file command.
the -p option helps to print out the output to the terminal.

### Git object: blobs
Git blobs (binary large object) are the object type Git uses to store the contents of files in a given repository. Blobs don't even include the filenames of each file or any other data. They just store the contents of a file.
