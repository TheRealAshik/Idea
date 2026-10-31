# 🧠 Idea Vault & Engineering Logbook

[![Status](https://img.shields.io/badge/status-active-brightgreen.svg)](#) [![License](https://img.shields.io/badge/license-MIT-blue.svg)](#) [![Maintenance](https://img.shields.io/badge/maintained-yes-success.svg)](#) [![Taxonomy](https://img.shields.io/badge/taxonomy-RFC--spec-orange.svg)](#)

> A unified, friction-free knowledge vault designed to capture, organize, and incubate technical concepts, project blueprints, architectural decisions, and day-to-day sparks from inception to execution.

---

## 📑 Table of Contents

- [Vision & Purpose](#-vision--purpose)
- [Repository Structure](#-repository-structure)
- [Directory Taxonomy](#-directory-taxonomy)
- [Naming Conventions](#-naming-conventions)
- [Tagging & Metadata Rules](#-tagging--metadata-rules)

---

## 🎯 Vision & Purpose

Great systems begin as transient thoughts. Without deliberate structure, notes scatter across scrapbooks, sticky notes, and lost branches. This repository acts as an immutable external memory and structured incubation chamber:

1. **Capture early:** Zero-friction logging of raw thoughts and developer brainstorms.
2. **Refine systematically:** Graduating raw ideas into formal specifications, Architectural Decision Records (ADRs), and execution plans.
3. **Track lifecycle:** Clear status states (`draft`, `in-review`, `accepted`, `in-progress`, `archived`) to see what is actionable at a glance.

---

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

## 📐 Naming Conventions

Standardized file naming guarantees natural alphabetical sorting, easy fuzzy-find search (`Ctrl+P` / `Cmd+P`), and predictable URLs.

### 1. General Rules
- **Lower kebab-case only:** Use lowercase alphanumeric characters separated by hyphens (`-`). Never use spaces or underscores.
- **File extension:** Always use `.md` for documentation.

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

## 🏷️ Tagging & Metadata Rules

Every file should begin with YAML frontmatter to facilitate indexing, filtering, and static search tools.

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

### Status Vocabulary
- `draft`: Incomplete concept or brainstorming phase.
- `in-review`: Ready for peer review or self-audit.
- `accepted`: Approved for execution or ratified as a standard.
- `in-progress`: Actively being engineered.
- `completed`: Implementation shipped and verified.
- `rejected`: Decided against with documented rationale.
- `archived`: Historical reference; no longer actively maintained.
