# Lesson 1 — How the Linux Shell Executes a Command

**Week:** 1  
**Module:** Linux processes, shell execution, and Bash foundations  
**Target time:** 60–90 minutes  
**Environment:** Linux or WSL (Ubuntu recommended)  
**Status:** In progress

## How to use this lesson

This file is the permanent lesson reference. In chat, we will work through only one numbered step at a time.

Ask questions whenever something is unclear. You can use these messages at any point:

- `Where are we?` — restate the current lesson and step
- `Resume` — repeat only the next action
- `Recap` — summarize what has been covered
- `Pause here` — create a stopping checkpoint
- `Explain more simply` — restart the current concept with less assumed knowledge
- `I am done with this step` — review the evidence and continue

Questions do not move the lesson forward automatically. After answering a question, Codex will identify the exact place to resume.

## Learning outcomes

By the end of this lesson, you should be able to:

1. Distinguish a terminal from a shell.
2. Identify the configured shell and the current shell process.
3. Explain how Bash resolves a command name.
4. Explain the role of the `PATH` environment variable.
5. Inspect a command's exit status.
6. Identify a simple parent-and-child process relationship.
7. Explain the difference between creating a process and loading a program into it.

## Safety and scope

The commands in this lesson do not require `sudo`. They inspect your own environment and briefly start a `sleep` process that you later stop.

Do not run the full page at once. Work through one step, understand it, and record your observations before continuing.

## Video and reference material

### Recommended video and notes

[MIT Missing Semester 2026 — Course Overview and Introduction to the Shell](https://missing.csail.mit.edu/2026/course-shell/)

The page contains the official lecture recording and notes. For this lesson, concentrate on:

- What a shell is
- Commands and arguments
- Builtin commands
- How `PATH` is used to locate programs
- Exit statuses

Pause before the advanced pipelines if the material begins moving faster than your current lesson.

### Optional primary reference

[GNU Bash Manual — Shell Operation](https://www.gnu.org/software/bash/manual/html_node/Shell-Operation.html)

The manual is a reference, not required reading from beginning to end.

## Core mental model

A **terminal** is the interface through which you type and see text. A **shell**, such as Bash, is the program that reads and interprets the commands typed into that terminal.

When you enter a command such as:

```bash
ls -la /tmp
```

Bash roughly performs these operations:

1. Reads the command line.
2. Parses it into a command name and arguments.
3. Performs expansions, including variables and wildcards.
4. Determines whether the command is an alias, function, builtin, or external executable.
5. For an external executable, searches the directories listed in `PATH`.
6. Creates a child process and loads the selected program into it.
7. Normally waits for the foreground command to finish.
8. Receives the command's exit status.
9. Displays another prompt.

On Linux, process creation and program loading are commonly described using two operations:

- `fork` creates a new process based on the calling process.
- `exec` replaces the program running inside a process with another program.

The child created by the shell can load `ls`; the interactive parent shell remains available after `ls` finishes.

# Step 1 of 5 — Identify the shell

## Command 1

Run this command by itself:

```bash
printf '%s\n' "$SHELL"
```

### What each part means

- `printf` prints formatted text.
- `'%s\n'` is the format: `%s` is a string and `\n` adds a newline.
- `$SHELL` asks Bash to expand the `SHELL` environment variable.
- The double quotes keep the expanded value together as one argument.

Typical output:

```text
/bin/bash
```

`SHELL` usually identifies your configured login shell. It is useful, but it does not always prove which shell process is currently interpreting the command. The next command inspects the current process.

## Command 2

```bash
ps -p "$$" -o pid,ppid,comm,args
```

### What each part means

- `ps` displays process information.
- `$$` is Bash's special value for the current shell process ID.
- `-p "$$"` asks `ps` to display that process.
- `-o` selects the output columns.
- `pid` is the process ID.
- `ppid` is the parent process ID.
- `comm` is the short command name.
- `args` is the full command and its arguments.

Example:

```text
PID    PPID  COMMAND  COMMAND
2417   2416  bash     -bash
```

Record the exact output and explain what you believe the PID and PPID represent.

**Chat checkpoint:** Stop here and share your output before continuing to Step 2.

# Step 2 of 5 — Compare command types

Run these one at a time:

```bash
type cd
type ls
type echo
type -a echo
command -V pwd
```

The output may identify commands as shell builtins, aliases, functions, or external executable files.

Record:

- The type reported for each command
- Anything unexpected
- Why you think `cd` needs to run inside the current shell

# Step 3 of 5 — Examine command lookup

Run:

```bash
printf '%s\n' "$PATH" | tr ':' '\n'
command -v ls
command -v python
```

`PATH` is a colon-separated list of directories. When Bash needs an external program, it searches those directories in order.

Record:

- The first three directories in your `PATH`
- The executable selected for `ls`
- What happened when looking for `python`
- What you think would happen if two `PATH` directories contained the same command name

# Step 4 of 5 — Examine exit statuses

Run each pair separately. Inspect `$?` immediately after the command being tested.

```bash
true
echo "$?"
```

```bash
false
echo "$?"
```

```bash
ls /a-path-that-does-not-exist
echo "$?"
```

```bash
bash -c 'exit 17'
echo "$?"
```

Conventionally, zero means success and a nonzero value indicates another outcome. The exact meaning of a nonzero value depends on the program.

Record every result and explain why `$?` must be inspected before running another unrelated command.

# Step 5 of 5 — Observe a child process

Start a background process:

```bash
sleep 60 &
```

Save its process ID:

```bash
child_pid=$!
printf 'Child PID: %s\n' "$child_pid"
```

Inspect it:

```bash
ps -o pid,ppid,stat,comm,args -p "$child_pid"
```

Stop it and ask the shell to collect its result:

```bash
kill "$child_pid"
wait "$child_pid"
echo "$?"
```

Record:

- The value stored in `$!`
- The PID and PPID of `sleep`
- Whether the shell appears to be the parent
- The final exit status
- What you believe `wait` did

## Lab record

Create:

```text
labs/linux-processes-and-shell/day-01-command-execution.md
```

Use these sections:

```markdown
# Day 1 — Shell Command Execution

## Environment

## Terminal versus shell

## Step 1 — Shell process observations

## Step 2 — Command-type observations

## Step 3 — PATH observations

## Step 4 — Exit-status observations

## Step 5 — Parent and child process observations

## Predictions that were incorrect

## What I understand now

## What remains unclear

## Knowledge check

## Time spent
```

## Knowledge check

Answer without searching. Use your own words.

1. What is the difference between a terminal and a shell?
2. Why can an external program not permanently change its parent shell's working directory?
3. What is the difference between `fork` and `exec`?
4. What does `PATH` control?
5. Why must `$?` be inspected immediately?
6. What relationship did you observe between Bash and the background `sleep` process?

## Completion evidence

This lesson is complete when:

- All five guided steps have been performed.
- Observations are recorded in the lab file.
- The knowledge check is answered in the learner's own words.
- Unclear concepts are listed rather than hidden.
- The lab is committed and pushed to the Week 1 branch.

Suggested commit message:

```text
docs: complete shell command execution lab
```

## Next lesson

Lesson 2 will examine processes and threads more deeply, including process states, parent-child relationships, and the `/proc` filesystem.
