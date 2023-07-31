# Removing Files

## standart remove comand from cli

_rm [filename]_ >> removes file from your working directory, it shows up under the “Changes not  
staged for commit” (that is, unstaged) area.

## git remove comand

_git rm [filename]_ >> command remove file from your tracked files (more accurately, remove it  
from your staging area) and then commit, and also removes the file from your working directory  
so you don’t see it as an untracked file the next time around.