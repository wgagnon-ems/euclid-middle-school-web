# EMS Task 003: Website purpose and information architecture

Status: **Structure implemented as a local prototype; design, content, and publication decisions remain open**, November 6, 2026. The next phase is review of the existing site and an evidence-informed design direction. This document does not authorize publication.

## Owner direction after Task 003

The project owner has defined the site as an **independent, unofficial student reference resource for grades 6–8, covering science and social studies**. It is not part of the official Euclid website. This resolves the proposed site's purpose and public status at a high level. The one-page orientation and official-resource link hub below was drafted before that direction and is superseded as a proposed first release. Its page structure, audiences, and link categories are not approved for the student reference site.

The owner has since approved a content-independent structure-first step. The local four-page foundation now exists. Review and refine its design, usability, and accessibility before incorporating teacher-selected curriculum topics or educational resources; do not invent curriculum content. Before adding educational content, the owner still needs to decide the first-release topics, whether the reference will contain original explanations or curated links, and the sources and review process for that content. Ownership, maintenance, final disclosure wording, and any school branding or affiliation claims also need review before publication. GitHub connection and deployment remain separate work.

## Structure-first decision, October 14, 2026

Build a locally reviewable starting page with separate Grade 6, Grade 7, and Grade 8 destinations. Each grade destination contains Science and Social Studies sections. Keep Home and grade navigation consistent, and provide direct subject links within each grade so students can find a section and recover from a wrong choice. Mark all pages clearly as a preview with no learning topics or resources available yet. This four-page structure replaces the superseded one-page link-hub proposal below; it does not approve curriculum content or publication.

Use lightweight, static HTML and CSS with relative links so the prototype works locally and under a GitHub Pages project path. Add no script, build system, external service, or dependency for this structure. Future teacher-selected topics can be added as clearly headed subsections under the appropriate grade and subject after content review; reviewed resources can be linked from those subsections. Keep labels and navigation stable as content grows. Consider any additional page only if reviewed content becomes hard to scan.

Before a future resource is included, review its educational relevance, factual accuracy, accessibility, privacy and data flows, advertising or tracking, cost, copyright or reuse terms, and maintenance needs. Record who reviewed it and how its link and content will be rechecked. Do not add placeholder curriculum claims or unreviewed resources to the prototype.

## Cognitive accessibility requirements for the student reference

Students may have autism, ADHD, dyslexia or other learning disabilities, reading or language comprehension difficulties, executive-function difficulties, or visual, motor, and other disabilities. Students who share a diagnosis may still have different needs and preferences. Plan for independent navigation, comprehension, predictability, and reduced cognitive load without asking students to disclose a diagnosis. Cognitive accessibility is foundational alongside the WCAG 2.2 Level AA target; meeting WCAG criteria alone does not establish cognitive usability. Use W3C's [*Making Content Usable for People with Cognitive and Learning Disabilities*](https://www.w3.org/TR/coga-usable/) as a research source for content clarity, finding information, focus, error recovery, and different ways of using the site, subject to the verification note below.

The future content and information architecture should meet these expectations:

- **Understand purpose and location:** Students can quickly tell that this is an independent, unofficial science and social studies reference for grades 6–8, what they can find here, and where they are within it. Navigation describes destinations in terms students understand.
- **Find material predictably:** Use clear, consistent labels for the same subjects, grades, and topics wherever they appear. Keep navigation and interaction behavior consistent so students do not have to relearn it. Make the destination of each link or action clear before selection.
- **Stay focused:** Present only choices that help with the current task. Avoid unnecessary distractions, interruptions, and competing paths through the same material. Do not make students remember information from a previous step when it can be available at the point of need.
- **Read and act with confidence:** Break explanations and instructions into manageable sections with informative headings and direct language. Explain unfamiliar terms and make instructions explicit and sequential when a task has steps. Keep the presentation age-appropriate without diluting academic vocabulary, factual accuracy, or rigor.
- **Recover easily:** A wrong destination should be easy to recognize and leave. Students should be able to return to a known subject, grade, or starting point and try another path without losing their place or needing adult help.
- **Use assistive technology:** The eventual site must work with keyboard navigation, screen readers, magnification and reflow, and other assistive technologies. Preserve semantic structure, visible focus, and the ability to understand and operate content when motion is reduced. Check these experiences during implementation, rather than assuming that WCAG checks alone establish cognitive usability.

