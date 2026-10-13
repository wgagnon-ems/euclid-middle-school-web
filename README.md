# Euclid Middle School website project

This repository is the early workspace for a planned website for Euclid Middle School (Littleton Public Schools, Colorado; grades 6–8). The likely audiences are students, families, staff, and the wider school community; the exact site scope and content are still to be planned. This repository has not been verified as an officially authorized district publication.

## Current status

As of October 13, 2026, the repository contains planning and handoff documents but no website pages, application code, dependency manifest, or build system. Local Git is on `main` with no commits, tracked files, or configured remote. GitHub Pages is the intended static host; no GitHub connection or deployment has been verified.

## Repository organization

- [AGENTS.md](AGENTS.md): development rules for future Codex sessions.
- [CURRENT_STATE.md](CURRENT_STATE.md): current handoff, verified status, and next priorities.
- [PROJECT_LOG.md](PROJECT_LOG.md): dated decisions and progress.
- `.gitignore`: local, sensitive, dependency, and generated-file exclusions.
- `docs/adr/` and `docs/plans/`: currently empty directories reserved for future decisions and plans. `.agent/` is also currently empty. Empty directories are not tracked by Git.

## Local development

Windows Codex and the Windows repository at `C:\Users\gagno\Projects\ems\euclid-middle-school-web` are the established development environment. On that workstation, open PowerShell in the repository and inspect the handoff and Git status before starting work:

```powershell
Set-Location C:\Users\gagno\Projects\ems\euclid-middle-school-web
Get-Content CURRENT_STATE.md
git status --short
```

The separately configured EMS Codex launcher lives under `~/.codex-ems`; it is not part of this repository. WSL is optional for tasks that need it. There are currently no project-specific installation, run, build, or automated test commands. For documentation changes, use `git diff --check` for tracked edits and review untracked additions separately; run relevant checks as tooling is added.

## Project commitments

The accessibility target is WCAG 2.2 Level AA. Development must protect student privacy: use synthetic data, avoid exposing private student information, and avoid unnecessary analytics or unapproved third-party services. School-specific facts need authoritative verification before publication. See [AGENTS.md](AGENTS.md) for working rules and [PROJECT_LOG.md](PROJECT_LOG.md) for recorded decisions.
