# Topics: questions across NeuroAI

[Home](../README.md) · [Start here](../start-here/README.md) · [Learn](../learn/README.md) · [Topics](README.md) · [Resources](../resources/README.md) · [Projects](../projects/README.md) · [Community](../community/README.md)

> Start with a scientific question, then follow it across models, methods, measurements, and practical resources.

NeuroAI questions overlap. A study of memory can also ask how a model learns, how it represents a task, and whether its activity resembles neural data. The topics below are entry points, not exclusive categories. **Architecture**, **algorithm**, and **measurement** are crosscutting dimensions: compare what a network is made of, how it learns or computes, and what evidence is used to assess it.

Current coverage includes visual, auditory, and language brain-model comparison, multisensory inference, learning rules, recurrent dynamics, memory, reinforcement learning, continual learning, and embodied models. The selections connect computational hypotheses with neural or behavioral measurements where available. Coverage remains selective; useful expansion areas include sensory and motor development, causal tests of model mechanisms, and cross-species or naturalistic neural data.

| Scientific question | Start with |
| --- | --- |
| How do models and brains represent sensory input? | [Perception and representations](#perception-and-representations) |
| Which properties of artificial networks agree with neural measurements? | [Comparing brains and models](#comparing-brains-and-models) |
| How can predictions and feedback support learning? | [Learning rules and predictive coding](#learning-rules-and-predictive-coding) |
| How can recurrent systems support memory, planning, and decisions? | [Memory, planning, and decision-making](#memory-planning-and-decision-making) |
| How can learning continue without erasing earlier skills? | [Generalization and adaptation](#generalization-and-adaptation) |
| How do recurrent activity and circuit mechanisms shape computation? | [Neural dynamics and circuit computation](#neural-dynamics-and-circuit-computation) |
| How do bodies and environments shape intelligent behavior? | [Embodied intelligence](#embodied-intelligence) |

## Comparing brains and models

**Question:** Which properties of a model agree with neural measurements, and how do we measure that agreement?

**Overview:** Models can be compared with neural responses or with one another at the level of representational geometry. These comparisons answer different questions: predictive fit asks whether model activity predicts measured responses, while representational similarity asks whether patterns of relationships among stimuli are alike. Neither alone establishes that the model uses the same mechanism as a brain.

**Background and start reading:** Begin with the [modeling foundations in Learn](../learn/README.md#reviews-and-foundations), then read Kriegeskorte et al. for representational similarity analysis (RSA). Continue with Yamins et al. for task-optimized visual models, then choose Caucheteux and King for language, Kell et al. in [Perception and representations](#perception-and-representations) for audition, or Kornblith et al. for CKA.

**Selected papers:**

- [Representational similarity analysis: connecting the branches of systems neuroscience](https://www.frontiersin.org/journals/systems-neuroscience/articles/10.3389/neuro.06.004.2008/full) - Kriegeskorte, Mur, and Bandettini, 2008, *Frontiers in Systems Neuroscience*. Introduces comparisons through representational dissimilarity matrices across models, brain regions, and measurement methods.
- [Performance-optimized hierarchical models predict neural responses in higher visual cortex](https://pmc.ncbi.nlm.nih.gov/articles/PMC4060707/) - Yamins et al., 2014, *PNAS*. Demonstrates how task-optimized visual models can predict neural responses in macaque V4 and IT; an entry point to task-driven modeling.
- [Brains and algorithms partially converge in natural language processing](https://www.nature.com/articles/s42003-022-03036-1) - Caucheteux and King, 2022, *Communications Biology*. Compares language-model representations with human fMRI and MEG responses, examining the roles of architecture, training, and word prediction.
- [Similarity of Neural Network Representations Revisited](https://proceedings.mlr.press/v97/kornblith19a.html) - Kornblith et al., 2019, *ICML*. **Method and model experiments.** Develops centered kernel alignment (CKA) for comparing learned representations and examines how the invariances of a similarity measure affect its interpretation. Read alongside RSA before choosing a model-comparison metric; this paper's experiments compare artificial networks.

**Related resources:** Use [Net2Brain](../resources/tools.md#net2brain) for documented model-to-brain comparison workflows and [Narratives](../resources/datasets.md#narratives) for a language-fMRI reading route. The [Algonauts Project](../resources/benchmarks.md#algonauts-project) offers another encoding-model evaluation setting; inspect its data and completed-challenge status before planning an exercise.

**Project next steps:** Choose a stimulus set and a measured response, make a model prediction before inspecting the comparison, and state which result would count against the model. Compare at least one alternative architecture or objective and report the limits of the measurement.

**Bounded research questions:** Does the model predict responses to held-out stimuli or held-out subjects? Which transformations leave the chosen similarity score unchanged, and are those transformations relevant to the scientific claim? Does the same ranking of models hold across neural regions or measurement methods?

## Perception and representations

**Question:** How do computational models represent sensory input, combine cues, and predict perception?

**Overview:** Perception research connects sensory input, internal representations, and neural or behavioral measurements. The papers below offer three different approaches: hierarchical prediction, task-optimized auditory networks, and probabilistic inference about whether cues share a source. Agreement with perception or brain responses must be separated from evidence about the underlying implementation.

**Background and start reading:** Start with sensory-system and network-modeling foundations in [Learn](../learn/README.md#neuroscience-and-modeling-textbooks). Read Rao and Ballard for hierarchical prediction, Kell et al. for task-optimized auditory modeling, or Körding et al. for a probabilistic model of multisensory behavior. Basic conditional probability helps with the latter; use the [comparison methods above](#comparing-brains-and-models) when evaluating neural agreement.

**Selected papers:**

- [Predictive coding in the visual cortex: a functional interpretation of some extra-classical receptive-field effects](https://www.nature.com/articles/nn0199_79) - Rao and Ballard, 1999, *Nature Neuroscience*. A hierarchical visual model in which feedback carries predictions and feedforward signals carry residual errors.
- [A Task-Optimized Neural Network Replicates Human Auditory Behavior, Predicts Brain Responses, and Reveals a Cortical Processing Hierarchy](https://mcdermottlab.mit.edu/papers/Kell_etal_2018_DNN_auditory_cortex.pdf) - Kell et al., 2018, *Neuron*. **Model, human behavior, and fMRI comparison; author-hosted published PDF.** Optimizes a network for word and musical-genre recognition, then compares its errors and layer representations with human measurements. Extends task-driven sensory modeling to audition; predictive agreement does not identify a unique cortical implementation. [Published article](https://doi.org/10.1016/j.neuron.2018.03.044).
- [Causal Inference in Multisensory Perception](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0000943) - Körding et al., 2007, *PLOS ONE*. **Computational theory and human psychophysics.** Models whether auditory and visual cues arise from one source or separate sources, accounting for partial cue integration in spatial localization. A compact entry into Bayesian multisensory modeling; the paper tests behavioral predictions and leaves the neural implementation open.

**Related resources:** [Net2Brain](../resources/tools.md#net2brain) supplies a route into representation comparisons. For an auditory spiking-classification exercise, inspect [Spiking Heidelberg Datasets](../resources/datasets.md#spiking-heidelberg-datasets): their input events come from a cochlear model, rather than recorded neurons. The [bilingual glossary](../start-here/glossary.md) clarifies recurring modeling terms.

**Project next steps:** Use [Compare a paper and its figures](../projects/README.md#compare-a-paper-and-its-figures) to separate model, behavioral, and neural evidence. For a computational comparison, specify the input statistics, represented quantities, and prediction, then compare matched alternatives. The [representation project](../projects/README.md#compare-model-representations) is a route into layer comparisons.

**Bounded research questions:** Which receptive-field effects follow from the model's assumptions? Does an auditory model predict held-out sounds beyond its training categories? When do cue discrepancies favor integration or segregation? Which measurements distinguish the proposed computation from an alternative with matched behavioral performance?

## Learning rules and predictive coding

**Question:** How can networks use predictions and feedback to change their weights?

**Overview:** Learning-rule studies ask how a system assigns credit to synapses and which signals, connections, or timing assumptions are needed. A local update expression is one part of the account; the origin and delivery of its learning signals also matter.

**Background and start reading:** Read Richards et al. and Yang and Wang in [Learn](../learn/README.md#reviews-and-foundations), then use Lillicrap et al. (2020) as a conceptual entry on credit assignment. Clopath et al. offers a separate route into modeling synaptic-plasticity observations. Compare one rule at a time, stating its signals and purpose; an objective approximation and a fit to plasticity protocols are different claims.

**Selected papers:**

- [Backpropagation and the brain](https://www.cs.toronto.edu/~hinton/absps/backpropandbrain.pdf) - Lillicrap et al., 2020, *Nature Reviews Neuroscience*. **Perspective; author-hosted PDF.** Explains the credit-assignment problem and argues that feedback-induced activity differences could approximate gradient signals. A useful conceptual entry point, with proposed implementations rather than a demonstration that cortex uses backpropagation. [Publisher record](https://www.nature.com/articles/s41583-020-0277-3).
- [Random synaptic feedback weights support error backpropagation for deep learning](https://www.nature.com/articles/ncomms13276) - Lillicrap et al., 2016, *Nature Communications*. Introduces feedback alignment and studies learning with fixed random feedback weights instead of exact transposed forward weights.
- [An Approximation of the Error Backpropagation Algorithm in a Predictive Coding Network with Local Hebbian Synaptic Plasticity](https://pmc.ncbi.nlm.nih.gov/articles/PMC5467749/) - Whittington and Bogacz, 2017, *Neural Computation*. Relates predictive-coding weight updates to backpropagation under specified assumptions; a starting point for studying local credit assignment.
- [A solution to the learning dilemma for recurrent networks of spiking neurons](https://www.nature.com/articles/s41467-020-17236-y) - Bellec et al., 2020, *Nature Communications*. **Learning algorithm and model experiments.** Introduces e-prop, combining synaptic eligibility traces with learning signals to train recurrent spiking networks online. Use it to examine temporal credit assignment, the approximation to backpropagation through time, and which signals would require biological validation.
- [Connectivity reflects coding: a model of voltage-based STDP with homeostasis](https://infoscience.epfl.ch/record/144104) - Clopath et al., 2010, *Nature Neuroscience*. **Learning-rule model and simulations; institutional full-text record.** Combines presynaptic spikes, postsynaptic voltage, and homeostasis to model plasticity protocols and study how input coding affects recurrent connectivity. Complements task-driven credit assignment with a phenomenological synaptic rule; matching selected plasticity observations does not establish a universal learning mechanism. [Publisher record; subscription preview](https://www.nature.com/articles/nn.2479).

**Related resources:** Explore [spiking neural network tools](../resources/tools.md#spiking-neural-networks) and [cognitive task and recurrent network tools](../resources/tools.md#cognitive-tasks-and-recurrent-networks). [NeuroBench](../resources/benchmarks.md#neurobench) provides an efficiency-evaluation route; check the chosen workload and metric definitions separately from biological claims. The [glossary](../start-here/glossary.md) and [Learn foundations](../learn/README.md#reviews-and-foundations) provide background on learning rules and objectives.

**Project next steps:** Use [Inspect a spiking mechanism](../projects/README.md#inspect-a-spiking-mechanism) to trace a rule's signals and compare controlled input protocols. For a task-driven rule, compare learning quality, timing, and required information under a shared task. Keep the optimizer, credit-assignment procedure, and biological claim distinct.

**Bounded research questions:** Under what assumptions do the updates approximate gradient descent? Which nonlocal signals are required and how are they computed? Does a rule continue to work when feedback, recurrent state, or neural timing constraints change?

## Memory, planning, and decision-making

**Question:** How do learned representations support prediction, adaptation, planning, and value-based decisions?

**Overview:** These studies connect learned state or value representations with behavior over time. Successor representations, recurrent meta-learning, relational memory, planning, and distributional value coding address related questions while making different assumptions about experience, state, reward, and task structure.

**Background and start reading:** Use the [computational neuroscience and modeling textbooks](../learn/README.md#neuroscience-and-modeling-textbooks) for reinforcement-learning and recurrent-network background. Start with Stachenfeld et al.'s predictive-map account, then choose spatial memory, rapid adaptation, relational generalization, or replay and planning. Dabney et al. adds a route from reward-prediction errors to distributions of future reward; read it with the distinction between a mean and a probability distribution in mind.

**Selected papers:**

- [The hippocampus as a predictive map](https://gershmanlab.com/pubs/Stachenfeld17.pdf) - Stachenfeld, Botvinick, and Gershman, 2017, *Nature Neuroscience*. **Computational theory and model results; author-hosted PDF.** Uses the successor representation, which summarizes expected future state occupancy, to account for properties of hippocampal place representations and propose a role for entorhinal grid cells. Distinguish the model's predictions from evidence that the brain implements the proposed learning rule. [Publisher record, including correction](https://www.nature.com/articles/nn.4650).
- [Prefrontal cortex as a meta-reinforcement learning system](https://www.nature.com/articles/s41593-018-0147-8) - Wang et al., 2018, *Nature Neuroscience*. Uses recurrent meta-reinforcement learning to develop a theory of how prefrontal dynamics can support rapid adaptation.
- [A recurrent network model of planning explains hippocampal replay and human behavior](https://www.nature.com/articles/s41593-024-01675-7) - Jensen, Hennequin, and Mattar, 2024, *Nature Neuroscience*. Models when an agent benefits from planning and compares its rollouts with human behavior and rodent hippocampal replay.
- [The Tolman-Eichenbaum Machine: Unifying Space and Relational Memory through Generalization in the Hippocampal Formation](https://discovery.ucl.ac.uk/id/eprint/10115119/) - Whittington et al., 2020, *Cell*. **Model and neural-data comparison; institutional full text.** Separates relational structure from sensory information to model generalization across environments and spatial and nonspatial representations. Includes a test of predicted structural transfer using simultaneously recorded place and grid cells; agreement with these measurements leaves other model assumptions open to testing.

- [A distributional code for value in dopamine-based reinforcement learning](https://willdabney.com/publication/distributions_from_dopamine/) - Dabney et al., 2020, *Nature*. **Computational theory and mouse neural recordings; author abstract and shared-reading link.** Derives predictions from distributional reinforcement learning, which represents multiple possible reward outcomes, and tests them against dopamine-neuron responses. Connects an AI value-learning idea to neural measurements without establishing every component of its biological implementation. [Publisher record](https://www.nature.com/articles/s41586-019-1924-6).

**Related resources:** Try a task from [cognitive task and recurrent network tools](../resources/tools.md#cognitive-tasks-and-recurrent-networks), find neural data through the [datasets index](../resources/datasets.md), and check available [benchmarks](../resources/benchmarks.md). The [glossary](../start-here/glossary.md) supports unfamiliar terms.

**Project next steps:** Fix the task and information available to the agent, then compare a memory or planning model with a simpler baseline. Record behavioral performance and, when relevant, a neural prediction before analysis.

**Bounded research questions:** Which task structures favor cached predictions over explicit rollouts? What evidence distinguishes rapid within-task adaptation from a changed representation? Does a model predict held-out relational or spatial transfer?

## Generalization and adaptation

**Question:** How can learning continue across changing tasks while retaining earlier abilities?

**Overview:** Sequential learning can fail through interference: adapting parameters to new data may reduce performance on older tasks. Weight protection and replay are distinct strategies, and generalization across related tasks can change how much either strategy is needed. Their comparison depends on the task sequence, memory budget, and test-time information.

**Background and start reading:** The [NeuroAI course](../learn/README.md#courses-and-tutorials) introduces generalization and learning. Read Kirkpatrick et al. for weight protection, van de Ven et al. for generative replay, or Flesch et al. for a human–network comparison of training schedules. Then choose an evaluation that makes the task sequence, representation, and memory assumptions explicit; related multitask representations appear in [Neural dynamics and circuit computation](#neural-dynamics-and-circuit-computation).

**Selected papers:**

- [Overcoming catastrophic forgetting in neural networks](https://arxiv.org/abs/1612.00796) - Kirkpatrick et al., 2017, *PNAS*. **Learning algorithm and model experiments; author manuscript on arXiv.** Introduces elastic weight consolidation (EWC), which penalizes changes to parameters estimated to matter for previous tasks. Connects synaptic consolidation to sequential classification and reinforcement learning; a computational analogy rather than direct evidence for EWC in biological synapses. [Published article](https://doi.org/10.1073/pnas.1611835114).
- [Brain-inspired replay for continual learning with artificial neural networks](https://www.nature.com/articles/s41467-020-17866-2) - van de Ven, Siegelmann, and Tolias, 2020, *Nature Communications*. **Learning algorithm and model experiments.** Studies generative replay and proposes replaying internal representations using context-modulated feedback. Complements weight protection with a rehearsal mechanism, while the proposed correspondence to biological replay remains a hypothesis.

- [Comparing continual task learning in minds and machines](https://ora.ox.ac.uk/objects/uuid%3A5f8eb699-735a-412b-a6fe-b288e02cf977) - Flesch et al., 2018, *PNAS*. **Human behavior and model experiments; institutional full-text record.** Compares blocked and interleaved learning of two categorization rules in people and neural networks, relating interference to learned representations. Adds a behavioral comparison to weight protection and replay; conclusions are bounded by the studied tasks and training schedules. [Published article](https://www.pnas.org/doi/10.1073/pnas.1800755115).

**Related resources:** [Avalanche](../resources/tools.md#avalanche) provides a continual-learning experiment framework, and [CORe50](../resources/benchmarks.md#core50) offers sequential object-learning protocols. Inspect each scenario's task boundaries and test information before comparing methods. Learning background is in [Learn](../learn/README.md#reviews-and-foundations).

**Project next steps:** Follow [Test sequential learning](../projects/README.md#test-sequential-learning) to compare weight protection, stored-example replay, and generative replay under a shared task sequence and memory budget. A reading comparison can instead examine blocked versus interleaved schedules in Flesch et al. Specify whether task identity is supplied at test time, whether classes accumulate, and how retention and new learning are measured; conclusions depend on that setup.

**Bounded research questions:** How does the result change when replay memory or parameter capacity is controlled? Which task similarities permit positive transfer rather than interference? Does a biological analogy make a testable prediction beyond matching an engineering score?

## Neural dynamics and circuit computation

**Question:** How do recurrent activity, circuit structure, and neural timescales support computation?

**Overview:** Population dynamics describe how neural activity changes over time; recurrent models can test how such activity supports a computation. The selected papers connect movement-related trajectories, context-dependent decisions, controlled pattern generation, and multitask representations. A useful distinction is between structure observed in recorded activity and a proposed circuit that generates it.

**Background and start reading:** Begin with [Neuronal Dynamics](../learn/README.md#neuroscience-and-modeling-textbooks) for mathematical foundations and [Yang and Wang's primer](../learn/README.md#reviews-and-foundations) for neural-network modeling. Basic linear algebra and differential equations help with the analyses. Read Churchland et al. for population trajectories, Mante et al. for a task-specific recurrent explanation, Sussillo and Abbott for training temporal outputs, or Yang et al. for multitask organization. For a spiking learning-mechanism connection, see e-prop in [Learning rules and predictive coding](#learning-rules-and-predictive-coding).

**Selected papers:**

- [Neural population dynamics during reaching](https://pmc.ncbi.nlm.nih.gov/articles/PMC3393826/) - Churchland et al., 2012, *Nature*. **Macaque neural recordings and population analysis; PMC author manuscript.** Uses jPCA to characterize rotational structure in motor and premotor population activity during reaching. Introduces a dynamical view of movement-related activity; rotations in a projection do not identify the circuit or feedback that generates them. [Publisher record](https://www.nature.com/articles/nature11129).
- [Context-dependent computation by recurrent dynamics in prefrontal cortex](https://neurophysics.ucsd.edu/courses/physics_171/Newsome_line_decision.pdf) - Mante et al., 2013, *Nature*. **Macaque recordings and trained recurrent model; institution-hosted published PDF.** Studies decisions based on either motion or color, using population analysis and a recurrent network to explain context-dependent selection and integration of evidence. The trained network supplies a candidate computation, rather than direct identification of the monkeys' learned circuitry. [Publisher record](https://www.nature.com/articles/nature12742).
- [Generating Coherent Patterns of Activity from Chaotic Neural Networks](https://www.snn.ru.nl/computational-neuroscience/paul/Generating%20coherent%20patterns%20of%20activity%20from%20chaotic%20neural%20networks%20-%20Sussillo%26Abbott%202009.pdf) - Sussillo and Abbott, 2009, *Neuron*. **Training method and model experiments; institution-hosted published PDF.** Introduces FORCE learning to shape initially chaotic recurrent networks into generators of controlled temporal outputs. Its error/readout units and information used by weight updates need separate assessment before a biological interpretation. [Published article](https://doi.org/10.1016/j.neuron.2009.07.018).
- [Task representations in neural networks trained to perform many cognitive tasks](https://www.cns.nyu.edu/wanglab/publications/pdf/yang.nn2019.pdf) - Yang et al., 2019, *Nature Neuroscience*. **Recurrent-model experiments and neural-data comparison; author-hosted published PDF.** Trains networks on 20 cognitive tasks and analyzes functional clusters, task relationships, and limited compositional representations. Compares selected task representations with monkey prefrontal data; explicit rule inputs and the training protocol constrain the biological interpretation. [Publisher record](https://www.nature.com/articles/s41593-018-0310-2).

**Related resources:** Use [cognitive task and recurrent network tools](../resources/tools.md#cognitive-tasks-and-recurrent-networks) to construct task models, or inspect [LFADS-torch](../resources/tools.md#lfads-torch) for latent population modeling, including its license limits. The [IBL Brainwide Map](../resources/datasets.md#ibl-brainwide-map) and [Neural Latents Benchmark](../resources/benchmarks.md#neural-latents-benchmark) offer recorded-data and evaluation routes. Check temporal resolution, population sampling, and behavioral conditions before framing a question.

**Project next steps:** Follow [Compare latent neural trajectories](../projects/README.md#compare-latent-neural-trajectories) to distinguish descriptive structure from held-out predictive performance, or [Compare models on a cognitive task](../projects/README.md#compare-models-on-a-cognitive-task) to test a recurrent computation. Define the neural timescale and alternative model before comparing activity or behavior; state what the data can resolve.

**Bounded research questions:** Which temporal features are necessary for the task? Does a circuit mechanism predict a measurable perturbation or activity pattern beyond behavioral fit? How sensitive is the proposed computation to the timescale and population sampling of the available data?

## Embodied intelligence

**Question:** What changes when a model must act through a body and interact with an environment?

**Overview:** Embodied models couple perception, action, and environmental feedback. They can test how bodily constraints shape behavior and internal representations, while agreement with neural measurements remains evidence for a model rather than proof of a unique biological implementation.

**Background and start reading:** Begin with Zador et al.'s NeuroAI agenda in [Learn](../learn/README.md#reviews-and-foundations). Read Banino et al. for learned navigation, then Aldarondo et al. for a biomechanical model compared with neural recordings.

**Selected papers:**

- [Vector-based navigation using grid-like representations in artificial agents](https://discovery.ucl.ac.uk/id/eprint/10048194/) - Banino et al., 2018, *Nature*. **Model experiments; institutional accepted manuscript.** Trains a recurrent path-integration network whose grid-like representations support a navigation agent, including shortcut behavior. A bridge between representation learning and spatial control; grid-like activity in a trained model does not establish the learning mechanism of biological grid cells. [Publisher record](https://www.nature.com/articles/s41586-018-0102-6).
- [A virtual rodent predicts the structure of neural activity across behaviours](https://pmc.ncbi.nlm.nih.gov/articles/PMC12080270/) - Aldarondo et al., 2024, *Nature*. **Embodied model and neural-data comparison; PMC author manuscript.** Trains a controller of a biomechanical rat model to imitate real rat movements and compares its activity with motor cortex and striatal recordings. Connects inverse dynamics and motor variability to neural measurements; predictive agreement supports testing control hypotheses without establishing a unique neural implementation. [Publisher record, including correction](https://www.nature.com/articles/s41586-024-07633-4).

**Related resources:** Inspect [MyoSuite](../resources/tools.md#myosuite) for musculoskeletal-control environments and the [datasets index](../resources/datasets.md) for behavior and neural recordings. The [project index](../projects/README.md) can help turn a question about a body or controller into a bounded exercise.

**Project next steps:** Separate the contributions of the body, sensory inputs, objective, and controller architecture. Compare matched models against both behavioral and neural measurements before interpreting a learned representation as a biological mechanism.

**Bounded research questions:** Which behaviors depend on body dynamics rather than a static input-output mapping? Does a model trained on one environment predict behavior or neural activity in another? Which perturbation would distinguish controller explanations that fit the same behavior?
