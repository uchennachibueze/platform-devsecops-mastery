## LFS101 — Command Line Operations

**Status:** Completed  
**Completion date:** August 6, 2026

### Concepts I learned

- I learned about absolute and relative path and the easy way to identify an absolute path. It starts with a / while relative path can start with a .. or ~
- I learned about the pushd and popd commands used to add and remove directory paths to a stack for history keeping and ease of navigation
- I learned about the find and locate commands used to search files. The locate uses updatedb database to locate its files. So if the database is not updated, it wouldn't locate the file

### Commands I practised

| Command | Purpose | Example I ran |
|---|---|---|
| `pwd` | This is used to see the present working directory | pwd |
| `cd` |  This is used to navigate a path|  cd ~/home|
| `ls` |  This is used to list content of a directory|  ls -la /root|
| `type` |  This is used as an option in find and is used to specify the type of file or directory when using find|  find / -type d -name test|
| `which` |  This is used to find the location of a file or program |  which firefox|
| `man` |  This is used to access the manual pages or documentation in Linux|  man|

### What was already familiar
Some of the commands were already familiar like the cd, pwd, ls etc
### What was new or unclear
Popd and pushd were new to me
### How this applies to DevOps or DevSecOps
This will be useful in DevOps or DevSecOps especially when we get to bash scripting

mkdir -p allowed us to create  multiple directories in one commmand
The braces is like an array of directory names
which is used to find file specified, type is used as an option for find to specify the type of object to find, command -v is used to find the path of a program
. in find is used to search for files or program in the current directory
