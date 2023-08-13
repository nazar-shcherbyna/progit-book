# Rebase

The project snapshot will be the same in comparison with _merge_ command, but _git_ history will be creaner

#### Merged _develop_ to _master_ process three

**git switch master**

**git merge develop**

![merge-process-tree](/assets/images/rebase/merge-process-tree.png)

#### Rebase _master_ to _develop_ process three

**git switch develop**

**git rebase master**

**git switch master**

**git merge develop**

![merge-process-tree](/assets/images/rebase/rebase-process-tree.png)

This operation works by going to the common ancestor of the two branches(the one you're on and the one you are rebasing onto), getting the diff introduced by each commit of the branch you're on, saving those diffs to temporary files, resetting the current branch to the same commit as the branch you are rebasing onto, and finally applying each change in turn.

### Example with branches _develop_ and _feature_.

The example implies that you've checked out from **develop** to **feature**, made a few commits and would like to move changes only from **feature** to **master** directly.

**git rebase develop** - save all changes of all commits from the common ancestor commit to the last commit in **feature** in temporary files, reset **feature** to common ancestor commit with **develop**, reapply changes on feature.(As described above)

**git switch develop**

**git merge feature**

### Moving changes from three ways diverged branch to mainline

Suppose you have the mainline branch **master**, the dev branch **develop** and diverged from the develop branch **feature**.

![start three](/assets/images/rebase/--onto-start-tree.png)

decided to merge the **feature** branch into **master**. But you want to hold off **develop** changes untill it's nedded further. You cat take the changes on **feature** that aren't on the **develop** branch(C8 and C9) and replay them onto the master branch by using the _--onto_ option in _git rebase_:

**git rebase --onto master develop feature**

This command takes the branch **feature**, figures out changes since it was diverged from the **develop** branch, replay these changes in the **feature** branch as if it was based directly off the master branch instead.

![rebased three](/assets/images/rebase/--onto-rebased-master-to-feature-tree.png)

And now you can finish rebase through merge **feature** to **master** directly

**git checkout master**  
**git merge feature**

![rebased three](/assets/images/rebase/--onto-merged-to-master-tree.png)
