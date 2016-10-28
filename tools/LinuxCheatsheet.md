# Linux Cheatsheet

## Useful Linux commands
| Command                 | Meaning                                                          |
|-------------------------|------------------------------------------------------------------|
| `apropos` *keyword*     | searches in the manuals for the given *keyword*, see also: `man` |
| `cd`                    | change current directory to home directory (equivalent to `cd ~` or `cd $HOME`)  |
| `cd` *dir*              | change current directory to *dir*                                |
| `cd ..`                 | change the current directory to parent of the current directory  |
|                         | (chain these like so: `cd ../..` for 2 dirs up, etc.)  |
| `cp` *fname1* *fname2*  | copies file (or path) *fname1* to file (or path) *fname2*, see also: `mv` |
| `exit`                  | closes the current (tab) in the terminal                         |
| `find -name` *filename* | recursively finds all files which match the given *filename*     |
| `info` *command*        | shows info about the *command*                                   |
| `ls`                    | list all the files in the current directory                      |
| `ls` *dir*              | list all the files in directory *dir*                            |
| `ls -l`                 | list all files in the current directory with more file details   |
| `man` *command*         | shows the manual on how to use *command*                         |
| `mkdir` *dir*           | make a new directory with name *dir*                             |
| `mv` *fname1* *fname2*  | moves (or renames) file (or path) *fname1* to file (or path) *fname2*, see also: `cp` |
| `pwd`                   | prints the Path of the current Worknig Directory                 |
| `rm` *filename*         | delete the file with the given *filename*                        |
| `rm -r` *dir*           | delete the given directory and its contents *dir*                |
| `shutdown now`          | shuts down the computer                                          |
| `touch` *filename*      | make a new file with the given *filename*                        |

## Useful Linux programs
| Command                 | Meaning                                                          |
|-------------------------|------------------------------------------------------------------|
| `eclipse`               | programming IDE for Java/Python/C++                              |
| `gedit`                 | text editor with a graphical userinterface                       | 
| `gimp`                  | image manipulation and paint program                             |
| `libreoffice`           | office suite to create documents, presentations, ...             |
| `nano`                  | basic text editor which works in the terminal (for the adventurous: try `vim` and `emacs`) |
| `nano` *filename*       | starts nano to edit the file *filename*                          |
| `python`                | starts interactive python console on the terminal                |
| `python` *filename*     | uses python to execute file *filename*                           |
| `scp`                   | utility to copy files from and/or to anoter machine              |
|                         | (e.g. `scp localFile user@otherMachine:remoteFile`), see `man scp` for more info |
| `sftp` *user@machine*   | utility to *put* and *get* files as *user* on *machine*, see `man sftp` for more info  |
| `ssh` *user@machine*    | remotely login to a terminal as the given *user* on *machine*    |

## Useful shortcuts on the desktop
| Command                 | Meaning                                                          |
|-------------------------|------------------------------------------------------------------|
| `alt` + `shift`         | switch between programs                                          |
| `ctrl` + `alt` + `T`    | start a new terminal                                             |
| `windows key` (*hold*)  | show desktop shortcuts                                           |
| `windows key` (*press*) | open launcher                                                    |

## Useful shortcuts in a terminal
| Command                 | Meaning                                                          |
|-------------------------|------------------------------------------------------------------|
| `ctrl` + `C`            | cancel: stop the current command                                 |
|`ctrl`+`D`               | end of file/transmission: stop the current session               |
|                         | (works in the shell, (i)python interpreter, ...)                 |
| `ctrl` + `L`            | clear the current terminal window                                |
| `ctrl` + `Z`            | Stop/pause the current task and bring us back to the shell.      |
|                         | Use `fg` to bring it back to the foreground. Use `bg` to start it again,|
|                         | but keep it hidden in the background (can be brought back with `fg`). |
|                         | Also try `jobs` and be sure to check the manpages of these commands.|
| `ctrl` + `shift` + `T`  | start a new tab in the terminal                                  |
| `tab`                   | autocomplete current command                                     |
