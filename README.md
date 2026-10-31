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
