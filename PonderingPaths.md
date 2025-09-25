# Pondering Paths

## The Root

Alright, so the filesystem starts at /. Under that, there are a whole mess of other directories, configuration files, programs, and, most importantly, flags. In this level, we've added a program right in /, called pwn, that will give you the flag. All you need to do for this level is to invoke this program!
You can invoke a program by providing its path on the command line. In this case, you'll be giving the exact path, starting from /, so the path would be /pwn. This style of path, one that starts with the root directory, is referred to as an "absolute path".
Start the challenge, launch a terminal, invoke the pwn program using its absolute path, and Capture that Flag! Good luck!
### Solve
*Flag:* `pwn.college{UnsTNgIgSaHENpxjlAWCuZ8lxXJ.QX4cTO0wiN1gjNzEzW}`
```
hacker@paths~the-root:~$ /pwn
BOOM!!!
Here is your flag:
pwn.college{UnsTNgIgSaHENpxjlAWCuZ8lxXJ.QX4cTO0wiN1gjNzEzW}
```
Invoked the pwn program using its absolute path, which can be done using the "/" before the program.

### New learnings
I learnt about absolute paths and invoking programs through their absolute paths

## Program and Absolute paths

Let's explore a slightly more complicated path! Except for in the previous level, challenges in pwn.college are in the challenge directory and the challenge directory is, in turn, right in the root directory (/).
The path to the challenge directory is, thus, /challenge. The name of the challenge program in this level is run, and it lives in the /challenge directory. Thus, the path to the run challenge program is /challenge/run.
This challenge again requires you to execute it by invoking its absolute path. You'll want to execute the run file that is in the challenge directory that is, in turn,
in the / directory. If you invoke the challenge correctly, it will give you the flag. Good luck!

### Solve
*Flag:* `pwn.college{EfR-0I67Pf4NbZ7IM-osPimYuZT.QX1QTN0wiN1gjNzEzW}`
```
hacker@paths~program-and-absolute-paths:~$ /challenge/run
Correct!!!
/challenge/run is an absolute path! Here is your flag:
pwn.college{EfR-0I67Pf4NbZ7IM-osPimYuZT.QX1QTN0wiN1gjNzEzW}

```
To execute the run file in the challenge directory , the directory needs to be invoked first, then the run program, thus to invoke the directory "/challenge" which is followed by the execution of the program "/run"

### New learnings
I learnt about invoking directories and the programs within them using a single command.

## Position thy self
The Linux filesystem has tons of directories with tons of files. You can navigate around directories by using the cd (change directory) command and passing a path to it as an argument, as so:
```
hacker@dojo:~$ cd /some/new/directory
hacker@dojo:/some/new/directory$
```
This affects the "current working directory" of your process (in this case, the bash shell). Each process has a directory in which it's currently hanging out. The reasons for this will become clear later in the module.
As an aside, now you can see what the ~ was in the prompt! It shows the current path that your shell is located at.
This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program. Good luck!

### Solve
*Flag:* `pwn.college{EGjD5gjFZsTBPc7Y_ERRb4OgsC7.QX2QTN0wiN1gjNzEzW} `

```
hacker@paths~position-thy-self:~$ /challenge/run
Incorrect...
You are not currently in the /proc/132 directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-thy-self:~$ cd /proc/132
hacker@paths~position-thy-self:/proc/132$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{EGjD5gjFZsTBPc7Y_ERRb4OgsC7.QX2QTN0wiN1gjNzEzW}
hacker@paths~position-thy-self:/proc/132$

```
After finding the path of /challenge/run , it can be executed from that path using cd to change the directory to the one where the file to be executed is at followed by the execution of that file /challenge/run

### New Learnings
I learnt how to execute programs from different directories and change directories .


## Position Elsewhere
The Linux filesystem has tons of directories with tons of files. You can navigate around directories by using the cd (change directory) command and passing a path to it as an argument, as so:
```
hacker@dojo:~$ cd /some/new/directory
hacker@dojo:/some/new/directory$
```
This affects the "current working directory" of your process (in this case, the bash shell). Each process has a directory in which it's currently hanging out. The reasons for this will become clear later in the module.

As an aside, now you can see what the ~ was in the prompt! It shows the current path that your shell is located at.

This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program. Good luck!
### Solve
*Flag:* `pwn.college{kXKzkslrvtPCRlHFYhC15017nMg.QX3QTN0wiN1gjNzEzW}`

```
hacker@paths~position-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /usr/share/doc/fontconfig directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-elsewhere:~$ cd /usr/share/doc/fontconfig
hacker@paths~position-elsewhere:/usr/share/doc/fontconfig$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{kXKzkslrvtPCRlHFYhC15017nMg.QX3QTN0wiN1gjNzEzW}
hacker@paths~position-elsewhere:/usr/share/doc/fontconfig$

```
First the directory had to be changed using 'cd' to find /challenge/run followed by the execution of the latter file.

### New Learnings
I learnt more about the application of cd to change directory 

## Position yet Elsewhere
The Linux filesystem has tons of directories with tons of files. You can navigate around directories by using the cd (change directory) command and passing a path to it as an argument, as so:
```
hacker@dojo:~$ cd /some/new/directory
hacker@dojo:/some/new/directory$
```
This affects the "current working directory" of your process (in this case, the bash shell). Each process has a directory in which it's currently hanging out. The reasons for this will become clear later in the module.

As an aside, now you can see what the ~ was in the prompt! It shows the current path that your shell is located at.

