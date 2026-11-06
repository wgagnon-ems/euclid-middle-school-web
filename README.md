# Euclid Middle School website project

This repository is the early workspace for an independent, unofficial student reference website for grades 6–8 covering science and social studies. It is not part of the official Euclid Middle School website. The grade and subject structure is available for local review; first-release educational content and publication still need project-owner decisions.

## Current status

As of November 6, 2026, the repository contains a local, content-free website prototype: a starting page, one page for each grade, and one stylesheet. It has no JavaScript, dependency manifest, or build system. Topics and resources have not been selected, and the pages are visibly marked as a preview. Local Git is on `main` with one foundation commit and no configured remote; the prototype and later documentation updates remain uncommitted. GitHub Pages is the intended static host; no GitHub connection or deployment has been verified. The [website purpose and information architecture plan](docs/plans/website-purpose-and-information-architecture.md) records the approved structure, next design and accessibility review phase, research verification limits, and open content decisions.

## Repository organization

- [AGENTS.md](AGENTS.md): development rules for future Codex sessions.
- [CURRENT_STATE.md](CURRENT_STATE.md): current handoff, verified status, and next priorities.
- [PROJECT_LOG.md](PROJECT_LOG.md): dated decisions and progress.
- `.gitignore`: local, sensitive, dependency, and generated-file exclusions.
- `docs/plans/`: website purpose and information architecture plan, including pending owner decisions. `docs/adr/` and `.agent/` are currently empty; empty directories are not tracked by Git.
- `index.html`: starting page with grade choices.
- `grade-6.html`, `grade-7.html`, `grade-8.html`: grade pages with Science and Social Studies sections.
- `styles.css`: shared, responsive presentation and focus styles.

## Local development

Windows Codex and the Windows repository at `C:\Users\gagno\Projects\ems\euclid-middle-school-web` are the established development environment. On that workstation, open PowerShell in the repository and inspect the handoff and Git status before starting work:

```powershell
Set-Location C:\Users\gagno\Projects\ems\euclid-middle-school-web
Get-Content CURRENT_STATE.md
git status --short
```

Open `index.html` in a browser to review the prototype locally. Its relative links also support a GitHub Pages project path if hosting is later approved. The separately configured EMS Codex launcher lives under `~/.codex-ems`; it is not part of this repository. WSL is optional for tasks that need it. There are no project-specific installation, build, or automated test commands. For documentation changes, use `git diff --check` for tracked edits and review untracked additions separately; run relevant checks as tooling is added.

The next phase is to review the existing site and agree on its visual design, cognitive accessibility, and Chromebook and smartphone usability before design implementation. When teachers later provide approved topics, add each topic under the matching grade and subject heading. Add resource links only after the relevance, accuracy, accessibility, privacy, advertising, cost, copyright, and maintenance review described in the plan. Keep preview notices until the content and publication review is complete.

## Project commitments

The accessibility target is WCAG 2.2 Level AA, with cognitive accessibility foundational to the student experience. Development must protect student privacy: use synthetic data, avoid exposing private student information, and avoid unnecessary analytics or unapproved third-party services. School-specific facts need authoritative verification before publication. See [AGENTS.md](AGENTS.md) for working rules and [PROJECT_LOG.md](PROJECT_LOG.md) for recorded decisions.
