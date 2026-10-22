# Contributing

Thank you for helping readers find useful NeuroAI resources. Suggest an addition with the resource issue template, or submit a focused pull request. Corrections and link repairs are welcome.

## What belongs here

A resource should connect neuroscience or cognition to AI through a concrete question, method, model, dataset, or evaluation. Suitable entries include introductory materials, informative research papers, documented tools, reusable neural data, and model-comparison benchmarks.

Explain what a reader can learn or do with the resource. Prefer the author, publisher, institution, or maintainer's page. General machine-learning libraries, broad neuroscience directories, promotional pages, and link collections without descriptions usually belong in a more general list.

## Before submitting

- Search the canonical entries in `learn/`, `topics/`, `resources/`, and `community/` for duplicates, including alternate titles and preprint versions.
- Open the destination and verify the resource name, scope, and authors or maintainers.
- For papers, verify the publication year and venue; identify preprints and perspectives explicitly. Link the published version or clearly label an author manuscript.
- For software, inspect the documentation, examples, license, and stated dependencies. Disclose if you have only reviewed documentation rather than used it.
- For datasets, check access conditions and permitted use. An accessible landing page does not imply unrestricted data access.
- Describe a specific benefit and any relevant limitations, such as an archived repository, closed submission server, or legacy dependencies.
- Disclose your relationship to a resource you created or maintain.

## Entry format

```text
- [Resource name](canonical URL) - One or two factual sentences explaining its purpose, NeuroAI relevance, and any important access or maintenance limitation.
```

For a paper, begin the description with `Author et al., year, *Venue*.` Match the surrounding style and write the description in your own words. Explain the resource's purpose, relevant background, and any important access or maintenance limits. Background guidance may apply to a whole section when its resources have similar requirements. Distinguish a perspective, a mathematical result, computational experiments, and neural or behavioral evidence where that distinction matters. Avoid star counts, citation counts, promotional claims, and unsupported statements of biological plausibility.

## Where to add an entry

Each resource has one canonical description. Choose its home by resource type and primary purpose, then link to that entry from related topics, pathways, and projects:

| Destination | What belongs here |
| --- | --- |
| [learn/README.md](learn/README.md) | Preparation, textbooks, field reviews, public lectures, courses, and tutorials. |
| [topics/README.md](topics/README.md) | Research papers and methods papers, grouped around scientific questions. |
| [resources/tools.md](resources/tools.md) | Software, simulators, analysis libraries, task environments, and data tooling. |
| [resources/datasets.md](resources/datasets.md) | Neural and behavioral datasets, collections, and archives. |
| [resources/benchmarks.md](resources/benchmarks.md) | Evaluation tasks, metrics, baselines, and submission or local-evaluation resources. |
| [community/README.md](community/README.md) | Related collections, research conversations, conferences, and training entry points. |

The root [README](README.md) and [resource index](resources/README.md) provide navigation. [Start here](start-here/README.md) and its [pathways](start-here/pathways.md) help readers choose an entry point. [Projects](projects/README.md) assemble exercises from canonical resources; include the goal, background, materials, steps, expected output, and interpretation limits. Describe an exercise as proposed unless you have actually run it and can document the run.

For a paper relevant to several themes, choose its closest primary question and add internal links from the others. Themes overlap: research questions, model families, algorithms, and measurement methods do not form one mutually exclusive taxonomy. Reuse a suitable section before adding another page, and explain any coverage gap without creating an empty topic directory.

Keep entry introductions accessible to readers crossing fields, and allow a no-code route when appropriate. Explain technical terms or link to the [bilingual glossary](start-here/glossary.md). The [Chinese guide](start-here/README.zh-CN.md) is an introduction and need not mirror every resource. Update routes and cross-links when a changed entry affects them.

The old `research/README.md`, `practice/README.md`, `docs/learning-paths.md`, and `docs/getting-started.zh-CN.md` paths are compatibility navigation. Add new descriptions to their current destinations, and retain existing heading anchors when changing those old pages.

## Validation

Check the Markdown preview and run these commands from the repository root with [lychee](https://github.com/lycheeverse/lychee) 0.24.2:

```sh
lychee --offline --include-fragments --no-progress './**/*.md'
lychee --no-progress --max-concurrency 4 --timeout 30 --max-retries 2 './**/*.md'
```

The first command checks local files and heading links. The second requests external URLs. A `403`, `429`, timeout, or publisher login redirect requires manual review: record the outcome rather than treating it as proof that the resource disappeared. Conversely, an HTTP `200` alone does not establish that the page still contains the intended material.

Pull requests run the local-link check. A weekly run and a manually triggered run also check external links, with results in the Actions job summary. See [curation notes](docs/curation.md).

## Licensing

By contributing original descriptions and curation to this list, you agree to release those contributions under the repository's [CC0 license](LICENSE). Link to third-party resources instead of copying their text, figures, or datasets. Their own licenses continue to apply.
