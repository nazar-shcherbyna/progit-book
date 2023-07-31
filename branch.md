# Work with branches

## Rename branch

_git branch --move old-name new-name_ >> rename only a local branch
_git push --set-upsteam origin new-name_ >> push __new-branch__ name to the remote and set it to upstream
_git push origin --delete old-name_ >> remove __old-branch__ from the origin

## Rename _master_ branch

the process start the same as just renaming any other branch

_git branch --move master main_
_git push --set-upstream origin main_

Local __master__ branch is gone, as it's replaced with the __main__ branch.  
The __main__ branch is presents on the remote. However the old __master__ branch is still presents on the remote.
Other collaborators will continue to use the __master__ branch as the base of their work, 
untill you make some further changes.

Now you have a few more tasks in front of you to complete the transition:

>> Any projects that depends on this one will need to update their code and/or configuration.
>> Update any test-runner configuration files.
>> Adjust build and release scripts.
>> Redirect settings on your repo host for things like the repo's default branch, merge rules, and other things that match branch names.
>> Update references to the __master__ branch in the documentation.
>> Close or merge any pull requests that reffers to the __master__ branch.

After you've done all these tasks, and are certain the __main__ branch is performs just as the __master__ branch, you can delete the __master__ branch

_git push origin --delete master_
