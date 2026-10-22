# Curation and maintenance

## Scope

This list serves curious readers, students, people crossing between neuroscience and AI, model builders, researchers, and educators. It favors a manageable set of entry points across neural inspiration, models of brain computation, and empirical comparisons of brains and artificial networks. The [companion computational neuroscience list](https://github.com/kianmax0/awesome-computational-neuroscience) covers broader mathematical, biological, and analysis resources.

The resource links on the canonical pages in `learn/`, `topics/`, `resources/`, and `community/` are also the sources for their descriptions. The root README provides goal-based navigation. [Start here](../start-here/README.md), [pathways](../start-here/pathways.md), and [projects](../projects/README.md) connect those entries without duplicating descriptions. Placement, topic boundaries, background guidance, and suggested exercises are editorial choices. Inclusion does not mean a tool has been installed, an experiment reproduced, or a biological claim independently validated.

## Initial review: 2026-10-11

This historical audit covered the original single-page resource directory, before the resources were moved to topical pages.

The first pass checked paper identities and descriptions against publisher pages or author manuscripts, and checked courses, tools, datasets, and benchmarks against their official pages or maintainer repositories. Search-indexed source text was used where a live publisher page blocked automated access. No software installation or paper reproduction was performed.

Specific decisions:

- The Hassabis et al. review links to a university-hosted copy of the published paper because the publisher endpoint returned HTTP 403 during automated checking.
- The Zador et al. entry uses the published 2023 title and labels the work as a perspective.
- The Yang and Wang primer identifies the publication and labels its arXiv link as the author preprint.
- NeuroGym links to its current `neurogym/neurogym` repository.
- The Meta NeuroAI suite is categorized as neural-data infrastructure.
- PsychRNN carries a compatibility note because its README documents older Python and TensorFlow test environments.
- Neural Latents Benchmark carries its official notice that EvalAI submissions closed in January 2026, while local evaluation remains available.
- Natural Scenes Dataset carries its data-access agreement requirement.
- Allen Brain Observatory links to the ecosystem overview to distinguish Visual Coding and Visual Behavior collections and recording modalities.
- Model fit, computational results, and biological mechanisms are described separately.

Validation of that original layout on this date used lychee 0.24.2. The offline run passed 42 local-link occurrences with fragment checking enabled. A separate full request run passed all 73 link occurrences (47 unique targets), with no errors, timeouts, or exclusions. These results establish link-check outcomes at review time; page content and scientific quality require the source review described above.

## Directory restructuring

The directory restructuring moved the existing 27 resource entries into four topical pages: `learn/README.md`, `research/README.md`, `practice/README.md`, and `community/README.md`. It added no resources. The root README became a navigation page, and the Chinese guide and contribution instructions were updated to link to the new destinations. The initial audit counts above describe the original layout; they are not validation results for the restructured directory.

Validation of the new layout confirmed that all 27 original resource descriptions and URLs were preserved verbatim, with one entry per resource. Lychee 0.24.2 passed 87 local-link occurrences with fragment checking enabled, and a separate full request run passed all 118 link occurrences (49 unique targets), with no errors, timeouts, or exclusions. Both workflow jobs now cover every Markdown page recursively.

## Ongoing review

The current resource map separates introductions and learning materials, research questions and papers, practical resource types, project exercises, and community entry points. Current content is selective; a topic's presence does not imply comprehensive coverage. The [2026-10-22 restructuring record](curation-notes/2026-10-22-navigation-restructure.md) documents the migration of the 55-entry starting collection. The subsequent [coverage expansion](curation-notes/2026-10-22-coverage-expansion.md) adds 26 resources, bringing the collection to 81, with linked source evidence for learning, research, and practical additions. Earlier review results above describe earlier layouts.

1. Review proposed additions against [the contribution criteria](../CONTRIBUTING.md). Record why the resource helps readers and disclose whether it was used or only inspected.
2. Review the weekly external-link report in GitHub Actions. Check failed URLs manually, follow legitimate project moves, and replace stale URLs with canonical destinations.
3. Revisit tool maintenance and dataset access notes when updating the list. Retain historically useful resources with explicit limitations.
4. Remove a resource if its relevance or provenance cannot be established. Explain the reason in the pull request or commit.
5. After substantive changes, inspect the rendered root README, start-here pages, canonical resource pages, and projects, including Chinese text, tables, navigation, and local cross-links. Preserve existing guide paths and heading anchors as short navigation pages when moving material.

The workflow runs local file and heading checks on pushes and pull requests. On Mondays at 02:00 UTC, and on manual dispatch, it additionally checks external URLs. External-link failures remain visible for review; publisher access restrictions are not globally ignored. The workflow produces a job summary and does not automatically add, remove, or endorse resources.

Scheduled checks depend on GitHub Actions being enabled and may be delayed or disabled under GitHub's scheduling policies. They support human curation; they do not verify scientific claims or promise future updates.
