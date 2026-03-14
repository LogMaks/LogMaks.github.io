---
title: "A PhD Research Project: Hierarchical Decision-Making Under Uncertainty"
image: "/assets/post.jpg"
excerpt: "Recently Published Research: Reinforcement Learning Under Epistemic Uncertainty"
---

On a recently accepted paper, a proof-of-concept implementation, and the broader direction of the research

Recently the thoughts of Marvin had to step aside for a while: most of my time was devoted to working on research papers that will eventually form part of my PhD dissertation. Fortunately, the effort was worthwhile — the papers have been accepted after peer review. This makes it a good moment to briefly summarize the core ideas behind the research project and the direction in which it is evolving.

The main article can be found here:
https://www.elibrary.ru/item.asp?id=89021776

A proof-of-concept implementation is also available:
https://www.elibrary.ru/item.asp?id=88851718

If anyone is interested in reading the full versions, feel free to contact me.
Below is a short overview of the conceptual motivation behind the project.

## Decision-Making Under Uncertainty

At its core, the problem addressed in this research arises from a simple observation: humans constantly face decisions. Some are trivial, others are strategic, and many are made under incomplete information with consequences that unfold over time.
For this reason, decision theory should not be viewed merely as a managerial or applied discipline. Its foundations lie in mathematics — particularly in probability theory, statistics, stochastic processes, and optimization.
The main difficulty is that decisions rarely occur in fully known environments. Both humans and complex technical systems operate under uncertainty. In fact, uncertainty is not merely noise around an otherwise deterministic world — it is a fundamental property of real systems.
This is why plans often fail even when they appear logically sound: the environment does not necessarily evolve according to a simple linear model.
As a consequence, overly simplified models quickly reach their limits. Real systems evolve with delays, branching processes, hidden states, partial observability, and irregular timing of events. Therefore uncertainty should be treated not as a nuisance, but as a central object of analysis.
Closely related to uncertainty is the notion of entropy. While commonly known from physics, Shannon's information theory interprets entropy as a measure of uncertainty and the amount of information required to describe a system. The less predictable a system is, the more information is required to understand and manage it.

## Reinforcement Learning and Markov Decision Processes

This perspective naturally leads to reinforcement learning (RL) — one of the key paradigms of modern machine learning.
In general terms, reinforcement learning studies how an agent interacts with an environment, receives feedback in the form of rewards, and gradually learns strategies that maximize long-term performance.
However, RL is not merely about selecting profitable actions. It describes a dynamic process in which states, actions, observations, and rewards evolve over time.
A common introductory example is the multi-armed bandit problem. In this scenario, an agent must choose between several options without knowing in advance which one is best. The agent must simultaneously explore new possibilities and exploit accumulated knowledge.
This illustrates a fundamental tension in decision-making: the balance between exploration and exploitation.
Extending this idea leads to Markov decision processes (MDPs). In an MDP framework we consider:
- an agent
- an environment
- a set of states
- a set of actions
- a reward function

and a probabilistic transition function.

The transition function is particularly important. An action does not guarantee a specific outcome; instead, it changes the probability distribution of future states. This probabilistic structure makes the model far more realistic.The world does not respond deterministically. It responds with variability, delays, noisy observations, and unexpected deviations.

## Beyond Classical Reinforcement Learning

Despite its strength, classical RL is still insufficient for many real-world systems.
In practice: 

- the environment is only partially observable
- events occur at irregular times
- relevant variables may be hidden
- and computational resources are limited.

A simple state-action transition model is often not expressive enough to capture these realities. This is where the present research project begins. The goal is not to restate reinforcement learning theory, but to adapt it to real decision-making environments where uncertainty, time irregularity, and limited information are fundamental constraints. The practical motivation for this research lies in industrial maintenance and equipment management. In such contexts, the question of when to intervene in the operation of equipment is critical. Intervening too late can lead to failures and costly repairs, while intervening too early can waste resources and reduce operational efficiency.
The key question can be formulated simply: When should a system intervene in the operation of equipment in order to prevent failures while avoiding unnecessary resource expenditure?
In practice, this question is much more complex than it appears. Equipment rarely switches directly from "working" to "broken". Instead it degrades gradually, operates under changing loads, accumulates hidden defects, and may display ambiguous early signals of future failure. Therefore decisions must rely not only on current observations but also on predictions about possible future trajectories.