This challenge will require you to execute the /challenge/run program from a specific path (which it will tell you). You'll need to cd to that directory before rerunning the challenge program. Good luck!
### Solve
*Flag:* `pwn.college{EltRbkdL-GTm-iW1nylqPF2oPl8.QX4QTN0wiN1gjNzEzW}`

```
hacker@paths~position-yet-elsewhere:~$ /challenge/run
Incorrect...
You are not currently in the /proc/131 directory.
Please use the `cd` utility to change directory appropriately.
hacker@paths~position-yet-elsewhere:~$ cd /proc/131
hacker@paths~position-yet-elsewhere:/proc/131$ /challenge/run
Correct!!!
/challenge/run is an absolute path, invoked from the right directory!
Here is your flag:
pwn.college{EltRbkdL-GTm-iW1nylqPF2oPl8.QX4QTN0wiN1gjNzEzW}
hacker@paths~position-yet-elsewhere:/proc/131$

```
This program too involve fiinding and changing the current working directory to the one where the file to be executed is at using cd followed by its exection
### New Learnings
I gained more clarity and can now easily use cd to change to any directory

## Implicit Relative Paths, from /

Now you're familiar with the concept of referring to absolute paths and changing directories. If you put in absolute paths everywhere, then it really doesn't matter what directory you are in, as you likely found out in the previous three challenges.

However, the current working directory does matter for relative paths.

A relative path is any path that does not start at root (i.e., it does not start with /).
A relative path is interpreted relative to your current working directory (cwd).
Your cwd is the directory that your prompt is currently located at.
This means how you specify a particular file, depends on where the terminal prompt is located.

Imagine we want to access some file located at /tmp/a/b/my_file.

If my cwd is /, then a relative path to the file is tmp/a/b/my_file.
If my cwd is /tmp, then a relative path to the file is a/b/my_file.
If my cwd is /tmp/a/b/c, then a relative path to the file is ../my_file. The .. refers to the parent directory.
Let's try it here! You'll need to run /challenge/run using a relative path while having a current working directory of /. For this level, I'll give you a hint. Your relative path starts with the letter c 😊

### Solve
*Flag:* ` pwn.college{c01AmqItlqWFDnkjBfeZAmV-s_h.QX5QTN0wiN1gjNzEzW} `

```
hacker@paths~implicit-relative-paths-from-:~$ cd /
hacker@paths~implicit-relative-paths-from-:/$ challenge/run
Correct!!!
challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{c01AmqItlqWFDnkjBfeZAmV-s_h.QX5QTN0wiN1gjNzEzW}
hacker@paths~implicit-relative-paths-from-:/$

```
First the current working directory had to be changed to root(/) and since relative paths don't start from root, only challenge/run had to executed since cwd was already root.
### New Learnings
I learnt about relative paths and how to execute them . 



## Explicit Relative Paths, from /
Previously, your relative path was "naked": it directly specified the directory to descend into from the current directory. In this level, we're going to explore more explicit relative paths.

In most operating systems, including Linux, every directory has two implicit entries that you can reference in paths: . and ... The first, ., refers right to the same directory, so the following absolute paths are all identical to each other:

/challenge
/challenge/.
/challenge/./././././././././
/./././challenge/././
The following relative paths are also all identical to each other:

challenge
./challenge
./././challenge
challenge/.
Of course, if your current working directory is /, the above relative paths are equivalent to the above absolute paths.

This challenge will get you using . in your relative paths. Get ready!

### Solve
*Flag:* `pwn.college{k8EtSJu82iXhtx1ClB9bBI0vB7P.QXwUTN0wiN1gjNzEzW}`

```
hacker@paths~explicit-relative-paths-from-:~$ cd /
hacker@paths~explicit-relative-paths-from-:/$ ./challenge/run
Correct!!!
./challenge/run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{k8EtSJu82iXhtx1ClB9bBI0vB7P.QXwUTN0wiN1gjNzEzW}

```
./ , / and /././ before file name are all identical and refer to the same file.

### New Learnings
In this program, I learnt about explicit paths and the application of '.' which refers to the same directory.



## Implicit Relative Path
In this level, we'll practice referring to paths using . a bit more. This challenge will need you to run it from the /challenge directory. Here, things get slightly tricky.

Linux explicitly avoids automatically looking in the current directory when you provide a "naked" path. Consider the following:
```
hacker@dojo:~$ cd /challenge
hacker@dojo:/challenge$ run
```
This will not invoke /challenge/run. This is actually a safety measure: if Linux searched the current directory for programs every time you entered a naked path, you could accidentally execute programs in your current directory that happened to have the same names as core system utilities! As a result, the above commands will yield the following error:
```
bash: run: command not found
```
We'll explore the mechanisms behind this concept later, but in this challenge, we'll learn how to explicitly use relative paths to launch run in this scenario. The way to do this is to tell Linux that you explicitly want to execute a program in the current directory, using . like in the previous levels. Give it a try now!

### Solve
*Flag:* `pwn.college{UigKinOIoccwvyNgZwq9VPKWxHJ.QXxUTN0wiN1gjNzEzW}`

```
hacker@paths~implicit-relative-path:~$ cd /challenge
hacker@paths~implicit-relative-path:/challenge$ ./run
Correct!!!
./run is a relative path, invoked from the right directory!
Here is your flag:
pwn.college{UigKinOIoccwvyNgZwq9VPKWxHJ.QXxUTN0wiN1gjNzEzW}

```
To explicitly use relative paths the file had to be executed with '.' at the start after changing the directory.
### New Learnings
I learnt more about the application of explicit paths and executing programs using it .





