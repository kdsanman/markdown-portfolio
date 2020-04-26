If you're ever wondering where you are in the program, use the command **list**. It will display the line you're on now in your program. If you get an error, or don't see what you think you should be seeing, re-compile your program with the CFLAGS as shown below. These flags can also be in your Makefile, but if there is no make file in your directory this workaround should do it.
```
$ rm c/file/executable
$ CFLAGS="-Wall -g" make c/file/executable
```
