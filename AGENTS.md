# Codex guidance for Euclid Middle School

This repository is for a planned website for Euclid Middle School, Littleton Public Schools, Colorado (grades 6–8). Student safety, privacy, accessibility, and factual accuracy are nonnegotiable.

- Target WCAG 2.2 Level AA. For applicable UI work, use semantic HTML, keyboard access, visible focus, responsive layouts, and reduced-motion support. Check the relevant experience with available tools and report any gaps.
- Never collect or expose private student information. Use synthetic data for development and examples.
- Do not add unnecessary analytics, advertising trackers, or unapproved third-party services. Raise privacy or security concerns before introducing external data flows.
- Verify school-specific facts against authoritative sources before publishing them; do not invent names, dates, policies, contact details, or claims of district authorization.
- Prefer simple, maintainable, standards-based code that works on school Chromebooks and mobile devices. Keep dependencies minimal and changes focused.
- GitHub Pages is the intended static host, subject to decisions recorded in this repository. Do not assume deployment is configured.
- Run checks relevant to each change, including available build or validation commands when they exist. State exactly what passed, failed, or was not run.
- Escalate requirements that conflict with privacy, security, accessibility, or the agreed architecture rather than silently compromising them.

[CURRENT_STATE.md](CURRENT_STATE.md) is the latest handoff and active-status snapshot. [PROJECT_LOG.md](PROJECT_LOG.md) records dated decisions and progress. Consult them when resuming work or when historical decisions matter; minor changes do not require rereading the full log. Treat the live repository as authoritative and preserve unrelated work.
