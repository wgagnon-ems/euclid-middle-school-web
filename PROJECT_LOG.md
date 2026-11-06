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

### EMS Task 003: website purpose and information architecture

- Rechecked the live repository: `main` now has the foundation commit `9731c3a` and no configured remote; earlier no-commit statements describe the pre-commit state. No website implementation or existing plan was present.
- Confirmed the user-provided existing school URL returned HTTP 200 and the title “Home | Euclid Middle School” on October 13, 2026. Individual school pages and their content were not reviewed.
- Added `docs/plans/website-purpose-and-information-architecture.md` as a proposal for an accessible, privacy-conscious, one-page orientation and verified-link hub. It treats the existing school site as the destination for official, changing information and marks purpose, affiliation, content, and publication as owner decisions.
- Updated the current-status snapshot and README for the live repository state. No HTML, CSS, JavaScript, dependency, workflow, commit, push, or deployment was added during Task 003.

### Owner direction after Task 003

- The owner clarified that the site is an independent, unofficial student reference resource for grades 6–8 covering science and social studies, separate from the official Euclid website.
- Recorded this direction in the existing plan and handoff. The prior one-page official-resource hub proposal is superseded. First-release topics, content format, sources, review responsibility, and page organization remain undecided, so the plan-review step is still open. No website pages were implemented.
- The owner further specified that cognitive accessibility is foundational alongside WCAG 2.2 AA for students with varied accessibility needs. The existing plan now sets expectations for comprehension, predictable navigation, low cognitive load, error recovery, assistive-technology compatibility, and age-appropriate rigor. It also requires appropriately authorized, privacy-conscious feedback from representative students and educators before release, without collecting disability information. Content and structure decisions remain open; no testing or website implementation was performed.

## October 14, 2026

### Accessible website structure

- The owner approved building the content-independent grade and subject structure before collecting curriculum topics from teachers. The Task 003 plan now records this structure-first decision while keeping content, usability authorization, and publication decisions open.
- Added a local static preview: `index.html` for grade selection; `grade-6.html`, `grade-7.html`, and `grade-8.html` with Science and Social Studies sections; and shared `styles.css`. All pages state that topics and resources are unavailable and that the site is independent and unofficial. No curriculum claims, resources, JavaScript, dependencies, services, or data collection were added.
- Static checks parsed all four pages and passed for headings, landmarks, internal links and fragments, focus targets, and stylesheet references. The lowest checked text contrast ratio was 8.30:1. `git diff --check` and trailing-whitespace checks passed. Source review found no external data flows or private student information. Headless Edge and Chrome did not produce screenshots in this environment, so rendered layout, interactive keyboard use, screen-reader behavior, and zoom/device reflow remain to be checked in a browser.
- Updated the README and current-state handoff. No commit, push, or deployment was performed.

## October 21, 2026

### Intended WSL environment separation

- The owner specified two independent WSL environments: `Ubuntu-24.04` is intended to be the default distribution dedicated to Lost Without, while `EMS` is dedicated to this project. The Ubuntu installation and default setting remain unverified; this is the intended configuration, not a confirmed system state.
- EMS commands and scripts that launch WSL must explicitly use `wsl.exe -d EMS` and must not depend on the default distribution.
- Scoped inspection found no WSL invocation in this repository or in the EMS launcher files under `C:\Users\gagno\.codex-ems` (`Start-EMS-Codex.ps1`, its two backup copies, and the empty `Start-EMS-Codex(1).ps1`). The active launcher starts Windows Codex directly. No existing inspected EMS launch script needs a WSL selection correction.
- Documentation only was updated. No launcher, WSL distribution, or system default setting was modified, and no WSL configuration command was run.

## November 6, 2026

### Accessibility research and design planning

- Rechecked the live `main` working tree and preserved the uncommitted four-page prototype and prior documentation. Updated the existing website plan, current-state handoff, and README; no new plan or task tracker was created.
- Prioritized review of the existing website, evidence-informed cognitive accessibility, and equally usable Chromebook and personal-smartphone experiences before design implementation or teacher-selected curriculum content. The plan separates measurable WCAG 2.2 AA checks from design choices that need evaluation with users.
- Recorded W3C WCAG 2.2, W3C cognitive accessibility guidance, CAST UDL, and official platform accessibility documentation as research sources and mapped their intended uses. Live requests to W3C, CAST, Google, Apple, and Android pages failed DNS resolution, so no external source findings were independently verified and platform-specific procedures remain pending.
- Owner review of the design direction precedes implementation. Publication, curriculum, authorized usability feedback, and deployment decisions remain open. This update changed documentation only; no website code, configuration, dependency, commit, push, or deployment was performed.
