# Tools and infrastructure

[Home](../README.md) · [Start here](../start-here/README.md) · [Learn](../learn/README.md) · [Topics](../topics/README.md) · [Resources](README.md) · [Projects](../projects/README.md) · [Community](../community/README.md)

Tools here cover task design, recurrent and spiking models, representation analysis, and neural-data workflows. Compare purpose and requirements before choosing a tool, then follow its setup instructions and a documented example matching your task.

| Need | Resource | What it supports | What you need or should check |
| --- | --- | --- | --- |
| Define and compare cognitive-task agents or models | [NeuroGym](#neurogym) | Neuroscience-inspired tasks through a shared Gymnasium interface | Choose a task and an agent or model to train and compare; follow the repository setup instructions. |
| Work with cognitive tasks and recurrent networks | [PsychRNN](#psychrnn) | Cognitive-task and recurrent-network modeling | Check compatibility with its documented older Python and TensorFlow testing matrix before choosing it for a new project. |
| Infer latent dynamics from population recordings | [lfads-torch](#lfads-torch) | LFADS models, held-out neural prediction, and single- or multi-session examples | License limits use to internal noncommercial research and prohibits modification or derivative works; review its older pinned dependencies. |
| Train spiking networks in PyTorch | [snnTorch](#snntorch) | Surrogate-gradient learning, neuron models, and tutorials | Follow the project setup and tutorial instructions. |
| Build spiking networks or convert ANNs | [SpikingJelly](#spikingjelly) | Spiking networks, ANN-to-SNN conversion, and event-based datasets | Use documentation matching the installed release. |
| Simulate neuron, synapse, or plasticity equations | [Brian 2](#brian-2) | Equation-based spiking-network simulation | Tutorials introduce simulation step by step; use compatibility guidance for the chosen release. |
| Load event-based vision or audio data | [Tonic](#tonic) | Event-dataset loaders and transformations | Pair with an SNN framework; it is data tooling, not a network trainer. Check dataset terms. |
| Compare representational geometries | [rsatoolbox](#rsatoolbox) | Dissimilarity matrices, model comparisons, noise ceilings, and uncertainty estimates | Demos cover basic workflows and neuroimaging modalities; follow project setup instructions. |
| Learn embeddings from neural activity | [CEBRA](#cebra) | Contrastive neural embeddings using time or auxiliary behavioral variables | APIs can change; version 0.4.0 onward uses Apache 2.0, earlier releases have academic-use terms, and the project discloses patents. |
| Extract model features and compare them with brain responses | [Net2Brain](#net2brain) | Feature extraction, dissimilarity matrices, RSA, and encoding analyses | Check the chosen model family's dependencies and its model/data terms; some model collections require Linux. |
| Compare learning rules under sequential experience | [Avalanche](#avalanche) | Replay, elastic weight consolidation (EWC), and accuracy/forgetting metrics | Specify the stream, task-label availability, and memory budget; dataset terms are separate from the library's MIT license. |
| Study muscle-driven control and adaptation | [MyoSuite](#myosuite) | MuJoCo musculoskeletal environments, sensory feedback, and motor-control tasks | Match documentation, environment version, and training backend; some environment changes require retraining older policies. |
| Assemble neural-data research workflows | [Meta NeuroAI suite](#meta-neuroai-suite) | Loaders, dataset retrieval, training, and evaluation tools | Follow the suite's repository setup instructions. |

## Cognitive tasks and recurrent networks

Define behavioral tasks and study how neural-network models solve them.

### NeuroGym

- [NeuroGym](https://github.com/neurogym/neurogym) - Neuroscience-inspired behavioral tasks with a shared Gymnasium interface for training and comparing agents and neural-network models.

### PsychRNN

- [PsychRNN](https://github.com/murraylab/PsychRNN) - Cognitive-task and recurrent-network modeling toolkit. Its documented testing matrix uses older Python and TensorFlow releases; check compatibility before choosing it for a new project.

## Neural population dynamics

Infer low-dimensional dynamics from many simultaneously recorded neurons, then evaluate predictions on held-out activity. Inferred latent states depend on the model and are not direct measurements of circuit mechanisms.

### lfads-torch

- [lfads-torch](https://github.com/arsedler9/lfads-torch) - PyTorch implementation of latent factor analysis via dynamical systems (LFADS), with neural-population denoising, single- and multi-session examples, and Neural Latents Benchmark integration. Its license restricts use to internal noncommercial research and prohibits modification or derivative works; check its older pinned dependencies before reuse.

## Spiking neural networks

Build and train networks whose neurons communicate through spikes.

### snnTorch

- [snnTorch](https://github.com/jeshraghian/snntorch) - PyTorch-based spiking neural networks with surrogate-gradient learning, neuron models, and worked tutorials.

### SpikingJelly

- [SpikingJelly](https://github.com/fangwei123456/spikingjelly) - PyTorch framework for spiking neural networks, ANN-to-SNN conversion, and event-based datasets; use documentation matching the installed release.

### Brian 2

- [Brian 2](https://brian2.readthedocs.io/en/stable/) - Equation-based spiking-network simulator for testing neuron, synapse, and plasticity mechanisms. Tutorials introduce simulation step by step; use the compatibility guidance for the release you choose.

### Tonic

- [Tonic](https://tonic.readthedocs.io/en/latest/) - Loaders and transformations for event-based vision and audio datasets, with an N-MNIST first example and tutorials on event representations. Pair it with an SNN framework; it is data tooling, not a network trainer, and dataset terms vary.

## Representation analysis

Compare model features with brain or behavioral measurements, or learn embeddings of neural activity. An embedding or a good fit alone does not establish a biological mechanism.

### rsatoolbox

- [rsatoolbox](https://rsatoolbox.readthedocs.io/en/stable/) - Python tools for representational similarity analysis: construct dissimilarity matrices, compare model predictions with measured representations, and estimate noise ceilings or uncertainty. Demos cover basic workflows and neuroimaging modalities.

### CEBRA

- [CEBRA](https://cebra.ai/docs/) - Contrastive learning of neural embeddings using time or auxiliary behavioral variables, with worked hippocampal, visual-cortex, and decoding notebooks. APIs can change between versions; version 0.4.0 onward uses Apache 2.0, earlier releases have academic-use terms, and the project discloses patents.

### Net2Brain

- [Net2Brain](https://net2brain.readthedocs.io/en/latest/) - Extract features from pretrained models, construct representational dissimilarity matrices, and compare them with brain responses using RSA or encoding analyses. Tutorials connect these stages; check model-specific dependencies and reuse terms, since some model collections require Linux.

## Continual learning

Test how learning new experiences changes performance on earlier ones. The stream, access to task labels, and replay memory are part of the experimental design.

### Avalanche

- [Avalanche](https://avalanche.continualai.org/) - PyTorch framework for comparing continual-learning strategies such as replay and elastic weight consolidation (EWC), with shared data streams and accuracy, transfer, and forgetting metrics. Use it to test learning-rule tradeoffs under a stated experience sequence and memory budget; dataset licenses remain separate from the MIT-licensed library.

## Embodied control

Study how a controller interacts with a simulated body and its sensory feedback. Task success in a simulator does not establish that the controller matches biological motor learning.

### MyoSuite

- [MyoSuite](https://myosuite.readthedocs.io/en/latest/) - MuJoCo musculoskeletal environments for studying reaching, manipulation, locomotion, and adaptation to muscle changes, with neuroscience tutorials and trained-policy examples. Match the documentation to the environment and backend you use; documented environment changes can require retraining older policies.

## Neural-data infrastructure

Load datasets and organize model training and evaluation.

### Meta NeuroAI suite

- [Meta NeuroAI suite](https://github.com/facebookresearch/neuroai) - NeuralSet data loaders, NeuralFetch dataset retrieval, NeuralTrain training, and NeuralBench evaluation tools for neural-data research.
