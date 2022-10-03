# MissingSemesterOfCS

## Brief Introduction
The "Missing Semester Of CS" course wants to tech us "computing ecosystem literacy" that is how to master tools like the command-line, text-editor, version control system and so on.

Mastering these tools not only enables you to spend less time on figuring out how to bend your tools to your will, but it also lets you solve problems that would previously seem impossibly complex.

- Course homepage: https://missing.csail.mit.edu/
- Lecture video resource link: https://www.bilibili.com/video/BV1x7411H7wa

## Watch!
This doc only covered the essential useful skill&knowledge about the terminal, the git and so on. If you want to get more information about these tools, like how to beautify the terminal fonts and colors and others, please google it :)

## Terminal & Shell Scripts
Terminal,also called shell,is a tool for computer users to type-in commands and control the operating system. For example, we can type ```shutdown now```to shut down my linux computer immediately.


### Type commands on the terminal
In myself conclusion, there are three steps to type commands:
1. Make sure what you want to do with commands? For example, I want to let terminal show the current UTC time.
2. Figure out which command and parameters will satisfy the task. For example, ```date -u``` is the one possible command; and "-u" is the parameter to told the date command:"we need the UTC time"
3. Type commands on the terminal and check the return information.

![img.png](img.png)
   
### String value in Shell
We can use quotes to contain string value,like:

```shell
echo "Hello world!"
```

### Variable Assignment
Be careful that the variable assignment can't work with blanks between "=".

![img_11.png](img_11.png)

### Use Variables
Shell grammar specified '$' symbol for variable usages:

```shell
echo $PATH
```

### Use Command as variables which contained return values
pwd is a command which return current working directory. "$(pwd)" is a syntax that uses commands as a variable which contains the command return value. 

![img_15.png](img_15.png)

### Variable replacement in double quote string
If you need replace variables in string, please use double
quote string, and don't use single quote string.

![img_10.png](img_10.png)

### Define a shell script and call it
The first line in the shell script which started with "#!" told
shell that the script should be run with python program.

![img_16.png](img_16.png)

Inside the shell script,we use"$1","$2"..."$n" get the input parameters.

![img_12.png](img_12.png)

Make a shell command through calling "source xxx.sh"

![img_13.png](img_13.png)


   
### Use "shellcheck" for your scripts checking
For example:

![img_17.png](img_17.png)



### Feel Free to use 'man' or 'tldr' commands
Working with terminals, it is important that you should feel free to use 'man' commands, which can print help docs.

```shell
# print help doc about ls
man ls 

# print help doc about shutdown
man shutdown

# print simple example doc about shutdown
tldr shutdown
```


### Simple File System Operation
Using 'pwd' to get current path of file system

![img_1.png](img_1.png)

Using 'ls' to list files under current path

![img_5.png](img_5.png)

Using 'cd' to change path

![img_2.png](img_2.png)

Using 'which' to search binary runnable file

![img_3.png](img_3.png)

Using 'find' to find file

![img_4.png](img_4.png)

Using 'mv' to move file

```shell
# move current hello.md file to up level and rename to helloworld
mv hello.md ../helloWorld.md
```

Using 'cp' to copy file

```shell
# copy hello.md to hello2.md
cp hello.md hello2.md
```

### File Standard I/O Operators
We can use '<' symbol for input redirection,and use '>' or '>>' symbol for output redirection:

![img_6.png](img_6.png)

- '<' and '>' use covered writing mode.
- '>>' uses appending writing mode.

Using 'tee' command to check the content which we wrote into file:

![img_9.png](img_9.png)

### Error output Operator
Symbol "$?" is a error output operator and the error code 0 is stand for no error, the error code 1 is stand for has errors.

![img_14.png](img_14.png)

### File System Search Operation
Command "find" is a powerful operation which help you find any type of files, such as special name of file, special type of file, special modification status of file and so on. 

![img_19.png](img_19.png)
![img_18.png](img_18.png)

### Network Operation
The "curl" is a network command which can fetch http result from designated url parameters.  

![img_7.png](img_7.png)

We can use "ping" to check the connection between our computer and opposite website server.  

![img_8.png](img_8.png)
   
### Extra references: Linux Shell Tutorials
- Chinese Version: https://linux.vbird.org/linux_basic/
  - I think this website is the best linux tutorial in Chinese.
- English Version: 

## Version Control Tools

The version control tool can save you from disaster, help you collaborate with others, and quickly find and isolate problematic changes. 

