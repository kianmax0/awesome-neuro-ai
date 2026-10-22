# Pathways through NeuroAI

[Home](../README.md) · [Start here](README.md) · [Learn](../learn/README.md) · [Topics](../topics/README.md) · [Resources](../resources/README.md) · [Projects](../projects/README.md) · [Community](../community/README.md)

Choose a route by the outcome you want. The routes are modular: skip material you already know, and use only the optional preparation that helps with your next step.

## Machine learning to neuroscience

**First outcome:** Explain what a model predicts about a neural measurement, what data support that prediction, and what the comparison cannot establish.

**Optional preparation:** Review neural recordings and neuron or circuit models in [Neuroscience and modeling textbooks](../learn/README.md#neuroscience-and-modeling-textbooks) if those are unfamiliar. You can begin with a paper and its figures before learning the modeling details.

1. Choose a question under [comparing brains and models](../topics/README.md#comparing-brains-and-models) or [perception and representations](../topics/README.md#perception-and-representations). You can study visual, auditory, or multisensory examples; the measurement and task determine what the model comparison means.
2. Read one entry paper's abstract, task description, and main figures. Identify the neural data, model inputs and outputs, comparison baseline, and evaluation measure.
3. Inspect the relevant [representation-analysis tools](../resources/tools.md#representation-analysis) or [benchmark](../resources/benchmarks.md) to see what is measured and how results are evaluated.
4. State separately whether the model predicts behavior, neural responses, or both. Note which alternative model or explanation remains plausible.

**Optional next step:** Use the [model-representation comparison project](../projects/README.md#compare-model-representations) if you want to compare two artificial models before adding neural data.

## Neuroscience to machine learning

**First outcome:** Describe a behavioral or neural task as explicit inputs, outputs, objective, and evaluation conditions, then explain what an artificial model learns under those conditions.

**Optional preparation:** Review vectors, probability, or optimization in [Programming and mathematics](../learn/README.md#programming-and-mathematics) only as needed. If coding is new, start with the Python/NumPy material there and follow a small official example before changing a model.

1. Choose a question under [learning rules and predictive coding](../topics/README.md#learning-rules-and-predictive-coding) or [memory, planning, and decision-making](../topics/README.md#memory-planning-and-decision-making).
2. Define the task: what information is available at each step, what response is required, and how success is measured.
3. Follow a course exercise or tool example from [Learn](../learn/README.md#courses-and-tutorials) or [cognitive tasks and recurrent networks](../resources/tools.md#cognitive-tasks-and-recurrent-networks).
4. Compare the model with a simple alternative under the same task and evaluation conditions. Report what changed, what stayed fixed, and what the result says about the model rather than the biological system.

**Optional next step:** Use the [cognitive task and recurrent-network project](../projects/README.md#compare-models-on-a-cognitive-task) to make the comparison concrete.

For reward-driven behavior, use [Reinforcement learning and cognitive modeling](../learn/README.md#reinforcement-learning-and-cognitive-modeling) to distinguish the task's rewards, a model's value estimates, and its learning signals. For time-dependent activity, pair the recurrent-network review in [Learn](../learn/README.md#reviews-and-foundations) with the papers under [Neural dynamics and circuit computation](../topics/README.md#neural-dynamics-and-circuit-computation).

## For students

**First outcome:** Produce a one-page reading note with a research question, task, model, evidence, and one limitation.

Pick the missing foundation rather than completing every resource. Use [Brain Facts](../learn/README.md#neuroscience-and-modeling-textbooks) for introductory biology; use [Programming and mathematics](../learn/README.md#programming-and-mathematics) for coding or quantitative gaps; use [Reviews and foundations](../learn/README.md#reviews-and-foundations) for an overview; then choose one [topic](../topics/README.md). If you already have a paper-reading habit, start at the topic and look up background only when a term or method blocks you.

For a first coding outcome, plot how a simple model's output changes with one parameter. Label its input, output, axes, and units where applicable, and explain its array shapes. Continue to a [project](../projects/README.md) when you can explain the result and rerun the example.

## For builders

**First outcome:** Run one documented example and record a comparison you can rerun.

Choose a [project](../projects/README.md) and define its observable output before selecting [software](../resources/tools.md), [data](../resources/datasets.md), or a [benchmark](../resources/benchmarks.md). Start from the smallest relevant official example and inspect its setup, data permissions, and computational requirements. Record versions, configuration, seeds when applicable, data splits, and the command used. Compare with a stated baseline under matched conditions, then explain one result and one limitation. If a remote benchmark is unavailable, use a documented local evaluation where one is provided and state which protocol you used.

## For researchers

**First outcome:** Draft a short comparison brief that could distinguish at least two explanations.

Start from a question in [Topics](../topics/README.md), then inspect the closest papers and relevant [data](../resources/datasets.md), [benchmarks](../resources/benchmarks.md), and [tools](../resources/tools.md). Specify the task, comparison models, training and evaluation conditions, metric, and interpretation of positive, null, or reversed results. The [research comparison brief](../projects/README.md#write-a-research-comparison-brief) provides a compact structure. Separate predictive fit from evidence for a biological mechanism.

## Choose a focused modeling route

| Question you want to work on | Reading and practical entry | A bounded next step |
| --- | --- | --- |
| How do models explain sensory and language responses? | [Perception](../topics/README.md#perception-and-representations), [Narratives](../resources/datasets.md#narratives), [Net2Brain](../resources/tools.md#net2brain), and [Algonauts](../resources/benchmarks.md#algonauts-project) | Compare models using matched stimuli and an explicitly defined held-out target. |
| What computation is captured by neural population dynamics? | [Dynamics papers](../topics/README.md#neural-dynamics-and-circuit-computation), [population-model tools](../resources/tools.md#neural-population-dynamics), and [population evaluation](../resources/benchmarks.md#neural-latents-benchmark) | [Compare latent neural trajectories](../projects/README.md#compare-latent-neural-trajectories). |
| How do learning rules retain past experience? | [Generalization and adaptation](../topics/README.md#generalization-and-adaptation), [Avalanche](../resources/tools.md#avalanche), and [CORe50](../resources/benchmarks.md#core50) | [Test retention alongside new learning](../projects/README.md#test-sequential-learning). |
| What role do spikes, plasticity, and timing play? | [Learning rules](../topics/README.md#learning-rules-and-predictive-coding), [spiking tools](../resources/tools.md#spiking-neural-networks), and [converted auditory events](../resources/datasets.md#spiking-heidelberg-datasets) | [Change one specified mechanism](../projects/README.md#inspect-a-spiking-mechanism) under a fixed input protocol. |
| How do body mechanics shape behavior? | [Embodied intelligence](../topics/README.md#embodied-intelligence) and [MyoSuite](../resources/tools.md#myosuite) | Compare a specified controller or input condition while holding the environment and evaluation fixed. |

## For teaching

**First outcome:** Help learners compare two claims or models and identify what evidence would change their interpretation.

Use [Learn](../learn/README.md) to select a reading or course segment, then choose a question from [Topics](../topics/README.md). For a no-code class, pair a paper's figures with the [paper and figure comparison](../projects/README.md#compare-a-paper-and-its-figures). For a coding class, select one official example listed in [Resources](../resources/README.md) and make its inputs, outputs, and evaluation visible. Ask learners to distinguish a model result from a claim about how brains work. Adjust the mathematics and programming to the course; neither is a universal prerequisite for discussing the evidence.
