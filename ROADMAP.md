# Platform and DevSecOps Engineering Mastery Roadmap

## Purpose

This program will strengthen my foundations, deepen my practical engineering ability, and prepare me for DevOps, DevSecOps, cloud, and platform-engineering roles.

The program is evidence-based. Completing a tutorial or declaring confidence does not demonstrate mastery. Progress must be supported by working implementations, troubleshooting exercises, tests, documentation, and retention assessments.

## Target outcomes

By December 2026, I aim to:

- Strengthen Linux, networking, Git, and Python fundamentals.
- Build production-quality automation and applications.
- troubleshoot containers and Kubernetes systematically.
- Design secure CI/CD pipelines.
- Provision Azure infrastructure using Terraform.
- Publish several well-documented portfolio projects.
- Prepare for DevOps, DevSecOps, cloud, and platform-engineering interviews.

By December 2027, I aim to:

- Design secure and reliable delivery platforms.
- Apply distributed-systems and SRE principles.
- Build reusable developer-platform capabilities.
- Defend architecture and security trade-offs.
- Lead technical investigations and incident response.
- Operate at a strong senior platform/DevSecOps engineering level.

## Program principles

- Begin each module with a baseline assessment.
- Accelerate through subjects already demonstrated.
- Learn concepts through implementation.
- Include failure and troubleshooting exercises.
- Treat security, reliability, testing, and documentation as default requirements.
- Preserve assessment answers as historical evidence.
- Use pull requests for meaningful changes.
- Base mastery decisions on reviewed evidence.
- Prefer a few excellent portfolio projects over many incomplete repositories.

# Stage 0 — Baseline and program setup

**Target:** July–August 2026  
**Status:** In progress

## Objectives

- [x] Create the public program repository.
- [x] Establish a branch and pull-request workflow.
- [x] Complete the initial written baseline assessment.
- [x] Record the initial engineering journal entry.
- [ ] Complete and test the Linux system-baseline script.
- [ ] Complete the laboratory documentation.
- [ ] Create the initial mastery dashboard.
- [ ] Establish the weekly planning and review process.

## Exit criteria

Stage 0 is complete when:

- The Week 0 pull request satisfies all requirements.
- The diagnostic script runs successfully.
- The initial baseline has been reviewed.
- Every domain has a provisional mastery level.
- Week 1 has been designed from the assessment evidence.

# Stage 1 — Graduation and job-readiness runway

**Target:** August–December 2026

## Module 1 — Linux, Bash, Python, and Git foundations

**Target:** August 2026

### Topics

- Linux processes, threads, signals, and exit codes
- Shell execution and environment variables
- Files, permissions, and file descriptors
- CPU, memory, disk, and process troubleshooting
- Bash scripting and error handling
- Python data structures, functions, exceptions, and testing
- Python environments, packaging, logging, and CLI development
- Git objects, commits, branches, tags, references, and reflog

### Deliverables

- [ ] Tested Linux system-baseline script
- [ ] Python system-diagnostics CLI
- [ ] Git internals investigation laboratory
- [ ] Automated tests and CI workflow
- [ ] Troubleshooting documentation

### Milestone

Build and release a tested system-diagnostics toolkit that demonstrates Linux, Bash, Python, Git, testing, and documentation skills.

## Module 2 — Networking and web foundations

**Target:** September 2026

### Topics

- IP addressing and subnetting
- Routing, NAT, and firewalls
- TCP and UDP
- DNS resolution
- HTTP request and response behaviour
- TLS certificates and handshakes
- Reverse proxies and load balancers
- Network troubleshooting and packet capture

### Deliverables

- [ ] Small Python HTTP server
- [ ] Nginx reverse-proxy laboratory
- [ ] DNS troubleshooting scenario
- [ ] TLS and local certificate-authority laboratory
- [ ] Packet-capture investigation report
- [ ] 502 Bad Gateway troubleshooting exercise

### Milestone

Diagnose an unseen DNS, TCP, TLS, or HTTP failure and document the investigation from symptoms to prevention.

## Module 3 — Software engineering and CI/CD

**Target:** October 2026

### Topics

- FastAPI application design
- PostgreSQL and migrations
- Authentication and authorization
- Unit, integration, and API testing
- Logging and error handling
- Dependency and artifact management
- CI/CD design
- Secrets management
- Deployment safety and rollback

### Deliverables

- [ ] Production-style FastAPI service
- [ ] PostgreSQL integration
- [ ] Automated test suite
- [ ] Container image
- [ ] CI/CD workflow
- [ ] Security and quality checks
- [ ] Architecture documentation

### Milestone

Produce a versioned application artifact through a tested and secure delivery pipeline.

## Module 4 — Containers and Kubernetes

**Target:** November 2026

### Topics

