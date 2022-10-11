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

## Data Wrangling
Data Wrangling is mean for processing, transforming the original data.

### Using grep to extract text data
The img shows that we use "grep" to extract text line which contains "sshd". After that, using symbol ">" to output result into file "tsp.log".  

![img_20.png](img_20.png)

And, whatever, if you need to filter text data twice continuously.

![img_21.png](img_21.png)

### Using sed to do text search,replace,count,filter
For example, at below img, 's/.*Disconnected from//' means that searching any text starts with any word and end with 'Disconnected from', and replace with blank.

![img_22.png](img_22.png)

In addition,pipeline symbol "|" can forward the result of sed to another text processing commands like "uniq", "wc", and so on.

![img_23.png](img_23.png)

### Please debug regexp with tools
Regexp is too complicated to debug with your eyes, so, please debug it with regexp debugging tools,for example:
- regex101.com

## Version Control Tools

The version control tool can save you from disaster, help you collaborate with others, and quickly find and isolate problematic changes. 

### Git graph that show how to branch and merge
For example, we can do feature adding and bug fixing based on the same parent node,concurrently. After that, merging these two nodes into one node.

![img_24.png](img_24.png)

### New Git repo will create a hidden git folder 
When a new git repository has been created, the git will help us create a hidden folder which is a git metadata store.

![img_25.png](img_25.png)


### Use "git status" to check what's going on git 
For example:

![img_26.png](img_26.png)

### Use "git add" to add files which should be in the next snapshot
For example, if you want file "hello.txt" be included in the next snapshot, you should input "git add hello.txt".

![img_27.png](img_27.png)


### Use "git log" to check all history commit operations
For example:

![img_28.png](img_28.png)

### Use "git cat-file" to check git decimal version code

![img_29.png](img_29.png)

### Use "git checkout" to move the head of node
If you want to change your current working nodes, you can use "git checkout". This git command will set node,which you want,as a head node and change contents to that time.

![img_30.png](img_30.png)

### Use "git diff" show difference between two commit version of codes.

For example:

![img_31.png](img_31.png)

### Use "git branch" create a new branch 
For example:

![img_32.png](img_32.png)

### Use "git merge" to merge branch into current branch

For example, we check out to master branch, and merge cat branch into the master branch.

![img_33.png](img_33.png)
![img_34.png](img_34.png)


## Debugging and Profiling

A golden rule in programming is that code does not do what you expect it to do, but what you tell it to do. Bugs are gaps that between your expectation and your codes.

- A first approach to debug a program is to add print statements around where you have detected the problem, and keep iterating until you have extracted enough information to understand what is responsible for the issue.

- A second approach is to use logging in your program, instead of ad hoc print statements.


### The log file place

In UNIX systems, it is commonplace for programs to write their logs under /var/log.


On linux, use "journalctl" to check system log:

```shell
# On Linux
journalctl --since "1m ago" | grep Hello
```