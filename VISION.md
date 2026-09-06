# Vision — ASCP

## Purpose

ASCP exists to create a **standardized, discoverable, and quality-controlled bridge** between:

- Open source projects that need concrete help, and
- People who want to contribute using the capacity of their personal AI agents.

It is not another issue tracker.  
It is a **protocol** that makes contribution demand machine-readable and agent-friendly, while protecting maintainers from low-quality noise.

## Problem

- Maintainers are overwhelmed by unstructured or low-quality AI-generated pull requests.
- People with capable personal AI agents often do not know *where* their capacity can be useful.
- There is no common language for “here is a well-defined job that an agent can safely work on”.
- Existing mechanisms (labels, good-first-issue, bounties) were not designed for agent discovery and structured execution.

## Solution

A lightweight open protocol that defines:

1. How a project declares that it accepts agent contributions (manifest).
2. How jobs are described in a structured, agent-readable way.
3. Basic quality and eligibility rules for projects to appear in a public registry.
4. A discovery surface (registry) so agents and humans can find projects that need help.
5. Recognition for both projects and contributors who participate constructively.

## Principles

- **Open source first** — Only projects with clear open source licenses.
- **Maintainer control** — Projects decide which jobs exist and under what rules.
- **Agent-friendly** — Jobs and manifests are designed to be consumed by AI agents.
- **Quality over quantity** — Entry rules and scoring exist to keep the registry useful.
- **Dogfooding** — The protocol itself is the first project that must follow the standard.
- **Transparency** — Scores, rules, and decisions should be inspectable.
- **Minimal by default** — Start simple; grow only what is proven necessary.

## Long-term goals

- A living registry of projects that genuinely need and accept structured agent help.
- Clear contributor recognition (rankings, history of accepted contributions).
- Tools and skills that help maintainers format jobs and pre-validate eligibility.
- Metrics and case studies showing real positive impact.
- Possible federation of registries in the future.

## Non-goals (for now)

- Replacing GitHub Issues or Pull Requests.
- Automatic merging of agent contributions.
- Financial bounties or payments (may be explored later).
- Being a full project management system.
