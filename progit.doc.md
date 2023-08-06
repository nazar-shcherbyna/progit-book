## Pro Git

### Git Basics

#### Initializing a Repository in an Existing Directory

**git init** - creates a new sub directory named .git that contains all of your necessary repository files - a git repository skeleton.

#### Cloning an Existing Repository

**git clone [http://...] [dirname]** - creates a directory named [dirname],  
initializes .git directory inside, pulls down all the data  
for that repository, checks out a working copy of latest version.

### Undoing things

**git commit --amend** - takes staging area and uses it for preious commit. If you've made no  
changes since your last commit, than your snapshot will look exactly the same, and all you will  
change your commit message.

**git commit --amend --no-edit** - add additional changes with the same commit message
