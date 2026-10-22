# Benchmarks and evaluations

[Home](../README.md) · [Start here](../start-here/README.md) · [Learn](../learn/README.md) · [Topics](../topics/README.md) · [Resources](README.md) · [Projects](../projects/README.md) · [Community](../community/README.md)

Choose an evaluation by its target measurement and task. A benchmark score is tied to its datasets, metrics, and evaluation procedure; check those details before interpreting a model comparison.

| Resource | Evaluation type | What it evaluates | Access or status |
| --- | --- | --- | --- |
| [Brain-Score](#brain-score) | Brain–model comparison, including neural and behavioral measurements | Computational models against neural and behavioral measurements | Inspect the datasets, metrics, and evaluation procedures behind each score. |
| [Neural Latents Benchmark](#neural-latents-benchmark) | Population modeling | Latent-variable models of neural population activity | EvalAI submissions closed in January 2026; test data are provided for local evaluation. |
| [FALCON](#falcon) | Neural decoding across recording sessions | Decoders with limited recalibration data | Official test evaluation uses EvalAI and Docker; some evaluation data are withheld. |
| [SENSORIUM](#sensorium) | Visual response prediction | Mouse visual-cortex responses to natural images (2022) and videos (2023) | Historical competition editions with elapsed deadlines; use released resources and check evaluation availability before planning a submission. |
| [Algonauts Project](#algonauts-project) | Multimodal brain encoding and generalization | Human fMRI responses to movies using visual, audio, and language inputs | The 2025 competition ended; the official site advertises indefinite post-challenge ID/OOD benchmarks. Data access uses a contact-and-terms form; submission operability was not tested. |
| [NeuroBench](#neurobench) | Neuromorphic algorithm and system evaluation | Task performance alongside memory footprint, sparsity, and operation counts | Algorithm examples support local evaluation; hardware energy/latency require the separate system-track protocol. Check dataset and optional-component terms. |
| [CORe50](#core50) | Continual object recognition | Retention and adaptation as object instances or classes arrive in batches | Released data and multiple-run protocols support local evaluation under CC BY 4.0; original baseline code uses Caffe, while the project links an Avalanche implementation. |

## Benchmark details

### Brain-Score

- [Brain-Score](https://www.brain-score.org/) - Evaluates computational models against neural and behavioral measurements. Inspect the specific datasets, metrics, and evaluation procedures behind each score.

### Neural Latents Benchmark

- [Neural Latents Benchmark](https://neurallatents.github.io/) - Datasets, baselines, and tools for evaluating latent-variable models of neural population activity. EvalAI submissions closed in January 2026; the project provides test data for local evaluation.

### FALCON

- [FALCON](https://snel-repo.github.io/falcon/) - Benchmark for testing neural decoders across recording sessions with limited recalibration data. The maintainer repository supplies dataset notebooks, baseline decoders, and local validation; official test evaluation uses EvalAI and Docker, with some evaluation data withheld.

### SENSORIUM

- [SENSORIUM](https://sensorium-competition.net/) - Benchmarks for predicting mouse visual-cortex responses to natural images (2022) and videos (2023), with datasets, baseline models, and starter notebooks. These are historical competition editions with elapsed deadlines; use their released resources and check evaluation availability before planning a submission.

### Algonauts Project

- [Algonauts Project](https://algonautsproject.com/2025/) - The 2025 edition evaluates models predicting human fMRI responses to multimodal movies, with visual frames, audio, transcripts, a development kit, and in-distribution/out-of-distribution tests. The competition has ended and data access uses a contact-and-terms form; the official site advertises indefinite post-challenge benchmarks, but their submission workflow was not tested here.

### NeuroBench

- [NeuroBench](https://neurobench.readthedocs.io/en/latest/) - Benchmark framework with local ANN/SNN examples that measure task performance alongside memory footprint, sparsity, and synaptic-operation counts, including speech and neural motor-prediction tasks. Hardware energy and latency require the separate system-track protocol; check dataset terms and the noncommercial license of the optional Speech2Spikes component.

### CORe50

- [CORe50](https://vlomonaco.github.io/core50/) - Continual object-recognition benchmark with RGB-D views of household objects, fixed test sessions, and multiple-run protocols for new instances, new classes, or both. Use the released batches to compare retention and adaptation; resources are CC BY 4.0, and the project links an Avalanche implementation alongside its original Caffe baselines.

## Where to continue

Browse [Comparing brains and models](../topics/README.md#comparing-brains-and-models) to connect model comparisons to a scientific question. The [project suggestions](../projects/README.md) help frame a bounded evaluation; [learning pathways](../start-here/pathways.md) point to background material.
