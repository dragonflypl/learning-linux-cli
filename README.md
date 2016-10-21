# learning-linux-cli

## Working with CLI

### Connecting to consoles

- ```who``` - displays info about connection
- ```tty``` - display terminal device (?)
- switching between consoles: ctrl + alt + Fx | ```chvt 1...7```
- logging out: ctrl + d | ```exit``` | ```logout```

### Recalling previous commands from history

- ```!<string>``` - will execute last command staring with a string. 
- ```ctrl + r``` will start interactive search (?) in the history
- ```!?<string>``` - will execute last command that has a string anywhere in the command

## Analyzing files

### cat 

- ```cat <filename>```: simply displays the file
- ```cat -vet``` : shows hidden characters in the file

### cut

Command can be used to display certain fields within a file. ```-d``` is used to specify field delimiter.

```cut -f1,3 -d":" file.txt``` - show field 1 & 3 , delimiter is :

### sort - organize data in columns

```sort filename``` - outputs sorted file content. ```-r``` does reverse sorting. 

To sort by column use ```-k```, and to specify delimiter use ```-t```. ```-u```` is for unique.

To sort by numeric field, add ```-n``` that stands for numeric sort.

### head / tail - top / bottom n lines from the file (default is 10)

- ```-n <numlines>``` : displays n lines
- ```-f``` : follow the file, ```tail -f log.txt```

### more / less

- ```more``` page through the longer files. Don't use more, use less
- ```less``` "less is more" i.e. less can page up / down through files and it is possible to search
 - ```page up / page down / up / down```: to move between pages / lines
 - ```linenumber + G``` : go to line number
 - ```/``` : starts searching. moving forward is with ```n``` and backwards is with ```N```
 - ```?``` : starts searching backwards. moving backward is with ```n``` and forward is with ```N```
 - ```G``` – go to the end of file, so now using ? will search from the end
 - ```g``` – go to the start of file, so now using / will search from the beginning
 - ```F``` - simulate following the file (just like ```tail -f```)

## Working with streams and pipes

- ```>``` - write to file (override is exists), ```>>``` - append to file. Specifying ```2>``` means error output and ```1>``` std. output (which is the default) e.g. ```ls -l > file.txt 2> error.txt``` will write std output to file.txt and errors to error.txt.
- ```<``` - read from file
- ```|``` - unnamed pipe

### tee 

```tee``` command enables sending stream to both file & screen:

```
ls -l | tee dump.txt
```
## Create, kill and monitor process

- ```uptime``` - uptime stats.
- ```jobs``` - displays current background jobs. Basically if you can be logged only once to terminal, then if you have a long running operation, you can run it in background, and proceed to the second one.
- ```bg``` - displays background commands
 - ```<command> &``` - ```&``` suffix starts command in the background
 - ```ctrl + z``` - moves task to the background
 - ```fg <num>``` - brings task number ```<num>``` to the foreground

# Helper

- ```!$``` - represents last file/directory argument that was previoysly used
- ```dos2unix <filename>``` - removes additional hidden characters (like from windows) from the file
- ```ctrl + l``` - clear the screen
- ```echo $<name>``` - list env variables that start with name
- ```chsh -l``` - list available shells (e.g. bash)
- ```chsh -s <path-to-shell>``` - sets default sheel e.g. /usr/bin/bash
- ```cat /etc/shells``` - also lists available shells
- default shell location configuration: ```/etc/passwd```
- simple grepping: ```grep <stringtosearch> <filetosearch>```
