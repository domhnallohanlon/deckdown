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

### Adding Files

Any files that you create in your project are not automatically added to your repository (i.e they are not automatically monitored for changes) To 