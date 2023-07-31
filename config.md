# Config

## Config types

There are three types of config files:

> --system(uses throught systems for all users)
> --global(uses for current user)
> --local(uses by default in git directory(that is, .git/config). default flag)

_git config --list --show-origin_ >> view all configuration settings and where they are coming from

## Your identity

Each git command uses user.name and user.email from config and it's immutably baked into the commits
you start creating:

_git config --global user.name "[USERNAME]"_
_git config --global user.email [USERNAME]_

## Set default branch name

_git config --global init.defaultBranch main_

## Checking your settings

_git config --list_ >> view all configuration settings. Can be used with config flags by types(-s, -g, -l). See Config types above.