# C - Simple Shell
<h1 align="center"><img src="https://github.com/daveeazi/simple_shell/blob/master/Images/testshell.JPG"></h1>

### C Group Project Syscall
This group project describes a simple UNIX command interpreter based on bash and Sh
It implements some of the functionalities of the original bash shell such as; listing, searching in the path variable, exit and env builtins, among others. It is built for learning purposes and as a required project for [Alx Software Engineering](https://www.alxafrica.com/) curriculum

### Description
This is a shell written in [C](https://en.wikipedia.org/wiki/C_(programming_language)).<br>
It is based on The [Thompson Shell](https://en.wikipedia.org/wiki/Thompson_shell).

### Essential Functionalities of the Simple Shell:
> Displays a prompt "#cisfun$ " and waits for user input.\
> Runs all commands of type "executable program" (ls and /bin/ls).\
> Runs the following build_in commands: **exit**, **env**, **setenv** and **unsetenv**.\
> Handles commands with arguments.\
> Handles the PATH global variable.\
> Handles The EOF (End Of File) condition.\
> Handles the Ctrl + C signal -> It doesn't exit the shell

### Functions
 - **AUTHORS** -> List of contributors to this repository
 - **man_1_simple_shell** -> Manual page for the simple_shell
 - **shell.h** -> Header file
 - **shell.c** -> main function
	- **sig_handler** -> handles the Ctrl + C signal
	- **_EOF** -> handles the End Of File condition
 - **string.c**
	- **_putchar** -> prints a character
	- **_puts** -> prints a string
	- **_strlen** -> gives the length of a string
	- **_strdup** -> copies a string in a newly allocated memory
	- **concat_all** -> concatenates 3 strings in a newly allocated memory
 - **line_exec.c**
	- **splitstring** -> splits a string into an array of words
	- **execute** -> executes a command using execve
	- **realloc** -> reallocates a memory block
	- **freearv** -> frees a 2 dimensional array
 - **linkpath.c**
	- **_getenv** -> returns the value of a global variable
	- **add_node_end** -> adds a node in a singly linked list
	- **linkpath** -> creates a singly linked list for PATH directories
	- **_which** -> finds the pathname of a command
	- **free_list** -> frees the linked list of PATH value
 - **checkbuild.c**
	- **checkbuild** -> checks if a command is a build-in command
 - **buildin.c**
	- **exitt** -> handles the exit buildin command
	- **_atoi** -> converts a string into an integer
	- **env** -> prints the current environment
	- **_setenv** -> Initialize a new global variable, or modify an existing one
	- **_unsetenv** -> remove a global variable

****
### List of allowed functions and system calls for this project
 - access (man 2 access)
 - chdir (man 2 chdir)
 - close (man 2 close)
 - closedir (man 3 closedir)
 - execve (man 2 execve)
 - exit (man 3 exit)
 - _exit (man 2 _exit)
 - fflush (man 3 fflush)
 - fork (man 2 fork)
 - free (man 3 free)
 - getcwd (man 3 getcwd)
 - getline (man 3 getline)
 - isatty (man 3 isatty)
 - kill (man 2 kill)
 - malloc (man 3 malloc)
 - open (man 2 open)
 - opendir (man 3 opendir)
 - perror (man 3 perror)
 - read (man 2 read)
 - readdir (man 3 readdir)
 - signal (man 2 signal)
 - stat (__xstat) (man 2 stat)
 - lstat (__lxstat) (man 2 lstat)
 - fstat (__fxstat) (man 2 fstat)
 - strtok (man 3 strtok)
 - wait (man 2 wait)
 - waitpid (man 2 waitpid)
 - wait3 (man 2 wait3)
 - wait4 (man 2 wait4)
 - write (man 2 write)

### Installation
Clone the below repository and compile the files into an executable using the GCC compiler.
```
https://github.com/daveeazi/simple_shell.git.
```
### Environment
Our shell was built and tested on  Ubuntu 20.04 LTS.

### Basic usage :bulb:
- First, [fork this repository](https://docs.github.com/en/github/getting-started-with-github/fork-a-repo).
- Then [clone it to your local machine](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository).
- Create an executable by running the following command:
- Type cd simple_shell
- `gcc -Wall -Werror -Wextra -pedantic *.c -o hsh`
- From there, type in the following command and press your enter button.
- `./hsh`
- When you want to exit the shell, you can use one of the following methods:
> **1: Type the command "exit"**
````
exit
````
> **2: Press on Ctrl + D**
- Final step: ENJOY!

## Example :computer:
````
ubunto@ubuntu:~/OS/simple_shell$ gcc -Wall -Wextra -Werror -pedantic *.c -o hsh
ubunto@ubuntu:~/OS/simple_shell$ ./hsh
#cisfun$ echo Hello, This is an example
Hello, This is an example
#cisfun$ ls
README.md  checkbuild.c  line_exec.c  shell.c  string.c
buildin.c  hsh		 linkpath.c   shell.h
#cisfun$ ^C
#cisfun$ ls -l
total 52
-rw-r--r-- 1 ubunto ubunto  3067 Aug 9 04:22 README.md
-rw-r--r-- 1 ubunto ubunto  2183 Aug 9 16:17 buildin.c
-rw-r--r-- 1 ubunto ubunto   574 Aug 9 15:59 checkbuild.c
-rwxr-xr-x 1 ubunto ubunto 18144 Aug 9 04:22 hsh
-rw-r--r-- 1 ubunto ubunto  2091 Aug 9 14:49 line_exec.c
-rw-r--r-- 1 ubunto ubunto  199 Aug 9 14:30 linkpath.c
-rw-r--r-- 1 ubunto ubunto   951 Aug 9 16:09 shell.c
-rw-r--r-- 1 ubunto ubunto  1351 Aug 9 15:58 shell.h
-rw-r--r-- 1 ubunto ubunto  1727 Aug 9 14:30 string.c
#cisfun$ exit
ubunto@ubuntu:~/OS/simple_shell$
````

## Help
If you need help to get started with hsh simple shell, email one of the contributers as listed in [AUTHORS](https://github.com/daveeazi/simple_shell/blob/master/AUTHORS).

## Authors
* [**David Atat**](https://github.com/daveeazi) Mail at: <davidatat8@gmail.com>
* [**Alphonsus Oshiole**](https://github.com/Alphydoo) Mail at <aaoshiole@yahoo.com>

## Acknowledgments
- Our fellow cohort members.
- The creators of the C language.
- Our software engineer-in-residence.
- Betty, Alx Holberton.
