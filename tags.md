# Tags

Git has an ability to tag a specific point in a repository's history as being important.

**git tag --list** - list all tags. Flag **-l** or **--list** can be skipped because git implicitly assumes you want listing and provides one. But using **-l** or **--list** flag is mandatory if you want to use wildcards.

Git supports two types of tags - _lightweight_ and _annotated_.

### Lightweight

It's just a pointer to a specific commit, basically commit checksum stored in a file - no other information is kept.

**git tag [tag-name]**

### Annotated

Stores in the git database as full object with tag metadata - tagger name, tagger email, date, tagging massege. Can be signed and veryfied.

**git tag -a [tag-name] -m '[tag-message]'** - create and annotated tag with message.

**git tag -a [tag-name] -m '[tag-message]' [commit-hash]** - create annotated tag from specific commit.

**git show [tag-name]** - show tag's data.

### Sharing tags

By default, the **git push** command doesn't transfer tags to temote servers. You have to explicitly push tags to a shared server after you have created them.

**git push origin [tag-name]**

If you have a lot of tags that you want to push up at once, use _--tags_ option:

**git push origin --tags** - transfer all tags(annotated and lightweight) to the remove server that are not already there.

**git push origin --follow-tags** - push only annotated tags.

Now, if someone clones or pull from your repository, they will get all your tags as well.

### Deleting tags

**git tag -d [tag-name]** - delete tag locally

**git push origin :refs/tags/[tag-name]** - delete tag on a remote

**git push origin --delete [tag-name]** - the same as above but more intuitive
