# | Linux Cheatsheet |

## Navigation
``` pwd ``` Where am I?
- no usefull switch for you


``` cd ``` Change directory.\
\
```ls``` list files/dir
- ```la``` or ```ls -la``` -a all(hidden dir)
- ```ls -ltrh``` l : length, t :sort by time, r :reverse sort, h : size\

\
```tree``` list directories in tree shape.
- ```tree -a``` -a : hidden dir
- ```tree -L 'number'``` -L : max depth-number

##  File Operations
```cat``` concatenate/display file content.
- ```cat -n``` shows line number
- `cat f1 f2` print both f1 and f2

\
`less`  display file content with more tools than `cat`.
- `less -N` -N : Line number 

\
`head` and `tail` Prints first and last part of file
- `head/tail -n [number]` Shows n first/last line
- `tail -f` Follows the log file(If new data adds in the file it will print them as well)

\
`cp` Copy file/dir
- `cp -r` -r : recursive(ALL the files/dirs) 
- `cp -f` -f : overwrite destination without prompting
- `-rf` is commoonly used

\
`rm` Remove file/dir
-Switches are the same as `cp`
- `rm -i` asks before every remove

\
`mv` Move file/dir
- Same as `cp` & `rm`

\
`mkdir` Makes dir
- `mkdir -p` makes parent dir, No error if dir exists

\
`touch` Changes file timestamp
- mostly used for making new file: `touch [file name]`
- `touch -am` -a : changes access time, -m : changes modification time

## Search
`find` Search for a file/dir in dir
- `find -type [type]` search for file in [type extension]
- `find -name "name"` Search for this name specidicly

\
`grep` search for patterns in files
- `grep -i` Checks for both upper/lower case
- `grep -r` checks every file in dir, recursivly
- `grep -n` line number

## Permissions

`chmod` Changes file mod(premissions ---)  
r:4, w:2, x:1 \
owner-group-other
- `chmod nnn [file]` changes premisson to nnn 
- `chmod +x [file]` adds execute to premission 
- `-R` for recursive in a dir

\
`chown` Changes file owner and group.
- `chown [owner] [file]` Changes file owner 
- `chown [owner]:[group] [file]` Changes owner and group
- `-R` same as chmod

## Processes

`ps` List current procesors.
- `ps aux` Every processor with BSD syntax
- `ps -U [user group]` processor for user group

\
`top` Disply current process. 

\
`kill` Sends signal to a process(Default: kill, terminate)
- `kill [PIDs]` kills PID(s)
- `kill -9 [PID]` kills processor[PID]
- `kill -9 -1` kills as much process as it can
- `kill -l` lists signal names

\
Also read `pgrep - pkill - pidwait`.


## Networking

## Archives

## Users & Groups

## Useful One-Liners

## Enumeration Commands

