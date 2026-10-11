# Research: questions and mechanisms

[Home](../README.md) · [Learn](../learn/README.md) · [Research](../research/README.md) · [Practice](../practice/README.md) · [Community](../community/README.md)

> Explore papers organized around the questions they help answer.

**For:** Readers who want to connect a scientific question to models, methods, and evidence.

**Start with:** Choose one question below. For modeling background, read Yang and Wang's primer in [Learn](../learn/README.md#reviews-and-foundations).

| Research question | Section | Main topics |
| --- | --- | --- |
| How well do artificial networks explain brain activity? | [Comparing brains and models](#comparing-brains-and-models) | Representational similarity, visual models, language models. |
| How can neural mechanisms inform learning algorithms? | [Learning rules and predictive coding](#learning-rules-and-predictive-coding) | Prediction errors, feedback alignment, local credit assignment. |
| How can networks model flexible behavior? | [Memory, planning, and decision-making](#memory-planning-and-decision-making) | Recurrent dynamics, meta-learning, planning, hippocampal replay. |

## Comparing brains and models

**Question:** Which properties of a model agree with neural measurements, and how do we measure that agreement?

- [Representational similarity analysis: connecting the branches of systems neuroscience](https://www.frontiersin.org/journals/systems-neuroscience/articles/10.3389/neuro.06.004.2008/full) - Kriegeskorte, Mur, and Bandettini, 2008, *Frontiers in Systems Neuroscience*. Introduces comparisons through representational dissimilarity matrices across models, brain regions, and measurement methods.
- [Performance-optimized hierarchical models predict neural responses in higher visual cortex](https://pmc.ncbi.nlm.nih.gov/articles/PMC4060707/) - Yamins et al., 2014, *PNAS*. Demonstrates how task-optimized visual models can predict neural responses in macaque V4 and IT; an entry point to task-driven modeling.
- [Brains and algorithms partially converge in natural language processing](https://www.nature.com/articles/s42003-022-03036-1) - Caucheteux and King, 2022, *Communications Biology*. Compares language-model representations with human fMRI and MEG responses, examining the roles of architecture, training, and word prediction.

Predictive fit and representational similarity measure particular aspects of agreement. Establishing a biological mechanism requires additional evidence beyond a good model-to-brain score.

**Next step:** Inspect a [Brain-Score benchmark](../practice/README.md#benchmarks) and its evaluation procedure.

## Learning rules and predictive coding

**Question:** How can networks use predictions and feedback to change their weights?

- [Predictive coding in the visual cortex: a functional interpretation of some extra-classical receptive-field effects](https://www.nature.com/articles/nn0199_79) - Rao and Ballard, 1999, *Nature Neuroscience*. A hierarchical visual model in which feedback carries predictions and feedforward signals carry residual errors.
- [Random synaptic feedback weights support error backpropagation for deep learning](https://www.nature.com/articles/ncomms13276) - Lillicrap et al., 2016, *Nature Communications*. Introduces feedback alignment and studies learning with fixed random feedback weights instead of exact transposed forward weights.
- [An Approximation of the Error Backpropagation Algorithm in a Predictive Coding Network with Local Hebbian Synaptic Plasticity](https://pmc.ncbi.nlm.nih.gov/articles/PMC5467749/) - Whittington and Bogacz, 2017, *Neural Computation*. Relates predictive-coding weight updates to backpropagation under specified assumptions; a starting point for studying local credit assignment.

**Next step:** Compare each rule's assumptions, required signals, and feedback connections. The [Chinese guide](../docs/getting-started.zh-CN.md) distinguishes mathematical, computational, and biological evidence.

## Memory, planning, and decision-making

**Question:** How can recurrent networks adapt their behavior and decide when to plan?

- [Prefrontal cortex as a meta-reinforcement learning system](https://www.nature.com/articles/s41593-018-0147-8) - Wang et al., 2018, *Nature Neuroscience*. Uses recurrent meta-reinforcement learning to develop a theory of how prefrontal dynamics can support rapid adaptation.
- [A recurrent network model of planning explains hippocampal replay and human behavior](https://www.nature.com/articles/s41593-024-01675-7) - Jensen, Hennequin, and Mattar, 2024, *Nature Neuroscience*. Models when an agent benefits from planning and compares its rollouts with human behavior and rodent hippocampal replay.

**Next step:** Explore a cognitive task using [NeuroGym](../practice/README.md#cognitive-tasks-and-recurrent-networks).
