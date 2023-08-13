# GIT commit

**git commit** - the command lunches configured editor and shows the default reminding message.

**git commit -v** - the same ad above but adds diff with changes after default message.

**git commit -m '[commit message]'** - make commit and add message to it.

### Undoing things

**git commit --amend** - takes staging area and uses it for preious commit. If you've made no changes since your last commit, than your snapshot will look exactly the same, and all you will change your commit message.

**git commit --amend --no-edit** - add additional changes with the same commit message
