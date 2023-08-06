# Rebase

This operation works by going to the common ancestor of the two branches(the one you're on and the one you are rebasing onto),  
getting the diff introduced by each commit of the branch you're on, saving those diffs to temporary files, resetting the  
current branch to the same commit as the branch you are rebasing onto, and finally applying each change in turn.

### Example with branches _develop_ and _feature_.

The example implies that you've checked out from **develop** to **feature**, made a few commits and would like  
to move changes to **develop**

**git rebase develop** - save all changes of all commits from the common ancestor commit to the last commit in **feature** in temporary files,  
reset **feature** to common ancestor commit with **develop**, reapply changes on feature.

**git switch develop**

**git merge feature**
