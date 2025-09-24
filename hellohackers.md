 # Hello Hackers
  ## Intro To Commands
  In this challenge, you will invoke your first command! When you type a command and hit enter, the command will be invoked, as so:  
  ```Ṅ
  hacker@dojo:~$ whoami  
hacker  
hacker@dojo:~$  Ṅ
```
Here, the user executed the whoami command, which simply prints the username (hacker) to the terminal. When the command terminates, the shell once again displays the prompt, ready for the next command.  

In this level, invoke the hello command to get the flag! Keep in mind: commands in Linux are case sensitive: hello is different from HELLO.  
  ### Solve
**Flag:** `pwn.college{0rs90QJ_h-Ze14KwK2J--ejb4wd.QX3YjM1wiN1gjNzEzW}`
```
hacker@hello~intro-to-commands:~$ hello
Success! Here is your flag:
pwn.college{0rs90QJ_h-Ze14KwK2J--ejb4wd.QX3YjM1wiN1gjNzEzW}
hacker@hello~intro-to-commands:~$ whoami
hacker
```

### New learnings
In this challenge, I learnt how to connect the terminal to pwn.college using SSH key and solve challenges using the terminal, also learnt about the execution of some basic commands.


## Intro to Arguments
Let's try something more complicated: a command with arguments, which is what we call additional data passed to the command. 
When you type a line of text and hit enter, the shell actually parses your input into a command and its arguments. The first word is the command, and the subsequent words are arguments. Observe:
```
hacker@dojo:~$ echo Hello
Hello
hacker@dojo:~$
```
In this case, the command was echo, and the argument was Hello. echo is a simple command that "echoes" all of its arguments back out onto the terminal, like you see in the session above.

Let's look at echo with multiple arguments:
```
hacker@dojo:~$ echo Hello Hackers!
Hello Hackers!
hacker@dojo:~$
```
In this case, the command was echo, and Hello and Hackers! were the two arguments to echo. Simple!

In this challenge, to get the flag, you must run the hello command (NOT the echo command) with a single argument of hackers. Try it now!
### Solve
**Flag:**  `pwn.college{Ik75K4ZH8uJWpgPvg-smqJ3XilQ.QX4YjM1wiN1gjNzEzW}`
```
hacker@hello~intro-to-arguments:~$ hello hackers
Success! Here is your flag:
pwn.college{Ik75K4ZH8uJWpgPvg-smqJ3XilQ.QX4YjM1wiN1gjNzEzW}
```
According to the description, command was hello and the argument was hackers thus the first word will be hello and second word will be hackers.

### New Learnings
In this challenge, I learnt about commands and arguments and how to execute them on terminal


## Command history
You're going to type a lot of commands, and typing everything from scratch can be annoying. Luckily, the shell saves a history of every command you invoke.
You can scroll through those saved commands with the up/down arrow keys, and we'll practice that in this challenge. This challenge will inject the flag into your history. 
Bring up a terminal, hit the up arrow, and grab it! In other challenges, the history will contain the log of the commands you've run, so if you need to run a similar 
command again, you can use the arrow keys to scroll through and find it!

### Solve
**Flag:**  `pwn.college{U6rCti6EY5-Q9Z1v6UJN_A7-Mpk.0lNzEzNxwiN1gjNzEzW}`
```
hacker@hello~command-history:~$ the flag is pwn.college{U6rCti6EY5-Q9Z1v6UJN_A7-Mpk.0lNzEzNxwiN1gjNzEzW}
```
According to the description, the arrow keys had to be used to execute previously executed commands without having to type them again,  thus the 'up' arrow key was used to find the flag.

### New Learnings
I learnt how to execute similar commands without having to type them again and thus save time in doing so.
