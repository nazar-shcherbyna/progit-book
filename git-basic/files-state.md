# Two files states it GIT

Each file in working directory can be in two states for git - **tracked** or **untracked**

**Tracked** files are files from the last snapshot, as well as newly staged files. Thay can be modified, unmodified, staged. In short **tracked** files are files that GIT knows about.

**Untracked** files are everything else - all files that were not in the last snapshot and are not in the staging area.

When a GIT repository is clonned first time, all the files are tracked and unmodified because GIT just checked them out and nobody has edited them yet.

![merge-process-tree](/assets/images/git-basic/files-state.png)