- Linux namespaces and control groups
- Container images and layers
- Container networking and storage
- Rootless containers and image hardening
- Kubernetes control-plane components
- Pods, Deployments, Services, and Ingress
- Configuration, secrets, RBAC, and network policies
- Health probes, resources, storage, and Helm
- Kubernetes troubleshooting

### Deliverables

- [ ] Hardened application container
- [ ] Kubernetes deployment
- [ ] Helm chart
- [ ] TLS ingress
- [ ] RBAC and network policies
- [ ] Metrics and logging
- [ ] Kubernetes failure laboratories

### Milestone

Deploy the production API to Kubernetes and independently diagnose several deliberately broken workloads.

## Module 5 — Terraform, Azure, and DevSecOps

**Target:** December 2026

### Topics

- Terraform state, modules, locking, and drift
- Azure identity and networking
- Managed identities and Key Vault
- AKS architecture
- Threat modelling
- SAST, DAST, and dependency analysis
- Secret and container scanning
- SBOM generation
- Artifact signing and provenance
- Policy as code and least-privilege access

### Deliverables

- [ ] Modular Terraform infrastructure
- [ ] Azure deployment architecture
- [ ] Threat model
- [ ] SBOM and vulnerability reports
- [ ] Signed container artifact
- [ ] Policy-as-code controls
- [ ] Operational runbooks
- [ ] Graduation capstone demonstration

### Stage 1 capstone

Build a secure cloud delivery platform that moves an application through:

```text
Pull request
→ automated tests
→ code and dependency analysis
→ container build
→ SBOM generation
→ vulnerability scanning
→ artifact signing
→ registry publication
→ Terraform-provisioned Azure infrastructure
→ AKS deployment
→ monitoring and alerting
```

# Stage 2 — Senior platform-engineering depth

**Target:** January–June 2027

## Focus areas

- [ ] Distributed-systems fundamentals
- [ ] Queues, caching, retries, and idempotency
- [ ] Database reliability
- [ ] Metrics, logs, and distributed tracing
- [ ] Service-level objectives and error budgets
- [ ] Incident response and postmortems
- [ ] Capacity and performance testing
- [ ] Backup and disaster-recovery validation
- [ ] Internal developer-platform design
- [ ] Reusable infrastructure and pipeline templates

## Stage 2 capstone

Build a small internal developer platform providing application templates, standard pipelines, infrastructure modules, secure defaults, observability, policy enforcement, and developer documentation.

# Stage 3 — Advanced DevSecOps and architecture

**Target:** July–December 2027

## Focus areas

- [ ] Identity federation and workload identity
- [ ] PKI and certificate lifecycle management
- [ ] Secrets rotation
- [ ] Software-supply-chain security
- [ ] Runtime and Kubernetes security
- [ ] Cloud security monitoring
- [ ] Incident forensics
- [ ] Architecture decision records
- [ ] Cost and performance optimization
- [ ] Migration planning
- [ ] Technical leadership and mentoring

## Final capstone

Design and demonstrate a secure enterprise delivery platform containing:

- Architecture documentation
- Threat model
- Terraform modules
- Reusable CI/CD templates
- Kubernetes deployment framework
- Policy-as-code controls
- Supply-chain security
- Observability
- Disaster-recovery plan
- Cost analysis
- Incident runbooks
- Executive presentation
- Live technical demonstration

# Portfolio milestones

- [ ] System-diagnostics toolkit
- [ ] Engineering foundations laboratory
- [ ] Production API
- [ ] Secure cloud platform
- [ ] DevSecOps laboratory
- [ ] Incident and troubleshooting laboratory
- [ ] Internal developer platform
- [ ] Final enterprise-platform design

# Mastery requirements

A topic may be marked mastered only when I can:

1. Explain how and why it works.
2. Implement it independently.
3. Diagnose an unfamiliar broken scenario.
4. Identify its security and reliability risks.
5. Produce maintainable code or configuration.
6. Document and defend important decisions.
7. Pass a later retention assessment.

# Schedule flexibility

The program supports three weekly operating modes:

- **Full week — 11–14 hours:** Complete learning, laboratory, project, troubleshooting, and documentation work.
- **Busy week — 6–8 hours:** Complete the essential lesson, one practical exercise, and one meaningful project improvement.
- **Survival week — 2–4 hours:** Complete one review, one small practical task, and one documented progress update.

Missed work moves forward to the next available week. A disrupted week does not require restarting the program.

# Current position

- **Current stage:** Stage 0 — Baseline and program setup
- **Current task:** Complete the Week 0 practical diagnostic
- **Current pull request:** [Week 0 assessment](https://github.com/uchennachibueze/platform-devsecops-mastery/pull/2)
- **Next milestone:** Final Week 0 review and initial mastery dashboard