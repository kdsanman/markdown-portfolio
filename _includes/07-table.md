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
