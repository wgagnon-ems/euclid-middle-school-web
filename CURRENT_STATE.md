# EMS Current State

Last updated: October 13, 2026.

## Development workflow

Use Windows Codex as the primary development environment and the Windows Git repository at `C:\Users\gagno\Projects\ems\euclid-middle-school-web` as the canonical workspace.

The dedicated EMS Codex home is `~/.codex-ems` (`C:\Users\gagno\.codex-ems`). The EMS launcher is `C:\Users\gagno\.codex-ems\Start-EMS-Codex.ps1`. Inspection on October 13 confirmed that its saved configuration sets `CODEX_HOME`, selects the Windows workspace, and launches Codex with `-c 'default_permissions=:workspace' -a on-request`. It does not set a model or reasoning effort; both remain user-managed. The launcher was inspected, not executed, during this update.

The user reports a successful Windows Codex launch with workspace permissions and on-request approvals. The previous hardened Windows launcher encountered sandbox initialization failures. WSL isolation tests passed according to the user; WSL is optional and should be used for tasks that specifically require it.

## Verified repository foundation

Before this documentation update, local Git reported `main` with no commits, no tracked files, and no configured remotes. The `.agent`, `docs/adr`, and `docs/plans` directories were empty. No existing `AGENTS.md`, `README.md`, `.gitignore`, or project logs were found.

This update creates root-level `PROJECT_LOG.md` and `CURRENT_STATE.md` as uncommitted handoff documentation. No GitHub repository, branch protections, or deployment status has been verified. GitHub connection, initial commit, and protections remain future work.

## Project direction

GitHub Pages is the intended hosting platform. Accessibility, student privacy, and maintainability must guide repository setup and website planning. Website scope, content, design, and technical implementation still need to be planned.

## Next session priorities

1. Establish `AGENTS.md`, `README.md`, and `.gitignore` with project-specific guidance and appropriate exclusions.
2. Review the repository foundation and agree on the structure needed for the website.
3. Connect the canonical Windows repository to the intended GitHub repository.
4. Make the initial commit and configure appropriate protections after reviewing the repository and available GitHub settings.
5. Begin website planning with accessibility, student privacy, maintainability, and GitHub Pages hosting in mind.

Start the next session by reading this file and `PROJECT_LOG.md`, then rechecking local repository status before acting. These priorities are plans, not completed work. The October 13 documentation task does not authorize security configuration changes, dependency installation, commits, pushes, or deployment.

## October 13, 2026 — EMS Task 001 update

`AGENTS.md`, `README.md`, and `.gitignore` now establish project-specific development rules, an accurate early-stage README, and local-file exclusions. No website code, dependency manifests, workflows, remotes, commits, or deployment configuration were added. The foundation files and both checkpoint documents remain uncommitted. The earlier priority to create the three foundation files is complete; the next development task is to review and plan the website structure and content before implementation. GitHub connection, initial commit, and protections remain separate future work.
