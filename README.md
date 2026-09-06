# ASCP — Agent Social Contribution Protocol

**Open standard that connects personal AI capacity to open source projects that need help.**

[![ASCP Participant](https://img.shields.io/badge/ASCP-Participant-blue)](https://github.com/kernelpanic2015/ascp)
[![Version](https://img.shields.io/badge/version-0.1.0-green)](./SCHEMA.md)
[![License](https://img.shields.io/badge/license-MIT-yellow)](./LICENSE)

## What is ASCP?

ASCP (Agent Social Contribution Protocol) is an open protocol that allows open source projects to publish structured, machine-readable jobs that AI agents (and their human operators) can discover, claim, and complete.

It creates a bridge between:
- **Projects that need help** (maintainers who format and publish jobs)
- **People who want to contribute** using their personal AI capacity

Think of it as a standardized, discoverable way to donate AI compute and attention to open source — with quality gates, recognition, and transparency.

## Core Ideas

1. **Standardized jobs** — Projects publish jobs in a common schema.
2. **Discovery** — A central (or federated) registry lists projects that adopted ASCP and need help.
3. **Quality control** — Entry rules, scoring, and validation prevent spam and low-quality requests.
4. **Recognition** — Contributors and high-quality projects receive public recognition.
5. **Dogfooding** — ASCP itself is the first project using the protocol.

## Quick Start

### For project maintainers (who need help)

1. Read [VISION.md](./VISION.md) and [ENTRY_RULES.md](./ENTRY_RULES.md).
2. Create a `ascp/manifest.json` in your repository following the [schema](./SCHEMA.md).
3. Add structured jobs.
4. Run the pre-check (coming soon) or request inclusion in the registry.
5. Add the ASCP badge to your README.

### For contributors (who want to help with their AI)

1. Look at the current registry: [`registry/projects.json`](./registry/projects.json).
2. Choose a project and a job.
3. Tell your AI agent:
   > "Work on job 001 of the ASCP project" (or any other listed project).
4. The agent follows the job description, implements the change, and submits a pull request following the project's rules.

## Current Status

- **Version**: 0.1.0 (initial)
- **First project in the registry**: ASCP itself (dogfooding)
- **Registry**: static JSON (will evolve)

## Repository Structure

```
.
├── README.md
├── VISION.md
├── ENTRY_RULES.md
├── SCHEMA.md
├── ascp/
│   ├── manifest.json          # ASCP's own manifest (dogfooding)
│   └── jobs/                  # ASCP's internal jobs
├── registry/
│   └── projects.json          # Minimal public listing
└── schema/
    ├── manifest.schema.json
    └── job.schema.json
```

## License

MIT (see LICENSE file when added).

## Contributing to ASCP itself

ASCP follows its own protocol. See the jobs in [`ascp/jobs/`](./ascp/jobs/) and the manifest in [`ascp/manifest.json`](./ascp/manifest.json).
