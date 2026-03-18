Unix had Bourne Shell
Gnu has Bourne Again Shell - BASH

### Files
Mounted into a single tree

/
- bin
- dev
- etc
- lib
- proc
- home
- usr
	- bin
		- emacs
		- firefox
		- more binaries
	- include
	- lib
	- sbin
	- share


*.* means current directory
*..* means parent directory


### Commands
#### ls
-l : see file details including permissions and ownership

#### chmod
change file permissions
`chmod a=r testfile` : allow read permission for everyone
`chmod u+x testfile` : allow execute permission for owner

#### cat
`cat testfile` : display contents of testfile
`cat filea fileb` : con*cat*enate file a and b

#### grep
searches text files for pattern

`grap Fred staff.csv students.csv` : Search staff and students for any instances of Fred
patterns are [[Regular Expressions]]

#### man
display manual page for command
`man command`
`man ls`

most commands also support `command --help`

 
 
### Permission
r
w
x

3 bit octal number
owner group other
read write execute
