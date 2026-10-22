# Learn: foundations and courses

[Home](../README.md) · [Start here](../start-here/README.md) · [Learn](README.md) · [Topics](../topics/README.md) · [Resources](../resources/README.md) · [Projects](../projects/README.md) · [Community](../community/README.md)

> Understand what NeuroAI studies and build the background to explore it.

**For:** Readers starting from scratch, crossing over from one field, or looking for a deeper mathematical reference.

**Start with:** Choose your current background and goal in the [learning pathways](../start-here/pathways.md). For a first look without coding, start with [the field overview](../start-here/README.md), Brain Facts, or the [public lecture](#public-lectures). Use the Python tutorial when you want to work with code, or Hassabis et al. for a conceptual review.

| Section | What you will find |
| --- | --- |
| [Programming and mathematics](#programming-and-mathematics) | Coding essentials, mathematical prerequisites, and a probabilistic modeling reference. |
| [Neuroscience and modeling textbooks](#neuroscience-and-modeling-textbooks) | A nontechnical introduction, neuron models, nonlinear dynamics, and a deeper theoretical reference. |
| [Reinforcement learning and cognitive modeling](#reinforcement-learning-and-cognitive-modeling) | Reward-based learning and probabilistic accounts of human learning and reasoning. |
| [Public lectures](#public-lectures) | A recorded introduction to the connection between brains and AI, without coding. |
| [Reviews and foundations](#reviews-and-foundations) | Field overviews, a proposed research agenda, and introductions to neural-network modeling. |
| [Courses and tutorials](#courses-and-tutorials) | Guided study and coding exercises in NeuroAI, computational neuroscience, and deep learning. |

## Programming and mathematics

Use these to fill a specific gap before moving into NeuroAI; you do not need to finish every book.

**Background and outcome:** Start the Python tutorial when you need to read or write array-based code. Use Mathematics for Machine Learning to review the mathematics a chosen model requires. Probabilistic Machine Learning is a deeper reference after introductory linear algebra and probability. A useful first outcome is a labeled plot whose inputs, outputs, and array shapes you can explain.

- [Python NumPy Tutorial](https://cs231n.github.io/python-numpy-tutorial/) - Stanford CS231n introduction to Python, NumPy arrays, plotting, and notebooks. A practical coding entry point; the page provides Jupyter and Colab versions.
- [Mathematics for Machine Learning](https://mml-book.com/) - Deisenroth, Faisal, and Ong, 2020. Linear algebra, vector calculus, probability, and optimization for readers preparing to study machine-learning models. Free author-provided PDF and accompanying exercises.
- [Probabilistic Machine Learning: An Introduction](https://probml.github.io/pml-book/book1.html) - Murphy, 2022. A deeper reference for probabilistic modeling and machine learning, with an author-provided draft and code for figures. Useful after basic linear algebra and probability.

## Neuroscience and modeling textbooks

Start with the biological primer if the terminology is new, then select a modeling text at the mathematical depth you need.

**Background and outcome:** Brain Facts is the no-code entry point. For Neuronal Dynamics and Theoretical Neuroscience, use the mathematical sections relevant to your chosen neuron, circuit, or learning model. Dynamical Systems in Neuroscience develops geometric intuition for how model activity changes over time; basic calculus helps with the equations. Try to connect each model variable to a biological quantity and identify what the abstraction omits.

- [Brain Facts: A Primer on the Brain and Nervous System](https://www.brainfacts.org/book) - Society for Neuroscience introduction to brain structure and function for general readers and students. Free digital editions provide a starting point before mathematical modeling.
- [Neuronal Dynamics](https://neuronaldynamics.epfl.ch/online/) - Gerstner, Kistler, Naud, and Paninski. Free online textbook progressing from neuron models to population activity, learning, and cognition; useful for connecting neural mechanisms to equations.
- [Theoretical Neuroscience](https://www.gatsby.ucl.ac.uk/~dayan/book/) - Dayan and Abbott. Mathematical treatment of neural coding, neuron and circuit models, and plasticity. The author page offers exercises and a sample chapter; the full book requires library or purchased access.
- [Dynamical Systems in Neuroscience: The Geometry of Excitability and Bursting](https://izhikevich.org/publications/dsn/index.htm) - Izhikevich. Introduces nonlinear dynamics through neuron models, using geometric explanations of stability, oscillations, and bursting to prepare readers for dynamical models of neural computation. The author page provides a free full-book PDF and errata.

## Reinforcement learning and cognitive modeling

**Background and outcome:** Use basic probability for either text; calculus helps with the reinforcement-learning derivations, and the cognitive-modeling examples introduce WebPPL, a probabilistic programming language. Start by describing an agent's observations, actions, and rewards, or a cognitive model's hypotheses and observations, before following an algorithm. These are modeling frameworks whose claims about brains or behavior need separate evidence.

- [Reinforcement Learning: An Introduction](http://incompleteideas.net/book/the-book-2nd.html) - Sutton and Barto, 2018, second edition. Covers policies, value functions, temporal-difference learning, and connections to psychology and neuroscience; the author page provides the full PDF, code links, and errata.
- [Probabilistic Models of Cognition](http://probmods.org/) - Goodman, Tenenbaum, and the ProbMods Contributors, 2016, second edition. Free online text modeling learning and reasoning as probabilistic inference, with WebPPL examples spanning concept learning, causal reasoning, and social cognition; read the conceptual chapters before attempting the code.

## Public lectures

**Background and outcome:** No coding is needed for this recorded conversation. After watching, write down one proposed lesson from brains for AI and one question that would require further evidence.

- [LIVE At the Lab: NeuroAI: Learning from the brain and AI](https://www.cshl.edu/videos/live-at-the-lab-neuroai-learning-from-the-brain-and-ai/) - Cold Spring Harbor Laboratory webinar with Anthony Zador, 2022. Public 43-minute recording introducing how lessons from the brain could inform AI, followed by audience questions; an accessible first look before the more technical reviews below.

## Reviews and foundations

**Background and outcome:** Read the introductions and main figures of Hassabis et al. and Zador et al. for orientation; technical details can wait. For Richards et al., Yang and Wang, and Barak, basic neural-network concepts help; the dynamics text above supplies further mathematical background. Write a short note identifying a paper's question, model, objective, learning mechanism, and evidence; the [glossary](../start-here/glossary.md) explains these terms.

- [Neuroscience-Inspired Artificial Intelligence](https://www.columbia.edu/cu/appliedneuroshp/Papers/out.pdf) - Hassabis et al., 2017, *Neuron*. Reviews interactions between neuroscience and AI, including attention, memory, and learning; a broad introduction to the field. University-hosted full-text PDF.
- [Catalyzing next-generation Artificial Intelligence through NeuroAI](https://www.nature.com/articles/s41467-023-37180-x) - Zador et al., 2023, *Nature Communications*. A perspective arguing for neuroscience-informed AI and an embodied Turing test; useful for understanding a proposed research agenda.
- [A deep learning framework for neuroscience](https://www.nature.com/articles/s41593-019-0520-2) - Richards et al., 2019, *Nature Neuroscience*. Organizes neural-network models around objective functions, learning rules, and architectures, providing a framework for asking neuroscientific questions.
- [Artificial neural networks for neuroscientists: A primer](https://arxiv.org/abs/2006.01001) - Yang and Wang, 2020, *Neuron*. Introduces neural-network models of behavior and neural circuits, with accompanying tutorial code; links to the author preprint.
- [Recurrent neural networks as versatile tools of neuroscience research](https://doi.org/10.1016/j.conb.2017.06.003) - Barak, 2017, *Current Opinion in Neurobiology*. Review of trained recurrent networks and the analysis of their dynamics as tools for generating neuroscientific hypotheses, including open theoretical challenges; publisher full text may require library or purchased access.

## Courses and tutorials

**Background and outcome:** Choose computational neuroscience to connect recordings with models, deep learning to understand training and evaluation, or NeuroAI to connect the fields. Coding exercises need basic Python; use the preparation materials above where needed. Select one module and one explainable result before attempting a whole course. The [projects](../projects/README.md) provide bounded follow-ups.

- [Neuromatch Academy: NeuroAI](https://neuroai.neuromatch.io/) - Open course materials and coding exercises on generalization, representations, architectures, and learning across natural and artificial intelligence.
- [Neuromatch Academy: Computational Neuroscience](https://compneuro.neuromatch.io/tutorials/intro.html) - Open coursebook covering neural data, dynamical systems, probabilistic modeling, and learning; useful preparation for NeuroAI.
- [Neuromatch Academy: Deep Learning](https://deeplearning.neuromatch.io/tutorials/intro.html) - Open coursebook with neural-network fundamentals and practical modeling exercises; useful preparation for readers coming from neuroscience.

- [Dive into Deep Learning](https://d2l.ai/) - Interactive deep-learning textbook with code and notebooks covering model training, optimization, convolutional networks, and recurrent networks. Useful for learning the implementation skills needed to reproduce NeuroAI models.
- [Neuronal Dynamics: Python Exercises](https://neuronaldynamics-exercises.readthedocs.io/en/latest/) - Official companion exercises on integrate-and-fire neurons, Hopfield networks, Hebbian learning, working memory, and decision-making. Choose one documented exercise and check its package requirements before running it.

## Where to go next

Choose a [learning route](../start-here/pathways.md), explore a question in [Topics](../topics/README.md), or select a [project](../projects/README.md). The [Chinese beginner guide](../start-here/README.zh-CN.md) offers another entry point. Background requirements depend on the activity; conceptual reading and discussion can begin before coding or mathematical modeling.
