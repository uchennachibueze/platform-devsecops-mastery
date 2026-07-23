# Week 0 Baseline Review

Assessment date: 2026-07-23  
Assessed by: Codex evidence-based review  
Outcome: Baseline accepted

## Purpose

This review records the learner's starting point before instruction. The submitted answers and Bash script are evaluated as unassisted baseline evidence, not as production-ready deliverables.

Incorrect, incomplete, or untested work is useful evidence at this stage because it identifies what should be taught and reassessed later. The original assessment answers and script should remain preserved so future work can demonstrate measurable improvement.

## Evidence reviewed

- [Initial written assessment](initial-assessment.md)
- [Baseline Bash attempt](../../labs/linux-system-baseline/system_baseline.sh)
- [Week 0 engineering journal](../../engineering-journal/week-00-baseline.md)
- [Program roadmap](../../ROADMAP.md)
- Repository branch, commit, and pull-request workflow

## Completion judgment

| Requirement | Result | Notes |
|---|---|---|
| Public repository established | Completed | Repository, README, Python `.gitignore`, and MIT licence are present |
| Branch and pull-request workflow used | Completed | Work was submitted through PR #2 |
| Thirty baseline questions answered | Completed | Honest uncertainty and “I do not know” responses were accepted |
| Practical Bash baseline attempted | Completed | The attempt provides evidence of current command and scripting knowledge |
| Engineering journal completed | Completed | Reflection identifies uncertainty and lack of recent Bash practice |
| Roadmap created | Completed | Program stages, modules, deliverables, and mastery requirements are documented |
| Initial structure created | Completed | Assessment, journal, lab, project, and architecture locations are represented |
| Functional diagnostic script | Not assessed as a Week 0 completion gate | Functionality becomes a Week 1 learning and reassessment target |
| Testing and failure investigation | Not demonstrated | No execution or investigation evidence was submitted |
| Technical lab documentation | Not demonstrated | The lab README is empty |

## Overall assessment

**Week 0 baseline status: Accepted**  
**Overall provisional mastery level: 1 — Familiar**

The assessment shows broad exposure across DevOps topics, but the current mental models are uneven and sometimes inaccurate. The central development need is not exposure to more tools. It is systematic reconstruction of foundational understanding followed by independent implementation and troubleshooting.

## Strengths

### Honest self-assessment

The learner did not hide gaps or inflate answers. This substantially improves the usefulness of the baseline and supports an adaptive curriculum.

### Operational instincts

The connectivity answer shows an instinct to begin with reachability, then inspect firewall and server configuration. The 502 answer correctly recognizes backend unavailability as a possible cause.

### Terraform and identity foundations

The Terraform-state answer recognizes state as essential infrastructure-management data that must be protected. The distinction between authentication and authorization is directionally correct.

### Python environment awareness

The virtual-environment answer correctly identifies dependency isolation and version-conflict prevention as central purposes.

### Security mindset

The answer about delivery-pipeline controls correctly places security throughout the lifecycle rather than at one isolated stage.

### Professional workflow exposure

The learner successfully created a repository, used a feature branch, committed changes, pushed the branch, and opened a pull request.

## Gaps identified

### Linux and Bash

- Processes and threads are confused.
- Shell command execution is understood only at a high level.
- File descriptors are not understood.
- `SIGTERM` and `SIGKILL` need a more accurate behavioral model.
- High-CPU investigation is limited to opening `top`.
- The Bash attempt does not yet demonstrate valid interpreter selection, non-interactive command use, structured output, comments, failure handling, or testing.

### Networking

- The browser request lifecycle was not explained.
- DNS is treated mainly as a catalogue rather than a distributed resolution system.
- TCP and TLS terminology is inaccurate.
- NAT is confused with domain-name mapping.
- Ping reachability is treated as stronger evidence than it actually provides.

### Git

- Branches are incorrectly modeled as folders.
- Tags and commits are not explained accurately.
- Detached HEAD is confused with commit ancestry.
- Fetch and pull behavior is reversed or unclear.
- Refspecs are not understood.
- Lost-commit recovery does not yet include reflog-based investigation.

### Python

- Lists and tuples are partly understood.
- Sets and dictionaries are modeled incorrectly.
- Exceptions and error return values are not distinguished conceptually.
- Predicate-based filtering is only partly explained.
- Test-case design is not yet demonstrated.

### Containers and Kubernetes

- Container portability is overstated and the shared-kernel model is missing.
- Namespaces and control groups are unknown.
- Services are incorrectly described as collections of Deployments.
- `kubectl apply` is treated as a forced overwrite instead of declarative reconciliation.
- CrashLoopBackOff is confused with image retrieval failure.

### Terraform, cloud, and security

- Terraform-state understanding is promising but does not yet cover sensitive values, locking, drift, or recovery.
- Least privilege is recognized but not defined precisely.
- SBOM knowledge is minimal.
- Security-throughout-the-pipeline is recognized but no specific controls are mapped to stages.

## Assessment limitations

The baseline did not include:

- A completed independent implementation
- Execution evidence
- An unseen troubleshooting challenge
- Security or reliability adaptation
- A code-review response
- A retention check

Because these areas were not assessed, no domain can yet receive Level 3 — Demonstrated or higher. Numeric scores are withheld rather than treating missing assessment categories as failures.

## Required learning response

Week 1 should begin with Linux and Bash foundations:

1. What happens when a shell executes a command
2. Processes, threads, process IDs, and parent processes
3. Exit codes
4. Signals and process termination
5. File descriptors and standard streams
6. Basic Bash structure
7. Non-interactive system-inspection commands
8. Error handling and observation of failures

After guided experiments, the learner should create an improved system-diagnostics script in a separate branch and pull request. The new implementation should be compared with the preserved baseline attempt.

## Reassessment conditions

Linux and Bash may advance beyond Level 1 when the learner can:

- Explain the relevant concepts accurately in their own words
- Build the diagnostic script independently after instruction
- Run and test it
- Diagnose at least one deliberately introduced failure
- Document its behavior and limitations
- Complete a later retention check

## Final decision

The Week 0 submission is accepted as an honest baseline. Its incomplete elements are recorded as learning evidence rather than treated as reasons to reject the assessment. PR #2 may be merged as the preserved starting point, after which Week 1 should proceed in a separate branch.
