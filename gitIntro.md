# Introduction to Git

## Version Control

version control systems allow you to revisit previous versions of a file by recording changes, allowing you to revert files, track modifications, and compare changes.

Local Version Control
- a database on your hard disk that stores file changes
    
Centralized Version control
- entails a single server storing all changes and file versions, accesible by multiple people
    
Distributed Version Control
- allows the creation of mirrored repos (backups) in case of failure of the CVCS server
    
What is Git?
- snapshots
    - git is a DVCS that stores data as snapshots and creates references to their location
- local operations
    - necessary info can be found locally, allowing for faster workflow without needing to fetch from the server and the ability to work offline
- tracking changes
    - every change applied it tracked by Git, and it detects corruption or data loss
- loss of data
    - minimizes possibility of irreversible damage by making it difficult to lose snapshots
- states
    - committed
        - data is securely store in a local database
    - modified
        - file has been changed, but not committed
    - staged
        - flagged a file's changed versio to be committed in the next snapshot

## History of Git

git came from the open source software project Linux kernel. Many of the devs on that project were using a DVCS called BitKeeper until they had a falling out with the company managing it and the chief architect on Linux kernel created Git instead.

## Getting Started

### Graphical Clients

git includes GUI tools, but users can add third-party tools as well.

### Initial Customization

`git config` allows you to configure your settings the way you like and do things like add your email and name to all commits.

### Default Text Editor

git defaults to the system's deafult text editor unless you manually change the system default to the editor of your choice.

### Check Settings

use `git config --list` to check your settings

## Setting up a Git Repository

### Importing

to import an existing project into git
- `cd` into the project directory
- `git init` to make a new .git subdirectory
- `git commit -m "COMMIT MESSAGE HERE"` to create an inital commit

### Cloning

you can copy an existing repo using `git clone ADDRESS OF REPO` and receive all versions of all the project's files.

## Workflow

### Local Repository Structure

the local repo has three components
- working directory (containing the files)
- index (used for staging)
- head (the most recent commit)
    
### Saving Changes

all files in a working copy of a project are either
- tracked (part of the most recent snapshot)
- untracked (not part of the most recent snapshot)

### The Life Cycle of File Status

after you edit a file it is flagged as modified

you stage the modified file

you commit the staged changes

### Check File Status

`git status` gives you the current state of files

### Tracking and Staging a New File

`git add FILENAME` tracks one file
`git add *` will track all of them

### Committing a File

`git commit -m "COMMIT MESSAGE HERE"` will record all of your staged files
`git commit -a` will commit all modifications

### Pushing Changes

`git push origin master` pushes changes from the local master branch to the remote repo 'origin'

### Stashing Changes

`git stash` temporarily hides changes, giving you a clean directory, then they can be retrieved with `stash apply`

## Remote Repositories

remote repos allow collaboration within teams by letting them clone the repos to their local branch.

`git remote` shows the short names of all specified remotes locally, while `git remote -v` shows the URLs by their short names.

[< table of contents](code102.md)

[< home](README.md)