## Design and accessibility direction, November 6, 2026

### Requirements and decisions to evaluate

Treat accessibility as a design input from the first review. The target is WCAG 2.2 Level AA or better, with cognitive accessibility evaluated through actual use. The starting experience should make the site's purpose and unofficial status immediately understandable; identify grade and subject clearly; use predictable page structures, consistent navigation and return paths, clear headings, descriptive links, and manageable reading sections. Keep age-appropriate academic rigor while explaining unfamiliar terms when content is later approved.

For the next design direction, specify color and contrast, typography and readability, spacing and content density, navigation and orientation, grade and subject presentation, future resource presentation patterns, responsive behavior, and assistive-technology support. Ensure text and controls remain understandable without color cues alone. Avoid unnecessary animation, autoplay, and distracting interactions. Preserve browser zoom, text scaling, reduced-motion settings, and other user preferences wherever practical. Do not assume a specialty font, color palette, or visual treatment benefits everyone with a particular disability.

**Objective checks:** Map applicable WCAG 2.2 AA criteria to the actual pages and check semantic structure, keyboard operation, visible focus and focus order, labels and link purpose, contrast, use of color, target size, text resizing, and reflow. Check screen-reader output and reduced-motion behavior where applicable. **Design choices to test:** Exact colors, font family and sizes, spacing, line length, content density, navigation presentation, and future resource layouts are proposals until evaluated for comprehension and usability. Record the evidence and tradeoffs for each choice rather than assigning a universal treatment to a diagnosis.

### Equal priority usage environments

- **School Chromebooks:** Review ChromeOS and Chrome at representative school-device screen sizes and resolutions, with keyboard and trackpad navigation, browser zoom and text enlargement, ChromeVox and Select-to-Speak where available, and realistic school-device performance and bandwidth. Do not assume a single Chromebook model, browser setting, or assistive-technology configuration.
- **Personal smartphones at home:** Review narrow portrait and landscape layouts, touch operation and adequately sized targets, browser text scaling and accessibility preferences, iPhone/Safari and Android/Chrome behavior, and VoiceOver and TalkBack compatibility. Content should reflow without unnecessary horizontal scrolling.
- **Cross-device continuity:** Keep grade and subject labels, navigation routes, and return paths understandable when a student moves between Chromebook and phone. A mobile layout may adapt visually, but it should not require learning a fundamentally different route to the same material.

### Research sources and verification

Use current primary sources, peer-reviewed research, and recognized accessibility authorities where possible. Distinguish a standard's testable requirement, an authority's design recommendation, and a local hypothesis requiring student use or educator review. The following sources guide the next research and test-plan pass:

