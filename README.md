# learning-linux-cli

## Working with CLI

### Connecting to consoles

- ```who``` - displays info about connection
- ```tty``` - display terminal device (?)
- switching between consoles: ctrl + alt + Fx | ```chvt 1...7```
- logging out: ctrl + d | ```exit``` | ```logout```

# Helper

- ```ctrl + l``` - clear the screen
- ```echo $<name>``` - list env variables that start with name
- ```chsh -l``` - list available shells (e.g. bash)
- ```chsh -s <path-to-shell>``` - sets default sheel e.g. /usr/bin/bash
- ```cat /etc/shells``` - also lists available shells
- default shell location configuration: ```/etc/passwd```
- simple grepping: ```grep <stringtosearch> <filetosearch>```
