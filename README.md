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
DIR1        DIR2         DIR3
```
*Options:*
```
ls -ltha 
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
cd DIR1
```
This command changes your current working directory to the location you provide it.  This can be either a relative path (extend from current directory) or an absolute path (extend from root).

```~``` - go to home directory

```..``` - change to parent directory

```-``` - return to previous working directory (undo)

```!$``` - reuse previous parameter

### Move/Rename Stuff
*Input:*
```
mv SOURCE DEST
```
This command can perform multiple functions.  Firstly, it can move the file/directory of SOURCE into the location of DEST.  Secondly, it can be used to rename the SOURCE file to whatever is provided as DEST.

```-n``` - prevents overwriting existing file

```-b``` - creates backup of DEST file

### More Useful Commands
### Global Regular Expression Print
*Input:*
```
grep "STRING" LOCATION
```

The grep command is used to search for matching expressions within a file or across director(ies).  It is useful when trying to find locations of called functions, parent classes, et cetera. within the code itself without knowing which file it is located in.

```-r``` - if the LOCATION of the file is unknown, you can recursively traverse the contents of an entire directory 

```-v``` - this option inverts the results to output non-matching files 

```-i``` - ignores case sensitive expression

#### Piping
*Input:*
```
history | grep "whatever"
```

A pipe is used to streamline the output of one command and redirect it as the input of another command.  It has many uses, but is this circumstance we can use it to search for an expression that was used as a command. 
 Using a pipe is often useful when trying to search for an expression when you have *some* idea of the scope/pool that you're searching amongst.  

In the example, we are searching for an expression within the pool of previous commands.

### Searching for a File
*Input:*
```
find LOCATION BY_CRITERIA
(e.g., find ./ -name "TEXTFILE")
```

The find command is used to search for content based on a variety of criteria the user wants to look/query by.  This can be by the name, size, time, et cetera.  Unlike grep, this command looks at the data surrounding the content rather than the content itself.  It is most commonly used to find the locations of files which you know the name of but fail to locate.  

```-name``` - search by name

```-size``` - search by size

```-newer``` - search by files newer than one provided

### Viewing System Resources
*Input:*
```
htop
```

This command will bring up dynamic screen that displays active resource consumption and usage directly in your terminal.  It visualizes things like processor usage, who is on your VM, what command they're using, thread and memory usage, et cetera.
![image](https://github.com/RocketSandwich/Brown-Bag-CLI/assets/93087022/d9c3ae27-32ea-4b4b-938b-92d50f36647f)


### Weird Commands
### Continouus Affirmative Response
*Input:*
```
yes
```

This command will indefinitely output a given response (default 'yes'), to the console with the only option to quit being ctrl^c.  Surprisingly, some people use this with piping to run some scripts overnight or away from the computer which require user response or prompting.  

### Reversal
*Input:*
```
rev TEXTFILE.txt
```

This command inverts all text within the file.