| Source | Decisions it should inform | Status on November 6, 2026 |
| --- | --- | --- |
| [W3C WCAG 2.2](https://www.w3.org/TR/WCAG22/) | Applicable, measurable Level AA criteria and technical validation. | Owner-supplied primary source; live content not retrieved in this update. |
| [W3C Making Content Usable for People with Cognitive and Learning Disabilities](https://www.w3.org/TR/coga-usable/) | Understandable purpose, predictable navigation, memory demands, distraction, and recovery objectives. This is guidance to evaluate, not a WCAG conformance claim. | Owner-supplied primary source; live content not retrieved in this update. |
| [CAST Universal Design for Learning Guidelines](https://udlguidelines.cast.org/) | Inclusive learning access, flexible support, and preserving meaningful academic engagement. | Owner-supplied primary source; live content not retrieved in this update. |
| Official Google ChromeOS/Chrome accessibility guidance, Apple iPhone/Safari/VoiceOver guidance, and Android/Chrome/TalkBack guidance | Platform-specific settings and assistive-technology procedures for the device matrix above. | Exact current pages, versions, and procedures require verification before test instructions are finalized. |

Live requests to the three linked primary sources and sample Google, Apple, and Android support pages failed because DNS resolution was unavailable in this environment. No external source findings or platform behavior were independently verified for this planning update. Revisit the sources when network access is available, cite the specific sections used, and change any proposed design or test requirement that the evidence does not support. Do not treat WCAG conformance as proof of cognitive accessibility or claim a treatment is universally effective for autism, ADHD, or dyslexia.

### Next development progression

1. **Phase A — Existing website review:** Inspect the local four-page prototype in a browser and establish actual navigation, hierarchy, styling, keyboard behavior, and accessibility. Identify what already works and record observed gaps before proposing changes. Prior static checks do not establish rendered, assistive-technology, or device behavior.
2. **Phase B — Research-backed design standards:** Verify relevant source guidance, develop a consistent direction for the design areas above, and distinguish measurable requirements from provisional values. Include Chromebook and smartphone behavior, cognitive accessibility, and assistive technology. Present the direction and evidence for owner review; colors, type sizes, and spacing are not final yet.
3. **Phase C — Implementation:** After owner approval of the design direction, apply agreed changes to the existing static architecture and conventions. Keep dependencies and features limited to demonstrated needs. Curriculum topics and resources remain a separate, teacher-selected and reviewed content step.
4. **Phase D — Accessibility and usability validation:** Use available automated checks and manual review for applicable WCAG 2.2 AA criteria, keyboard navigation and focus order, screen readers, zoom/text resizing/reflow, Chromebook and iPhone/Android use, navigation comprehension and cognitive load, and privacy, tracking, and security. Seek educator or representative student feedback only through the authorized, privacy-conscious process below. Record what was tested, passed, failed, and remains unverified; revise and retest before release.

### Usability validation before release

Use realistic, age-appropriate learning-finding tasks to check whether representative students can explain the site's purpose and unofficial status, locate appropriate science or social studies materials, navigate independently, and recover after choosing a wrong destination. Include keyboard and assistive-technology use where relevant. If students need repeated prompting, cannot explain where a choice leads, or cannot recover from a mistake, revise the content or navigation and check again. Seek educator feedback on clarity, age appropriateness, academic accuracy, and whether tasks reflect how students look for reference material.

Plan representative student and educator feedback before release only through an appropriately authorized process. Identify who can authorize recruitment and sessions, obtain any required student and guardian permissions, and agree on a minimal, privacy-conscious way to record task outcomes before testing. Do not recruit or test students until that authorization exists. Do not collect disability information, diagnoses, private student information, or identifiable recordings for this project; keep any approved observations limited to what is needed to improve usability and out of the public repository. If this feedback cannot be authorized, record the validation gap and resolve it before release.

## Original Task 003 proposal (superseded)

### Purpose and boundaries

The repository establishes a planned Euclid Middle School website, accessibility and privacy requirements, and GitHub Pages as the intended static host. It does not establish a specific public purpose, district authorization, or a replacement for the [existing school website](https://euclid.littletonpublicschools.net/). On October 13, 2026, that URL returned HTTP 200 with the title “Home | Euclid Middle School”; its individual pages and content were not reviewed for this plan.

**Recommended purpose, pending approval:** a small, public orientation and link hub that helps students and families find current information on the existing school or district site. The existing school site remains the destination for official, changing information. Any published version should disclose this project's status and avoid implying that it speaks for the school or district. If the owner wants a different purpose or an official district site, settle that role and authorization before implementation.

The proposed site would not host student accounts, forms, school records, copied schedules, staff directories, policy text, or time-sensitive announcements. It would link to authoritative pages after each destination is checked. GitHub Pages is an intended host, not a configured deployment.

### Audiences and navigation

Primary audiences are students in grades 6–8 and their families. Staff and other visitors may use the same public links; no staff-only area or separate audience pages are justified by the current goals.

The first release can be **one page** (`/`) with a skip link, one clearly labeled navigation landmark, and these in-page destinations:

1. **Start** — what this site is and a prominent link to the existing school website.
2. **Find information** — short, task-based groups of verified links to official resources.
3. **About this project** — ownership/status disclosure, source and freshness note, and a route back to the official site.

Use descriptive link text and a simple heading order. Only show navigation destinations that contain useful, approved content. If the link list grows enough to become hard to scan, move “Find information” to a separate page after review; do not add empty sections now.

### Page and content requirements

| Page or section | Proposed content | Source and release condition |
| --- | --- | --- |
| Start | A brief, plain-language explanation of the site's approved role; prominent official-site link; a few shortcuts if useful. | Owner-approved wording. The official home URL was reachable on October 13, 2026; verify it again before release. |
| Find information | A small set of links grouped by task, such as school news/calendar, learning resources, family information, and contact/help. Include a group only if it has useful public destinations. | Verify each destination and its label against the current school or district page before inclusion. Do not copy changing details or link to private/staff-only services as if public. These groups are proposals, not verified offerings. |
| About this project | Clear project status, who maintains it if approved for disclosure, a source/freshness note, and a link to the existing school website for authoritative information. | Owner approval for identity, wording, maintenance responsibility, and any claim of school or district affiliation. Do not invent contact details. |

**Evidence levels:** The official home URL and page title above were checked. The school's identity, district, and grade range are established in repository guidance, but should be confirmed from an authoritative source before public copy uses them. The site purpose, sections, and resource groups here are proposals. Deep links, service availability, dates, programs, schedules, policies, names, contact details, and authorization remain unverified. An official school or district page is the preferred source for each school-specific claim; if a claim lacks one, omit it from release copy.

### Minimum viable release

After the owner approves the role and public status, the smallest useful release is one lightweight static page containing the approved purpose and disclosure, a working link to the existing school website, and only a few individually verified public resource links. It needs a usable mobile and Chromebook layout, keyboard navigation, visible focus, and a documented content owner who can recheck links and wording. No build system, JavaScript, account, form, analytics, or third-party embed is required.

Future improvements, if a real need emerges: a separate resource page, more verified task links, translations reviewed by fluent speakers, and a lightweight link-review process. News feeds, calendars, search, and personalization require separate value, privacy, maintenance, and accessibility decisions.

### Accessibility and privacy

Target WCAG 2.2 Level AA from the first prototype. Use semantic landmarks and headings, a keyboard-usable skip link and navigation, visible focus, clear link labels, adequate contrast, responsive layouts, and plain language suitable for middle-school readers. Respect reduced-motion preferences if motion is introduced. Before release, check keyboard and screen-reader behavior, zoom/reflow, contrast, and mobile/Chromebook layouts; record any gaps.

Publish no private student information. Use synthetic examples during development. Avoid student data collection, advertising trackers, unnecessary analytics, external embeds, and unapproved third-party services. Ordinary links to verified official resources are sufficient for the proposed purpose. Review outgoing links and any future data flow before publication.

### Decisions requiring project-owner approval

1. Confirm the site's distinct purpose and whether a separate link hub adds value alongside the existing school site.
2. Confirm its ownership, permitted branding and affiliation language, and whether public publication has school or district authorization. Until then, treat any build as a reviewable prototype.
3. Approve the first-release link categories and exact destinations, including who verifies school-specific copy and maintains links.
4. Approve the public status/disclosure wording and the route for reporting stale or inaccessible links; do not publish personal contact information by default.
5. Confirm whether GitHub Pages is acceptable for the approved public role and who can authorize deployment. Hosting and deployment are not configured here.

### Recommended implementation sequence

1. Review and decide the outstanding purpose, authorization, content, and maintenance questions.
2. Inventory a few official public destinations; verify URLs, labels, and school-specific claims with their source pages.
3. Draft and review plain-language page copy and a minimal page outline before writing code.
4. Implement the approved single-page static site with semantic HTML and minimal CSS; add no dependency unless a concrete need warrants it.
5. Check content accuracy, privacy, accessibility, responsive behavior, and links; fix gaps before considering publication.
6. Separately decide repository connection, deployment settings, and a publication approval process.
