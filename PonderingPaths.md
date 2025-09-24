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


##
### Solve
*Flag:* ``

```
```

### New Learnings
