# Practice: tools, data, and evaluation

[Home](../README.md) · [Learn](../learn/README.md) · [Research](../research/README.md) · [Practice](../practice/README.md) · [Community](../community/README.md)

> Find software, recordings, and benchmarks for a concrete exercise or research project.

**For:** Readers ready to run a tutorial, build a model, or compare it with neural or behavioral data.

**Start with:** Choose a task or question, then select a tool and an evaluation. Access and compatibility notes appear next to each resource.

| You need to… | Go to | What is included |
| --- | --- | --- |
| Build or train a model | [Tools and environments](#tools-and-environments) | Cognitive tasks, recurrent networks, spiking networks, neural-data infrastructure. |
| Find neural recordings | [Datasets](#datasets) | Human visual fMRI and mouse visual-system recordings. |
| Evaluate a model | [Benchmarks](#benchmarks) | Brain–model comparisons and latent neural population models. |

## Tools and environments

### Cognitive tasks and recurrent networks

Define behavioral tasks and study how neural-network models solve them.

- [NeuroGym](https://github.com/neurogym/neurogym) - Neuroscience-inspired behavioral tasks with a shared Gymnasium interface for training and comparing agents and neural-network models.
- [PsychRNN](https://github.com/murraylab/PsychRNN) - Cognitive-task and recurrent-network modeling toolkit. Its documented testing matrix uses older Python and TensorFlow releases; check compatibility before choosing it for a new project.

### Spiking neural networks

Build and train networks whose neurons communicate through spikes.

- [snnTorch](https://github.com/jeshraghian/snntorch) - PyTorch-based spiking neural networks with surrogate-gradient learning, neuron models, and worked tutorials.
- [SpikingJelly](https://github.com/fangwei123456/spikingjelly) - PyTorch framework for spiking neural networks, ANN-to-SNN conversion, and event-based datasets; use documentation matching the installed release.

### Neural-data infrastructure

Load datasets and organize model training and evaluation.

- [Meta NeuroAI suite](https://github.com/facebookresearch/neuroai) - NeuralSet data loaders, NeuralFetch dataset retrieval, NeuralTrain training, and NeuralBench evaluation tools for neural-data research.

## Datasets

Neural recordings for fitting and comparing models. Check each dataset's access conditions and experimental design before use.

- [Natural Scenes Dataset](https://naturalscenesdataset.org/) - Human 7T fMRI recordings from eight participants viewing natural images, supporting visual encoding, decoding, and brain–model comparisons. Data access requires an agreement.
- [Allen Brain Observatory](https://alleninstitute.github.io/brain_observatory_ecosystem/) - Mouse visual-system datasets spanning two-photon imaging and Neuropixels recordings, with separate Visual Coding and Visual Behavior collections.

## Benchmarks

Evaluation suites define particular tasks, measurements, and metrics. Choose one that matches your research question.

- [Brain-Score](https://www.brain-score.org/) - Evaluates computational models against neural and behavioral measurements. Inspect the specific datasets, metrics, and evaluation procedures behind each score.
- [Neural Latents Benchmark](https://neurallatents.github.io/) - Datasets, baselines, and tools for evaluating latent-variable models of neural population activity. EvalAI submissions closed in January 2026; the project provides test data for local evaluation.

## Where to go next

Use [Research](../research/README.md) to connect an evaluation to a scientific claim, or follow the first exercise in the [Chinese beginner guide](../docs/getting-started.zh-CN.md).
