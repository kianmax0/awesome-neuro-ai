# Contributing

Thank you for helping readers find useful NeuroAI resources. Suggest an addition with the resource issue template, or submit a focused pull request. Corrections and link repairs are welcome.

## What belongs here

A resource should connect neuroscience or cognition to AI through a concrete question, method, model, dataset, or evaluation. Suitable entries include introductory materials, informative research papers, documented tools, reusable neural data, and model-comparison benchmarks.

Explain what a reader can learn or do with the resource. Prefer the author, publisher, institution, or maintainer's page. General machine-learning libraries, broad neuroscience directories, promotional pages, and link collections without descriptions usually belong in a more general list.

## Before submitting

- Search the topical pages in `learn/`, `research/`, `practice/`, and `community/` for duplicates, including alternate titles and preprint versions.
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

For a paper, begin the description with `Author et al., year, *Venue*.` Match the surrounding style. Keep one main entry per resource, use the closest existing section, and write the description in your own words. Avoid star counts, citation counts, promotional claims, and unsupported statements of biological plausibility.

## Where to add an entry

Each resource has one canonical entry on the closest topical page:

| Destination | Sections |
| --- | --- |
| [learn/README.md](learn/README.md) | Reviews and foundations; Courses and tutorials |
| [research/README.md](research/README.md) | Comparing brains and models; Learning rules and predictive coding; Memory, planning, and decision-making |
| [practice/README.md](practice/README.md) | Tools and environments; Datasets; Benchmarks |
| [community/README.md](community/README.md) | Related lists |

The root [README](README.md) provides navigation only. Add resource descriptions to the topical pages, and avoid repeating an entry across pages. The Chinese guide is an introduction, so it does not need to repeat every new entry. Update it when its learning routes or access notes would otherwise become misleading.

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
