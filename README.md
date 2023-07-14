# Brown-Bag-CLI

## What is the Command Line?
The Command Line Interface is a textual interface which allows user(s) to interact with a system.

## How do you interact with it?
The user(s) are able to type commands into the terminal window because of the shell (ie. bash, cmd, powershell, etc) which facilitates communication between the operating system and the user.  While the list of commands can vary between shell environments, most of them are perform similar functions.  I will be covering the Bourne-Again SHell (BASH) that comes with Linux systems in this presentation.

## Common Commands

### List Directory Contents
*Input:*
```
ls
```
This command outputs to the console the contents of a directory you specify.  If none is given, then it will list the contents of the current working directory. 

*Output:*
```
dir1        dir2         dir3
```
*Options:*
```
ls -lrtha 
```
I recommend using ```ll```, which is an alias for long-formatted listing

*Output:*
```
total 16K
drwxr-xr-x 5 root     root     4.0K Jun 26 10:22 ..
drwxr-xr-x 2 runner29 runner29 4.0K Jun 26 12:11 dir1
drwxr-xr-x 2 runner29 runner29 4.0K Jun 26 12:11 dir2
drwxr-xr-x 2 runner29 runner29 4.0K Jun 26 12:11 dir3
drwxrwxrwx 5 root     root     4.0K Jun 26 12:11 .
```

### Change Working Directory
*Input:*
```
cd dir1
```
This command moves your current working directory to the location you provide it.  This can be either a relative path (extend from current directory) or an absolute path (extend from root).

```~``` - go to home directory

```..``` - change to parent directory

```-``` - return to previous working directory (undo)

```!$``` - reuse previous parameter

### Move/Rename Stuff

### Useful Commands
- grep
-   v = non-matching files
-   i = ignore case
-   r = recursive
- piping
- find
- htop
- 
![image](https://github.com/RocketSandwich/Brown-Bag-CLI/assets/93087022/d9c3ae27-32ea-4b4b-938b-92d50f36647f)


### Weird Commands

