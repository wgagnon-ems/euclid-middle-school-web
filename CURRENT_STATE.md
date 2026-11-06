# EMS Current State

Last updated: November 6, 2026 (accessibility and design planning update).

## Current repository status

The Windows Git repository at `C:\Users\gagno\Projects\ems\euclid-middle-school-web` is the canonical workspace. Windows Codex is the primary development environment; WSL is optional for tasks that need it. The dedicated EMS Codex home and launcher are outside this repository, and model/reasoning settings remain user-managed.

The intended WSL setup has two independent distributions: `Ubuntu-24.04` as the default for Lost Without, and `EMS` for this project. The Ubuntu installation and default setting have not been independently verified. Any EMS command or script that launches WSL must select the EMS distribution explicitly with `wsl.exe -d EMS`; EMS must not rely on the default distribution. The October 21 scoped script review found no existing EMS launcher that invokes WSL, so no script correction was identified. No WSL distribution or default setting was changed.

The live repository is on `main` with one foundation commit (`9731c3a`, `docs: establish EMS repository foundation`) and no configured remote. This corrects the earlier handoff, which recorded the pre-commit state. The repository now has a local static prototype with a starting page, Grade 6–8 pages, and shared CSS. These pages, the plan, and later documentation updates remain uncommitted in the working tree. The site has no curriculum topics, resources, JavaScript, build system, dependency manifest, deployment workflow, or verified GitHub Pages site.

## Website direction

GitHub Pages remains the intended static host. WCAG 2.2 AA, cognitive accessibility, student privacy, school-specific factual verification, and maintainability are established requirements. This is an independent, unofficial student reference resource for grades 6–8 covering science and social studies, separate from the official Euclid website. The owner approved building the grade and subject structure before teachers provide topics. That local structure now exists. The next phase is to review its actual behavior and develop an evidence-informed visual design and accessibility direction for owner approval before design implementation or curriculum content. [EMS Task 003's website plan](docs/plans/website-purpose-and-information-architecture.md) is the detailed home for the phased work, cognitive accessibility, equal-priority Chromebook and smartphone requirements, source references, and verification limits; its earlier one-page official-resource hub proposal is superseded. The existing [school website](https://euclid.littletonpublicschools.net/) remains the source for official, changing school information. Its home URL returned HTTP 200 with the title “Home | Euclid Middle School” on October 13, 2026; individual pages were not verified.

## Next work

1. Review the existing prototype in a browser, identify what works and what needs improvement, and verify primary accessibility and platform guidance when network access is available. Current source retrieval failed because DNS resolution was unavailable; no external research findings were independently verified in this update.
2. Prepare a research-backed visual design and accessibility direction for owner review, including cognitive usability and equal-priority Chromebook and smartphone use. Exact colors, typography, spacing, and presentation patterns remain undecided.
3. After owner approval, implement the agreed design changes in the existing static architecture and validate WCAG 2.2 AA, keyboard and assistive-technology behavior, zoom and reflow, device usability, cognitive comprehension, and privacy/security. Record passes, failures, and unverified areas.
4. Keep teacher-selected first-release topics, original-versus-curated content, sources, and review responsibility as later decisions. Add no invented curriculum content. Agree on ownership, maintenance, disclosure wording, branding or affiliation claims, and authorized, privacy-conscious educator or student feedback before publication; do not conduct student testing without authorization.
5. Handle GitHub connection, protections, and deployment authorization as separate work. None is verified as configured.

The structure-first task added a local prototype only. No curriculum content, commit, push, or deployment was performed.
