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
- display certain columns of the file
- ```cat -vet``` : shows hidden characters in the file

### sort - organize data in columns

### head - top n lines from the file

### tail - bottom n lines from the file

### less - page through the file



# Helper

- ```dos2unix <filename>``` - removes additional hidden characters (like from windows) from the file
- ```ctrl + l``` - clear the screen
- ```echo $<name>``` - list env variables that start with name
- ```chsh -l``` - list available shells (e.g. bash)
- ```chsh -s <path-to-shell>``` - sets default sheel e.g. /usr/bin/bash
- ```cat /etc/shells``` - also lists available shells
- default shell location configuration: ```/etc/passwd```
- simple grepping: ```grep <stringtosearch> <filetosearch>```
