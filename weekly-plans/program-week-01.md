# Program Week 1 — Linux Processes and Shell Foundations

**Calendar period:** July 27–August 2, 2026 (ISO calendar week 31)  
**Early start:** July 24–26, if available  
**Target mode:** Full week, 11–14 hours  
**Current status:** In progress

## Weekly outcome

Understand how a Linux shell executes commands and how Linux represents and manages processes well enough to explain the concepts, perform guided investigations, and build an improved system-diagnostics script.

## Source-of-truth files

- [Lesson 1 — How the Linux Shell Executes a Command](../curriculum/week-01/lesson-01-shell-command-execution.md)
- [Current progress](../PROGRESS.md)
- [Mastery dashboard](../assessments/mastery-dashboard.md)
- [Week 0 baseline review](../assessments/baseline/week-00-review.md)
- [Original Bash baseline](../labs/linux-system-baseline/system_baseline.sh)

## Interaction method

The repository contains the complete permanent instructions. Chat is used for one-step-at-a-time coaching.

During a lesson, use:

- `Where are we?` to restate the current location
- `Resume` to repeat the next action
- `Recap` for a summary
- `Pause here` to create a stopping checkpoint
- `Explain more simply` to reduce assumed knowledge
- `I am done with this step` to request review and advance

Codex will label instructional responses with the program week, lesson, and step. Questions do not automatically advance the lesson.

## Required work

### Lesson 1 — Shell command execution

- [ ] Distinguish terminal from shell
- [ ] Identify the configured shell
- [ ] Inspect the current shell process
- [ ] Compare aliases, functions, builtins, and external commands
- [ ] Examine `PATH` command lookup
- [ ] Experiment with exit statuses
- [ ] Observe a parent-and-child process relationship
- [ ] Complete the Lesson 1 knowledge check
- [ ] Commit the Lesson 1 lab record

### Lesson 2 — Processes and threads

- [ ] Explain process versus thread accurately
- [ ] Inspect PID and PPID relationships
- [ ] Examine common process states
- [ ] Investigate process information under `/proc`
- [ ] Complete the process investigation lab

### Lesson 3 — Signals and exit codes

- [ ] Explain signal purpose
- [ ] Compare `SIGTERM` and `SIGKILL`
- [ ] Send and observe signals safely
- [ ] Interpret normal and signal-related exit statuses
- [ ] Complete the signal laboratory

### Lesson 4 — File descriptors and standard streams

- [ ] Explain file descriptors
- [ ] Identify standard input, output, and error
- [ ] Redirect output and error separately
- [ ] Inspect a process's open descriptors
- [ ] Complete the file-descriptor laboratory

### Weekly implementation

- [ ] Review the original Week 0 diagnostic attempt
- [ ] Design the improved script before coding
- [ ] Implement the required diagnostic sections
- [ ] Make commands non-interactive
- [ ] Add clear output headings
- [ ] Handle at least one command failure
- [ ] Test the script on Linux or WSL
- [ ] Document behavior and limitations
- [ ] Compare the implementation with the baseline attempt

## Suggested schedule

| Session | Focus | Target time |
|---|---|---:|
| Early start or Monday | Lesson 1: shell execution | 60–90 minutes |
| Tuesday | Lesson 2: processes and threads | 90 minutes |
| Wednesday | Lesson 3: signals and exit codes | 90 minutes |
| Thursday | Lesson 4: file descriptors and streams | 90 minutes |
| Friday | Rest, questions, or catch-up | Optional |
| Saturday | Improved system-diagnostics script | 2–3 hours |
| Sunday | Documentation, review, and assessment | 60–90 minutes |

## Flexible operating modes

### Full week — 11–14 hours

Complete all lessons, laboratories, implementation, documentation, and review.

### Busy week — 6–8 hours

Complete Lessons 1–3, one practical lab, and meaningful progress on the improved script.

### Survival week — 2–4 hours

Complete Lesson 1, record one practical observation, and update the journal with a revised plan.

Unfinished work carries forward. The week does not restart because of an interruption.

## Evidence expected

```text
curriculum/week-01/
└── lesson-01-shell-command-execution.md

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

Later lesson files will be added when their lessons begin. Do not create polished answers in advance.

## Assessment approach

Guided exercises support learning but do not independently prove mastery. The Program Week 1 assessment will consider:

- Concept explanations
- Accuracy of laboratory observations
- Independent implementation
- Testing behavior
- Troubleshooting approach
- Script quality
- Documentation and communication

A later retention check will be required before the topic can reach the highest mastery levels.

## Definition of completion

Program Week 1 is complete when:

- Required lessons and labs are completed.
- The improved diagnostic script runs and is documented.
- At least one failure has been investigated.
- The learner can explain the main concepts without relying heavily on notes.
- Work is submitted through a Program Week 1 pull request.
- Codex reviews the evidence and updates the mastery dashboard.

## Current checkpoint

**Program week:** 1  
**Lesson:** Lesson 1 — How the Linux Shell Executes a Command  
**Step:** Step 1 of 5 — Identify the shell  
**Next action:** Run the first command in Lesson 1 and share its output in chat.
