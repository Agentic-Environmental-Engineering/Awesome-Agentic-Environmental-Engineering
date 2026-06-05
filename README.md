# Agentic Environment Engineering for Large Language Models

<p align="center">
  <b>A survey of environment modeling, synthesis, evaluation, application, and agent-environment co-evolution.</b>
</p>

<p align="center">
  <a href="#overview"><img alt="Survey" src="https://img.shields.io/badge/Survey-Agentic%20Environment%20Engineering-2F855A"></a>
  <a href="#taxonomy-at-a-glance"><img alt="Taxonomy" src="https://img.shields.io/badge/Taxonomy-Lifecycle%20%2B%20Domains-2B6CB0"></a>
  <a href="resources/papers.md"><img alt="Resources" src="https://img.shields.io/badge/Resources-Curated%20Paper%20List-805AD5"></a>
  <a href="#citation"><img alt="Citation" src="https://img.shields.io/badge/Citation-BibTeX-D69E2E"></a>
</p>

<p align="center">
  <a href="#overview">Overview</a> |
  <a href="#taxonomy-at-a-glance">Taxonomy</a> |
  <a href="#curated-resources">Resources</a> |
  <a href="#citation">Citation</a> |
  <a href="CONTRIBUTING.md">Contributing</a>
</p>

<p align="center">
  <img src="assets/figures/overview.png" alt="Overview of agentic environment engineering" width="96%">
</p>

## Overview

Agentic environments are interactive systems in which large language model agents observe, act, receive feedback, and improve. They have become a key substrate for evaluating, training, and evolving LLM agents in realistic tasks such as web browsing, GUI control, tool use, code repair, embodied interaction, scientific discovery, and long-horizon planning.

This repository accompanies the survey **Agentic Environment Engineering for Large Language Models**. It organizes the field around the full environment engineering lifecycle: how environments are modeled, synthesized, evaluated, and used to drive agent-environment co-evolution.

> Paper status: the public PDF link will be added after the camera-ready PDF or arXiv version is available.

## What Is Agentic Environment Engineering?

Traditional data-centric development mainly provides static examples. Environment-centric development instead exposes an agent to an interactive world with observations, actions, tools, state transitions, and rewards. This shift enables:

| Perspective | From | To |
| --- | --- | --- |
| Learning signal | Static samples | Dynamic feedback |
| Interaction | Single-turn Q&A | Multi-turn tool and world interaction |
| System loop | Open-loop evaluation | Closed-loop agent-environment adaptation |
| Scaling unit | More data | More scenarios, dynamics, tasks, and rewards |

<p align="center">
  <img src="assets/figures/preliminaries.png" alt="From data engineering to environment engineering" width="82%">
</p>

## Taxonomy at a Glance

We structure agentic environments from three complementary views.

| View | Core question | Main categories |
| --- | --- | --- |
| Environment attributes | What properties define an environment? | symbolic/neural, open/closed loop, online/offline, MDP/POMDP, deterministic/nondeterministic, discrete/continuous, unimodal/multimodal, single/multi-agent |
| Environment domains | What task worlds do agents operate in? | GUI, deep research, embodied, game, tool, code, domain-specific, cross-domain |
| Environment lifecycle | How are environments built and used? | modeling, synthesis, quality control, agent evolution, environment evolution |

<p align="center">
  <img src="assets/figures/environment-attributes.png" alt="Environment attributes" width="86%">
</p>

## Environment Domains

Agentic environments cover diverse task worlds. The survey groups representative environments into eight domains: GUI, deep research, embodied, game, tool, code, domain-specific, and cross-domain.

<p align="center">
  <img src="assets/figures/environment-domains.png" alt="Environment domains" width="96%">
</p>

## Environment Synthesis and Evaluation

Environment synthesis aims to create scalable interactive worlds with reliable feedback.

| Direction | Description | Typical focus |
| --- | --- | --- |
| Symbolic synthesis | Uses explicit rules, programs, simulators, tools, or verifiers to construct environments. | correctness, controllability, executable feedback |
| Neural synthesis | Parameterizes environment dynamics through neural models or world models. | scalability, generativity, multimodal dynamics |
| Quality control | Measures whether synthesized environments are useful and trustworthy. | correctness, diversity, complexity, fidelity |

<p align="center">
  <img src="assets/figures/symbolic-synthesis.png" alt="Symbolic environment synthesis" width="88%">
</p>

<p align="center">
  <img src="assets/figures/neural-world-model.png" alt="Neural environment synthesis and world models" width="88%">
</p>

## Agent-Environment Co-Evolution

Environments are not only benchmarks. They can also drive agent improvement and evolve with the agent.

| Track | Representative mechanisms |
| --- | --- |
| Agent evolution | memory-centric experience evolution, orchestration-centric workflow evolution, trajectory-centric offline evolution, exploration-centric online evolution |
| Environment evolution | neural-driven evolution, difficulty-driven evolution, scaling-driven evolution |
| Co-evolution | adaptive task generation, curriculum design, self-play, environment scaling, online-offline learning loops |

<p align="center">
  <img src="assets/figures/agent-evolution.png" alt="Agent evolution in environments" width="90%">
</p>

<p align="center">
  <img src="assets/figures/environment-evolution.png" alt="Environment evolution" width="90%">
</p>

## Curated Resources

The curated paper list is maintained in [resources/papers.md](resources/papers.md). It follows the survey taxonomy and highlights representative work instead of mirroring the full bibliography.

Quick entry points:

| Resource | Description |
| --- | --- |
| [Curated paper list](resources/papers.md) | Representative environments, synthesis methods, evaluation work, and evolution methods. |
| [Original vector figures](assets/figures/pdf/) | Selected figures copied from the paper source as PDF, preserving the original content and style. |
| [Contribution guide](CONTRIBUTING.md) | Format for adding missing papers, benchmarks, environments, and project links. |
| [Paper folder](paper/) | Placeholder for the public survey PDF once released. |

## News

- 2026-06-05: Initial preview repository created with taxonomy figures, curated resources, and contribution guide.

## Citation

If this survey or repository is useful to your research, please cite:

```bibtex
@article{li2026agenticenvironmentengineering,
  title   = {Agentic Environment Engineering for Large Language Models},
  author  = {Li, Jiachun and Jin, Zhuoran and Men, Tianyi and Hao, Yupu and Zhu, Kejian and Wang, Lingshuai and Huang, Dongqi and Wang, Longxiang and Hua, Shengjia and Wang, Lu and Gao, Jinshan and Yuan, Hongbang and Xu, Ruilin and Liu, Kang and Zhao, Jun},
  journal = {Preprint},
  year    = {2026},
  note    = {Survey version v1, major update on May 19, 2026}
}
```

## Maintainers

This project is maintained by the authors of **Agentic Environment Engineering for Large Language Models**. For missing papers, broken links, or taxonomy suggestions, please open an issue or pull request.
