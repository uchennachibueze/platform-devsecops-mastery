# Program Week 1 — Linux Processes and Shell Foundations

**Original calendar period:** July 27–August 2, 2026
**Resumed:** August 5, 2026
**Completion target:** Flexible — continue until all Week 1 evidence is complete
**Target mode:** Full week, 11–14 hours
**Current status:** In progress

## Weekly outcome

Understand how a Linux shell executes commands and how Linux represents and manages processes well enough to:

* Explain the concepts accurately
* Perform guided system investigations
* Troubleshoot basic process-related issues
* Build an improved system-diagnostics script
* Document findings clearly in GitHub

This week builds the Linux foundation required for later work involving containers, Kubernetes, CI/CD agents, networking, monitoring, troubleshooting, and system security.

## Source-of-truth files

* [Lesson 1 — How the Linux Shell Executes a Command](../curriculum/week-01/lesson-01-shell-command-execution.md)
* [Current progress](../PROGRESS.md)
* [Mastery dashboard](../assessments/mastery-dashboard.md)
* [Week 0 baseline review](../assessments/baseline/week-00-review.md)
* [Original Bash baseline](../labs/linux-system-baseline/system_baseline.sh)

## Supporting learning resource

* [Linux Foundation LFS101 — Introduction to Linux](https://trainingportal.linuxfoundation.org/learn/course/introduction-to-linux-lfs101/)

LFS101 provides the structured learning material for the Linux portion of this program.

Relevant course topics may include:

* Linux philosophy and concepts
* Linux system startup
* Command-line operations
* Finding Linux documentation
* Processes
* File operations
* User environments
* Bash shell and scripting
* Networking
* Local security

Course completion alone does not demonstrate mastery. GitHub laboratories, independent implementations, troubleshooting exercises, explanations, documentation, and retention assessments remain the evidence used for mastery decisions.

Do not copy large sections of course material into the repository. Record concepts in your own words and document commands, observations, conclusions, and questions from your own environment.

## Interaction method

The repository contains the permanent program instructions. Chat is used for one-step-at-a-time coaching, explanation, review, and assessment.

During a lesson, use:

* `Where are we?` — Restate the current program location
* `Resume` — Repeat the immediate next action
* `Recap` — Summarize completed work and current understanding
* `Pause here` — Create a clear stopping checkpoint
* `Explain more simply` — Reduce assumed knowledge and explain from first principles
* `Explain more deeply` — Add technical detail and internals
* `I am done with this step` — Request review and advance to the next step
* `Review my work` — Request evidence-based feedback
* `Assess me` — Begin an independent knowledge or practical assessment

Instructional responses should identify:

* Program week
* Lesson
* Current step
* Immediate next action

Questions asked during a lesson do not automatically advance the lesson.

## Git workflow

Use the Week 1 branch:

```bash
git checkout main
git pull origin main
git checkout -b week-01/linux-processes-and-shell
```

If the branch already exists locally:

```bash
git checkout week-01/linux-processes-and-shell
git rebase main
```

Use meaningful commits throughout the week.

Example commit messages:

```text
docs: record shell identification observations
lab: investigate parent and child processes
lab: compare process termination signals
lab: explore standard streams and file descriptors
feat: improve Linux system baseline script
test: verify diagnostic script failure handling
docs: complete week 1 engineering journal
```

Push the branch regularly:

```bash
git push -u origin week-01/linux-processes-and-shell
```

Open a draft pull request when meaningful progress has been pushed. Do not merge the pull request until the Week 1 evidence has been reviewed.

## Required work

### Lesson 1 — Shell command execution

#### Learning objectives

* [ ] Distinguish a terminal from a shell
* [ ] Identify the configured login shell
* [ ] Identify the currently running shell process
* [ ] Explain how the shell reads and parses a command
* [ ] Compare aliases, functions, built-ins, and external commands
* [ ] Examine `PATH` command lookup
* [ ] Explain why some commands must be shell built-ins
* [ ] Experiment with exit statuses
* [ ] Observe a parent-and-child process relationship
* [ ] Complete the Lesson 1 knowledge check
* [ ] Commit the Lesson 1 lab record

#### Expected evidence

```text
labs/linux-processes-and-shell/
└── day-01-command-execution.md
```

The lab record should include:

* Commands executed
* Relevant output
* Observations
* Explanations in your own words
* Mistakes or unexpected results
* Questions that remain unclear

### Lesson 2 — Processes and threads

#### Learning objectives

* [ ] Explain the difference between a program and a process
* [ ] Explain process versus thread accurately
* [ ] Identify PID and PPID values
* [ ] Explain parent-and-child process relationships
* [ ] Examine foreground and background processes
* [ ] Use `ps`, `pstree`, `top`, or similar tools
* [ ] Examine common process states
* [ ] Investigate process information under `/proc`
* [ ] Explain what resources belong to a process
* [ ] Complete the process investigation lab
* [ ] Commit the Lesson 2 lab record

#### Expected evidence

```text
labs/linux-processes-and-shell/
└── day-02-processes-and-threads.md
```

### Lesson 3 — Signals and exit codes

#### Learning objectives

* [ ] Explain the purpose of Unix signals
* [ ] Explain the difference between `SIGTERM` and `SIGKILL`
* [ ] Send and observe signals safely
* [ ] Explain why `SIGTERM` should normally be attempted before `SIGKILL`
* [ ] Observe process termination
* [ ] Interpret successful and unsuccessful exit statuses
* [ ] Understand the importance of exit codes in CI/CD
* [ ] Investigate a process that does not terminate as expected
* [ ] Complete the signal laboratory
* [ ] Commit the Lesson 3 lab record

#### Expected evidence

```text
labs/linux-processes-and-shell/
└── day-03-signals-and-exit-codes.md
```

### Lesson 4 — File descriptors and standard streams

#### Learning objectives

* [ ] Explain what a file descriptor is
* [ ] Identify standard input, standard output, and standard error
* [ ] Explain file descriptors `0`, `1`, and `2`
* [ ] Redirect standard output
* [ ] Redirect standard error
* [ ] Redirect output and error separately
* [ ] Combine output and error when appropriate
* [ ] Use pipes between commands
* [ ] Inspect a process's open file descriptors
* [ ] Examine `/proc/<pid>/fd`
* [ ] Complete the file-descriptor laboratory
* [ ] Commit the Lesson 4 lab record

#### Expected evidence

```text
labs/linux-processes-and-shell/
└── day-04-file-descriptors.md
```

## Weekly implementation

Improve the original Week 0 Linux system-baseline script.

### Preparation

* [ ] Review the original Week 0 diagnostic attempt
* [ ] Identify weaknesses in the original script
* [ ] Write the improved script requirements before coding
* [ ] Decide how failures will be handled
* [ ] Decide how output will be structured

### Required diagnostic sections

The improved script should display:

* [ ] Operating-system information
* [ ] Hostname
* [ ] Current user
* [ ] System uptime
* [ ] CPU information
* [ ] Memory usage
* [ ] Disk usage
* [ ] Five processes using the most CPU
* [ ] Five processes using the most memory
* [ ] Listening network ports
* [ ] Current IP addresses

### Implementation requirements

* [ ] Use Bash
* [ ] Include a shebang
* [ ] Use clear comments
* [ ] Use readable headings
* [ ] Avoid interactive commands
* [ ] Quote variables appropriately
* [ ] Handle at least one possible command failure
* [ ] Return an intentional exit status
* [ ] Avoid exposing secrets or sensitive environment information
* [ ] Test the script on Linux or WSL
* [ ] Document supported environments
* [ ] Document known limitations
* [ ] Compare the result with the Week 0 baseline

### Expected evidence

```text
labs/linux-processes-and-shell/
└── improved-system-baseline/
    ├── README.md
    └── system_baseline.sh
```

## Suggested schedule

| Session            | Focus                                   |   Target time |
| ------------------ | --------------------------------------- | ------------: |
| Session 1          | Lesson 1 — Shell command execution      | 60–90 minutes |
| Session 2          | Lesson 2 — Processes and threads        |    90 minutes |
| Session 3          | Lesson 3 — Signals and exit codes       |    90 minutes |
| Session 4          | Lesson 4 — File descriptors and streams |    90 minutes |
| Supporting session | LFS101 study and review                 | 60–90 minutes |
| Saturday           | Improved system-diagnostics script      |     2–3 hours |
| Sunday             | Documentation, review, and assessment   | 60–90 minutes |

The calendar dates are flexible. Complete sessions in order even when work, school, or family responsibilities interrupt the original schedule.

## Flexible operating modes

### Full week — 11–14 hours

Complete:

* All four lessons
* All laboratories
* Relevant LFS101 material
* Improved diagnostic script
* Documentation
* Engineering journal
* Independent assessment
* Pull-request review

### Busy week — 6–8 hours

Complete:

* Lessons 1–3
* At least one complete practical lab
* Meaningful progress on the improved script
* Engineering journal update
* GitHub commits and branch push

### Survival week — 2–4 hours

Complete:

* Lesson 1
* One practical observation
* One meaningful Git commit
* A short journal update
* A revised completion plan

Unfinished work carries forward. The program week does not restart because of an interruption.

## Evidence expected

```text
curriculum/week-01/
└── lesson-01-shell-command-execution.md

weekly-plans/
└── program-week-01.md

labs/linux-processes-and-shell/
├── day-01-command-execution.md
├── day-02-processes-and-threads.md
├── day-03-signals-and-exit-codes.md
├── day-04-file-descriptors.md
└── improved-system-baseline/
    ├── README.md
    └── system_baseline.sh

engineering-journal/
└── week-01.md
```

Later lesson files may be added when their lessons begin. Do not create polished answers in advance.

## Engineering journal

Create:

```text
engineering-journal/week-01.md
```

Use this structure:

```markdown
# Week 1 — Linux Processes and Shell Foundations

## What I studied

## What I built

## Commands I used

## What I understood clearly

## What felt confusing

## What surprised me

## Problems I encountered

## How I investigated them

## Mistakes I made

## What I would explain differently now

## What remains unclear

## Evidence produced

## Time spent
```

Self-reflection helps guide future instruction but does not independently determine mastery.

## Assessment approach

Guided exercises support learning but do not independently prove mastery.

Program Week 1 assessment will consider:

* Conceptual explanations
* Accuracy of laboratory observations
* Independent implementation
* Testing behaviour
* Troubleshooting approach
* Security and reliability awareness
* Script quality
* Documentation and communication
* Ability to answer follow-up questions without being led
* Performance on an unfamiliar practical scenario

A later retention check is required before the topic can reach the highest mastery levels.

## Week 1 assessment areas

| Area                     | Evidence                                                                              |
| ------------------------ | ------------------------------------------------------------------------------------- |
| Conceptual understanding | Explanations of shells, processes, threads, signals, exit codes, and file descriptors |
| Practical implementation | Improved Bash system-baseline script                                                  |
| Troubleshooting          | Investigation of at least one unexpected process or command result                    |
| Security and reliability | Safe signal usage, defensive scripting, appropriate failure handling                  |
| Code quality             | Readability, quoting, structure, comments, exit handling                              |
| Documentation            | Lab records, README, journal, and pull-request description                            |
| Retention                | Later reassessment without preparation                                                |

## Promotion rules

Linux and Bash mastery will not increase merely because:

* A course chapter was completed
* A tutorial was followed
* A script produced output
* A checklist was marked complete
* Confidence increased

A higher level requires reviewed evidence.

Possible Week 1 outcomes include:

* **Level 1 — Familiar:** Concepts are recognized but not yet applied reliably
* **Level 2 — Developing:** Guided work can be completed with some support
* **Level 3 — Demonstrated:** Concepts can be explained and applied independently in familiar situations

Levels 4 and 5 require later unfamiliar troubleshooting, security adaptation, design judgment, and retention evidence.

## Pull-request requirements

The Week 1 pull request should contain:

* A clear title
* A concise summary of completed work
* Links to the main evidence files
* Testing performed
* Problems encountered
* Known limitations
* Questions or gaps requiring review

Suggested title:

```text
feat: complete week 1 Linux processes and shell foundations
```

Suggested description structure:

```markdown
## Summary

## Lessons completed

## Labs completed

## Implementation

## Testing performed

## Problems investigated

## Known limitations

## Evidence

## Questions for review
```

## Definition of completion

Program Week 1 is complete when:

* [ ] Required lessons and laboratories are completed
* [ ] Relevant LFS101 material has been studied
* [ ] The improved diagnostic script runs successfully
* [ ] The script is documented
* [ ] At least one command or process failure has been investigated
* [ ] The learner can explain the main concepts without relying heavily on notes
* [ ] The engineering journal has been completed
* [ ] Work has been submitted through a Week 1 pull request
* [ ] The evidence has been reviewed
* [ ] The mastery dashboard has been updated
* [ ] Any required reassessment has been recorded

## Current checkpoint

**Program week:** 1
**Lesson:** Lesson 1 — How the Linux Shell Executes a Command
**Step:** Step 1 of 5 — Identify the shell
**Status:** Ready to resume
**Next action:** Open `curriculum/week-01/lesson-01-shell-command-execution.md`, run the first command under Step 1, and share the command and output in chat.
