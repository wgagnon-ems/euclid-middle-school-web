# EMS Project Log

## October 13, 2026

### Development environment decisions and progress

- Windows Codex is the primary development environment. The Windows Git repository at `C:\Users\gagno\Projects\ems\euclid-middle-school-web` is the canonical workspace.
- EMS uses the dedicated Codex home `~/.codex-ems` (`C:\Users\gagno\.codex-ems` on this Windows account) and launcher `Start-EMS-Codex.ps1`.
- The user reports that Windows Codex successfully launched with workspace permissions and on-request approvals. The previous hardened Windows launcher encountered sandbox initialization failures.
- The user reports that WSL isolation tests passed. WSL is now optional and reserved for tasks that specifically require it.
- Model selection and reasoning effort remain user-managed.
- GitHub Pages remains the intended hosting platform. Accessibility, student privacy, and maintainability remain core project requirements.

### Repository and launcher preflight

- Inspected the Windows repository before writing these documents. Git reports branch `main` with no commits, no tracked files, and no configured remotes. No GitHub repository, hosting, or protection status was verified.
- The repository contains empty `.agent`, `docs/adr`, and `docs/plans` directories. No existing project logs, `AGENTS.md`, `README.md`, or `.gitignore` were found; these logs therefore add no duplicate history.
- Read `C:\Users\gagno\.codex-ems\Start-EMS-Codex.ps1`. Its saved configuration sets `CODEX_HOME` to `$HOME\.codex-ems`, changes to `$HOME\Projects\ems\euclid-middle-school-web`, and invokes `$env:LOCALAPPDATA\Programs\OpenAI\Codex\bin\codex.exe` with `-c 'default_permissions=:workspace' -a on-request`.
- The inspected launcher has no model or reasoning-effort arguments. Its saved configuration was verified by inspection; it was not rerun during this documentation update. Earlier launcher failures and WSL test results are user-reported history, not tests repeated here.
- Created `PROJECT_LOG.md` and `CURRENT_STATE.md` for the next ChatGPT session. No security configurations were modified, dependencies installed, commits made, pushes performed, or deployments performed.

### Planned next session work

1. Establish `AGENTS.md`, `README.md`, and `.gitignore`.
2. Review the repository foundation.
3. Connect the Windows repository to GitHub.
4. Make the initial commit and configure appropriate protections.
5. Begin website planning.

These steps remain planned; GitHub Pages is an intended destination, not a verified deployment.

### EMS Task 001: repository foundation

- Rechecked the October 13 checkpoint against the live repository: `main` has no commits, tracked files, or configured remote; only the two checkpoint documents existed as untracked files. The `.agent`, `docs/adr`, and `docs/plans` directories were empty. No website code, tooling, workflow, or deployment configuration was found.
- Added `AGENTS.md` with EMS-specific safety, privacy, accessibility, accuracy, implementation, and validation rules; `README.md` with verified project status and local workflow; and `.gitignore` for relevant local and generated files.
- Kept the existing checkpoint history and made no security configuration, dependency, Git remote, commit, push, or deployment changes. Website structure and content planning is the recommended next development task.
