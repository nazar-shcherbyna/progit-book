# .gitignore file

if you dont have it yet, run

**echo >> .gitignore** - create .gitignore

### The rules for the patterns you can put in the .gitignore file are as follows:

> - Blank lines and lines start with **_###_** are ignored.
> - Standart glob patterns work, and will be applied recursively throught the entire working three.
> - You can start patterns with a forward slash **_(#/#)_** to avoid recursively.
> - You can end patterns with a forward slash **_(#/#)_** to specify a directory.
> - You can negate a pattern by starting it with an exclamation point **_(#!#)_**.

### The ignore rules examples:

**\*.a** - ignore all .a files

**!lib.a** - ignore all .a files, but do track lib.a, even though you're ignoring .a files above

**/TODO** - only ignore the TODO file in the current directory, not subdir/TODO

**build/** - ignore all files in any directory named build

**doc/\*.txt** - ignore doc/notes.txt, but not doc/server/arch.txt

**doc/\*_/_.pdf** - ignore all .pdf files in the doc/ directory and any of its subdirectories
