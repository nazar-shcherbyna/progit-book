## Pro Git

### First time git setup

#### Configutation types

There are three types of config files:

> --system(uses throught systems for all users)
> --global(uses for current user)
> --local(uses by default in git directory(that is, .git/config). default flag)

_git config --list --show-origin_ >> view all configuration settings and where they are coming from

#### Your identity

Each git command uses user.name and user.email from config and it's immutably baked into the commits
you start creating:

_git config --global user.name "[USERNAME]"_
_git config --global user.email [USERNAME]_

#### Default branch name

_git config --global init.defaultBranch main_

#### Checking your settings

_git config --list_ >> view all configuration settings

### Git Basics

#### Initializing a Repository in an Existing Directory

_git init_ >> creates a new sub directory named .git that contains all of your necessary repository files - a git repository skeleton.

#### Cloning an Existing Repository

#git clone [http://...] [dirname]# - creates a directory named [dirname],  
initializes .git directory inside, pulls down all the data  
for that repository, checks out a working copy of latest version.

#### Ignoring Files

_cat .gitignore_ >> read .gitignore

#### The rules for the patterns you can put in the .gitignore file are as follows:

> - Blank lines and lines start with ### are ignored.
> - Standart glob patterns work, and will be applied recursively throught the entire working three.
> - You can start patterns with a forward slash (#/#) to avoid recursively.
> - You can end patterns with a forward slash (#/#) to specify a directory.
> - You can negate a pattern by starting it with an exclamation point(#!#).

`

# ignore all .a files

\*.a

# but do track lib.a, even though you're ignoring .a files above

!lib.a

# only ignore the TODO file in the current directory, not subdir/TODO

/TODO

# ignore all files in any directory named build

build/

# ignore doc/notes.txt, but not doc/server/arch.txt

doc/\*.txt

# ignore all .pdf files in the doc/ directory and any of its subdirectories

doc/\*_/_.pdf
`

### Removing Files

_rm [filename]_ >> removes file from your working directory, it shows up under the “Changes not  
staged for commit” (that is, unstaged) area.

_git rm [filename]_ >> command remove file from your tracked files (more accurately, remove it  
from your staging area) and then commit, and also removes the file from your working directory  
so you don’t see it as an untracked file the next time around.

### Undoing things

_git commit --amend_ >> takes staging area and uses it for preious commit. If you've made no  
changes since your last commit, than your snapshot will look exactly the same, and all you will  
change your commit message.

_git commit --amend --no-edit_ >> add additional changes with the same commit message
