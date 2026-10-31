<div align="center">

# 🧠 Idea Vault & Engineering Logbook

**A friction-free sanctuary designed to capture, organize, and incubate technical concepts, project blueprints, architectural decisions, and day-to-day sparks.**

<p align="center">
  <a href="#"><img src="https://img.shields.io/badge/status-active-success.svg?style=for-the-badge&logo=git&logoColor=white" alt="Status: Active" /></a>
  <a href="#"><img src="https://img.shields.io/badge/license-MIT-blue.svg?style=for-the-badge&logo=open-source-initiative&logoColor=white" alt="License: MIT" /></a>
  <a href="#"><img src="https://img.shields.io/badge/last%20commit-rolling-orange.svg?style=for-the-badge&logo=github&logoColor=white" alt="Last Commit" /></a>
  <a href="#"><img src="https://img.shields.io/badge/docs-structured-purple.svg?style=for-the-badge&logo=markdown&logoColor=white" alt="Documentation" /></a>
  <a href="#"><img src="https://img.shields.io/badge/taxonomy-RFC--spec-informational.svg?style=for-the-badge&logo=buffer&logoColor=white" alt="Taxonomy" /></a>
</p>

> *"Great systems begin as transient thoughts. Without disciplined structure and an immutable logbook, breakthroughs scatter to the wind."*

</div>

---

## 📑 Table of Contents

