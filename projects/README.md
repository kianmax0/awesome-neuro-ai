# NeuroAI projects

[Home](../README.md) · [Start here](../start-here/README.md) · [Learn](../learn/README.md) · [Topics](../topics/README.md) · [Resources](../resources/README.md) · [Projects](README.md) · [Community](../community/README.md)

These are bounded exercises for reading, comparing, and planning. They do not claim that this repository has run an official example or reproduced a published result. When a project uses a tutorial or tool, follow its official instructions and record what you actually did.

| Choose an activity | Useful background | Output |
| --- | --- | --- |
| [Compare a paper and its figures](#compare-a-paper-and-its-figures) | No coding | One-page evidence table |
| [Compare model representations](#compare-model-representations) | Activations, distances, and an example you can inspect or run | Two RDMs and a comparison note |
| [Compare models on a cognitive task](#compare-models-on-a-cognitive-task) | Python and basic model training | Matched task comparison and behavior plot |
| [Inspect a spiking mechanism](#inspect-a-spiking-mechanism) | Basic programming and model equations | One controlled parameter or rule comparison |
| [Test sequential learning](#test-sequential-learning) | Basic model training and evaluation | A task-by-training-stage performance matrix |
| [Compare latent neural trajectories](#compare-latent-neural-trajectories) | Arrays, basic statistics, and neural time series | A held-out comparison of population models |
| [Write a research comparison brief](#write-a-research-comparison-brief) | Reading research papers | Question, alternatives, and evaluation plan |

## Compare a paper and its figures

**Goal:** Explain what a paper asks, what its figures show, and how far the evidence supports its main claim.

**Background:** No coding required. Basic familiarity with reading scientific figures helps but is not essential.

**Inputs:** One paper linked from [Topics](../topics/README.md), its abstract, methods summary, main figures, and figure captions.

**Steps:**

1. Write the research question in one sentence.
2. For each main figure, note the task or data, the comparison, the measured outcome, and the reported result.
3. Mark which evidence is behavioral, neural, or computational, and which panels are controls or model analyses.
4. List one alternative explanation or missing comparison. Check whether the discussion acknowledges it.

**Outputs:** A one-page table or note that separates question, method, result, interpretation, and limitation.

**Interpretation:** A figure can support a narrow comparison without establishing a unique mechanism. State which claim is supported by which measurement, and what additional evidence would be needed for a stronger claim.

## Compare model representations

**Goal:** Compare how two models or two layers relate a shared set of inputs, without treating a similarity score as proof of biological equivalence.

**Background:** Familiarity with activations and pairwise distances is useful. If coding is new, first inspect an official course or tool example; this project does not require changing its implementation.

**Inputs:** The same stimuli in the same order, activations from two models or layers, and a chosen distance measure. See [representation-analysis tools](../resources/tools.md#representation-analysis) and [comparison papers](../topics/README.md#comparing-brains-and-models).

**Steps:**

1. Record the stimulus set, preprocessing, layer or feature chosen, and any feature normalization.
2. For each model, compute pairwise distances among the same stimuli to form a representational dissimilarity matrix (RDM).
3. Check that the stimulus order matches and that each matrix has the same dimensions. Exclude diagonal entries.
4. Compare only corresponding entries in one triangle, such as the upper triangle. Do not count both `(i, j)` and `(j, i)`: they repeat the same pair in a symmetric matrix.
5. Report the distance and matrix-comparison measure, sample count, and any uncertainty or repeated-run analysis.

**Outputs:** Two labeled RDMs, a comparison value or plot, and a short methods note with the exact matched entries.

**Interpretation:** Similar RDMs indicate that the chosen systems preserve similar pairwise relations for these inputs under these analysis choices. They do not show that the internal units or learning mechanisms are the same. Adding neural measurements requires a suitable dataset and evaluation design. Fit any mapping on data separate from its evaluation, and explain how repeated-measurement reliability or a noise ceiling is handled; see [datasets](../resources/datasets.md) and [benchmarks](../resources/benchmarks.md).

## Compare models on a cognitive task

**Goal:** Ask whether two models solve the same task under matched conditions, and describe how their performance and behavior differ.

**Background:** Basic Python and model-training familiarity are useful. Readers without these prerequisites can complete the paper-and-figure project instead.

**Inputs:** A documented task from [cognitive tasks and recurrent networks](../resources/tools.md#cognitive-tasks-and-recurrent-networks), its official example or baseline, and a simple comparison model or condition.

For a body-dependent task, the [embodied-control tools](../resources/tools.md#embodied-control) offer another entry. Record the environment, observations, action representation, and body or muscle constraints alongside the controller.

**Steps:**

1. Define observations, actions or responses, feedback, trial structure, and the success measure.
2. Choose a baseline and comparison before training. Keep the task, data conditions, and evaluation procedure matched.
3. Follow the official example instructions. Record versions, configuration, random seeds, training budget, and any deviations; the repository has not run the example for you.
4. Evaluate on the specified held-out conditions. Inspect example behavior as well as aggregate performance.
5. Note whether differences could arise from model capacity, training time, or other unmatched choices.

**Outputs:** A short comparison report with task definition, model conditions, evaluation results, variability across runs when available, and one behavior plot or example.

**Interpretation:** Better task performance supports a claim about performance under the evaluated conditions. It does not alone explain brain activity or establish a cognitive mechanism. To make a brain comparison, specify the neural measurement and evaluation separately.

## Inspect a spiking mechanism

**Goal:** Understand how one specified neuron, synapse, or learning-rule change affects a spiking model's activity or task behavior.

**Background:** Basic programming and comfort with equations are helpful. Start with a documented exercise in [Neuronal Dynamics](../learn/README.md#neuroscience-and-modeling-textbooks) or an official example in [spiking-neural-network tools](../resources/tools.md#spiking-neural-networks).

**Inputs:** One official exercise or model, fixed input protocol, one parameter or learning-rule condition to vary, and a predefined observable such as spike timing or task performance.

For an event-input task, inspect the [Spiking Heidelberg Datasets](../resources/datasets.md#spiking-heidelberg-datasets) and distinguish converted input events from biological recordings. If evaluating computational cost, follow a specified [NeuroBench](../resources/benchmarks.md#neurobench) protocol and keep algorithm metrics separate from measurements on actual hardware.

**Steps:**

1. Read the model equations and identify the changed quantity and its role.
2. Record the official example's stated setup and follow its instructions. Do not infer unreported settings.
3. Keep the input protocol and other settings fixed while changing one selected quantity.
4. Compare spike trains, activity summaries, or task performance using an appropriate measure; repeat runs if the setup is stochastic.
5. Connect the observed change to the proposed mechanism and list other explanations that remain possible.

**Outputs:** A brief methods record, parameter comparison, activity or performance figure, and an interpretation tied to the specified model.

**Interpretation:** The result describes the selected model and conditions. It is not direct evidence that biological neurons use the modeled mechanism. Report the exact official example and any changes; this repository does not claim the example has been executed.

## Test sequential learning

**Goal:** Measure both new learning and retention when a model encounters tasks or experiences sequentially.

**Background:** Basic model training, data splits, and repeated-run evaluation. Read the weight-protection and replay papers in [Generalization and adaptation](../topics/README.md#generalization-and-adaptation).

**Inputs:** A documented sequential-learning protocol such as [CORe50](../resources/benchmarks.md#core50), one baseline, and one weight-protection or replay method. [Avalanche](../resources/tools.md#avalanche) provides a practical implementation entry. Check the protocol's task boundaries, class availability, and whether task identity is given during evaluation.

**Steps:**

1. Specify the task sequence and fixed training and test partitions before training. State whether experiences arrive once or can be revisited.
2. Match model capacity and training budget. Account for stored examples, replay generators, auxiliary statistics, and other method-specific memory.
3. After each training stage, evaluate every task seen so far using the same test protocol. Retain the complete performance matrix rather than only a final average.
4. Report acquisition of each new task alongside changes in earlier-task performance. Repeat with recorded seeds and, when feasible, more than one task ordering.
5. Explain which assumptions would change if task boundaries or task labels were unavailable.

**Outputs:** A task-by-stage performance matrix, a retention and acquisition plot, and a methods note defining budgets, protocol, seeds, and any deviations from the documented example.

**Interpretation:** A method's ranking is conditional on its task sequence, supervision, memory, and evaluation protocol. Its connection to biological consolidation or replay is a separate hypothesis to assess against neural or behavioral evidence.

## Compare latent neural trajectories

**Goal:** Test whether a learned population model captures held-out neural activity, and examine how its latent trajectories relate to a task or behavior.

**Background:** Arrays, probability, and neural time series. Start from [Neural dynamics and circuit computation](../topics/README.md#neural-dynamics-and-circuit-computation), then inspect the [population-modeling benchmark](../resources/benchmarks.md#neural-latents-benchmark).

**Inputs:** A documented neural-population dataset and evaluation protocol, a simple baseline, and a [latent-model implementation](../resources/tools.md#neural-population-dynamics). Inspect the selected implementation's license and setup before choosing it. Use the dataset's intended split and measurement units.

**Steps:**

1. Record the task, recorded population, trial structure, binning, preprocessing, and available behavioral variables.
2. Choose the evaluation target and training partition before fitting. Fit preprocessing and any alignment on training data only.
3. Compare a simple baseline with a latent model under a stated capacity and training budget. Follow the benchmark's procedure for predicting held-out trials, time intervals, or neurons; specify which form of generalization is tested.
4. Evaluate predictive performance and variability before interpreting a trajectory plot. Keep fitting, model selection, and final testing separate.
5. Plot a small set of labeled trajectories and explain how coordinate choices, dimensionality, and preprocessing affect their appearance.

**Outputs:** A held-out evaluation table, a labeled trajectory figure, and a record of data partitions, model settings, seeds, and the official procedure followed.

**Interpretation:** A visually structured trajectory is a description of a fitted representation. A claim about circuit computation requires predictions that distinguish mechanisms under the relevant measurements and comparisons.

## Write a research comparison brief

**Goal:** Turn a broad NeuroAI interest into a question and comparison that can separate plausible explanations.

**Background:** Ability to read research papers. Coding or data access is not required to draft the brief.

**Inputs:** A question from [Topics](../topics/README.md), the closest papers, and any relevant [dataset](../resources/datasets.md), [benchmark](../resources/benchmarks.md), or [tool](../resources/tools.md).

**Steps:**

1. State the question and the closest prior result. Name the uncertainty that remains.
2. Describe at least two explanations and what each predicts under the same conditions.
3. Specify matched task, model, data, training, and evaluation conditions, including the comparison baseline.
4. Define the metric, data split, and how variation or measurement reliability will be handled.
5. State what positive, null, or reversed outcomes would support and what they would leave unresolved.

**Outputs:** A one- to two-page brief with question, rationale, comparison table, evaluation plan, and bounded interpretation.

**Interpretation:** A good plan makes the inference conditional on specified data and comparisons. Prediction of neural responses, success on a task, and evidence for a biological mechanism are distinct outcomes and should be reported separately.
