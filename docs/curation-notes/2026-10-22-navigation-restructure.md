# Resource-map restructuring: 2026-10-22

## Purpose and design

Help curious readers, people crossing between neuroscience and AI, students, builders, researchers, and educators find an appropriate entry point. The homepage routes by readers' goals; topics connect scientific questions to papers and practical resources; type indexes support direct lookup. Background and outcome guidance is editorial and depends on the chosen activity.

## Migration baseline

The input was the local working tree, including its uncommitted expansions: 15 learning resources, 17 research papers, 17 practical resources, and 6 community resources, for 55 canonical entries. The three 2026-10-11 expansion records are historical evidence and remain intact. Their paths and counts describe the collection at their review dates.

## Current homes

| Material | Canonical destination |
| --- | --- |
| Background, textbooks, reviews, courses, tutorials | [Learn](../../learn/README.md) |
| Research and methods papers | [Topics](../../topics/README.md) |
| Software and environments | [Tools](../../resources/tools.md) |
| Data collections and archives | [Datasets](../../resources/datasets.md) |
| Evaluation resources | [Benchmarks](../../resources/benchmarks.md) |
| Collections, conferences, research conversations | [Community](../../community/README.md) |

The [overview](../../start-here/README.md), [pathways](../../start-here/pathways.md), [bilingual glossary](../../start-here/glossary.md), [Chinese guide](../../start-here/README.zh-CN.md), and [projects](../../projects/README.md) refer to these homes. Topics overlap; an architecture, learning algorithm, measurement method, and scientific question are different descriptive dimensions.

The former research and practice pages, Chinese guide, and stage-based learning guide retain their original paths and headings as compatibility navigation. Historical review notes are not rewritten into claims about the current layout.

## Verification boundary

This change reorganizes existing resources and adds editorial guidance. It adds no new canonical external resources. Resource preservation, local links, Markdown rendering, and external requests are checked separately. Exercises are proposed activities; this restructuring does not install tools, run notebooks, download datasets, reproduce papers, or test benchmark submissions.

## Verification results

- Exact-line comparison against a snapshot of the initial working tree confirmed all 55 original canonical entries, descriptions, primary URLs, and caveats are preserved once each: 15 in Learn, 17 in Topics, 9 in Tools, 4 in Datasets, 4 in Benchmarks, and 6 in Community. Primary URLs are unique across those entries.
- The three original 2026-10-11 expansion records are byte-identical. All original Markdown paths remain present.
- A separate compatibility check passed all 69 original heading references. The homepage retains aliases for its former start-here, collection, and contributing headings; old guide and resource pages retain their original headings.
- The final Lychee 0.24.2 offline check, repeated after writing this record, found 535 link occurrences: 425 local occurrences passed with fragment checking and no errors; 110 external occurrences were excluded from that offline run.
- Pandoc rendered all Markdown pages. Structural inspection of the 13 current reader-facing pages confirmed one H1 per page, consistent table column counts, and no empty list items. Safari visual inspection covered the homepage, Chinese guide, and tool-selection table. The preview uses a local stylesheet; GitHub supplies its own styling.
- All three GitHub YAML files parse successfully. Whitespace checking passed. An independent reviewer inspected the new and modified documentation and found no material actionable defects.

## External-link review

The full request run checked 535 link occurrences (140 unique targets): 529 passed and 6 failed occurrences represented three unique destinations. Local links are included in that full-run total. These are request outcomes from this review, not a guarantee of continued access or source accuracy.

| Destination | Automated result | Follow-up and decision |
| --- | --- | --- |
| CCN conference site | Connection closed after redirecting to its www host. | A separate web read successfully opened the official conference page. Retain the canonical conference URL. |
| Neuronal Dynamics online textbook | Connection closed; a separate direct web read timed out. | Official EPFL search results still identify the book and its online edition, but current online-book access could not be confirmed in this review. Retain the source and its existing description; report the access limitation. |
| EWC paper's PNAS DOI | Publisher returned HTTP 403 after DOI redirection; a separate web read also could not retrieve the publisher page. | The existing author-manuscript link on arXiv opened successfully. Retain the manuscript as the main reading link and the DOI as the published-article reference. |

The failing destinations were not removed or globally excluded from checks. Their successful source reads or indexed records do not establish software compatibility, data access, or experimental reproducibility.
