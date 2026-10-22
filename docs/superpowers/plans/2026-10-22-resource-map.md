# NeuroAI Resource Map Implementation Plan

> **For agentic workers:** Use focused, independent document tasks with a final whole-repository review. Track steps with checkboxes.

**Goal:** Make this collection useful to curious readers, people crossing between neuroscience and AI, students, builders, researchers, and educators.

**Architecture:** Readers enter by goal, explore by scientific question, and look up resources by type. Each resource keeps one canonical description; learning routes, projects, and related themes link to that description. Keep the repository as a small Markdown collection.

**Tech Stack:** GitHub Markdown, existing lychee 0.24.2 link checks, Pandoc preview.

**Spec:** The information-architecture proposal accepted in the conversation on 2026-10-22, with explicit authorization to complete without further confirmation.

## Global constraints

- Preserve all 55 resource entries from the initial working tree, including their descriptions, URLs, and access caveats.
- Preserve pre-existing uncommitted expansion records. Work in the current checkout so those inputs are included; do not stage, commit, or discard the user's work.
- Keep English resource descriptions, an accessible Chinese entry point, and a bilingual glossary.
- Provide start-here, learn, topics, resources, projects, and community navigation; avoid thin topic files.
- Treat themes as overlapping navigation, and distinguish current coverage from suggested expansion.
- Reuse existing sources; this restructuring does not claim to have run tutorials or reproduced research.
- Retain old Markdown paths and section anchors as short navigation pages during migration.

## Review focus

- A curious reader can find a meaningful route without programming prerequisites.
- Readers from either field get explicit, different bridge routes and can skip material they know.
- Topic pages connect papers to tools, data, evaluations, and exercises without duplicate canonical entries.
- Legacy page paths and section fragments still lead to useful destinations.
- Historical curation results remain historical; new verification reports what was actually checked.

## Tasks

- [x] 1. Create start-here overview, pathways, bilingual glossary, Chinese guide, and projects using existing learning material.
- [x] 2. Build a question-led topics page with the 17 existing papers, related resources, entry readings, and bounded follow-up questions.
- [x] 3. Split the 17 practical resources into tools, datasets, and benchmarks, with a resource index and selection guidance.
- [x] 4. Update homepage, learn, community, contributor guidance, templates, and curation; turn old pages into compatibility navigation.
- [x] 5. Verify resource preservation and uniqueness, old and new local links, rendered navigation, and external destinations; get an independent review and fix material findings.

## Validation

- Compare the final canonical resource entries against the working-tree snapshot saved outside the repository before editing.
- Run `lychee --offline --include-fragments --no-progress './**/*.md'`.
- Run the documented full external-link check; manually review failed destinations without hiding failures.
- Render current user-facing pages and inspect representative routes and layout.
- Run `git diff --check`, review changed and untracked files, and confirm the original expansion records remain intact.

## Execution outcome

Completed in the existing checkout with focused parallel document tasks and a final independent review. All 55 original descriptions and primary URLs remain exact and unique; the three pre-existing expansion records are byte-identical. All original heading fragments are retained, including compatibility aliases on the homepage. Local links and YAML parsing pass, and all 13 current reader-facing pages render with one H1 and consistent tables. Homepage, Chinese entry, and tool selection layouts were visually inspected in Safari. The external request scan encountered three unique destinations with access or connection failures; their review and verification limits are recorded in the restructuring note. No files were staged or committed.
