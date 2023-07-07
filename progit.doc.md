##Pro Git##

###First time git setup###

####Configutation types####

There are three types of config files:

> --system(uses throught systems for all users)
> --global(uses for current user)
> --local(uses by default in git directory(that is, .git/config). default flag)

**git config --list --show-origin** >> view all configuration settings and where they are coming from

####Your identity####

Each git command uses user.name and user.email from config and it's immutably baked into the commits
you start creating:

git config --global user.name "[USERNAME]"
git config --global user.email [USERNAME]

####Default branch name####

git config --global init.defaultBranch main

####Checking your settings####

**git config --list** >> view all configuration settings
