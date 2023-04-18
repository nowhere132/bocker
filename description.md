# Description
This file is used to digging in source code, and break them into pieces 

## Table of Contents
- [Bocker Functions](#bocker-functions)
  - [bocker_check](#bockercheck)
  - [bocker_init](#bockerinit)
- [Bash Commands](#bash-commands)
  - [awk](#awk)
  - [cat](#cat)
  - [cp](#cp)
  - [grep](#grep)
  - [rm](#rm)

---
## Bocker Functions

### bocker_check
Its idea is: `condition === true ? 0 : 1`

### bocker_init

---
## Bash Commands
### awk
```shell
awk -F ': *' '$1 == "X-Docker-Token" { print $2 }'
awk '{print $1}'
awk '{print $2}'
```

### grep
```shell
grep -qw "$1"
grep "^$(ps o pid,cmd
grep -E "^\ *[0-9]+ unshare.*$1"
```
Command `grep` is abbr. for "Global Regular Expression Print"  
It's used to search for text patterns within files  
It has the following syntax `grep [options] [pattern] [file(s)]`  
Option `-r` or `--recursive` to search recursively (within directories and their subdirectories)  
Option `-i` or `--ignore-case` to perform a case-insensitive search  
Option `-q` or `--quiet` to suppress normal output. This option is used when you just want to check if a pattern exists in a file without displaying the matching lines  
Option `-w` or `--word-regexp` is used to search for whole word only  
Option `-E` or `--extended-regexp` to interpret as an extended regular expression (ERE). Further explanation: [link](https://unix.stackexchange.com/questions/50512/what-is-the-difference-between-grep-e-and-grep-e-option)  

### cp
Command `cp` has the following syntax: `cp [options] [source] [destination]`  
Option `-r` or `--recursive` to copy recursively  
Option `-f` or `--force` to overwrite without prompting for confirmation (if they already exist in the destination directory)  
Option `-d` or `--dir` to delete folders  
Option `--reflink[=always|auto|never]` to create file clones, also known as "reflinks", if supported by the file system. File clones are lightweight copies that share data blocks with the original file, which can save disk space  

### cat
Command `cat` shown in source code is following basic syntax `cat <filename>`  
It doesn't contain any options

### rm
Command `rm` has the following syntax `rm [options] [file(s) or directory(ies)]`  
Without options, we can delete 1 or many files using `rm <filename1> <filename2> ... <filename-n>`  
Option `-r` or `--recursive` to delete recursively
Option `-f` or `--force` to delete without prompting for confirmation, even if the files are write-protected  
Option `-d` or `--dir` to delete folders  
Option `-i` or `--interactive` to prompt for confirmation before removing each file. This is a safety measure to prevent accidental deletion