- [🎯 Vision & Purpose](#vision-purpose)
- [🗂️ Repository Structure](#repository-structure)
- [📚 Directory Taxonomy](#directory-taxonomy)
- [📐 Naming Conventions](#naming-conventions)
  - [General Rules](#general-rules)
  - [Format by Category](#format-by-category)
- [🏷️ Tagging & Metadata Rules](#tagging--metadata-rules)
  - [Frontmatter Specification](#frontmatter-specification)
  - [Status Vocabulary](#status-vocabulary)
- [🌱 Idea Lifecycle Workflow](#idea-lifecycle-workflow)
  - [Stage 1: Seed (Inception)](#stage-1-seed-inception)
  - [Stage 2: Sprout (Exploration & Spike)](#stage-2-sprout-exploration--spike)
  - [Stage 3: Sapling (RFC & Architecture)](#stage-3-sapling-rfc--architecture)
  - [Stage 4: Tree (Execution & Shipping)](#stage-4-tree-execution--shipping)
  - [Stage 5: Evergreen / Compost (Archive & Post-Mortem)](#stage-5-evergreen--compost-archive--post-mortem)
- [📝 Ready-to-Use Note Templates](#ready-to-use-note-templates)
  - [Template 1: Project Idea RFC](#template-1-project-idea-rfc)
  - [Template 2: Quick Thought / Brainstorm](#template-2-quick-thought--brainstorm)
  - [Template 3: Architectural Decision Record (ADR)](#template-3-architectural-decision-record-adr)
  - [Template 4: Execution Plan & Checklist](#template-4-execution-plan--checklist)
- [🚀 Demo Plan: Idea to Production](#demo-plan-idea-to-production)
  - [The Concept: LogPulse Telemetry Daemon](#the-concept-logpulse-telemetry-daemon)
  - [Step-by-Step Vault Walkthrough](#step-by-step-vault-walkthrough)
  - [Sample Execution Milestone Checklist](#sample-execution-milestone-checklist)
- [🔮 Next Steps & Future Enhancements](#next-steps--future-enhancements)
- [💡 Repository Hygiene & Best Practices](#repository-hygiene--best-practices)

---

<a id="vision-purpose"></a>
## 🎯 Vision & Purpose

Great systems begin as transient thoughts. Without deliberate structure, notes scatter across scrapbooks, sticky notes, and lost branches. This repository acts as an immutable external memory and structured incubation chamber:

1. **Capture early:** Zero-friction logging of raw thoughts and developer brainstorms.
2. **Refine systematically:** Graduating raw ideas into formal specifications, Architectural Decision Records (ADRs), and execution plans.
3. **Track lifecycle:** Clear status states (`draft`, `in-review`, `accepted`, `in-progress`, `archived`) to see what is actionable at a glance.

---

<a id="repository-structure"></a>
## 🗂️ Repository Structure

```text
idea-vault/
├── README.md                     # Central guide, taxonomy index, and handbook
├── projects/                      # Product specs, RFCs, and full-scale build proposals
│   ├── active/                   # Initiatives currently under active development
│   ├── proposals/                # Polished project proposals awaiting greenlight
│   └── archive/                  # Completed or decommissioned projects
├── dev-ideas/                     # Technical investigations, POC ideas, and tool explorations
├── thoughts/                      # Ephemeral sparks, reading notes, and quick reflections
├── decisions/                     # Architectural Decision Records (ADR format)
├── workflows/                     # Automated recipes, developer setup flows, and CI/CD habits
├── plans/                         # Concrete sprint roadmaps, step-by-step milestones, and checklists
└── templates/                     # Standardized document templates for fast scaffolding
    ├── project-rfc.md
    ├── quick-thought.md
    └── decision-record.md
```

---

<a id="directory-taxonomy"></a>
## 📚 Directory Taxonomy

| Directory | Purpose | Graduation Trigger |
| :--- | :--- | :--- |
| `projects/` | In-depth engineering proposals, system architectures, and product blueprints. | Moves to `active/` once work begins, or `archive/` when finished. |
| `dev-ideas/` | Technical experiments, CLI tools, libraries, or spike investigations. | Promoted to `projects/proposals/` once validated. |
| `thoughts/` | Stream-of-consciousness observations, tech stack critiques, and raw bookmarks. | Extracted into `dev-ideas/` or `decisions/` if viable. |
| `decisions/` | Context, trade-offs, and final consensus using the ADR format. | Remains permanent as an architectural record. |
| `workflows/` | Repeatable procedures, scripts, deployment recipes, and environment setups. | Maintained alongside tooling changes. |
| `plans/` | Time-boxed roadmaps, task breakdowns, release checklists, and execution logs. | Closed or archived upon completion. |
| `templates/` | Clean markdown boilerplates to initialize documents rapidly. | Updated as standards evolve. |

---

<a id="naming-conventions"></a>
## 📐 Naming Conventions

Standardized file naming guarantees natural alphabetical sorting, easy fuzzy-find search (`Ctrl+P` / `Cmd+P`), and predictable URLs.

<a id="general-rules"></a>
### 1. General Rules
- **Lower kebab-case only:** Use lowercase alphanumeric characters separated by hyphens (`-`). Never use spaces or underscores.
- **File extension:** Always use `.md` for documentation.

<a id="format-by-category"></a>
### 2. Format by Category

- **Projects & Proposals:** `projects/proposals/<topic-slug>.md`
  - *Example:* `projects/proposals/realtime-collaborative-whiteboard.md`

- **Decisions (ADRs):** `decisions/NNNN-<short-title>.md`
  - Zero-padded four-digit incremental sequence.
  - *Example:* `decisions/0001-adopt-sqlite-for-local-cache.md`
  - *Example:* `decisions/0002-migrate-auth-to-passkeys.md`

- **Dated Thoughts & Logs:** `thoughts/YYYY-MM-DD-<slug>.md`
  - *Example:* `thoughts/2025-05-18-optimizing-docker-build-caches.md`

- **Workflows & SOPs:** `workflows/<target>-<action>.md`
  - *Example:* `workflows/k8s-local-cluster-bootstrap.md`

- **Execution Plans:** `plans/<year>-q<quarter>-<project-name>.md`
  - *Example:* `plans/2025-q3-event-pipeline-rewrite.md`

---

<a id="tagging--metadata-rules"></a>
## 🏷️ Tagging & Metadata Rules

Every file should begin with YAML frontmatter to facilitate indexing, filtering, and static search tools.

<a id="frontmatter-specification"></a>
### Frontmatter Specification

```yaml
---
title: "Descriptive Title"
date: 2025-05-18
status: draft # [draft | in-review | accepted | in-progress | completed | rejected | archived]
tags:
  - architecture
  - backend
  - database
owner: "@octo-user"
---
```

<a id="status-vocabulary"></a>
### Status Vocabulary
- `draft`: Incomplete concept or brainstorming phase.
- `in-review`: Ready for peer review or self-audit.
- `accepted`: Approved for execution or ratified as a standard.
- `in-progress`: Actively being engineered.
- `completed`: Implementation shipped and verified.
- `rejected`: Decided against with documented rationale.
- `archived`: Historical reference; no longer actively maintained.

---

<a id="idea-lifecycle-workflow"></a>
## 🌱 Idea Lifecycle Workflow

Ideas in this repository transition through a progressive botanical lifecycle, minimizing noise while fostering high-leverage outcomes:

```text
  ┌──────────────┐      ┌──────────────┐      ┌──────────────┐      ┌──────────────┐
  │ 🌱 Seed      │ ───► │ 🌿 Sprout    │ ───► │ 🌳 Sapling   │ ───► │ 🌲 Tree      │
  │ (Inception)  │      │ (Exploration)│      │ (Proposal)   │      │ (Execution)  │
  └──────────────┘      └──────────────┘      └──────────────┘      └──────────────┘
    thoughts/             dev-ideas/            projects/             projects/active/
                                                proposals/            & plans/
```

<a id="stage-1-seed-inception"></a>
### Stage 1: Seed (Inception)
- **Location:** `thoughts/YYYY-MM-DD-<slug>.md`
- **Status:** `draft`
- **Activity:** Capture without friction. Unfiltered ideas, interesting blog posts, shower thoughts, and problem statements.
- **Exit Criteria:** Does this solve a real problem or present a compelling technical curiosity? If yes, upgrade to **Sprout**.

<a id="stage-2-sprout-exploration--spike"></a>
### Stage 2: Sprout (Exploration & Spike)
- **Location:** `dev-ideas/<slug>.md`
- **Status:** `draft` / `in-review`
- **Activity:** Conduct quick proof-of-concept (POC) scripts, evaluate alternative tools, determine technical viability, and list pros and cons.
- **Exit Criteria:** Technical feasibility demonstrated and scope warrants formal commitment. Upgrade to **Sapling**.

<a id="stage-3-sapling-rfc--architecture"></a>
### Stage 3: Sapling (RFC & Architecture)
- **Location:** `projects/proposals/<slug>.md` and `decisions/NNNN-<slug>.md`
- **Status:** `in-review` ➔ `accepted`
- **Activity:** Formulate a full specification covering requirements, system diagrams, data schemas, security implications, and milestones.
- **Exit Criteria:** Proposal is complete, risks are addressed, and implementation is greenlit. Move file to `projects/active/`.

<a id="stage-4-tree-execution--shipping"></a>
### Stage 4: Tree (Execution & Shipping)
- **Location:** `projects/active/<slug>.md` and `plans/<year>-q<quarter>-<slug>.md`
- **Status:** `in-progress` ➔ `completed`
- **Activity:** Code implementation, sprint tracking, release checklist sign-off, and deployment verification.
- **Exit Criteria:** All acceptance criteria fulfilled and merged to production.

<a id="stage-5-evergreen--compost-archive--post-mortem"></a>
### Stage 5: Evergreen / Compost (Archive & Post-Mortem)
- **Location:** `projects/archive/<slug>.md`
- **Status:** `completed` or `archived` / `rejected`
- **Activity:** Log lessons learned, retro observations, and maintain historical reference.

---

<a id="ready-to-use-note-templates"></a>
## 📝 Ready-to-Use Note Templates

Copy and paste these templates when creating new entries in the vault.

<a id="template-1-project-idea-rfc"></a>
### Template 1: Project Idea RFC

*Destination:* `projects/proposals/<kebab-slug>.md`

````markdown
---
title: "RFC: Project Name"
date: YYYY-MM-DD
status: draft # [draft | in-review | accepted | rejected]
tags:
  - rfc
  - proposal
  - architecture
owner: "@your-handle"
---

# 💡 RFC: Project Name

## 1. Summary & Problem Statement
Concise 2-3 sentence overview of what problem this solves and why it matters.

## 2. Motivation & Goals
- **Goal 1:** Primary objective.
- **Goal 2:** Secondary objective.
- **Non-Goals:** What we are explicitly NOT solving in this iteration.

## 3. High-Level Architecture & User Flow
Describe the components, architecture, and interaction flow:

```text
[Client/CLI] ─── HTTP/JSON ───► [API Gateway] ───► [Core Engine] ───► [Storage]
```

## 4. Technical Specifications
- **Language & Runtime:** e.g., TypeScript / Node.js 22 LTS or Rust.
- **Persistence:** SQLite / Postgres / Redis.
- **External Integrations:** APIs, third-party libraries.

## 5. Alternatives Considered
| Solution | Pros | Cons | Verdict |
| :--- | :--- | :--- | :--- |
| Proposed Solution | High throughput, type safe | Steeper initial setup | Recommended |
| Alternative A | Simpler prototype | Hard to scale | Rejected |

## 6. Implementation Milestones
- [ ] Phase 1: Prototype and schema design
- [ ] Phase 2: Core business logic and test suite
- [ ] Phase 3: CLI / UI surface and documentation
- [ ] Phase 4: Production release and benchmark verification

## 7. Open Questions & Risks
- [ ] Question 1: Unresolved risk or unknown dependency.
- [ ] Question 2: Performance under high concurrency.
````

<a id="template-2-quick-thought--brainstorm"></a>
### Template 2: Quick Thought / Brainstorm

*Destination:* `thoughts/YYYY-MM-DD-<kebab-slug>.md`

```markdown
---
title: "Thought: Short Catchy Name"
date: YYYY-MM-DD
status: draft
tags:
  - spark
  - reading-note
  - dev-habit
owner: "@your-handle"
---

# 💭 Thought: Short Catchy Name

## Context / Spark
What prompted this thought? (e.g., reading an article, debugging a tricky bug, watching a keynote).

## The Idea
Explain the concept in raw, unstructured prose or bullet points.
- Key observation:
- Potential utility:
- Interesting twist:

## Quick Pros & Cons
- **Pros:** Fast, high leverage, elegant.
- **Cons:** Additional moving part, unproven.

## Next Actions
- [ ] Research existing open-source libraries solving this.
- [ ] Convert into a `dev-ideas/` spike if viable.
```

<a id="template-3-architectural-decision-record-adr"></a>
### Template 3: Architectural Decision Record (ADR)

*Destination:* `decisions/NNNN-<kebab-slug>.md`

```markdown
---
title: "ADR NNNN: Decision Title"
date: YYYY-MM-DD
status: accepted # [draft | in-review | accepted | superseded | rejected]
tags:
  - adr
  - architecture
  - decisions
owner: "@your-handle"
---

# ADR NNNN: Decision Title

## Status
Accepted (YYYY-MM-DD)

## Context
What technical challenge or trade-off requires a concrete decision? Outline constraints, requirements, and operational environment.

## Decision
We will adopt `<Technology / Pattern / Approach>` because `<rationale>`.

## Consequences
### Positive
- Significant latency reduction across read operations.
- Type-safe query contracts between frontend and backend.

### Negative / Risks
- Adds an operational dependency that requires automated backups.
- Team requires ramp-up time on query mechanics.

## Alternatives Considered
- **Alternative 1:** Why it was discarded.
- **Alternative 2:** Why it was discarded.
```

<a id="template-4-execution-plan--checklist"></a>
### Template 4: Execution Plan & Checklist

*Destination:* `plans/YYYY-q<Q>-<kebab-slug>.md`

```markdown
---
title: "Plan: Project Sprint / Rollout Plan"
date: YYYY-MM-DD
status: in-progress # [draft | in-progress | completed | blocked]
tags:
  - roadmap
  - execution
  - plan
owner: "@your-handle"
---

# 📋 Plan: Project Sprint / Rollout Plan

## Scope & Target Date
- **Target Date:** YYYY-MM-DD
- **Primary Spec:** `projects/active/<spec-name>.md`

## Execution Checklist

### Phase 1: Preparation & Scaffolding
- [ ] Initialize repository structure and configuration files
- [ ] Configure CI pipelines with linter, test runner, and type check
- [ ] Define initial database migrations and seed fixtures

### Phase 2: Core Engineering
- [ ] Implement data models and validation schemas
- [ ] Construct business logic services
- [ ] Add unit tests (coverage > 80%)

### Phase 3: Polish & Release
- [ ] End-to-end integration testing
- [ ] Write documentation and quickstart instructions
- [ ] Ship v1.0.0 tag

## Blockers & Daily Log
- **YYYY-MM-DD:** Kickoff complete. Environment established.
```

---

<a id="demo-plan-idea-to-production"></a>
## 🚀 Demo Plan: Idea to Production

To observe how the Idea Vault functions in practice, here is an end-to-end walkthrough following a sample project through every stage of development.

<a id="the-concept-logpulse-telemetry-daemon"></a>
### The Concept: LogPulse Telemetry Daemon

**LogPulse** is a lightweight, zero-dependency background daemon written in Rust that monitors developer workstation latency, Docker CPU footprints, and battery impact, buffering metrics locally in SQLite and streaming them to a personal Grafana instance.

```text
+-------------------------------------------------------------------------------------------------+
|                                 LOGPULSE REPO MIGRATION PATH                                    |
|                                                                                                 |
|  1. Inception       thoughts/2025-01-14-workstation-metric-collector.md                         |
|          │                                                                                      |
|          ▼                                                                                      |
|  2. Exploration     dev-ideas/ebpf-vs-sysinfo-workstation-daemon.md                             |
|          │                                                                                      |
|          ▼                                                                                      |
|  3. Architecture    decisions/0001-use-sqlite-wal-for-metric-buffering.md                       |
|          │          projects/proposals/logpulse-daemon.md                                       |
|          ▼                                                                                      |
|  4. Execution       projects/active/logpulse-daemon.md                                          |
|          │          plans/2025-q1-logpulse-daemon-mvp.md                                        |
|          ▼                                                                                      |
|  5. Archive         projects/archive/logpulse-daemon.md (v1.0 Shipped)                          |
+-------------------------------------------------------------------------------------------------+
```

<a id="step-by-step-vault-walkthrough"></a>
### Step-by-Step Vault Walkthrough

#### 1. Inception: Seed
* **File:** `thoughts/2025-01-14-workstation-metric-collector.md`
* **Status:** `draft`
* **Content:** Developer notes battery drain when running 5 nested containers during local builds. Sketches an idea for a 5MB background daemon that samples procfs every 2s.

#### 2. Technical Investigation: Sprout
* **File:** `dev-ideas/ebpf-vs-sysinfo-workstation-daemon.md`
* **Status:** `in-review`
* **Content:** Compares eBPF kernel probes against standard `sysinfo` crates in Rust. Benchmarks reveal `sysinfo` uses <0.2% CPU and requires no root privileges on macOS and Linux.

#### 3. Formal Proposal & Architecture: Sapling
* **Files:**
  * `decisions/0001-use-sqlite-wal-for-metric-buffering.md` (`accepted`)
  * `projects/proposals/logpulse-daemon.md` (`accepted`)
* **Content:** Comprehensive system spec documenting CLI options (`logpulse start --interval 2s`), SQLite WAL compaction routines, and OpenTelemetry OTLP export format.

#### 4. Active Buildout: Tree
* **Files:**
  * Promoted `projects/proposals/logpulse-daemon.md` ➔ `projects/active/logpulse-daemon.md`
  * Created `plans/2025-q1-logpulse-daemon-mvp.md` (`in-progress`)
* **Content:** Milestone tracking, commit anchors, and progress checklist.

<a id="sample-execution-milestone-checklist"></a>
### Sample Execution Milestone Checklist

```markdown
## Milestone Tracking: LogPulse v1.0 MVP
Status: 🟡 In Progress | Target Release: 2025-03-31 | Lead: @octo-user

### Sprint 1: Kernel & System Sampling Engine
- [x] Spike cross-platform `sysinfo` bindings for macOS/Linux (Completed 2025-01-22)
- [x] Implement RingBuffer for burst metric containment (Completed 2025-01-28)
- [x] Unit test memory footprint under simulated 100-container stress load (Pass: 4.8MB peak)

### Sprint 2: Local Persistence & SQLite WAL
- [x] Configure SQLite with `PRAGMA journal_mode=WAL` and `synchronous=NORMAL`
- [x] Create schema migration for metric time-series table
- [ ] Implement automated compaction worker for records older than 7 days

### Sprint 3: CLI & Daemon Lifecycle
- [ ] Implement `clap`-based CLI commands: `logpulse daemon [start|stop|status]`
- [ ] Configure launchd (macOS) and systemd (Linux) service generators
- [ ] End-to-end test signal interruption handling (SIGINT / SIGTERM graceful flush)

### Sprint 4: Export Pipeline & v1.0.0 Release
- [ ] OpenTelemetry protocol (OTLP/gRPC) exporter integration
- [ ] Build GitHub Actions release matrix (x86_64 and aarch64 binaries)
- [ ] Publish documentation and release announcement
```

---

<a id="next-steps--future-enhancements"></a>
## 🔮 Next Steps & Future Enhancements

To further automate and scale this personal knowledge vault, the following upgrades are slated for implementation:

- [ ] **Automated Frontmatter Linter (GitHub Actions):** Enforce taxonomy standards, date formats, and valid status keys on every Pull Request.
- [ ] **Dynamic Index Generation Script:** A lightweight script (`scripts/reindex.py` or Node.js CLI) that scans metadata headers to generate an automated table of contents and tag cloud in the README.
- [ ] **Obsidian / Foam / VS Code Bi-Directional Linking:** Establish standardized wiki-links (`[[note-slug]]`) to visualize connections between ADRs and project specs in interactive graph viewers.
- [ ] **Semantic Search CLI:** Embed markdown contents using local embeddings (e.g., Chroma or LanceDB) to query historical insights using natural language.
- [ ] **Automated Graduation Assistant:** A bot that highlights stagnant `draft` ideas older than 60 days to review, graduate, or archive.

---

<a id="repository-hygiene--best-practices"></a>
## 💡 Repository Hygiene & Best Practices

1. **Atomic Commits:** When moving a project from `proposals/` to `active/`, make it a dedicated commit with a clear commit message: `feat(lifecycle): promote logpulse to active project`.
2. **Never Delete Abandoned Ideas:** Move them to `projects/archive/` or add a `status: rejected` header with a rationale section. Failed explorations prevent you from repeating the same dead ends in the future.
3. **Regular Triage Ritual:** Spend 15 minutes every Friday reviewing `thoughts/`—either graduate actionable concepts into `dev-ideas/` or mark them closed.
4. **Keep Specs Self-Contained:** Strive to include inline diagrams (ASCII or Mermaid) in RFCs so notes remain readable offline or in raw terminal environments.
