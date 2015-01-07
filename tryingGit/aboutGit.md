##About Version Control

Typically you files are stored on your computer in directories to keep everything organised. Typically you have Images, Documents, Videos and so on. When any one of these files is changed your directory shows you the most up-to-date version and rolling back any changes can be a difficult, if not impossible, task. **Version Control** makes managing versions of files easy and although it has its origins in software engineering it has a wide variety of applications today. The most popular type of version control software is **Git** which was developed by [Linus Torvalds.](http://web.archive.org/web/20040626044423/http://www.linux.org/info/linus.html)

## About Git
blah blah blah...distributed version control. terminal or gui

### Repositories
A repository is a directory where git keeps track of all the changes. It is useful to keep all files associated with a particular project in the one directory.

### "Gitting" Started
You create a git repository by entering the initialise command:

    git init

This creates a .git directory in your repository.

### Status Report

Running the status command tells you about any diffs (differences) such as creations, updates, deletions or conflicts that exist in your repository. It also lets you know what branch you're on.
To find this information simply type:

    git status

Git status is your friend - it keeps you up to date with any and all changes so use it often!

### Adding Files

Any files that you create in your project are not automatically added to your repository (i.e they are not automatically monitored for changes) To start tracking changes to a specific file use the command:

    git add <filename>

If you have more than one file that you want to add you can use the all flag:

    git add -A

### Getting Help 
There are lots of functions in git so one of the most useful ones to know when you are getting started is the help function:

    git --help

### Committing
 Even though you've added a file for tracking it's still not in the repository yet. To have the file included in the git repository use have to commit it using the commit command. Every commit must be accompanied with a brief message outlining what the commit was.

    git commit -m "a commit message"

You should try and keep related changes together in the same commits as this is best practice.

### History
 You can see a log of all the changes that have been made up to that point by running:
    git log 

>Use git log --summary to see more information for each commit. You can see 
>where new files were added for the first time or where files were deleted. 
>It's a good overview of what's going on in the project.

### Sharing
At this point the log shows the changes that you have made to the repository that is stored on your own computer. Part of the reason behind using git is that it is a *distributed* version control system. In order to make the most of this distributed proerty we have to push it to a remote repository.

### Online Repositories
There are several providers of remote repositories, with numerous free and paid options available. Two good examples are [BitBucket](https://bitbucket.org) and [GitHub](https://github.com)

### Git Remote

    git remote add origin <url.to/remote-repository.git>

### Git Push

Now that Git knows where your files should be sent it's time to push them to the remote repository:
    
    git push -u origin master

The -u flag "remembers" the destination (origin repository and master branch) so that for future use you need only type `git push`.

### Git Pull 

If you want to pull data from the master branch of the remote repository simply run:

    git pull origin master

### Git Diff

To get the diff of the most recent commit:

    git diff HEAD

To see that changes that have been staged call:

    git diff --staged

This will show all the changes that have been made to the tracked files. To quit git diff type <kbd>Shift</kbd> + <kbd>q</kbd>

### Git Reset

You can unstage (the opposite of `git add`) files by calling:

    git reset <filename>


### Git Branch

If you type the command `git branch` you will get a list of all the branched of this repository. The default branch is the master branch but it is easy to create others. 
Use branch if you want to add a new feature to the code, try something out or do some refactoring. This way any changes you make are made to the new branch rather than the master branch.

    git branch <name_of_branch>

### Pruning Branched

To delete a branch you're finished with use the delete flag with the branch command:

    git branch -d <merged_branch_to_delete>

If you haven't already merged the branch with the master (see: merging) the `-d` won't work. Instead you need to use:

    git branch -D <unmerged_branch_you_definitely_want_to_delete>

The `-D` has the same effect as forcing a delete `-d -f`


### Git Checkout
 Once you've created a new branch you have to switch to it. This is achieved by running the checkout command:

    git checkout <name_of_branch>

You can simultaneously create and checkout a new branch by using the branch flag with the checkout command:

    git checkout -b <name_of_new_branch>

### Removing Files

To remove a file from a repository use the rm command:

    git rm <file_to_remove>

If you want to delete a directory you have to force it like so:

    git rm -rf <directory/to/remove>

**WARNING** This deletes the directory and everything it contains so be careful that you're deleting the correct directory.

### Merging New Branches

First you need to make sure you're on the master branch:
    
    git checkout master

Once there you just have to call the merge command:

    git merge <branch_to_merge>


### Wild Cards

Adding add javascript files:

    git add '*.js'

Removing all the text files:

    git em '*.txt'  


## Lingo/Jargo

- staged:
    Files are ready to be committed.
- unstaged:
    Files with changes that have not been prepared to be commited.
- untracked:
    Files aren't tracked by Git yet. This usually indicates a newly created file.
- deleted:
    File has been deleted and is waiting to be removed from Git.
- Staging Area:
    A place where we can group files together before we "commit" them to Git.
- Commit
    A "commit" is a snapshot of our repository. This way if we ever need to look back at the changes we've made (or if someone else does), we will see a nice timeline of all changes.