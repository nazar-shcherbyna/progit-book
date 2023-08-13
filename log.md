# GIL log

**git log** - lists the commits made it the repository in reverse chronological order.

![options](/assets/images/log/options-flags.png)

**git log -p** - shows the difference introdced in each commit.

**git log -p -2** - shows only the last two commits with difference.

**git log --stat** - shows statistics for each commit.

**git log --pretty=oneline** - shows each commit as one line.

**git log --pretty=format:"%h - %an, %ar : %s"** - shows the commits with custom format.

![format signs](/assets/images/log/format-signs.png)

**git log --pretty=format:"%h %s" --graph** - shows the commits with graph.

**git log --since=2.weeks** - shows the commits for the last two weeks.

**git log --author=[author name]** - shows the commits by author.

**git log --grep=[pattern]** - shows the commits with pattern in commit message.

**git log [filename]** - shows the commits that introduced a change to the specified file.

**git log --follow [filename]** - shows the commits that introduced a change to the specified file, even if the file was renamed.

**git log [branchA]..[branchB]** - shows the commits that are in branchB but not in branchA.

**git log -- [filename]** - shows the commits that changed the file.
