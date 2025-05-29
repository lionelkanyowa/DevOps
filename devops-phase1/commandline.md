---
type: GuideStudy
title: Guide(Study):Introduction to the Command Line
tags: []
topic: null
assessmentsCovered: null
progress: In-Progress
lastReviewed: '2025-05-29'
domain: DevOps
linkTo: null
category: StudyGuide
---


### Summary

Basic fundamentals of the command Line.


### Content

## The CLI Display

- This is an example of the prompt on a Ubuntu linix server:

```bash
ubuntu@chopin:~$
```

This translate to the format below:

```bash
[user]@[hostname]:[current_directory]$
```



## CLI Input

`echo` - A command that sends text to the CLI's output

```bash
$ echo "Hello Word"
Hello World
```

`pwd` - (Print Working Directory) A command that shows where you are in your file structure.

```bash
$ pwd
/home/ubuntu
```

 

## Anatomy of a Command

Commands typed in a terminal take the following format:

`[command] [arguments...]`

`[command]` example: `/path/to/file` , `echo`

`[argument]` example: Strings being passed to a program: `"Hello World"`



### How a command and argument work together

```bash
# Command: compress the files-to-archive directory to archive.tgz in this
# directory.
$ tar -c -z -f ./archive.tgz ./files-to-archive/
```

- `tar` is the command and `-c`, `-z`, `-f`, `./archive.tgz`, `./files-to-archive/` are the arguments.

- This can also be written as `tar -czf, ./archive.tgz, ./files-to-archive/`



- To find out how a command works, in the terminal type: `man command`

    ```bash
    man echo
    ```

    ```bash
    ECHO(1)                                            User Commands                                            ECHO(1)
    
    NAME
           echo - display a line of text
    
    SYNOPSIS
           echo [SHORT-OPTION]... [STRING]...
           echo LONG-OPTION
    
    DESCRIPTION
           Echo the STRING(s) to standard output.
    
           -n     do not output the trailing newline
    
           -e     enable interpretation of backslash escapes
    
           -E     disable interpretation of backslash escapes (default)
    
           --help display this help and exit
    
           --version
                  output version information and exit
    
           If -e is in effect, the following sequences are recognized:
    
           \\     backslash
    
           \a     alert (BEL)
    
           \b     backspace
    
           \c     produce no further output
    
           \e     escape
    
           \f     form feed
    
           \n     new line
    
           \r     carriage return
    
           \t     horizontal tab
    
           \v     vertical tab
    
           \0NNN  byte with octal value NNN (1 to 3 digits)
    
           \xHH   byte with hexadecimal value HH (1 to 2 digits)
    
           NOTE:  your  shell  may  have  its own version of echo, which usually supersedes the version described here.
           Please refer to your shell's documentation for details about the options it supports.
    
    AUTHOR
           Written by Brian Fox and Chet Ramey.
    ```

## Some Command Line use-cases

- Restart servers

- Rename hundreds or thousands of files according to a prescribed pattern

- Manage system logs

- Set up scheduled tasks (cron jobs)

- Debug server issues

- Monkey patch code on a server

- Query data

- Set up databases and servers



## Common Commands

| Command | Description                                                                                       |
| :------ | :------------------------------------------------------------------------------------------------ |
| `cd`    | Change directory.                                                                                 |
| `ls`    | List files and directories in current directory.                                                  |
| `pwd`   | Display the path of the current directory.                                                        |
| `touch` | Create a file.                                                                                    |
| `mkdir` | Create a directory.                                                                               |
| `rm`    | Remove a file or directory. Warning: deleting a file or directory with this command is permanent! |
| `cp`    | Copy a file or directory.                                                                         |
| `mv`    | Move or rename a file or directory.                                                               |
| `echo`  | Print text to STDOUT.                                                                             |
| `cat`   | Display contents of a file.                                                                       |
| `more`  | Display contents of a file, starting at the top and letting the user scroll down.                 |
| `less`  | Display contents of a file in an even more interactive way.                                       |
| `head`  | Display the first part of a file.                                                                 |
| `tail`  | Display the last part of a file.                                                                  |
| `man`   | Display documentation about a command.                                                            |

- `cd /`- Gets you to the core root directory of your system.

- `ls -lah` - Gives more information about each item in the directory

- `cd` or `cd ~` - Gets you to your home directory irregardless of where you are in your file structure.

- A file can be moved or renamed using the `mv` command `mv [source] destination]`:

    ```bash
    $ mv example.txt example1.txt 
    ```

    ```bash
    $ mkdir tmp
    $ mv example1.txt tmp 
    ```

- Moving and renaming at the same time:

    ```bash
    $ mv tmp/example1.txt example2.txt
    ```

- Using the `cp` command to copy files from one location to another. `cp [source] [destination]`:

    ```bash
    $ pwd
    /Users/lionelkanyowa/devops/devops-phase1/practice
    $ cp example2.txt tmp
    $ ls
    example2.txt tmp
    ls tmp
    example2.txt
    ```

- The `cp` command can be used to copy and paste a file with a new name:

    ```bash
    $ cp example2.txt example3.txt
    $ ls
    example2.txt example3.txt
    ```

### Removing files and folders

```bash
$ ls
example2.txt  example3.txt tmp
$ rm example2.txt
$ rm example3.txt
$ ls
tmp
```

- Removing a folder:

    ```bash
    $ cd ..
    $ ls
    loveseat_project.py practice
    rm -r practice
    $ ls
    loveseat_project.py
    ```





​



