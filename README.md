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

### sort - organize data in columns

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
 - G – go to the end of file, so now using ? will search from the end
 - g – go to the start of file, so now using / will search from the beginning
 - F - simulate following the file (just like ```tail -f```)


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