## Hierarchical Decision-Making

To address this challenge, the project introduces a separation between strategic and tactical levels of decision-making. This structure is closely related to hierarchical reinforcement learning. 
At the strategic level, the system operates with higher-level behavioral scenarios — often described as options in hierarchical RL. These represent classes of actions such as: 

- initiating preventive maintenance
- reallocating resources
- switching to a conservative operating mode
- postponing intervention
- preparing for repair operations.

At the tactical level, the system reacts to the immediate operational context: resource availability, local constraints, sensor signals, and evolving conditions in the environment.In simple terms:

- the strategic layer decides what general course of action should be taken
- the tactical layer decides how that action should be implemented in the current situation.

This separation is not merely conceptual elegance. It also addresses a practical computational issue. Flat decision spaces quickly become intractable as the number of states and actions grows. Hierarchical structures help organize the decision space and significantly reduce computational complexity. One of the central goals of the project is therefore not only to create an intelligent system, but also a computationally economical one.A theoretically optimal model that requires excessive computational resources is rarely useful in real engineering environments.

## Human-in-the-Loop

Another fundamental question arises in automated decision systems: Should machines be allowed to fully determine what constitutes a good or bad decision?
In critical technical systems, completely removing the human operator from the decision loop would be methodologically questionable.Machines may be consistent and computationally efficient, but humans still provide elements that algorithms struggle to replicate: contextual understanding, professional intuition, and the ability to interpret unusual situations beyond the available data. For this reason the project explicitly introduces a Human-in-the-Loop architecture. This mechanism does not simply allow an operator to confirm decisions. Instead it integrates human expertise directly into critical decision points. In this framework, the human is no longer an external supervisor of the algorithm. Rather, the operator becomes part of a coupled human-machine decision system. Decisions emerge from the interaction between computational models, observed data, and human judgement. In this sense automation does not replace the decision-maker but forms a symbiotic decision architecture that strengthens system reliability where purely statistical models may fall short.

## Toward Economical Decision Systems

Although the current research focuses primarily on hierarchical reinforcement learning, a natural extension of the work leads toward ideas related to Karl Friston's perspective on efficient behavior and uncertainty management. Friston's work emphasizes the importance of minimizing free energy — a concept that can be interpreted as a measure of surprise or uncertainty. In this view, effective decision-making is not just about maximizing rewards, but also about reducing uncertainty and maintaining computational economy. This perspective aligns with the goals of the current research project, which seeks to create a decision system that is not only effective but also computationally efficient and robust under uncertainty. This does not mean that the current project is built on active inference or the free-energy principle. Such a claim would be premature.However, the underlying logic of the research points toward a broader question: Can decision-making be understood not only as reward maximization, but also as a process of reducing uncertainty while maintaining computational economy?

In this view, effective decisions should balance:

- goal achievement
- uncertainty reduction
and the cost of representing and computing policies.

Future research may therefore move toward architectures where control systems operate as economical predictive-control loops, minimizing unnecessary complexity while maintaining reliable decision performance. Such a direction could connect hierarchical reinforcement learning with broader principles of information-efficient decision systems.

## Current Status and Next Steps

The acceptance of the article and the publication of the proof-of-concept represent an important milestone. They indicate that the conceptual framework has passed an initial stage of external evaluation.
However, this should not be seen as a final result. Rather, the project currently represents a transition from an internal research idea to a structured and publicly discussable framework. The next steps will involve further development of the theoretical model, more extensive simulations, and eventually real-world applications in industrial settings.The most important outcome at this stage is not the completion of the system, but the confirmation that the research direction is coherent, mathematically grounded, and practically motivated.
The broader vision is to create a decision system that can be applied in various domains where uncertainty, time irregularity, and limited information are fundamental challenges. This could include not only industrial maintenance but also areas such as healthcare, finance, and autonomous systems. The ultimate goal is to contribute to the development of intelligent decision systems that are both effective and computationally efficient, capable of operating reliably in complex and uncertain environments.