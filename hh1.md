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
