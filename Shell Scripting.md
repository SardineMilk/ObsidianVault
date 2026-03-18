You can save commands to a text file and have the shell run those commands

```hello.sh
#!/bin/sh
echo Hello World
```
#! tells linux its a script
/bin/sh is which program should be used to execute it (default shell)

```
nano hello.sh
chmod +x hello.sh
./hello.sh
```


### Arguments
$# : number of arguments
$0 : script name
$1 : first argument
$2 : second argument
etc
$@ : all arguments


### Examples
```
#!/bin/sh
for i in $(seq 0 9); do
	if [ $(expr $i % 3) -eq 0 ]; then
		echo "$i is divisible by 3"
	fi
done
```
