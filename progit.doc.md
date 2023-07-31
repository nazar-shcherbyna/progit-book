## Pro Git

### Git Basics

#### Initializing a Repository in an Existing Directory

_git init_ >> creates a new sub directory named .git that contains all of your necessary repository files - a git repository skeleton.

#### Cloning an Existing Repository

#git clone [http://...] [dirname]# - creates a directory named [dirname],  
initializes .git directory inside, pulls down all the data  
for that repository, checks out a working copy of latest version.

### Undoing things

_git commit --amend_ >> takes staging area and uses it for preious commit. If you've made no  
changes since your last commit, than your snapshot will look exactly the same, and all you will  
change your commit message.

_git commit --amend --no-edit_ >> add additional changes with the same commit message
