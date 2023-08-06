# Work with branches

### Rename branch

**git branch --move old-name new-name** - rename only a local branch  
**git push --set-upsteam origin new-name** - push **new-branch** name to the remote and set it to upstream  
**git push origin --delete old-name** - remove **old-branch** from the origin

### Rename _master_ branch

the process start the same as just renaming any other branch

**git branch --move master main**  
**git push --set-upstream origin main**

Local **master** branch is gone, as it's replaced with the **main** branch.  
The **main** branch is presents on the remote. However the old **master** branch is still presents on the remote.
Other collaborators will continue to use the **master** branch as the base of their work,
untill you make some further changes.

Now you have a few more tasks in front of you to complete the transition:

> > Any projects that depends on this one will need to update their code and/or configuration.
> > Update any test-runner configuration files.
> > Adjust build and release scripts.
> > Redirect settings on your repo host for things like the repo's default branch, merge rules, and other things that match branch names.
> > Update references to the **master** branch in the documentation.
> > Close or merge any pull requests that reffers to the **master** branch.

After you've done all these tasks, and are certain the **main** branch is performs just as the **master** branch, you can delete the **master** branch

**git push origin --delete master**
