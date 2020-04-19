### How do I debug my C program using Mac OS?
To debug a C program on Mac OS we can use *LLDB Debugger*. 

### Cheat Sheet
| Command | Explanation|
| --------| -----------|
| *run [args]* | Start your program with *[args]* |
| *breakpoint set --name [file:]function* | Set a break point at [file:]function. You can also use *b*. |
| *thread backtrace* | Dump a backtrace of the current calling stack. Shorthand is *bt*. |
| *print expr* | Print the value of expr. Shorthand is *p*. |
| *continue* | Continue running the program. Shorthand is *c*. |
| *next* | Next line, but step _over_ function calls. Shorthand is *n*. |
| *step* | Next line, by step _into_ function calls. Shorthand is *s*. |
| *quit* | Exit LDDB |
| *help* | List the types of comands. |
| *shell* | Start a shell as a playground. |
| *clear* | Remove a breakpoint. |
| *info break, info watch* | Show information about breakpoints and watchpoints, respectively. |
| *attach -p pid* | Attach to a running process so you can debug it. |
| *detach* | Detach from the process. |
| *list* | List out the next ten source lines. Add a - to list the previous ten sources. |

### Tutorial
Let's go through a quick tutorial so you can get the hang of it. Head over to your Terminal and navigate to a directory with a `C` file. 
Doesn't matter which one, but make sure it compiles and runs with no errors.
```
$ cd path/to/directory/with/C/file
$ lldb
(lldb) _
````

#### Pro tip: How to exit this shell?
To exit the shell, use `Control+D`. Try it now! Now this time, use this command instead to return to the shell.
```
$ lldb [filename].c
(lldb) target create "[filename]"
Current executable set to '[filename]' (x86_64).
```
#### running the file
To run the file, use the command `run` in the shell. If your program has no errors, you should something similar to this output:
```
(lldb) run
Process 1234 launched: '/Users/path/to/file' (x86_64)
{Text output}
Process 1234 exited with status = 0 (0x00000000)
```

#### Setting a breakpoint
Let's start by setting a `breakpoint` on the `main` function of our C program. We can do that by using the following command where we
specify the name of the function where we want the breakpoint to be set.
```
(lldb) breakpoint set --name main
Breakpoint 1: where = filename`main, address = 0x0000000.....
```
Now run the program. The output is Assembly Code. 
<br>
If we wanted to set the breakpoint at another function, we would replace `main` in the command above with the function name.
