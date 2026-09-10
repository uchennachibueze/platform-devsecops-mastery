## Step 1 — Shell process observations
emmachi72@UC-DELL:~$ printf '%s\n' "$SHELL"
/bin/bash
emmachi72@UC-DELL:~$ ps -p "$$" -o pid,ppid,comm,args
    PID    PPID COMMAND         COMMAND
  32163   32158 bash            -bash
emmachi72@UC-DELL:~$

$SHELL represents the current shell 

PID represents process id

PPID represents the parent process id

comm shows the command

args shows the arguments

The parent of my shell is 32158

type is a command that gives information about a command

