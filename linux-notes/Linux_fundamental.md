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

## Permissions

## Processes

## Networking

## Archives

## Users & Groups

## Useful One-Liners

## Enumeration Commands

