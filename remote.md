# Remote

**git ls-remote** - browse all references which presented on the server

**git remote show origin** - show all branches on the server. Doesn't show tags

**git remote -v** - show all remote urls

### Pull Requsets on the remote

When someone creates a pull request git creates sort of pseudo-branch on the server with a new reference
refs/pull/[#number]/head. You won't get such branch after **git clone** command, but it is there in obscured way
You can pull that reference to your topic branch to check out chenges applying next command:

**git pull origin refs/pulls/[#number]/head**
