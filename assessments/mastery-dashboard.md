# Mastery Dashboard

Last assessed: 2026-07-23  
Assessed by: Codex evidence-based review  
Assessment type: Unassisted Week 0 baseline

## Mastery scale

| Level | Meaning |
|---:|---|
| 0 — Not assessed | No evidence has been reviewed |
| 1 — Familiar | Recognizes the concept but cannot yet explain or apply it reliably |
| 2 — Developing | Can complete some guided work but still needs help |
| 3 — Demonstrated | Can explain and apply the skill independently in a familiar situation |
| 4 — Proficient | Can troubleshoot, secure, and adapt the skill in unfamiliar situations |
| 5 — Mastered | Can design with it, defend trade-offs, teach it, and solve unseen problems |

## Current dashboard

| Domain | Level | Assessment status | Primary evidence | Required next evidence |
|---|---:|---|---|---|
| Linux and Bash | 1 — Familiar | Baseline assessed | Written answers and Bash attempt | Guided labs, independent script, and troubleshooting exercise |
| Networking | 1 — Familiar | Baseline assessed | Written answers | Packet investigation and unseen connectivity scenario |
| Git | 1 — Familiar | Baseline assessed | Written answers and PR workflow | Git-internals lab and recovery challenge |
| Python | 1 — Familiar | Baseline assessed | Written answers | Tested Python implementation completed independently |
| Containers and Kubernetes | 1 — Familiar | Baseline assessed | Written answers | Container-isolation lab and Kubernetes troubleshooting challenge |
| Terraform, cloud, and security | 2 — Developing | Baseline assessed | Written answers and prior conceptual familiarity | Secure infrastructure implementation and threat-based review |

**Overall provisional level: 1 — Familiar**

The overall level is not an average of self-reported confidence. It reflects the strongest level consistently supported by the reviewed evidence.

## Why numeric scores are not assigned yet

The mastery rubric includes independent implementation, unseen troubleshooting, security and reliability analysis, code or configuration quality, documentation, and retention. Week 0 did not assess all of those areas. Assigning a score out of 100 now would incorrectly treat unassessed areas as failures.

Numeric scores will begin when a module includes enough evidence to apply the full rubric fairly.

## Domain findings

### Linux and Bash — Level 1: Familiar

**Demonstrated:**

- Recognizes commands associated with host, process, and network inspection.
- Knows that `top` can be used when investigating CPU usage.
- Recognizes a basic script as a sequence of commands.

**Not yet demonstrated:**

- Accurate process-versus-thread model
- Shell command-execution lifecycle
- File descriptors
- Reliable signal semantics
- Non-interactive system inspection
- Bash structure, comments, failure handling, and testing

**Next assessment:** Week 1 Linux and Bash practical work.

### Networking — Level 1: Familiar

**Demonstrated:**

- Recognizes DNS, TCP, TLS, HTTP, firewalls, and gateway failures.
- Shows useful instinct to test connectivity and inspect firewall configuration.
- Identifies an unavailable backend as a possible source of a 502 response.

**Not yet demonstrated:**

- Complete browser request lifecycle
- Accurate NAT model
- Accurate TCP and TLS terminology
- Layered DNS, transport, TLS, and HTTP diagnosis
- Evidence-driven port and service testing

**Next assessment:** Networking foundations and packet-analysis module.

### Git — Level 1: Familiar

**Demonstrated:**

- Can use branches, commits, pushes, and pull requests operationally.
- Recognizes fetch, pull, tags, commits, and reset as Git concepts.

**Not yet demonstrated:**

- Accurate branch and tag model
- Detached HEAD
- Refspecs
- Fetch-versus-pull behaviour
- Lost-commit recovery using references and reflog

**Next assessment:** Git objects and references laboratory.

### Python — Level 1: Familiar

**Demonstrated:**

- Understands the purpose of a Python virtual environment.
- Recognizes a function, parameters, list comprehension, and predicate-based filtering.
- Knows that lists and tuples differ in mutability.

**Not yet demonstrated:**

- Accurate set and dictionary models
- Exception-versus-return-value trade-offs
- Test-case design
- Independent Python implementation

**Next assessment:** Python foundations and testing exercises.

### Containers and Kubernetes — Level 1: Familiar

**Demonstrated:**

- Recognizes Pods, Deployments, Services, images, and `kubectl apply`.
- Knows that Pods are a fundamental Kubernetes workload unit.

**Not yet demonstrated:**

- Container-versus-VM isolation model
- Namespaces and control groups
- Accurate Pod, Deployment, and Service relationships
- Declarative reconciliation
- CrashLoopBackOff diagnosis

**Next assessment:** Container internals and Kubernetes foundations modules.

### Terraform, cloud, and security — Level 2: Developing

**Demonstrated:**

- Understands that Terraform state maps configuration to managed infrastructure and must be protected.
- Distinguishes authentication from authorization at a basic level.
- Recognizes that security controls should span the delivery lifecycle.
- Shows awareness of least privilege and bills of materials.

**Not yet demonstrated:**

- Sensitive-data risks inside state
- Precise least-privilege application
- SBOM purpose and use
- Independent security-control implementation
- Threat modelling and supply-chain assurance

**Next assessment:** Terraform, cloud, and DevSecOps modules, with smaller security checks integrated earlier.

## Promotion rules

A level increases only when reviewed evidence supports it. Confidence, tutorial completion, or a working final command alone will not raise a level.

To reach Level 3 or above, the evidence must include independent implementation and explanation. Level 4 additionally requires unfamiliar troubleshooting, security, and adaptation. Level 5 requires design judgment, trade-off defence, teaching ability, and later retention.

## Reassessment schedule

- Linux and Bash: Week 1
- Git fundamentals: During the first foundation module
- Python fundamentals: During the first foundation module
- Networking: Networking module
- Containers and Kubernetes: Containers and Kubernetes module
- Terraform, cloud, and security: DevSecOps module, with ongoing evidence collected throughout the program
