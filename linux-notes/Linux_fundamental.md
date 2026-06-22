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

`ip` Shows network devices, interfaces, route and addresses
- `ip a` a: address, shows all interfaces with their status and ip
- `ip r` r: route
- `ip -d []` d: detail

\
`netstat` Network status, shows active connection, sockets, interface static and routes
- `netstat -a` a: all, shows all sockets
- `netstat -n` shows sockets numerical
- `netstat -an` most used.
- `netstat -r` r: route, shows route table
- `netstat -i` i: interface

\
`ss` Similar to netstat
- `ss -u/-t` udp/tcp 
- `ss -l` l: listening
- `ss -n` n: numerical
- `ss -tlupn` listening ports, tcp and udp, numerical

\
`curl` Transfer Urls (your unautomated webbrowser) --supports many protocols
- `curl -I` shows only headers
- `curl -v` shows request and response with detail  
- `curl -L` follows for redirect
- `curl -O` saves to file
- `curl -X [HTTP method]` http methods
- `curl -X [URL] -d "info"` Posts "info" to URL
- `curl -H "header: value"` adds header 
- `curl -b "session:..."` sending cookie
- `curl -c` downloading cookie
- `curl -u user:pass` authenticate with user and pass --basic auth
- `curl --proxy [URL]` send request from a proxy

\
`wget` Network downloader
- `wget -O [file name]` saves with specefic file name
- `wget -c` continue downloading interupted downloads
- `wget -b` downloads in background
- `wget -m` mirrors url(download website)

\
`ping` Pong
- `ping -c [number]` c: counter
- `ping -s [size]` packet size

\
`tracerout` Trace packets route

\
`dig` Shows Domain Info
- `dig [URL]` A records
- `dig [URL] +short` only IP
- `dig [URL] MX NS TXT` shows MX, NS, TXT records
- `dig @ip(dns) [URL]` use ip(dns) as dns

\
`nslookup` and `whois` are also useful tools for OSINT

## Archives

`tar` Makes an archive for created files
- `tar -czvf [archive].tar.gz dir` create archive 
- `tar -xzvf [archive].tar.gz` extract
- `tar -tvf [archive].tar` list contents  
for gzip should add `-z` and for xz should add `-J`

\
`zip` zip a file or dir
- `zip -r [archive].zip dir` zips dir to archive.zip
- `unzip [archive].zip` unzip a file


## Users & Groups

## Useful One-Liners

## Enumeration Commands

