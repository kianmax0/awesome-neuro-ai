# Awesome NeuroAI [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Curated resources for understanding intelligence through neuroscience and artificial intelligence.

Explore how neural computation can inform AI, how artificial networks can model brains, and how to compare the two. This list emphasizes useful entry points, original research, documented tools, and data with a clear connection to NeuroAI.

[中文入门说明](docs/getting-started.zh-CN.md) · [Contributing](CONTRIBUTING.md) · [Curation notes](docs/curation.md)

## Contents

- [Start here](#start-here)
- [Reviews and foundations](#reviews-and-foundations)
- [Courses and tutorials](#courses-and-tutorials)
- [Comparing brains and models](#comparing-brains-and-models)
- [Learning rules and predictive coding](#learning-rules-and-predictive-coding)
- [Memory, planning, and decision-making](#memory-planning-and-decision-making)
- [Tools and environments](#tools-and-environments)
- [Datasets](#datasets)
- [Benchmarks](#benchmarks)
- [Related lists](#related-lists)
- [Contributing](#contributing)
- [License](#license)

## Start here

Choose a route based on the question you want to answer:

1. **What is NeuroAI?** Read Hassabis et al. and Zador et al. in [Reviews and foundations](#reviews-and-foundations), then work through the [Neuromatch NeuroAI course](#courses-and-tutorials).
2. **How well does a model explain brain activity?** Begin with representational similarity analysis and task-optimized visual models in [Comparing brains and models](#comparing-brains-and-models), then inspect a [Brain-Score benchmark](#benchmarks).
3. **How can neural mechanisms inform learning?** Compare the assumptions in [Learning rules and predictive coding](#learning-rules-and-predictive-coding). For a coding exercise, follow an official snnTorch tutorial in [Tools and environments](#tools-and-environments).
4. **How can networks model cognition?** Read Yang and Wang's primer, explore [memory and planning](#memory-planning-and-decision-making), and try a NeuroGym task from [Tools and environments](#tools-and-environments).

Python, linear algebra, probability, and basic neural-network training are useful prerequisites. The computational neuroscience and deep learning courses below provide background. The Chinese guide includes a suggested first exercise and a small glossary.

## Reviews and foundations

- [Neuroscience-Inspired Artificial Intelligence](https://www.columbia.edu/cu/appliedneuroshp/Papers/out.pdf) - Hassabis et al., 2017, *Neuron*. Reviews interactions between neuroscience and AI, including attention, memory, and learning; a broad introduction to the field. University-hosted full-text PDF.
- [Catalyzing next-generation Artificial Intelligence through NeuroAI](https://www.nature.com/articles/s41467-023-37180-x) - Zador et al., 2023, *Nature Communications*. A perspective arguing for neuroscience-informed AI and an embodied Turing test; useful for understanding a proposed research agenda.
- [A deep learning framework for neuroscience](https://www.nature.com/articles/s41593-019-0520-2) - Richards et al., 2019, *Nature Neuroscience*. Organizes neural-network models around objective functions, learning rules, and architectures, providing a framework for asking neuroscientific questions.
- [Artificial neural networks for neuroscientists: A primer](https://arxiv.org/abs/2006.01001) - Yang and Wang, 2020, *Neuron*. Introduces neural-network models of behavior and neural circuits, with accompanying tutorial code; links to the author preprint.

## Courses and tutorials

- [Neuromatch Academy: NeuroAI](https://neuroai.neuromatch.io/) - Open course materials and coding exercises on generalization, representations, architectures, and learning across natural and artificial intelligence.
- [Neuromatch Academy: Computational Neuroscience](https://compneuro.neuromatch.io/tutorials/intro.html) - Open coursebook covering neural data, dynamical systems, probabilistic modeling, and learning; useful preparation for NeuroAI.
- [Neuromatch Academy: Deep Learning](https://deeplearning.neuromatch.io/tutorials/intro.html) - Open coursebook with neural-network fundamentals and practical modeling exercises; useful preparation for readers coming from neuroscience.

## Comparing brains and models

- [Representational similarity analysis: connecting the branches of systems neuroscience](https://www.frontiersin.org/journals/systems-neuroscience/articles/10.3389/neuro.06.004.2008/full) - Kriegeskorte, Mur, and Bandettini, 2008, *Frontiers in Systems Neuroscience*. Introduces comparisons through representational dissimilarity matrices across models, brain regions, and measurement methods.
- [Performance-optimized hierarchical models predict neural responses in higher visual cortex](https://pmc.ncbi.nlm.nih.gov/articles/PMC4060707/) - Yamins et al., 2014, *PNAS*. Demonstrates how task-optimized visual models can predict neural responses in macaque V4 and IT; an entry point to task-driven modeling.
- [Brains and algorithms partially converge in natural language processing](https://www.nature.com/articles/s42003-022-03036-1) - Caucheteux and King, 2022, *Communications Biology*. Compares language-model representations with human fMRI and MEG responses, examining the roles of architecture, training, and word prediction.

Predictive fit and representational similarity measure particular aspects of agreement. Establishing a biological mechanism requires additional evidence beyond a good model-to-brain score.

## Learning rules and predictive coding

- [Predictive coding in the visual cortex: a functional interpretation of some extra-classical receptive-field effects](https://www.nature.com/articles/nn0199_79) - Rao and Ballard, 1999, *Nature Neuroscience*. A hierarchical visual model in which feedback carries predictions and feedforward signals carry residual errors.
- [Random synaptic feedback weights support error backpropagation for deep learning](https://www.nature.com/articles/ncomms13276) - Lillicrap et al., 2016, *Nature Communications*. Introduces feedback alignment and studies learning with fixed random feedback weights instead of exact transposed forward weights.
- [An Approximation of the Error Backpropagation Algorithm in a Predictive Coding Network with Local Hebbian Synaptic Plasticity](https://pmc.ncbi.nlm.nih.gov/articles/PMC5467749/) - Whittington and Bogacz, 2017, *Neural Computation*. Relates predictive-coding weight updates to backpropagation under specified assumptions; a starting point for studying local credit assignment.

## Memory, planning, and decision-making

- [Prefrontal cortex as a meta-reinforcement learning system](https://www.nature.com/articles/s41593-018-0147-8) - Wang et al., 2018, *Nature Neuroscience*. Uses recurrent meta-reinforcement learning to develop a theory of how prefrontal dynamics can support rapid adaptation.
- [A recurrent network model of planning explains hippocampal replay and human behavior](https://www.nature.com/articles/s41593-024-01675-7) - Jensen, Hennequin, and Mattar, 2024, *Nature Neuroscience*. Models when an agent benefits from planning and compares its rollouts with human behavior and rodent hippocampal replay.

## Tools and environments

- [NeuroGym](https://github.com/neurogym/neurogym) - Neuroscience-inspired behavioral tasks with a shared Gymnasium interface for training and comparing agents and neural-network models.
- [PsychRNN](https://github.com/murraylab/PsychRNN) - Cognitive-task and recurrent-network modeling toolkit. Its documented testing matrix uses older Python and TensorFlow releases; check compatibility before choosing it for a new project.
- [snnTorch](https://github.com/jeshraghian/snntorch) - PyTorch-based spiking neural networks with surrogate-gradient learning, neuron models, and worked tutorials.
- [SpikingJelly](https://github.com/fangwei123456/spikingjelly) - PyTorch framework for spiking neural networks, ANN-to-SNN conversion, and event-based datasets; use documentation matching the installed release.
- [Meta NeuroAI suite](https://github.com/facebookresearch/neuroai) - NeuralSet data loaders, NeuralFetch dataset retrieval, NeuralTrain training, and NeuralBench evaluation tools for neural-data research.

## Datasets

- [Natural Scenes Dataset](https://naturalscenesdataset.org/) - Human 7T fMRI recordings from eight participants viewing natural images, supporting visual encoding, decoding, and brain–model comparisons. Data access requires an agreement.
- [Allen Brain Observatory](https://alleninstitute.github.io/brain_observatory_ecosystem/) - Mouse visual-system datasets spanning two-photon imaging and Neuropixels recordings, with separate Visual Coding and Visual Behavior collections.

## Benchmarks

- [Brain-Score](https://www.brain-score.org/) - Evaluates computational models against neural and behavioral measurements. Inspect the specific datasets, metrics, and evaluation procedures behind each score.
- [Neural Latents Benchmark](https://neurallatents.github.io/) - Datasets, baselines, and tools for evaluating latent-variable models of neural population activity. EvalAI submissions closed in January 2026; the project provides test data for local evaluation.

## Related lists

- [Awesome NeuroAI Papers](https://github.com/CYHSM/awesome-neuro-ai-papers) - A broader reading list of papers and reviews at the intersection of deep learning and neuroscience.
- [NeuroAI Trainee Resources](https://github.com/8erberg/NeuroAI_Trainee_Resources) - Training resources and community entry points for students exploring NeuroAI.
- [Awesome Computational Neuroscience](https://github.com/kianmax0/awesome-computational-neuroscience) - Companion collection covering mathematical models, neural computation, simulation tools, and neural-data analysis.

## Contributing

Suggest a resource or a correction through an issue or pull request. Include its original source, a short explanation of its NeuroAI relevance, and any access or maintenance limitations. See the [contribution guidelines](CONTRIBUTING.md) for selection criteria and the [curation notes](docs/curation.md) for the maintenance process.

## License

The original list text and curation are released under [CC0 1.0 Universal](LICENSE). Linked publications, datasets, software, and third-party marks retain their own licenses and terms.
