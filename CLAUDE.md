# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Repo Is

A catalog of AI agent personas ("The Agency") — Markdown files with YAML frontmatter, organized into division directories (`engineering/`, `marketing/`, `music/`, …). There is no application code or test suite; the tooling is bash scripts in `scripts/` that validate the catalog and convert/install it into agentic coding tools (Claude Code, Cursor, Codex, Gemini CLI, OpenCode, etc.). Scripts require only bash 3.2 + coreutils (no jq) so they behave identically on macOS and CI.

## Commands

```bash
./scripts/lint-agents.sh [file ...]          # validate agent frontmatter/structure (no args = all divisions)
./scripts/check-agent-originality.sh <file>  # near-duplicate detection vs the whole roster (CI runs it)
./scripts/check-divisions.sh                 # division set consistency (see contract below)
./scripts/check-tools.sh                     # tool set consistency (tools.json contract)
./scripts/convert.sh [--tool <name>]         # regenerate integrations/<tool>/ output
./scripts/install.sh --tool <t> --division <d> --dry-run   # preview an install
./scripts/install.sh --list teams            # division list with agent counts
```

CI (`.github/workflows/`): `lint-agents.yml` lints + originality-checks only the agent files changed in a PR; `check-divisions.yml` and `check-tools.yml` enforce the two contracts. Note: `check-divisions.sh` reads `git ls-files`, so new files must be staged/committed before it passes.

## Agent File Format

Filename convention: `<division>/<division>-<agent-name>.md` (e.g. `marketing/marketing-tiktok-strategist.md`).

- Frontmatter: `name`, `description`, `color` are **required** (lint ERROR); `emoji` and `vibe` are conventional; optional `services:` list (name/url/tier) for agents depending on external services.
- Body sections use `##` headers. `convert.sh` splits them into two semantic groups for tools like OpenClaw: persona headers matching identity/communication/style/critical-rules go to SOUL.md; everything else (mission, deliverables, workflow, metrics) goes to AGENTS.md. Lint warns if either group is empty — keep at least one header of each kind.
- LF line endings only (lint rejects CRLF; enforced by `.gitattributes`).
- Recommended sections (lint WARNs): Identity, Core Mission, Critical Rules. Follow the full template in CONTRIBUTING.md.
- New agents must pass the originality check — re-skins of existing agents (find-replace a platform/country) get flagged and closed.

## The Two Consistency Contracts

**Divisions** — `divisions.json` (repo root) is the source of truth. Adding a division requires updating, in lockstep (CI fails otherwise):
1. Create the directory with ≥1 frontmatter agent file
2. `divisions.json` entry (label, Lucide icon PascalCase, hex color)
3. `AGENT_DIRS` in `scripts/convert.sh` and `scripts/lint-agents.sh` (checked), plus `scripts/install.sh` (both `AGENT_DIRS` and `ALL_DIVISIONS`), `scripts/build-hermes-plugin.py`, and `scripts/check-agent-originality.sh` (keep in sync)
4. Path filters in `.github/workflows/lint-agents.yml` (both the `paths:` list and the `git diff` globs)
5. README roster section + agent/division counts in Stats; CONTRIBUTING division list

Non-division top-level dirs: `strategy/` (frontmatter-less NEXUS playbooks), `integrations/` (conversion output), `examples/`, `scripts/` — listed in `NON_DIVISION_DIRS` in `check-divisions.sh`; never add them to division lists.

**Tools** — `tools.json` (repo root) is the source of truth for supported install targets. Adding a tool requires: an entry in `tools.json` (id/label/kebab/format/installKind/dest), a `convert_<tool>` function (or reused `format`) in `convert.sh`, and an `install_<tool>` in `install.sh`. Same `format` name guarantees byte-identical rendered output; `installKind` is `per-agent`, `roster`, or `plugin`.

## Generated Output Is Not Committed

`convert.sh` writes to `integrations/<tool>/`; those generated agent/skill files are gitignored (only the per-tool `README.md`s and `mcp-memory/` are tracked). Never commit conversion output — PRs containing it get closed.

## Scope Norms (from CONTRIBUTING.md)

The ideal PR is one new/improved agent `.md` file. Tooling, CI, or multi-file architectural changes are expected to go through a GitHub Discussion first. Bulk reformatting of existing agents is unwelcome. When adding an agent, also add its row to the README roster table for its division and bump the agent count in the README Stats section.
