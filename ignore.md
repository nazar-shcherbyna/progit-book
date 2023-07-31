# .gitignore file

## create

_echo >> .gitignore_ >> create .gitignore

## The rules for the patterns you can put in the .gitignore file are as follows:

`
> - Blank lines and lines start with ### are ignored.
> - Standart glob patterns work, and will be applied recursively throught the entire working three.
> - You can start patterns with a forward slash (#/#) to avoid recursively.
> - You can end patterns with a forward slash (#/#) to specify a directory.
> - You can negate a pattern by starting it with an exclamation point(#!#).
`

## the ignore rules examples

### ignore all .a files

\*.a

### ignore all .a files, but do track lib.a, even though you're ignoring .a files above

!lib.a

### only ignore the TODO file in the current directory, not subdir/TODO

/TODO

### ignore all files in any directory named build

build/

### ignore doc/notes.txt, but not doc/server/arch.txt

doc/\*.txt

### ignore all .pdf files in the doc/ directory and any of its subdirectories

doc/\*_/_.pdf
