### Standard Input/Output
When a Unix program starts, the shell gives it 3 input/output streams
- **standard input** 
- **standard output**
- **standard error**
By default
- input is connected to the keyboard
- output+error are connected to the stream

Most command line programs that take filenames will read from standard input by default
- unless filenames are specified
- The `-` symbol specifies to read from standard input

#### Output Redirection
Adding `> filename` to the end of a command redirects standard output to a file called "filename"
`ls -l > dir.list` will write a directory listing to a file, rather than printing it in the command line

`> filename` overwrites any existing file at filename
`>> filename` appends to any existing file

#### Input redirection
`< filename` connects standard input to a file instead of keyboard
`sort < dir.list` takes the contents of dir.list, sorts them, then prints to command line
`sort < dir.list > dir_sorted` does the same, but outputs to file dir_sorted  

#### Pipes
Connect two programs using a **pipe** |
The output of the first program becomes the input to the next
All errors still go to the screen
`ls -l | sort > dir_sorted`

### Wildcards 
Shells expand wildcard patterns, matching against filenames

#### *
`echo a*` will echo every file starting with a

#### ?
? matches any single character
`rm ??.png` deletes all .png files in current directory with exactly 2 characters before extension

#### \[\]
[] matches a set of single characters
`ls file[aeiou].txt` lists all existing of filea.txt, filee.txt, filei.txt, fileu.txt
`ls file[a-f].txt` lists all existing of filea.txt to filef.txt

### Quoting
To escape special characters like ?, use a backslash or single quotes
single quotes also let you use filenames that have spaces
`echo This is a star: \*`
`echo 'This is a star: *'`
`echo "Hey, $USER, this is a star: *"` <- expand only $


### Exit Status
When programs finish they return an exit status/exit code/return status
Successful: returns 0
Unsuccessful: returns a non-zero value