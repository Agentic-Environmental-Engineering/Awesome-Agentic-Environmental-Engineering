# Agentic Environment Engineering for Large Language Models

<p align="center">
  <b>A survey of environment modeling, synthesis, evaluation, and application for LLM agents.</b>
</p>

<p align="center">
  <a href="https://arxiv.org/abs/2606.12191"><img alt="arXiv" src="https://img.shields.io/badge/arXiv-2606.12191-B31B1B"></a>
  <a href="#introduction"><img alt="Survey" src="https://img.shields.io/badge/Survey-Agentic%20Environment%20Engineering-2F855A"></a>
  <a href="#environment-attribute"><img alt="Taxonomy" src="https://img.shields.io/badge/Taxonomy-Attributes%20%2B%20Domains-2B6CB0"></a>
  <a href="#citation"><img alt="Citation" src="https://img.shields.io/badge/Citation-Cite%20Our%20Survey-D69E2E"></a>
</p>

<p align="center">
  <a href="#news">News</a> |
  <a href="#table-of-content">Table of Content</a> |
  <a href="#introduction">Introduction</a> |
  <a href="#preliminaries">Preliminaries</a> |
  <a href="#environment-attribute">Attributes</a> |
  <a href="#environment-domain">Domains</a> |
  <a href="#environment-synthesis-and-evaluation">Synthesis</a> |
  <a href="#agent-evolution">Agent Evolution</a> |
  <a href="#environment-evolution">Environment Evolution</a> |
  <a href="#challenges--future-directions">Future Directions</a> |
  <a href="#citation">Citation</a> |
  <a href="#contact">Contact</a>
</p>

<p align="center">
  <img src="assets/figures/overview.png" alt="Overview of agentic environment engineering" width="96%">
</p>

## News

- [June 10, 2026]: Our survey paper is available on arXiv. [Paper](https://arxiv.org/abs/2606.12191)

## Table of Content

- [News](#news)
- [Introduction](#introduction)
- [Preliminaries](#preliminaries)
- [Environment Attribute](#environment-attribute)
- [Environment Domain](#environment-domain)
- [Environment Synthesis and Evaluation](#environment-synthesis-and-evaluation)
- [Agent Evolution](#agent-evolution)
- [Environment Evolution](#environment-evolution)
- [Challenges & Future Directions](#challenges--future-directions)
- [Citation](#citation)
- [Contact](#contact)

## Introduction

We maintain this repository as the public companion to our survey **Agentic Environment Engineering for Large Language Models: A Survey of Environment Modeling, Synthesis, Evaluation, and Application**. In the paper, we study agentic environments as dynamic, interactive systems that support the evaluation, training, and continual improvement of LLM agents.

We organize the surveyed works following our taxonomy and lifecycle view, so readers can quickly navigate representative environments, synthesis methods, evaluation practices, and agent-environment co-evolution methods without digging through a flat reference list.

Our survey is organized around three research questions: what characteristics and categories define agentic environments, how agentic environments can be systematically constructed and evaluated, and how agentic environments facilitate the closed-loop co-evolution process of agents and environments.

> Paper: [arXiv](https://arxiv.org/abs/2606.12191)

| Research question | Covered modules |
| --- | --- |
| What are the key characteristics and categories of agentic environments? | Environment Attribute; Environment Domain |
| How can agentic environments be constructed and evaluated? | Environment Synthesis and Evaluation |
| How do agentic environments facilitate agent-environment co-evolution? | Agent Evolution; Environment Evolution; Challenges & Future Directions |

## Preliminaries

We define an environment as a stochastic dynamical system with which an agent interacts, commonly formalized as a POMDP with state space, action space, transition function, reward function, observation space, observation function, and discount factor. In this setting, an LLM agent selects actions from its interaction history, receives observations and rewards, and optimizes its policy through environment-agent alignment.

A central motivation is the shift from static data engineering to environment engineering. Instead of learning only from fixed corpora or pre-collected trajectories, agents can learn through dynamic interaction, feedback, and curriculum-like adjustment of task complexity.

| Perspective | Traditional data engineering | Environment engineering |
| --- | --- | --- |
| Learning source | Static corpus or pre-collected trajectories | Dynamic interaction with an environment |
| Interaction pattern | Single-turn question answering | Multi-turn interaction with tools, executors, retrievers, or agents |
| Feedback loop | Open-loop learning against fixed answers | Closed-loop feedback from state changes and rewards |
| Adaptation | Fixed data difficulty | Task complexity can be adjusted with agent capability |

<p align="center">
  <img src="assets/figures/preliminaries.png" alt="From data engineering to environment engineering" width="82%">
</p>

## Environment Attribute

We characterize agentic environments through eight attributes that determine how agents perceive, interact with, and make decisions in environments: representation, feedback, timing, observability, stochasticity, continuity, modality, and cardinality.

| Attribute | Categories used in the survey |
| --- | --- |
| Representation | Symbolic vs. neural |
| Feedback | Open-loop vs. closed-loop |
| Timing | Online vs. offline |
| Observability | MDP vs. POMDP |
| Stochasticity | Deterministic vs. nondeterministic |
| Continuity | Discrete vs. continuous |
| Modality | Unimodal vs. multimodal |
| Cardinality | Single-agent vs. multi-agent |

<p align="center">
  <img src="assets/figures/environment-attributes.png" alt="Environment attributes" width="86%">
</p>

## Environment Domain

We group representative agentic environments into eight domains. These domains describe the task worlds in which agents operate and the capabilities that current environments evaluate or support.

| Domain | Representative focus in the survey |
| --- | --- |
| GUI | Desktop, mobile, and web GUI environments |
| Deep Research | Browsing, information seeking, long-form research, and report-generation environments |
| Embodied | Household, robotics, navigation, science, and virtual embodied environments |
| Game | Open-world, puzzle reasoning, social deduction, adventure quest, and strategy management games |
| Tool | Conventional tool use, user-simulated tool use, and MCP-based tool use |
| Code | Code generation, understanding, verification, debugging, and repository-level tasks |
| Domain-Specific | Specialized disciplinary or industrial settings, including biomedicine and healthcare, science and technology, and finance and investment |
| Cross-Domain | General-purpose environments and benchmarks spanning multiple task worlds |

<p align="center">
  <img src="assets/figures/environment-domains.png" alt="Environment domains" width="96%">
</p>

### Related Papers

#### GUI

- **WebShop: Towards Scalable Real-World Web Interaction with Grounded Language Agents** [[Paper]](http://papers.nips.cc/paper_files/paper/2022/hash/82ad13ec01f9fe44c01cb91814fd7b8c-Abstract-Conference.html) ![](https://img.shields.io/badge/NeurIPS-2022-blue)
- **Mobile-env: Building qualified evaluation benchmarks for llm-gui interaction** [[Paper]](https://arxiv.org/abs/2305.08144) ![](https://img.shields.io/badge/arXiv-2023.05-red)
- **Android in the Wild: A Large-Scale Dataset for Android Device Control** [[Paper]](https://doi.org/10.48550/arXiv.2307.10088) ![](https://img.shields.io/badge/arXiv-2023.07-red)
- **Mind2Web: Towards a Generalist Agent for the Web** [[Paper]](http://papers.nips.cc/paper_files/paper/2023/hash/5950bf290a1570ea401bf98882128160-Abstract-Datasets_and_Benchmarks.html) ![](https://img.shields.io/badge/NeurIPS-2023-blue)
- **Mobile-Bench: An Evaluation Benchmark for LLM-based Mobile Agents** [[Paper]](https://aclanthology.org/2024.acl-long.478/) ![](https://img.shields.io/badge/ACL-2024-blue)
- **WebArena: A Realistic Web Environment for Building Autonomous Agents** [[Paper]](https://openreview.net/forum?id=oKn9c6ytLx) ![](https://img.shields.io/badge/ICLR-2024-blue)
- **MobileAgentBench: An Efficient and User-Friendly Benchmark for Mobile LLM Agents** [[Paper]](https://doi.org/10.48550/arXiv.2406.08184) ![](https://img.shields.io/badge/arXiv-2024.06-red)
- **WebCanvas: Benchmarking Web Agents in Online Environments** [[Paper]](https://doi.org/10.48550/arXiv.2406.12373) ![](https://img.shields.io/badge/arXiv-2024.06-red)
- **WorkArena: How Capable are Web Agents at Solving Common Knowledge Work Tasks?** [[Paper]](https://proceedings.mlr.press/v235/drouin24a.html) ![](https://img.shields.io/badge/ICML-2024-blue)
- **On the Multi-turn Instruction Following for Conversational Web Agents** [[Paper]](https://doi.org/10.18653/v1/2024.acl-long.477) ![](https://img.shields.io/badge/ACL-2024-blue)
- **VisualWebArena: Evaluating Multimodal Agents on Realistic Visual Web Tasks** [[Paper]](https://doi.org/10.18653/v1/2024.acl-long.50) ![](https://img.shields.io/badge/ACL-2024-blue)
- **WebVoyager: Building an End-to-End Web Agent with Large Multimodal Models** [[Paper]](https://doi.org/10.18653/v1/2024.acl-long.371) ![](https://img.shields.io/badge/ACL-2024-blue)
- **Windows agent arena: Evaluating multi-modal os agents at scale** [[Paper]](https://arxiv.org/abs/2409.08264) ![](https://img.shields.io/badge/arXiv-2024.09-red)
- **On the Effects of Data Scale on UI Control Agents** [[Paper]](http://papers.nips.cc/paper_files/paper/2024/hash/a79f3ef3b445fd4659f44648f7ea8ffd-Abstract-Datasets_and_Benchmarks_Track.html) ![](https://img.shields.io/badge/NeurIPS-2024-blue)
- **OSWorld: Benchmarking Multimodal Agents for Open-Ended Tasks in Real Computer Environments** [[Paper]](http://papers.nips.cc/paper_files/paper/2024/hash/5d413e48f84dc61244b6be550f1cd8f5-Abstract-Datasets_and_Benchmarks_Track.html) ![](https://img.shields.io/badge/NeurIPS-2024-blue)
- **AgentStudio: A Toolkit for Building General Virtual Agents** [[Paper]](https://openreview.net/forum?id=axUf8BOjnH) ![](https://img.shields.io/badge/ICLR-2025-blue)
- **An Illusion of Progress? Assessing the Current State of Web Agents** [[Paper]](https://doi.org/10.48550/arXiv.2504.01382) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **AndroidWorld: A Dynamic Benchmarking Environment for Autonomous Agents** [[Paper]](https://openreview.net/forum?id=il5yUQsrjC) ![](https://img.shields.io/badge/ICLR-2025-blue)
- **VideoWebArena: Evaluating Long Context Multimodal Agents with Video Understanding Web Tasks** [[Paper]](https://openreview.net/forum?id=unDQOUah0F) ![](https://img.shields.io/badge/ICLR-2025-blue)
- **Mind2Web 2: Evaluating Agentic Search with Agent-as-a-Judge** [[Paper]](https://doi.org/10.48550/arXiv.2506.21506) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **OSWorld-MCP: Benchmarking MCP Tool Invocation In Computer-Use Agents** [[Paper]](https://doi.org/10.48550/arXiv.2510.24563) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **MobileWorld: Benchmarking Autonomous Mobile Agents in Agent-User Interactive and MCP-Augmented Environments** [[Paper]](https://doi.org/10.48550/arXiv.2512.19432) ![](https://img.shields.io/badge/arXiv-2025.12-red)

#### Deep Research

- **GAIA: a benchmark for General AI Assistants** [[Paper]](https://openreview.net/forum?id=fibxvahvs3) ![](https://img.shields.io/badge/ICLR-2024-blue)
- **ProxyQA: An Alternative Framework for Evaluating Long-Form Text Generation with Large Language Models** [[Paper]](https://doi.org/10.18653/v1/2024.acl-long.368) ![](https://img.shields.io/badge/ACL-2024-blue)
- **Measuring short-form factuality in large language models** [[Paper]](https://arxiv.org/abs/2411.04368) ![](https://img.shields.io/badge/arXiv-2024.11-red)
- **OpenScholar: Synthesizing Scientific Literature with Retrieval-augmented LMs** [[Paper]](https://doi.org/10.48550/arXiv.2411.14199) ![](https://img.shields.io/badge/arXiv-2024.11-red)
- **AI Idea Bench 2025: AI Research Idea Generation Benchmark** [[Paper]](https://doi.org/10.48550/arXiv.2504.14191) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **BrowseComp-ZH: Benchmarking Web Browsing Ability of Large Language Models in Chinese** [[Paper]](https://doi.org/10.48550/arXiv.2504.19314) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **BrowseComp: A Simple Yet Challenging Benchmark for Browsing Agents** [[Paper]](https://doi.org/10.48550/arXiv.2504.12516) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **DeepResearchGym: A Free, Transparent, and Reproducible Evaluation Sandbox for Deep Research** [[Paper]](https://doi.org/10.48550/arXiv.2505.19253) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **InfoDeepSeek: Benchmarking Agentic Information Seeking for Retrieval-Augmented Generation** [[Paper]](https://doi.org/10.48550/arXiv.2505.15872) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **DeepResearch Bench: A Comprehensive Benchmark for Deep Research Agents** [[Paper]](https://doi.org/10.48550/arXiv.2506.11763) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **DRAGged into Conflicts: Detecting and Addressing Conflicting Sources in Search-Augmented LLMs** [[Paper]](https://doi.org/10.48550/arXiv.2506.08500) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **Multimodal DeepResearcher: Generating Text-Chart Interleaved Reports From Scratch with Agentic Framework** [[Paper]](https://doi.org/10.48550/arXiv.2506.02454) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **DeepReview: Improving LLM-based Paper Review with Human-like Deep Thinking Process** [[Paper]](https://aclanthology.org/2025.acl-long.1420/) ![](https://img.shields.io/badge/ACL-2025-blue)
- **PaperBench: Evaluating AI's Ability to Replicate AI Research** [[Paper]](https://proceedings.mlr.press/v267/starace25a.html) ![](https://img.shields.io/badge/ICML-2025-blue)
- **ResearcherBench: Evaluating Deep AI Research Systems on the Frontiers of Scientific Inquiry** [[Paper]](https://doi.org/10.48550/arXiv.2507.16280) ![](https://img.shields.io/badge/arXiv-2025.07-red)
- **WebWalker: Benchmarking LLMs in Web Traversal** [[Paper]](https://aclanthology.org/2025.acl-long.508/) ![](https://img.shields.io/badge/ACL-2025-blue)
- **Characterizing Deep Research: A Benchmark and Formal Definition** [[Paper]](https://doi.org/10.48550/arXiv.2508.04183) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **ReportBench: Evaluating Deep Research Agents via Academic Survey Tasks** [[Paper]](https://doi.org/10.48550/arXiv.2508.15804) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **WideSearch: Benchmarking Agentic Broad Info-Seeking** [[Paper]](https://doi.org/10.48550/arXiv.2508.07999) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **Open Data Synthesis For Deep Research** [[Paper]](https://doi.org/10.48550/arXiv.2509.00375) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **Dr. Bench: A Multidimensional Evaluation for Deep Research Agents, from Answers to Reports** [[Paper]](https://arxiv.org/abs/2510.02190) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **Humanity's Last Code Exam: Can Advanced LLMs Conquer Human's Hardest Code Competition?** [[Paper]](https://aclanthology.org/2025.findings-emnlp.1152/) ![](https://img.shields.io/badge/EMNLP_Findings-2025-blue)
- **SurveyGen: Quality-Aware Scientific Survey Generation with Large Language Models** [[Paper]](https://doi.org/10.18653/v1/2025.emnlp-main.136) ![](https://img.shields.io/badge/EMNLP-2025-blue)
- **MMDeepResearch-Bench: A Benchmark for Multimodal Deep Research Agents** [[Paper]](https://doi.org/10.48550/arXiv.2601.12346) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **OmniGAIA: Towards Native Omni-Modal AI Agents** [[Paper]](https://doi.org/10.48550/arXiv.2602.22897) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **Vision-DeepResearch Benchmark: Rethinking Visual and Textual Search for Multimodal Large Language Models** [[Paper]](https://arxiv.org/abs/2602.02185) ![](https://img.shields.io/badge/arXiv-2026.02-red)

#### Embodied

- **Vision-and-Language Navigation: Interpreting Visually-Grounded Navigation Instructions in Real Environments** [[Paper]](http://openaccess.thecvf.com/content_cvpr_2018/html/Anderson_Vision-and-Language_Navigation_Interpreting_CVPR_2018_paper.html) ![](https://img.shields.io/badge/CVPR-2018-blue)
- **Habitat: A Platform for Embodied AI Research** [[Paper]](https://doi.org/10.1109/ICCV.2019.00943) ![](https://img.shields.io/badge/ICCV-2019-blue)
- **RLBench: The Robot Learning Benchmark & Learning Environment** [[Paper]](https://arxiv.org/abs/1909.12271) ![](https://img.shields.io/badge/IEEE_RA--L-2020-blue)
- **ALFRED: A Benchmark for Interpreting Grounded Instructions for Everyday Tasks** [[Paper]](https://openaccess.thecvf.com/content_CVPR_2020/html/Shridhar_ALFRED_A_Benchmark_for_Interpreting_Grounded_Instructions_for_Everyday_Tasks_CVPR_2020_paper.html) ![](https://img.shields.io/badge/CVPR-2020-blue)
- **Beyond the Nav-Graph: Vision-and-Language Navigation in Continuous Environments** [[Paper]](https://doi.org/10.1007/978-3-030-58604-1_7) ![](https://img.shields.io/badge/ECCV-2020-blue)
- **Room-Across-Room: Multilingual Vision-and-Language Navigation with Dense Spatiotemporal Grounding** [[Paper]](https://doi.org/10.18653/v1/2020.emnlp-main.356) ![](https://img.shields.io/badge/EMNLP-2020-blue)
- **ALFWorld: Aligning Text and Embodied Environments for Interactive Learning** [[Paper]](https://openreview.net/forum?id=0IOX0YcCdTn) ![](https://img.shields.io/badge/ICLR-2021-blue)
- **panda-gym: Open-source goal-conditioned environments for robotic learning** [[Paper]](https://arxiv.org/abs/2106.13687) ![](https://img.shields.io/badge/arXiv-2021.06-red)
- **BEHAVIOR: Benchmark for Everyday Household Activities in Virtual, Interactive, and Ecological Environments** [[Paper]](https://proceedings.mlr.press/v164/srivastava22a.html) ![](https://img.shields.io/badge/CoRL-2021-blue)
- **TEACh: Task-Driven Embodied Agents That Chat** [[Paper]](https://ojs.aaai.org/index.php/AAAI/article/view/20097) ![](https://img.shields.io/badge/AAAI-2022-blue)
- **ScienceWorld: Is your Agent Smarter than a 5th Grader?** [[Paper]](https://doi.org/10.18653/v1/2022.emnlp-main.775) ![](https://img.shields.io/badge/EMNLP-2022-blue)
- **MetaDrive: Composing Diverse Driving Scenarios for Generalizable Reinforcement Learning** [[Paper]](https://doi.org/10.1109/TPAMI.2022.3190471) ![](https://img.shields.io/badge/TPAMI-2023-blue)
- **ReALFRED: An Embodied Instruction Following Benchmark in Photo-Realistic Environments** [[Paper]](https://arxiv.org/abs/2407.18550) ![](https://img.shields.io/badge/ECCV-2024-blue)
- **Robocasa: Large-scale simulation of everyday tasks for generalist robots** [[Paper]](https://arxiv.org/abs/2406.02523) ![](https://img.shields.io/badge/arXiv-2024.06-red)
- **LEGENT: Open Platform for Embodied Agents** [[Paper]](https://doi.org/10.18653/v1/2024.acl-demos.32) ![](https://img.shields.io/badge/ACL-2024-blue)
- **RoboFactory: Exploring Embodied Agent Collaboration with Compositional Constraints** [[Paper]](https://doi.org/10.48550/arXiv.2503.16408) ![](https://img.shields.io/badge/arXiv-2025.03-red)
- **Decoupled Diffusion Sparks Adaptive Scene Generation** [[Paper]](https://doi.org/10.48550/arXiv.2504.10485) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **Scenario Dreamer: Vectorized Latent Diffusion for Generating Driving Simulation Environments** [[Paper]](https://openaccess.thecvf.com/content/CVPR2025/html/Rowe_Scenario_Dreamer_Vectorized_Latent_Diffusion_for_Generating_Driving_Simulation_Environments_CVPR_2025_paper.html) ![](https://img.shields.io/badge/CVPR-2025-blue)
- **EmbodiedBench: Comprehensive Benchmarking Multi-modal Large Language Models for Vision-Driven Embodied Agents** [[Paper]](https://proceedings.mlr.press/v267/yang25f.html) ![](https://img.shields.io/badge/ICML-2025-blue)
- **Sari Sandbox: A Virtual Retail Store Environment for Embodied AI Agents** [[Paper]](https://doi.org/10.48550/arXiv.2508.00400) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **SimuHome: A Temporal-and Environment-Aware Benchmark for Smart Home LLM Agents** [[Paper]](https://arxiv.org/abs/2509.24282) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **ET-Plan-Bench: Embodied Task-level Planning Benchmark Towards Spatial-Temporal Cognition with Foundation Models** [[Paper]](https://doi.org/10.1109/IROS60139.2025.11246658) ![](https://img.shields.io/badge/IROS-2025-blue)

#### Game

- **MineDojo: Building Open-Ended Embodied Agents with Internet-Scale Knowledge** [[Paper]](http://papers.nips.cc/paper_files/paper/2022/hash/74a67268c5cc5910f64938cac4526a90-Abstract-Datasets_and_Benchmarks.html) ![](https://img.shields.io/badge/NeurIPS-2022-blue)
- **Describe, Explain, Plan and Select: Interactive Planning with Large Language Models Enables Open-World Multi-Task Agents** [[Paper]](https://arxiv.org/abs/2302.01560) ![](https://img.shields.io/badge/arXiv-2023.02-red)
- **Clembench: Using Game Play to Evaluate Chat-Optimized Language Models as Conversational Agents** [[Paper]](https://arxiv.org/abs/2305.13455) ![](https://img.shields.io/badge/arXiv-2023.05-red)
- **Minigrid & Miniworld: Modular & Customizable Reinforcement Learning Environments for Goal-Oriented Tasks** [[Paper]](https://arxiv.org/abs/2306.13831) ![](https://img.shields.io/badge/arXiv-2023.06-red)
- **Avalon's Game of Thoughts: Battle Against Deception through Recursive Contemplation** [[Paper]](https://arxiv.org/abs/2310.01320) ![](https://img.shields.io/badge/arXiv-2023.10-red)
- **AvalonBench: Evaluating LLMs Playing the Game of Avalon** [[Paper]](https://arxiv.org/abs/2310.05036) ![](https://img.shields.io/badge/arXiv-2023.10-red)
- **SmartPlay: A Benchmark for LLMs as Intelligent Agents** [[Paper]](https://arxiv.org/abs/2310.01557) ![](https://img.shields.io/badge/arXiv-2023.10-red)
- **LMRL Gym: Benchmarks for Multi-Turn Reinforcement Learning with Language Models** [[Paper]](https://arxiv.org/abs/2311.18232) ![](https://img.shields.io/badge/arXiv-2023.11-red)
- **LLM-Powered Hierarchical Language Agent for Real-time Human-AI Coordination** [[Paper]](https://arxiv.org/abs/2312.15224) ![](https://img.shields.io/badge/arXiv-2023.12-red)
- **WhodunitBench: Evaluating Large Multimodal Agents via Murder Mystery Games** [[Paper]](https://proceedings.neurips.cc/paper_files/paper/2024/hash/9dd4533e7e4e5ed809344280609c5b05-Abstract-Datasets_and_Benchmarks_Track.html) ![](https://img.shields.io/badge/NeurIPS-2024-blue)
- **CivRealm: A Learning and Reasoning Odyssey in Civilization for Decision-Making Agents** [[Paper]](https://arxiv.org/abs/2401.10568) ![](https://img.shields.io/badge/arXiv-2024.01-red)
- **Enhance Reasoning for Large Language Models in the Game Werewolf** [[Paper]](https://arxiv.org/abs/2402.02330) ![](https://img.shields.io/badge/arXiv-2024.02-red)
- **GTBench: Uncovering the Strategic Reasoning Limitations of LLMs via Game-Theoretic Evaluations** [[Paper]](https://arxiv.org/abs/2402.12348) ![](https://img.shields.io/badge/arXiv-2024.02-red)
- **LLMArena: Assessing Capabilities of Large Language Models in Dynamic Multi-Agent Environments** [[Paper]](https://arxiv.org/abs/2402.16499) ![](https://img.shields.io/badge/arXiv-2024.02-red)
- **PokeLLMon: A Human-Parity Agent for Pokemon Battles with Large Language Models** [[Paper]](https://arxiv.org/abs/2402.01118) ![](https://img.shields.io/badge/arXiv-2024.02-red)
- **GameBench: Evaluating Strategic Reasoning Abilities of LLM Agents** [[Paper]](https://arxiv.org/abs/2406.06613) ![](https://img.shields.io/badge/arXiv-2024.06-red)
- **The Overcooked Generalisation Challenge: Evaluating Cooperation with Novel Partners in Unknown Environments Using Unsupervised Environment Design** [[Paper]](https://arxiv.org/abs/2406.17949) ![](https://img.shields.io/badge/arXiv-2024.06-red)
- **Baba Is AI: Break the Rules to Beat the Benchmark** [[Paper]](https://arxiv.org/abs/2407.13729) ![](https://img.shields.io/badge/arXiv-2024.07-red)
- **Diffusion Models Are Real-Time Game Engines** [[Paper]](https://arxiv.org/abs/2408.14837) ![](https://img.shields.io/badge/arXiv-2024.08-red)
- **GameTraversalBenchmark: Evaluating Planning Abilities Of Large Language Models Through Traversing 2D Game Maps** [[Paper]](https://arxiv.org/abs/2410.07765) ![](https://img.shields.io/badge/arXiv-2024.10-red)
- **ING-VP: MLLMs cannot Play Easy Vision-based Games Yet** [[Paper]](https://arxiv.org/abs/2410.06555) ![](https://img.shields.io/badge/arXiv-2024.10-red)
- **KOR-Bench: Benchmarking Language Models on Knowledge-Orthogonal Reasoning Tasks** [[Paper]](https://arxiv.org/abs/2410.06526) ![](https://img.shields.io/badge/arXiv-2024.10-red)
- **BALROG: Benchmarking Agentic LLM and VLM Reasoning On Games** [[Paper]](https://arxiv.org/abs/2411.13543) ![](https://img.shields.io/badge/arXiv-2024.11-red)
- **GameArena: Evaluating LLM Reasoning through Live Computer Games** [[Paper]](https://arxiv.org/abs/2412.06394) ![](https://img.shields.io/badge/arXiv-2024.12-red)
- **GAMEBoT: Transparent Assessment of LLM Reasoning in Games** [[Paper]](https://arxiv.org/abs/2412.13602) ![](https://img.shields.io/badge/arXiv-2024.12-red)
- **Collab-Overcooked: Benchmarking and Evaluating Large Language Models as Collaborative Agents** [[Paper]](http://dx.doi.org/10.18653/v1/2025.emnlp-main.249) ![](https://img.shields.io/badge/EMNLP-2025-blue)
- **GameFactory: Creating New Games with Generative Interactive Videos** [[Paper]](https://arxiv.org/abs/2501.08325) ![](https://img.shields.io/badge/arXiv-2025.01-red)
- **TextGames: Learning to Self-Play Text-Based Puzzle Games via Language Model Reasoning** [[Paper]](https://arxiv.org/abs/2502.18431) ![](https://img.shields.io/badge/arXiv-2025.02-red)
- **DSGBench: A Diverse Strategic Game Benchmark for Evaluating LLM-based Agents in Complex Decision-Making Environments** [[Paper]](https://arxiv.org/abs/2503.06047) ![](https://img.shields.io/badge/arXiv-2025.03-red)
- **Factorio Learning Environment** [[Paper]](https://arxiv.org/abs/2503.09617) ![](https://img.shields.io/badge/arXiv-2025.03-red)
- **SPIN-Bench: How Well Do LLMs Plan Strategically and Reason Socially?** [[Paper]](https://arxiv.org/abs/2503.12349) ![](https://img.shields.io/badge/arXiv-2025.03-red)
- **MineWorld: a Real-Time and Open-Source Interactive World Model on Minecraft** [[Paper]](https://arxiv.org/abs/2504.08388) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **TextArena** [[Paper]](https://arxiv.org/abs/2504.11442) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **KORGym: A Dynamic Game Platform for LLM Reasoning Evaluation** [[Paper]](https://arxiv.org/abs/2505.14552) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **VideoGameBench: Can Vision-Language Models complete popular video games?** [[Paper]](https://arxiv.org/abs/2505.18134) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **GVGAI-LLM: Evaluating Large Language Model Agents with Infinite Games** [[Paper]](https://arxiv.org/abs/2508.08501) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **FlashAdventure: A Benchmark for GUI Agents Solving Full Story Arcs in Diverse Adventure Games** [[Paper]](https://arxiv.org/abs/2509.01052) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **V-GameGym: Visual Game Generation for Code Large Language Models** [[Paper]](https://doi.org/10.48550/arXiv.2509.20136) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **AI Gamestore: Scalable, Open-Ended Evaluation of Machine General Intelligence with Human Games** [[Paper]](https://arxiv.org/abs/2602.17594) ![](https://img.shields.io/badge/arXiv-2026.02-red)

#### Tool

- **ToolTalk: Evaluating Tool-Usage in a Conversational Setting** [[Paper]](https://doi.org/10.48550/arXiv.2311.10775) ![](https://img.shields.io/badge/arXiv-2023.11-red)
- **API-Bank: A Comprehensive Benchmark for Tool-Augmented LLMs** [[Paper]](https://doi.org/10.18653/v1/2023.emnlp-main.187) ![](https://img.shields.io/badge/EMNLP-2023-blue)
- **MINT: Evaluating LLMs in Multi-turn Interaction with Tools and Language Feedback** [[Paper]](https://openreview.net/forum?id=jp3gWrMuIZ) ![](https://img.shields.io/badge/ICLR-2024-blue)
- **ToolLLM: Facilitating Large Language Models to Master 16000+ Real-world APIs** [[Paper]](https://openreview.net/forum?id=dHng2O0Jjr) ![](https://img.shields.io/badge/ICLR-2024-blue)
- **tau-bench: A Benchmark for Tool-Agent-User Interaction in Real-World Domains** [[Paper]](https://doi.org/10.48550/arXiv.2406.12045) ![](https://img.shields.io/badge/arXiv-2024.06-red)
- **AppWorld: A Controllable World of Apps and People for Benchmarking Interactive Coding Agents** [[Paper]](https://doi.org/10.18653/v1/2024.acl-long.850) ![](https://img.shields.io/badge/ACL-2024-blue)
- **StableToolBench: Towards Stable Large-Scale Benchmarking on Tool Learning of Large Language Models** [[Paper]](https://doi.org/10.18653/v1/2024.findings-acl.664) ![](https://img.shields.io/badge/ACL_Findings-2024-blue)
- **FlowBench: Revisiting and Benchmarking Workflow-Guided Planning for LLM-based Agents** [[Paper]](https://doi.org/10.18653/v1/2024.findings-emnlp.638) ![](https://img.shields.io/badge/EMNLP_Findings-2024-blue)
- **ToolEyes: Fine-Grained Evaluation for Tool Learning Capabilities of Large Language Models in Real-world Scenarios** [[Paper]](https://aclanthology.org/2025.coling-main.12/) ![](https://img.shields.io/badge/COLING-2025-blue)
- **tau^2-Bench: Evaluating Conversational Agents in a Dual-Control Environment** [[Paper]](https://doi.org/10.48550/arXiv.2506.07982) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **Evaluating Personalized Tool-Augmented LLMs from the Perspectives of Personalization and Proactivity** [[Paper]](https://aclanthology.org/2025.acl-long.1064/) ![](https://img.shields.io/badge/ACL-2025-blue)
- **The Berkeley Function Calling Leaderboard (BFCL): From Tool Use to Agentic Evaluation of Large Language Models** [[Paper]](https://proceedings.mlr.press/v267/patil25a.html) ![](https://img.shields.io/badge/ICML-2025-blue)
- **UserBench: An Interactive Gym Environment for User-Centric Agents** [[Paper]](https://doi.org/10.48550/arXiv.2507.22034) ![](https://img.shields.io/badge/arXiv-2025.07-red)
- **MCP-Bench: Benchmarking Tool-Using LLM Agents with Complex Real-World Tasks via MCP Servers** [[Paper]](https://doi.org/10.48550/arXiv.2508.20453) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **MCP-Universe: Benchmarking Large Language Models with Real-World Model Context Protocol Servers** [[Paper]](https://doi.org/10.48550/arXiv.2508.14704) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **MCPToolBench++: A Large Scale AI Agent Model Context Protocol MCP Tool Use Benchmark** [[Paper]](https://doi.org/10.48550/arXiv.2508.07575) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **MCPVerse: An Expansive, Real-World Benchmark for Agentic Tool Use** [[Paper]](https://doi.org/10.48550/arXiv.2508.16260) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **Mcpmark: A benchmark for stress-testing realistic and comprehensive mcp use** [[Paper]](https://arxiv.org/abs/2509.24002) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **TRAJECT-Bench:A Trajectory-Aware Benchmark for Evaluating Agentic Tool Use** [[Paper]](https://doi.org/10.48550/arXiv.2510.04550) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **ACEBench: A Comprehensive Evaluation of LLM Tool Usage** [[Paper]](https://aclanthology.org/2025.findings-emnlp.697/) ![](https://img.shields.io/badge/EMNLP_Findings-2025-blue)
- **M^3-Bench: Multi-Modal, Multi-Hop, Multi-Threaded Tool-Using MLLM Agent Benchmark** [[Paper]](https://doi.org/10.48550/arXiv.2511.17729) ![](https://img.shields.io/badge/arXiv-2025.11-red)

#### Code

- **Program synthesis with large language models** [[Paper]](https://arxiv.org/abs/2108.07732) ![](https://img.shields.io/badge/arXiv-2021.08-red)
- **InterCode: Standardizing and Benchmarking Interactive Coding with Execution Feedback** [[Paper]](https://arxiv.org/abs/2306.14898) ![](https://img.shields.io/badge/NeurIPS-2023-blue)
- **CodeAgent: Enhancing Code Generation with Tool-Integrated Agent Systems for Real-World Repo-level Coding Challenges** [[Paper]](https://aclanthology.org/2024.acl-long.737/) ![](https://img.shields.io/badge/ACL-2024-blue)
- **CRUXEval: A Benchmark for Code Reasoning, Understanding and Execution** [[Paper]](https://arxiv.org/abs/2401.03065) ![](https://img.shields.io/badge/arXiv-2024.01-red)
- **DebugBench: Evaluating Debugging Capability of Large Language Models** [[Paper]](https://arxiv.org/abs/2401.04621) ![](https://img.shields.io/badge/arXiv-2024.01-red)
- **Livecodebench: Holistic and contamination free evaluation of large language models for code** [[Paper]](https://arxiv.org/abs/2403.07974) ![](https://img.shields.io/badge/arXiv-2024.03-red)
- **SWE-bench: Can Language Models Resolve Real-world Github Issues?** [[Paper]](https://openreview.net/forum?id=VTF8yNQM66) ![](https://img.shields.io/badge/ICLR-2024-blue)
- **CodeRAG-Bench: Can Retrieval Augment Code Generation?** [[Paper]](https://arxiv.org/abs/2406.14497) ![](https://img.shields.io/badge/arXiv-2024.06-red)
- **SWT-Bench: Testing and Validating Real-World Bug-Fixes with Code Agents** [[Paper]](https://arxiv.org/abs/2406.12952) ![](https://img.shields.io/badge/arXiv-2024.06-red)
- **Swe-bench multimodal: Do ai systems generalize to visual software domains?** [[Paper]](https://arxiv.org/abs/2410.03859) ![](https://img.shields.io/badge/arXiv-2024.10-red)
- **CSR-Bench: Benchmarking LLM Agents in Deployment of Computer Science Research Repositories** [[Paper]](https://aclanthology.org/2025.naacl-long.633/) ![](https://img.shields.io/badge/NAACL-2025-blue)
- **CodeElo: Benchmarking Competition-level Code Generation of LLMs with Human-comparable Elo Ratings** [[Paper]](https://doi.org/10.48550/arXiv.2501.01257) ![](https://img.shields.io/badge/arXiv-2025.01-red)
- **Kernelbench: Can llms write efficient gpu kernels?** [[Paper]](https://arxiv.org/abs/2502.10517) ![](https://img.shields.io/badge/arXiv-2025.02-red)
- **FEA-Bench: A Benchmark for Evaluating Repository-Level Code Generation for Feature Implementation** [[Paper]](https://arxiv.org/abs/2503.06680) ![](https://img.shields.io/badge/arXiv-2025.03-red)
- **BigCodeBench: Benchmarking Code Generation with Diverse Function Calls and Complex Instructions** [[Paper]](https://openreview.net/forum?id=YrycTjllL0) ![](https://img.shields.io/badge/ICLR-2025-blue)
- **Multi-SWE-bench: A Multilingual Benchmark for Issue Resolving** [[Paper]](https://arxiv.org/abs/2504.02605) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **SWE-Bench Pro: Can AI Agents Solve Long-Horizon Software Engineering Tasks?** [[Paper]](https://doi.org/10.48550/arXiv.2509.16941) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **NL2Repo-Bench: Towards Long-Horizon Repository Generation Evaluation of Coding Agents** [[Paper]](https://arxiv.org/abs/2512.12730) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **IDE-Bench: Evaluating Large Language Models as IDE Agents on Real-World Software Engineering Tasks** [[Paper]](https://arxiv.org/abs/2601.20886) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **Terminal-Bench: Benchmarking Agents on Hard, Realistic Tasks in Command Line Interfaces** [[Paper]](https://doi.org/10.48550/arXiv.2601.11868) ![](https://img.shields.io/badge/arXiv-2026.01-red)

#### Domain-Specific

- **BioCoder: a benchmark for bioinformatics code generation with large language models** [[Paper]](https://doi.org/10.1093/bioinformatics/btae230) ![](https://img.shields.io/badge/Bioinform-2024-blue)
- **NATURAL PLAN: Benchmarking LLMs on Natural Language Planning** [[Paper]](https://doi.org/10.48550/arXiv.2406.04520) ![](https://img.shields.io/badge/arXiv-2024.06-red)
- **TravelPlanner: A Benchmark for Real-World Planning with Language Agents** [[Paper]](https://proceedings.mlr.press/v235/xie24j.html) ![](https://img.shields.io/badge/ICML-2024-blue)
- **Benchmarking Data Science Agents** [[Paper]](https://doi.org/10.18653/v1/2024.acl-long.308) ![](https://img.shields.io/badge/ACL-2024-blue)
- **DiscoveryWorld: A Virtual Environment for Developing and Evaluating Automated Scientific Discovery Agents** [[Paper]](http://papers.nips.cc/paper_files/paper/2024/hash/13836f251823945316ae067350a5c366-Abstract-Datasets_and_Benchmarks_Track.html) ![](https://img.shields.io/badge/NeurIPS-2024-blue)
- **MedAgentBench: Dataset for Benchmarking LLMs as Agents in Medical Applications** [[Paper]](https://doi.org/10.48550/arXiv.2501.14654) ![](https://img.shields.io/badge/arXiv-2025.01-red)
- **BixBench: a Comprehensive Benchmark for LLM-based Agents in Computational Biology** [[Paper]](https://doi.org/10.48550/arXiv.2503.00096) ![](https://img.shields.io/badge/arXiv-2025.03-red)
- **DSBench: How Far Are Data Science Agents from Becoming Data Science Experts?** [[Paper]](https://openreview.net/forum?id=DSsSPr0RZJ) ![](https://img.shields.io/badge/ICLR-2025-blue)
- **MLE-bench: Evaluating Machine Learning Agents on Machine Learning Engineering** [[Paper]](https://openreview.net/forum?id=6s5uXNWGIh) ![](https://img.shields.io/badge/ICLR-2025-blue)
- **ScienceAgentBench: Toward Rigorous Assessment of Language Agents for Data-Driven Scientific Discovery** [[Paper]](https://openreview.net/forum?id=6z4YKr0GK6) ![](https://img.shields.io/badge/ICLR-2025-blue)
- **CRMArena-Pro: Holistic Assessment of LLM Agents Across Diverse Business Scenarios and Interactions** [[Paper]](https://doi.org/10.48550/arXiv.2505.18878) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **Mle-dojo: Interactive environments for empowering llm agents in machine learning engineering** [[Paper]](https://arxiv.org/abs/2505.07782) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **MedAgentGym: A Scalable Agentic Training Environment for Code-Centric Reasoning in Biomedical Data Science** [[Paper]](https://arxiv.org/abs/2506.04405) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **Finance Agent Benchmark: Benchmarking LLMs on Real-world Financial Research Tasks** [[Paper]](https://doi.org/10.48550/arXiv.2508.00828) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **FinDeepResearch: Evaluating Deep Research Agents in Rigorous Financial Analysis** [[Paper]](https://doi.org/10.48550/arXiv.2510.13936) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **PaperArena: An Evaluation Benchmark for Tool-Augmented Agentic Reasoning on Scientific Literature** [[Paper]](https://doi.org/10.48550/arXiv.2510.10909) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **StockBench: Can LLM Agents Trade Stocks Profitably In Real-world Markets?** [[Paper]](https://doi.org/10.48550/arXiv.2510.02209) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **EcomBench: Towards Holistic Evaluation of Foundation Agents in E-commerce** [[Paper]](https://doi.org/10.48550/arXiv.2512.08868) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **MedAgentBench v2: Improving Medical LLM Agent Design** [[Paper]](https://doi.org/10.1142/9789819824755_0025) ![](https://img.shields.io/badge/PSB-2026-blue)
- **Advancing ESG Intelligence: An Expert-level Agent and Comprehensive Benchmark for Sustainable Finance** [[Paper]](https://arxiv.org/abs/2601.08676) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **BioAgent Bench: An AI Agent Evaluation Suite for Bioinformatics** [[Paper]](https://doi.org/10.48550/arXiv.2601.21800) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **MedMCP-Calc: Benchmarking LLMs for Realistic Medical Calculator Scenarios via MCP Integration** [[Paper]](https://doi.org/10.48550/arXiv.2601.23049) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **World of Workflows: a Benchmark for Bringing World Models to Enterprise Systems** [[Paper]](https://doi.org/10.48550/arXiv.2601.22130) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **EnterpriseOps-Gym: Environments and Evaluations for Stateful Agentic Planning and Tool Use in Enterprise Settings** [[Paper]](https://arxiv.org/abs/2603.13594) ![](https://img.shields.io/badge/arXiv-2026.03-red)
- **MetaClaw: Just Talk-An Agent That Meta-Learns and Evolves in the Wild** [[Paper]](https://arxiv.org/abs/2603.17187) ![](https://img.shields.io/badge/arXiv-2026.03-red)
- **Claw-Eval: Toward Trustworthy Evaluation of Autonomous Agents** [[Paper]](https://arxiv.org/abs/2604.06132) ![](https://img.shields.io/badge/arXiv-2026.04-red)
- **ClawArena: Benchmarking AI Agents in Evolving Information Environments** [[Paper]](https://arxiv.org/abs/2604.04202) ![](https://img.shields.io/badge/arXiv-2026.04-red)

#### Cross-Domain

- **Openai gym** [[Paper]](https://arxiv.org/abs/1606.01540) ![](https://img.shields.io/badge/arXiv-2016.06-red)
- **CAMEL: Communicative Agents for "Mind" Exploration of Large Language Model Society** [[Paper]](http://papers.nips.cc/paper_files/paper/2023/hash/a3621ee907def47c1b952ade25c67698-Abstract-Conference.html) ![](https://img.shields.io/badge/NeurIPS-2023-blue)
- **HuggingGPT: Solving AI Tasks with ChatGPT and its Friends in Hugging Face** [[Paper]](http://papers.nips.cc/paper_files/paper/2023/hash/77c33e6a367922d003ff102ffb92b658-Abstract-Conference.html) ![](https://img.shields.io/badge/NeurIPS-2023-blue)
- **TaskLAMA: Probing the Complex Task Understanding of Language Models** [[Paper]](https://doi.org/10.1609/aaai.v38i17.29918) ![](https://img.shields.io/badge/AAAI-2024-blue)
- **AgentBench: Evaluating LLMs as Agents** [[Paper]](https://openreview.net/forum?id=zAdUB0aCTQ) ![](https://img.shields.io/badge/ICLR-2024-blue)
- **AgentGym: Evolving Large Language Model-based Agents across Diverse Environments** [[Paper]](https://doi.org/10.48550/arXiv.2406.04151) ![](https://img.shields.io/badge/arXiv-2024.06-red)
- **AgentBoard: An Analytical Evaluation Board of Multi-turn LLM Agents** [[Paper]](http://papers.nips.cc/paper_files/paper/2024/hash/877b40688e330a0e2a3fc24084208dfa-Abstract-Datasets_and_Benchmarks_Track.html) ![](https://img.shields.io/badge/NeurIPS-2024-blue)
- **TaskBench: Benchmarking Large Language Models for Task Automation** [[Paper]](http://papers.nips.cc/paper_files/paper/2024/hash/085185ea97db31ae6dcac7497616fd3e-Abstract-Datasets_and_Benchmarks_Track.html) ![](https://img.shields.io/badge/NeurIPS-2024-blue)
- **Mlgym: A new framework and benchmark for advancing ai research agents** [[Paper]](https://arxiv.org/abs/2502.14499) ![](https://img.shields.io/badge/arXiv-2025.02-red)
- **Benchmarking Agentic Workflow Generation** [[Paper]](https://openreview.net/forum?id=vunPXOFmoi) ![](https://img.shields.io/badge/ICLR-2025-blue)
- **MedBrowseComp: Benchmarking Medical Deep Research and Computer Use** [[Paper]](https://doi.org/10.48550/arXiv.2505.14963) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **GEM: A Gym for Agentic LLMs** [[Paper]](https://doi.org/10.48550/arXiv.2510.01051) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **AutoEnv: Automated Environments for Measuring Cross-Environment Agent Learning** [[Paper]](https://doi.org/10.48550/arXiv.2511.19304) ![](https://img.shields.io/badge/arXiv-2025.11-red)
- **TPS-Bench: Evaluating AI Agents' Tool Planning & Scheduling Abilities in Compounding Tasks** [[Paper]](https://doi.org/10.48550/arXiv.2511.01527) ![](https://img.shields.io/badge/arXiv-2025.11-red)
- **WebMMU: A Benchmark for Multimodal Multilingual Website Understanding and Code Generation** [[Paper]](https://doi.org/10.18653/v1/2025.emnlp-main.1276) ![](https://img.shields.io/badge/EMNLP-2025-blue)
- **AgencyBench: Benchmarking the Frontiers of Autonomous Agents in 1M-Token Real-World Contexts** [[Paper]](https://doi.org/10.48550/arXiv.2601.11044) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **AgentVista: Evaluating Multimodal Agents in Ultra-Challenging Realistic Visual Scenarios** [[Paper]](https://doi.org/10.48550/arXiv.2602.23166) ![](https://img.shields.io/badge/arXiv-2026.02-red)

## Environment Synthesis and Evaluation

We divide automated environment synthesis into symbolic synthesis and neural synthesis. Symbolic synthesis uses explicit structures such as code, rules, simulators, tools, or verifiers to construct environments and provide reliable feedback. Neural synthesis parameterizes environment dynamics with neural models, especially world models.

For environment evaluation, we discuss quality control along four dimensions: correctness, diversity, complexity, and fidelity. These dimensions assess whether synthesized environments are executable, varied, appropriately challenging, and faithful to target systems or real-world dynamics.

| Component | Scope in our survey | Main concerns |
| --- | --- | --- |
| Symbolic synthesis | Task-driven, real-world-driven, and de novo environment construction | executable and verifiable feedback at scale |
| Neural synthesis | Pixel-level, word-level, and latent-level world modeling | adaptive simulated dynamics and interaction |
| Quality control and evaluation | Environment reliability and usefulness for agent learning or evaluation | correctness, diversity, complexity, fidelity |

<p align="center">
  <img src="assets/figures/symbolic-synthesis.png" alt="Symbolic environment synthesis" width="88%">
</p>

<p align="center">
  <img src="assets/figures/neural-world-model.png" alt="Neural environment synthesis and world models" width="88%">
</p>

### Related Papers

#### Symbolic Synthesis

- **Generalized Planning in PDDL Domains with Pretrained Large Language Models** [[Paper]](https://doi.org/10.1609/aaai.v38i18.30006) ![](https://img.shields.io/badge/AAAI-2024-blue)
- **EnvGen: Generating and Adapting Environments via LLMs for Training Embodied Agents** [[Paper]](https://doi.org/10.48550/arXiv.2403.12014) ![](https://img.shields.io/badge/arXiv-2024.03-red)
- **NL2Plan: Robust LLM-Driven Planning from Minimal Text Descriptions** [[Paper]](https://doi.org/10.48550/arXiv.2405.04215) ![](https://img.shields.io/badge/arXiv-2024.05-red)
- **Can Language Models Serve as Text-Based World Simulators?** [[Paper]](https://doi.org/10.18653/v1/2024.acl-short.1) ![](https://img.shields.io/badge/ACL-2024-blue)
- **Leveraging Environment Interaction for Automated PDDL Translation and Planning with Large Language Models** [[Paper]](http://papers.nips.cc/paper_files/paper/2024/hash/44af065477781e7f8a8589b14a62c489-Abstract-Conference.html) ![](https://img.shields.io/badge/NeurIPS-2024-blue)
- **WorldCoder, a Model-Based LLM Agent: Building World Models by Writing Code and Interacting with the Environment** [[Paper]](http://papers.nips.cc/paper_files/paper/2024/hash/820c61a0cd419163ccbd2c33b268816e-Abstract-Conference.html) ![](https://img.shields.io/badge/NeurIPS-2024-blue)
- **Generating Symbolic World Models via Test-time Scaling of Large Language Models** [[Paper]](https://openreview.net/forum?id=zVo6PfBa0K) ![](https://img.shields.io/badge/TMLR-2025-blue)
- **Synthesizing world models for bilevel planning** [[Paper]](https://openreview.net/forum?id=m9V4JHLJrD) ![](https://img.shields.io/badge/TMLR-2025-blue)
- **Welcome to the Era of Experience** [[Paper]](https://storage.googleapis.com/deepmind-media/Era-of-Experience%20/The%20Era%20of%20Experience%20Paper.pdf) ![](https://img.shields.io/badge/Google_AI-2025-blue)
- **Planetarium: A Rigorous Benchmark for Translating Text to Structured Planning Languages** [[Paper]](https://doi.org/10.18653/v1/2025.naacl-long.560) ![](https://img.shields.io/badge/NAACL-2025-blue)
- **R2E-Gym: Procedural Environments and Hybrid Verifiers for Scaling Open-Weights SWE Agents** [[Paper]](https://doi.org/10.48550/arXiv.2504.07164) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **SWE-smith: Scaling Data for Software Engineering Agents** [[Paper]](https://doi.org/10.48550/arXiv.2504.21798) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **lmgame-Bench: How Good are LLMs at Playing Games?** [[Paper]](https://arxiv.org/abs/2505.15146) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **Measuring General Intelligence with Generated Games** [[Paper]](https://doi.org/10.48550/arXiv.2505.07215) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **AgentSynth: Scalable Task Generation for Generalist Computer-Use Agents** [[Paper]](https://doi.org/10.48550/arXiv.2506.14205) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **MedAgentGym: A Scalable Agentic Training Environment for Code-Centric Reasoning in Biomedical Data Science** [[Paper]](https://arxiv.org/abs/2506.04405) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **TaskCraft: Automated Generation of Agentic Tasks** [[Paper]](https://doi.org/10.48550/arXiv.2506.10055) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **EmbodiedBench: Comprehensive Benchmarking Multi-modal Large Language Models for Vision-Driven Embodied Agents** [[Paper]](https://proceedings.mlr.press/v267/yang25f.html) ![](https://img.shields.io/badge/ICML-2025-blue)
- **Text2World: Benchmarking Large Language Models for Symbolic World Model Generation** [[Paper]](https://aclanthology.org/2025.findings-acl.1337/) ![](https://img.shields.io/badge/ACL_Findings-2025-blue)
- **Training Software Engineering Agents and Verifiers with SWE-Gym** [[Paper]](https://proceedings.mlr.press/v267/pan25g.html) ![](https://img.shields.io/badge/ICML-2025-blue)
- **Generalizable End-to-End Tool-Use RL with Synthetic CodeGym** [[Paper]](https://doi.org/10.48550/arXiv.2509.17325) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **Mcpmark: A benchmark for stress-testing realistic and comprehensive mcp use** [[Paper]](https://arxiv.org/abs/2509.24002) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **Scaling Agents via Continual Pre-training** [[Paper]](https://doi.org/10.48550/arXiv.2509.13310) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **Towards General Agentic Intelligence via Environment Scaling** [[Paper]](https://doi.org/10.48550/arXiv.2509.13311) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **V-GameGym: Visual Game Generation for Code Large Language Models** [[Paper]](https://doi.org/10.48550/arXiv.2509.20136) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **OSWorld-MCP: Benchmarking MCP Tool Invocation In Computer-Use Agents** [[Paper]](https://doi.org/10.48550/arXiv.2510.24563) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **PaperArena: An Evaluation Benchmark for Tool-Augmented Agentic Reasoning on Scientific Literature** [[Paper]](https://doi.org/10.48550/arXiv.2510.10909) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **AutoEnv: Automated Environments for Measuring Cross-Environment Agent Learning** [[Paper]](https://doi.org/10.48550/arXiv.2511.19304) ![](https://img.shields.io/badge/arXiv-2025.11-red)
- **Procedural Environment Generation for Tool-Use Agents** [[Paper]](https://doi.org/10.18653/v1/2025.emnlp-main.936) ![](https://img.shields.io/badge/EMNLP-2025-blue)
- **Agent2World: Learning to Generate Symbolic World Models via Adaptive Multi-Agent Feedback** [[Paper]](https://doi.org/10.48550/arXiv.2512.22336) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **AutoForge: Automated Environment Synthesis for Agentic Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2512.22857) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **DeepSeek-V3.2: Pushing the Frontier of Open Large Language Models** [[Paper]](https://doi.org/10.48550/arXiv.2512.02556) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **Training Versatile Coding Agents in Synthetic Environments** [[Paper]](https://arxiv.org/abs/2512.12216) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **Endless Terminals: Scaling RL Environments for Terminal Agents** [[Paper]](https://doi.org/10.48550/arXiv.2601.16443) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **EnvScaler: Scaling Tool-Interactive Environments for LLM Agent via Programmatic Synthesis** [[Paper]](https://doi.org/10.48550/arXiv.2601.05808) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **InfiniteWeb: Scalable Web Environment Synthesis for GUI Agent Training** [[Paper]](https://doi.org/10.48550/arXiv.2601.04126) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **LLM-in-Sandbox Elicits General Agentic Intelligence** [[Paper]](https://doi.org/10.48550/arXiv.2601.16206) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **LongCat-Flash-Thinking-2601 Technical Report** [[Paper]](https://doi.org/10.48550/arXiv.2601.16725) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **MedMCP-Calc: Benchmarking LLMs for Realistic Medical Calculator Scenarios via MCP Integration** [[Paper]](https://doi.org/10.48550/arXiv.2601.23049) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **MEnvAgent: Scalable Polyglot Environment Construction for Verifiable Software Engineering** [[Paper]](https://doi.org/10.48550/arXiv.2601.22859) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **MiMo-V2-Flash Technical Report** [[Paper]](https://doi.org/10.48550/arXiv.2601.02780) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **SCALER:Synthetic Scalable Adaptive Learning Environment for Reasoning** [[Paper]](https://doi.org/10.48550/arXiv.2601.04809) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **Agent world model: Infinity synthetic environments for agentic reinforcement learning** [[Paper]](https://arxiv.org/abs/2602.10090) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **AI Gamestore: Scalable, Open-Ended Evaluation of Machine General Intelligence with Human Games** [[Paper]](https://arxiv.org/abs/2602.17594) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **AutoWebWorld: Synthesizing Infinite Verifiable Web Environments via Finite State Machines** [[Paper]](https://arxiv.org/abs/2602.14296) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **CLI-Gym: Scalable CLI Task Generation via Agentic Environment Inversion** [[Paper]](https://arxiv.org/abs/2602.10999) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **DockSmith: Scaling Reliable Coding Environments via an Agentic Docker Builder** [[Paper]](https://doi.org/10.48550/arXiv.2602.00592) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **FinMTM: A Multi-Turn Multimodal Benchmark for Financial Reasoning and Agent Evaluation** [[Paper]](https://doi.org/10.48550/arXiv.2602.03130) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **GameDevBench: Evaluating Agentic Capabilities Through Game Development** [[Paper]](https://arxiv.org/abs/2602.11103) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **GLM-5: from Vibe Coding to Agentic Engineering** [[Paper]](https://doi.org/10.48550/arXiv.2602.15763) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **Hybrid-Gym: Training Coding Agents to Generalize Across Tasks** [[Paper]](https://arxiv.org/abs/2602.16819) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **Immersion in the GitHub Universe: Scaling Coding Agents to Mastery** [[Paper]](https://arxiv.org/abs/2602.09892) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **On Data Engineering for Scaling LLM Terminal Capabilities** [[Paper]](https://arxiv.org/abs/2602.21193) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **ScaleEnv: Scaling Environment Synthesis from Scratch for Generalist Interactive Tool-Use Agent Training** [[Paper]](https://arxiv.org/abs/2602.06820) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **SciAgentGym: Benchmarking Multi-Step Scientific Tool-use in LLM Agents** [[Paper]](https://arxiv.org/abs/2602.12984) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **SWE-Universe: Scale Real-World Verifiable Environments to Millions** [[Paper]](https://doi.org/10.48550/arXiv.2602.02361) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **DIVE: Scaling Diversity in Agentic Task Synthesis for Generalizable Tool Use** [[Paper]](https://arxiv.org/abs/2603.11076) ![](https://img.shields.io/badge/arXiv-2026.03-red)
- **KAT-Coder-V2 Technical Report** [[Paper]](https://arxiv.org/abs/2603.27703) ![](https://img.shields.io/badge/arXiv-2026.03-red)
- **LOGIGEN: Logic-Driven Generation of Verifiable Agentic Tasks** [[Paper]](https://arxiv.org/abs/2603.00540) ![](https://img.shields.io/badge/arXiv-2026.03-red)
- **Safe and Scalable Web Agent Learning via Recreated Websites** [[Paper]](https://arxiv.org/abs/2603.10505) ![](https://img.shields.io/badge/arXiv-2026.03-red)
- **SWE-Hub: A Unified Production System for Scalable, Executable Software Engineering Tasks** [[Paper]](https://arxiv.org/abs/2603.00575) ![](https://img.shields.io/badge/arXiv-2026.03-red)

#### Neural Synthesis and World Models

- **Recurrent World Models Facilitate Policy Evolution** [[Paper]](https://proceedings.neurips.cc/paper/2018/hash/2de5d16682c3c35007e4e92982f1a2ba-Abstract.html) ![](https://img.shields.io/badge/NeurIPS-2018-blue)
- **Self-Supervised Learning from Images with a Joint-Embedding Predictive Architecture** [[Paper]](https://arxiv.org/abs/2301.08243) ![](https://img.shields.io/badge/CVPR-2023-blue)
- **Reasoning with Language Model is Planning with World Model** [[Paper]](https://doi.org/10.18653/v1/2023.emnlp-main.507) ![](https://img.shields.io/badge/EMNLP-2023-blue)
- **Learning and Leveraging World Models in Visual Representation Learning** [[Paper]](https://arxiv.org/abs/2403.00504) ![](https://img.shields.io/badge/arXiv-2024.03-red)
- **Pandora: Towards General World Model with Natural Language Actions and Video States** [[Paper]](https://doi.org/10.48550/arXiv.2406.09455) ![](https://img.shields.io/badge/arXiv-2024.06-red)
- **Diffusion Models Are Real-Time Game Engines** [[Paper]](https://arxiv.org/abs/2408.14837) ![](https://img.shields.io/badge/arXiv-2024.08-red)
- **Dino-wm: World models on pre-trained visual features enable zero-shot planning** [[Paper]](https://arxiv.org/abs/2411.04983) ![](https://img.shields.io/badge/arXiv-2024.11-red)
- **Agent Planning with World Knowledge Model** [[Paper]](http://papers.nips.cc/paper_files/paper/2024/hash/d032263772946dd5026e7f3cd22bce5b-Abstract-Conference.html) ![](https://img.shields.io/badge/NeurIPS-2024-blue)
- **Diffusion for World Modeling: Visual Details Matter in Atari** [[Paper]](http://papers.nips.cc/paper_files/paper/2024/hash/6bdde0373d53d4a501249547084bed43-Abstract-Conference.html) ![](https://img.shields.io/badge/NeurIPS-2024-blue)
- **Dino-foresight: Looking into the future with dino** [[Paper]](https://arxiv.org/abs/2412.11673) ![](https://img.shields.io/badge/arXiv-2024.12-red)
- **Is Your LLM Secretly a World Model of the Internet? Model-Based Planning for Web Agents** [[Paper]](https://openreview.net/forum?id=c6l7yA0HSq) ![](https://img.shields.io/badge/TMLR-2025-blue)
- **Cosmos World Foundation Model Platform for Physical AI** [[Paper]](https://doi.org/10.48550/arXiv.2501.03575) ![](https://img.shields.io/badge/arXiv-2025.01-red)
- **EnerVerse: Envisioning Embodied Future Space for Robotics Manipulation** [[Paper]](https://doi.org/10.48550/arXiv.2501.01895) ![](https://img.shields.io/badge/arXiv-2025.01-red)
- **GAIA-2: A Controllable Multi-View Generative World Model for Autonomous Driving** [[Paper]](https://doi.org/10.48550/arXiv.2503.20523) ![](https://img.shields.io/badge/arXiv-2025.03-red)
- **MineWorld: a Real-Time and Open-Source Interactive World Model on Minecraft** [[Paper]](https://arxiv.org/abs/2504.08388) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **Vimo: A generative visual gui world model for app agents** [[Paper]](https://arxiv.org/abs/2504.13936) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **Dreamgen: Unlocking generalization in robot learning through video world models** [[Paper]](https://arxiv.org/abs/2505.12705) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **Seq-JEPA: Autoregressive Predictive Learning of Invariant-Equivariant World Models** [[Paper]](https://arxiv.org/abs/2505.03176) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **Cosmos-Drive-Dreams: Scalable Synthetic Driving Data Generation with World Foundation Models** [[Paper]](https://doi.org/10.48550/arXiv.2506.09042) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **Dyna-Think: Synergizing Reasoning, Acting, and World Model Simulation in AI Agents** [[Paper]](https://doi.org/10.48550/arXiv.2506.00320) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **Matrix-Game: Interactive World Foundation Model** [[Paper]](https://doi.org/10.48550/arXiv.2506.18701) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **Medical World Model: Generative Simulation of Tumor Evolution for Treatment Planning** [[Paper]](https://doi.org/10.48550/arXiv.2506.02327) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **V-JEPA 2: Self-Supervised Video Models Enable Understanding, Prediction and Planning** [[Paper]](https://doi.org/10.48550/arXiv.2506.09985) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **World modelling improves language model agents** [[Paper]](https://arxiv.org/abs/2506.02918) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **AdaWorld: Learning Adaptable World Models with Latent Actions** [[Paper]](https://proceedings.mlr.press/v267/gao25u.html) ![](https://img.shields.io/badge/ICML-2025-blue)
- **Back to the features: Dino as a foundation for video world models** [[Paper]](https://arxiv.org/abs/2507.19468) ![](https://img.shields.io/badge/arXiv-2025.07-red)
- **Empowering World Models with Reflection for Embodied Video Prediction** [[Paper]](https://proceedings.mlr.press/v267/chi25b.html) ![](https://img.shields.io/badge/ICML-2025-blue)
- **NeuralOS: Towards Simulating Operating Systems via Neural Generative Models** [[Paper]](https://doi.org/10.48550/arXiv.2507.08800) ![](https://img.shields.io/badge/arXiv-2025.07-red)
- **Simura: A world-model-driven simulative reasoning architecture for general goal-oriented agents** [[Paper]](https://arxiv.org/abs/2507.23773) ![](https://img.shields.io/badge/arXiv-2025.07-red)
- **Genie Envisioner: A Unified World Foundation Platform for Robotic Manipulation** [[Paper]](https://doi.org/10.48550/arXiv.2508.05635) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **Learning Primitive Embodied World Models: Towards Scalable Robotic Learning** [[Paper]](https://doi.org/10.48550/arXiv.2508.20840) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **Matrix-Game 2.0: An Open-Source, Real-Time, and Streaming Interactive World Model** [[Paper]](https://doi.org/10.48550/arXiv.2508.13009) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **KeyWorld: Key Frame Reasoning Enables Effective and Efficient World Models** [[Paper]](https://doi.org/10.48550/arXiv.2509.21027) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **Planning with Reasoning using Vision Language World Model** [[Paper]](https://doi.org/10.48550/arXiv.2509.02722) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **CWM: An Open-Weights LLM for Research on Code Generation with World Models** [[Paper]](https://doi.org/10.48550/arXiv.2510.02387) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **R-WoM: Retrieval-augmented World Model For Computer-use Agents** [[Paper]](https://doi.org/10.48550/arXiv.2510.11892) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **Simulating Environments with Reasoning Models for Agent Training** [[Paper]](https://doi.org/10.48550/arXiv.2511.01824) ![](https://img.shields.io/badge/arXiv-2025.11-red)
- **Unlocking Smarter Device Control: Foresighted Planning with a World Model-Driven Code Execution Approach** [[Paper]](https://aclanthology.org/2025.findings-emnlp.213/) ![](https://img.shields.io/badge/EMNLP_Findings-2025-blue)
- **GTM: Simulating the World of Tools for AI Agents** [[Paper]](https://doi.org/10.48550/arXiv.2512.04535) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **Web World Models** [[Paper]](https://doi.org/10.48550/arXiv.2512.23676) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **FlowDreamer: A RGB-D World Model With Flow-Based Motion Representations for Robot Manipulation** [[Paper]](https://doi.org/10.1109/LRA.2026.3653273) ![](https://img.shields.io/badge/IEEE_RAL-2026-blue)
- **Causal World Modeling for Robot Control** [[Paper]](https://doi.org/10.48550/arXiv.2601.21998) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **Cosmos Policy: Fine-Tuning Video Models for Visuomotor Control and Planning** [[Paper]](https://doi.org/10.48550/arXiv.2601.16163) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **Imagine-then-Plan: Agent Learning from Adaptive Lookahead with World Models** [[Paper]](https://doi.org/10.48550/arXiv.2601.08955) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **MobileDreamer: Generative Sketch World Model for GUI Agent** [[Paper]](https://doi.org/10.48550/arXiv.2601.04035) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **Code2World: A GUI World Model via Renderable Code Generation** [[Paper]](https://arxiv.org/abs/2602.09856) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **EchoJEPA: A Latent Predictive Foundation Model for Echocardiography** [[Paper]](https://arxiv.org/abs/2602.02603) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **Generative Visual Code Mobile World Models** [[Paper]](https://doi.org/10.48550/arXiv.2602.01576) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **LIVE: Long-horizon Interactive Video World Modeling** [[Paper]](https://doi.org/10.48550/arXiv.2602.03747) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **SWE-World: Building Software Engineering Agents in Docker-Free Environments** [[Paper]](https://doi.org/10.48550/arXiv.2602.03419) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **WebWorld: A Large-Scale World Model for Web Agent Training** [[Paper]](https://arxiv.org/abs/2602.14721) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **World action models are zero-shot policies** [[Paper]](https://arxiv.org/abs/2602.15922) ![](https://img.shields.io/badge/arXiv-2026.02-red)

#### Quality Control and Evaluation

- **InterCode: Standardizing and Benchmarking Interactive Coding with Execution Feedback** [[Paper]](https://arxiv.org/abs/2306.14898) ![](https://img.shields.io/badge/NeurIPS-2023-blue)
- **Self-Supervised Learning from Images with a Joint-Embedding Predictive Architecture** [[Paper]](https://arxiv.org/abs/2301.08243) ![](https://img.shields.io/badge/CVPR-2023-blue)
- **Mobile-env: Building qualified evaluation benchmarks for llm-gui interaction** [[Paper]](https://arxiv.org/abs/2305.08144) ![](https://img.shields.io/badge/arXiv-2023.05-red)
- **API-Bank: A Comprehensive Benchmark for Tool-Augmented LLMs** [[Paper]](https://doi.org/10.18653/v1/2023.emnlp-main.187) ![](https://img.shields.io/badge/EMNLP-2023-blue)
- **Mind2Web: Towards a Generalist Agent for the Web** [[Paper]](http://papers.nips.cc/paper_files/paper/2023/hash/5950bf290a1570ea401bf98882128160-Abstract-Datasets_and_Benchmarks.html) ![](https://img.shields.io/badge/NeurIPS-2023-blue)
- **Reasoning with Language Model is Planning with World Model** [[Paper]](https://doi.org/10.18653/v1/2023.emnlp-main.507) ![](https://img.shields.io/badge/EMNLP-2023-blue)
- **AgentBench: Evaluating LLMs as Agents** [[Paper]](https://openreview.net/forum?id=zAdUB0aCTQ) ![](https://img.shields.io/badge/ICLR-2024-blue)
- **NL2Plan: Robust LLM-Driven Planning from Minimal Text Descriptions** [[Paper]](https://doi.org/10.48550/arXiv.2405.04215) ![](https://img.shields.io/badge/arXiv-2024.05-red)
- **ToolLLM: Facilitating Large Language Models to Master 16000+ Real-world APIs** [[Paper]](https://openreview.net/forum?id=dHng2O0Jjr) ![](https://img.shields.io/badge/ICLR-2024-blue)
- **WebArena: A Realistic Web Environment for Building Autonomous Agents** [[Paper]](https://openreview.net/forum?id=oKn9c6ytLx) ![](https://img.shields.io/badge/ICLR-2024-blue)
- **AgentGen: Enhancing Planning Abilities for Large Language Model based Agent via Environment and Task Generation** [[Paper]](https://doi.org/10.48550/arXiv.2408.00764) ![](https://img.shields.io/badge/arXiv-2024.08-red)
- **Diffusion Models Are Real-Time Game Engines** [[Paper]](https://arxiv.org/abs/2408.14837) ![](https://img.shields.io/badge/arXiv-2024.08-red)
- **Agent Planning with World Knowledge Model** [[Paper]](http://papers.nips.cc/paper_files/paper/2024/hash/d032263772946dd5026e7f3cd22bce5b-Abstract-Conference.html) ![](https://img.shields.io/badge/NeurIPS-2024-blue)
- **Diffusion for World Modeling: Visual Details Matter in Atari** [[Paper]](http://papers.nips.cc/paper_files/paper/2024/hash/6bdde0373d53d4a501249547084bed43-Abstract-Conference.html) ![](https://img.shields.io/badge/NeurIPS-2024-blue)
- **Leveraging Environment Interaction for Automated PDDL Translation and Planning with Large Language Models** [[Paper]](http://papers.nips.cc/paper_files/paper/2024/hash/44af065477781e7f8a8589b14a62c489-Abstract-Conference.html) ![](https://img.shields.io/badge/NeurIPS-2024-blue)
- **Generating Symbolic World Models via Test-time Scaling of Large Language Models** [[Paper]](https://openreview.net/forum?id=zVo6PfBa0K) ![](https://img.shields.io/badge/TMLR-2025-blue)
- **Is Your LLM Secretly a World Model of the Internet? Model-Based Planning for Web Agents** [[Paper]](https://openreview.net/forum?id=c6l7yA0HSq) ![](https://img.shields.io/badge/TMLR-2025-blue)
- **EnerVerse: Envisioning Embodied Future Space for Robotics Manipulation** [[Paper]](https://doi.org/10.48550/arXiv.2501.01895) ![](https://img.shields.io/badge/arXiv-2025.01-red)
- **MedAgentBench: Dataset for Benchmarking LLMs as Agents in Medical Applications** [[Paper]](https://doi.org/10.48550/arXiv.2501.14654) ![](https://img.shields.io/badge/arXiv-2025.01-red)
- **GAIA-2: A Controllable Multi-View Generative World Model for Autonomous Driving** [[Paper]](https://doi.org/10.48550/arXiv.2503.20523) ![](https://img.shields.io/badge/arXiv-2025.03-red)
- **R2E-Gym: Procedural Environments and Hybrid Verifiers for Scaling Open-Weights SWE Agents** [[Paper]](https://doi.org/10.48550/arXiv.2504.07164) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **SWE-smith: Scaling Data for Software Engineering Agents** [[Paper]](https://doi.org/10.48550/arXiv.2504.21798) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **Dreamgen: Unlocking generalization in robot learning through video world models** [[Paper]](https://arxiv.org/abs/2505.12705) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **Measuring General Intelligence with Generated Games** [[Paper]](https://doi.org/10.48550/arXiv.2505.07215) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **AgentSynth: Scalable Task Generation for Generalist Computer-Use Agents** [[Paper]](https://doi.org/10.48550/arXiv.2506.14205) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **Dyna-Think: Synergizing Reasoning, Acting, and World Model Simulation in AI Agents** [[Paper]](https://doi.org/10.48550/arXiv.2506.00320) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **Matrix-Game: Interactive World Foundation Model** [[Paper]](https://doi.org/10.48550/arXiv.2506.18701) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **TaskCraft: Automated Generation of Agentic Tasks** [[Paper]](https://doi.org/10.48550/arXiv.2506.10055) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **AdaWorld: Learning Adaptable World Models with Latent Actions** [[Paper]](https://proceedings.mlr.press/v267/gao25u.html) ![](https://img.shields.io/badge/ICML-2025-blue)
- **Training Software Engineering Agents and Verifiers with SWE-Gym** [[Paper]](https://proceedings.mlr.press/v267/pan25g.html) ![](https://img.shields.io/badge/ICML-2025-blue)
- **Genie Envisioner: A Unified World Foundation Platform for Robotic Manipulation** [[Paper]](https://doi.org/10.48550/arXiv.2508.05635) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **GVGAI-LLM: Evaluating Large Language Model Agents with Infinite Games** [[Paper]](https://arxiv.org/abs/2508.08501) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **MCP-Universe: Benchmarking Large Language Models with Real-World Model Context Protocol Servers** [[Paper]](https://doi.org/10.48550/arXiv.2508.14704) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **Planning with Reasoning using Vision Language World Model** [[Paper]](https://doi.org/10.48550/arXiv.2509.02722) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **V-GameGym: Visual Game Generation for Code Large Language Models** [[Paper]](https://doi.org/10.48550/arXiv.2509.20136) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **OSWorld-MCP: Benchmarking MCP Tool Invocation In Computer-Use Agents** [[Paper]](https://doi.org/10.48550/arXiv.2510.24563) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **PaperArena: An Evaluation Benchmark for Tool-Augmented Agentic Reasoning on Scientific Literature** [[Paper]](https://doi.org/10.48550/arXiv.2510.10909) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **Agent2World: Learning to Generate Symbolic World Models via Adaptive Multi-Agent Feedback** [[Paper]](https://doi.org/10.48550/arXiv.2512.22336) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **AutoForge: Automated Environment Synthesis for Agentic Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2512.22857) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **Endless Terminals: Scaling RL Environments for Terminal Agents** [[Paper]](https://doi.org/10.48550/arXiv.2601.16443) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **EnvScaler: Scaling Tool-Interactive Environments for LLM Agent via Programmatic Synthesis** [[Paper]](https://doi.org/10.48550/arXiv.2601.05808) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **InfiniteWeb: Scalable Web Environment Synthesis for GUI Agent Training** [[Paper]](https://doi.org/10.48550/arXiv.2601.04126) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **MobileDreamer: Generative Sketch World Model for GUI Agent** [[Paper]](https://doi.org/10.48550/arXiv.2601.04035) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **Terminal-Bench: Benchmarking Agents on Hard, Realistic Tasks in Command Line Interfaces** [[Paper]](https://doi.org/10.48550/arXiv.2601.11868) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **Agent world model: Infinity synthetic environments for agentic reinforcement learning** [[Paper]](https://arxiv.org/abs/2602.10090) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **AI Gamestore: Scalable, Open-Ended Evaluation of Machine General Intelligence with Human Games** [[Paper]](https://arxiv.org/abs/2602.17594) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **AutoWebWorld: Synthesizing Infinite Verifiable Web Environments via Finite State Machines** [[Paper]](https://arxiv.org/abs/2602.14296) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **CLI-Gym: Scalable CLI Task Generation via Agentic Environment Inversion** [[Paper]](https://arxiv.org/abs/2602.10999) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **GameDevBench: Evaluating Agentic Capabilities Through Game Development** [[Paper]](https://arxiv.org/abs/2602.11103) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **Immersion in the GitHub Universe: Scaling Coding Agents to Mastery** [[Paper]](https://arxiv.org/abs/2602.09892) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **ScaleEnv: Scaling Environment Synthesis from Scratch for Generalist Interactive Tool-Use Agent Training** [[Paper]](https://arxiv.org/abs/2602.06820) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **SciAgentGym: Benchmarking Multi-Step Scientific Tool-use in LLM Agents** [[Paper]](https://arxiv.org/abs/2602.12984) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **SWE-Universe: Scale Real-World Verifiable Environments to Millions** [[Paper]](https://doi.org/10.48550/arXiv.2602.02361) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **SWE-World: Building Software Engineering Agents in Docker-Free Environments** [[Paper]](https://doi.org/10.48550/arXiv.2602.03419) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **WebWorld: A Large-Scale World Model for Web Agent Training** [[Paper]](https://arxiv.org/abs/2602.14721) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **LOGIGEN: Logic-Driven Generation of Verifiable Agentic Tasks** [[Paper]](https://arxiv.org/abs/2603.00540) ![](https://img.shields.io/badge/arXiv-2026.03-red)
- **Safe and Scalable Web Agent Learning via Recreated Websites** [[Paper]](https://arxiv.org/abs/2603.10505) ![](https://img.shields.io/badge/arXiv-2026.03-red)
- **SWE-Hub: A Unified Production System for Scalable, Executable Software Engineering Tasks** [[Paper]](https://arxiv.org/abs/2603.00575) ![](https://img.shields.io/badge/arXiv-2026.03-red)

## Agent Evolution

We discuss how environments support agent capability growth. Agent evolution includes external structural adaptations, such as memory and workflow evolution, and internal parametric changes, such as offline trajectory-centric evolution and online exploration-centric reinforcement learning.

| Direction | Representative mechanisms |
| --- | --- |
| Memory-centric experience evolution | Instance trajectories, abstract scripts, structured skills |
| Orchestration-centric workflow evolution | Fixed workflows, automated workflows, evolving workflows |
| Trajectory-centric offline evolution | Task synthesis, trajectory synthesis, trajectory refinement |
| Exploration-centric online evolution | Reasoning structure design, reward design, training algorithm optimization |

<p align="center">
  <img src="assets/figures/agent-evolution.png" alt="Agent evolution in environments" width="90%">
</p>

### Related Papers

#### Memory-Centric Experience Evolution

- **MemGPT: Towards LLMs as Operating Systems** [[Paper]](https://doi.org/10.48550/arXiv.2310.08560) ![](https://img.shields.io/badge/arXiv-2023.10-red)
- **Voyager: An Open-Ended Embodied Agent with Large Language Models** [[Paper]](https://openreview.net/forum?id=ehfRiF0R3a) ![](https://img.shields.io/badge/TMLR-2024-blue)
- **Synapse: Trajectory-as-Exemplar Prompting with Memory for Computer Control** [[Paper]](https://openreview.net/forum?id=Pc8AU1aF5e) ![](https://img.shields.io/badge/ICLR-2024-blue)
- **Agent-Pro: Learning to Evolve via Policy-Level Reflection and Optimization** [[Paper]](https://doi.org/10.18653/v1/2024.acl-long.292) ![](https://img.shields.io/badge/ACL-2024-blue)
- **Agent Workflow Memory** [[Paper]](https://doi.org/10.48550/arXiv.2409.07429) ![](https://img.shields.io/badge/arXiv-2024.09-red)
- **CoPS: Empowering LLM Agents with Provable Cross-Task Experience Sharing** [[Paper]](https://doi.org/10.48550/arXiv.2410.16670) ![](https://img.shields.io/badge/arXiv-2024.10-red)
- **Embodied large language models enable robots to complete complex tasks in unpredictable environments** [[Paper]](https://doi.org/10.1038/s42256-025-01005-x) ![](https://img.shields.io/badge/Nat._Mach._Intell.-2025-blue)
- **Inducing Programmatic Skills for Agentic Tasks** [[Paper]](https://doi.org/10.48550/arXiv.2504.06821) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **SkillWeaver: Web Agents can Self-Improve by Discovering and Honing Skills** [[Paper]](https://doi.org/10.48550/arXiv.2504.07079) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **Darwin Godel Machine: Open-Ended Evolution of Self-Improving Agents** [[Paper]](https://doi.org/10.48550/arXiv.2505.22954) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **Rethinking Memory in AI: Taxonomy, Operations, Topics, and Future Directions** [[Paper]](https://doi.org/10.48550/arXiv.2505.00675) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **Agent KB: Leveraging Cross-Domain Experience for Agentic Problem Solving** [[Paper]](https://doi.org/10.48550/arXiv.2507.06229) ![](https://img.shields.io/badge/arXiv-2025.07-red)
- **Enhancing Open-Domain Task-Solving Capability of LLMs via Autonomous Tool Integration from GitHub** [[Paper]](https://aclanthology.org/2025.acl-long.845/) ![](https://img.shields.io/badge/ACL-2025-blue)
- **Memp: Exploring Agent Procedural Memory** [[Paper]](https://doi.org/10.48550/arXiv.2508.06433) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **ReasoningBank: Scaling Agent Self-Evolving with Reasoning Memory** [[Paper]](https://doi.org/10.48550/arXiv.2509.25140) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **DeepAgent: A General Reasoning Agent with Scalable Toolsets** [[Paper]](https://doi.org/10.48550/arXiv.2510.21618) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **Training-Free Group Relative Policy Optimization** [[Paper]](https://doi.org/10.48550/arXiv.2510.08191) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **FLEX: Continuous Agent Evolution via Forward Learning from Experience** [[Paper]](https://doi.org/10.48550/arXiv.2511.06449) ![](https://img.shields.io/badge/arXiv-2025.11-red)
- **O-Mem: Omni Memory System for Personalized, Long Horizon, Self-Evolving Agents** [[Paper]](https://arxiv.org/abs/2511.13593) ![](https://img.shields.io/badge/arXiv-2025.11-red)
- **Experience-Evolving Multi-Turn Tool-Use Agent with Hybrid Episodic-Procedural Memory** [[Paper]](https://arxiv.org/abs/2512.07287) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **Memory in the Age of AI Agents** [[Paper]](https://doi.org/10.48550/arXiv.2512.13564) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **Reinforcement Learning for Self-Improving Agent with Skill Library** [[Paper]](https://doi.org/10.48550/arXiv.2512.17102) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **Remember Me, Refine Me: A Dynamic Procedural Memory Framework for Experience-Driven Agent Evolution** [[Paper]](https://doi.org/10.48550/arXiv.2512.10696) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **WorldMM: Dynamic Multimodal Memory Agent for Long Video Reasoning** [[Paper]](https://doi.org/10.48550/arXiv.2512.02425) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **Learning How to Remember: A Meta-Cognitive Management Method for Structured and Transferable Agent Memory** [[Paper]](https://arxiv.org/abs/2601.07470) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **Bifrost: Steering Strategic Trajectories to Bridge Contextual Gaps for Self-Improving Agents** [[Paper]](https://arxiv.org/abs/2602.05810) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **Learning Physical Principles from Interaction: Self-Evolving Planning via Test-Time Memory** [[Paper]](https://arxiv.org/abs/2602.20323) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **Rethinking Memory Mechanisms of Foundation Agents in the Second Half: A Survey** [[Paper]](https://doi.org/10.48550/arXiv.2602.06052) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **SkillOrchestra: Learning to Route Agents via Skill Transfer** [[Paper]](https://arxiv.org/abs/2602.19672) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **SkillRL: Evolving Agents via Recursive Skill-Augmented Reinforcement Learning** [[Paper]](https://arxiv.org/abs/2602.08234) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **Think While Watching: Online Streaming Segment-Level Memory for Multi-Turn Video Reasoning in Multimodal Large Language Models** [[Paper]](https://arxiv.org/abs/2603.11896) ![](https://img.shields.io/badge/arXiv-2026.03-red)

#### Orchestration-Centric Workflow Evolution

- **LLM+P: Empowering Large Language Models with Optimal Planning Proficiency** [[Paper]](https://doi.org/10.48550/arXiv.2304.11477) ![](https://img.shields.io/badge/arXiv-2023.04-red)
- **ReAct: Synergizing Reasoning and Acting in Language Models** [[Paper]](https://openreview.net/forum?id=WE_vluYUL-X) ![](https://img.shields.io/badge/ICLR-2023-blue)
- **ReWOO: Decoupling Reasoning from Observations for Efficient Augmented Language Models** [[Paper]](https://arxiv.org/abs/2305.18323) ![](https://img.shields.io/badge/arXiv-2023.05-red)
- **AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation Framework** [[Paper]](https://doi.org/10.48550/arXiv.2308.08155) ![](https://img.shields.io/badge/arXiv-2023.08-red)
- **CAMEL: Communicative Agents for "Mind" Exploration of Large Language Model Society** [[Paper]](http://papers.nips.cc/paper_files/paper/2023/hash/a3621ee907def47c1b952ade25c67698-Abstract-Conference.html) ![](https://img.shields.io/badge/NeurIPS-2023-blue)
- **HuggingGPT: Solving AI Tasks with ChatGPT and its Friends in Hugging Face** [[Paper]](http://papers.nips.cc/paper_files/paper/2023/hash/77c33e6a367922d003ff102ffb92b658-Abstract-Conference.html) ![](https://img.shields.io/badge/NeurIPS-2023-blue)
- **Self-Refine: Iterative Refinement with Self-Feedback** [[Paper]](http://papers.nips.cc/paper_files/paper/2023/hash/91edff07232fb1b55a505a9e9f6c0ff3-Abstract-Conference.html) ![](https://img.shields.io/badge/NeurIPS-2023-blue)
- **Tree of Thoughts: Deliberate Problem Solving with Large Language Models** [[Paper]](http://papers.nips.cc/paper_files/paper/2023/hash/271db9922b8d1f4dd7aaef84ed5ac703-Abstract-Conference.html) ![](https://img.shields.io/badge/NeurIPS-2023-blue)
- **MAGIS: LLM-Based Multi-Agent Framework for GitHub Issue Resolution** [[Paper]](https://arxiv.org/abs/2403.17927) ![](https://img.shields.io/badge/NeurIPS-2024-blue)
- **Simulate Before Act: Model-Based Planning for Web Agents** [[Paper]](https://openreview.net/forum?id=JDa5RiTIC7) ![](https://img.shields.io/badge/OpenReview-2024-blue)
- **SWE-agent: Agent-Computer Interfaces Enable Automated Software Engineering** [[Paper]](https://arxiv.org/abs/2405.15793) ![](https://img.shields.io/badge/NeurIPS-2024-blue)
- **QuantAgent: Seeking Holy Grail in Trading by Self-Improving Large Language Model** [[Paper]](https://doi.org/10.48550/arXiv.2402.03755) ![](https://img.shields.io/badge/arXiv-2024.02-red)
- **Embodied LLM Agents Learn to Cooperate in Organized Teams** [[Paper]](https://doi.org/10.48550/arXiv.2403.12482) ![](https://img.shields.io/badge/arXiv-2024.03-red)
- **Agent hospital: A simulacrum of hospital with evolvable medical agents** [[Paper]](https://arxiv.org/abs/2405.02957) ![](https://img.shields.io/badge/arXiv-2024.05-red)
- **DSPy: Compiling Declarative Language Model Calls into State-of-the-Art Pipelines** [[Paper]](https://openreview.net/forum?id=sY5N0zY5Od) ![](https://img.shields.io/badge/ICLR-2024-blue)
- **Large Language Models as Tool Makers** [[Paper]](https://openreview.net/forum?id=qV83K9d5WB) ![](https://img.shields.io/badge/ICLR-2024-blue)
- **MetaGPT: Meta Programming for A Multi-Agent Collaborative Framework** [[Paper]](https://openreview.net/forum?id=VtmBAGCN7o) ![](https://img.shields.io/badge/ICLR-2024-blue)
- **ToolChain: Efficient Action Space Navigation in Large Language Models with A Search** [[Paper]](https://openreview.net/forum?id=B6pQxqUcT8) ![](https://img.shields.io/badge/ICLR-2024-blue)
- **CodeNav: Beyond tool-use to using real-world codebases with LLM agents** [[Paper]](https://arxiv.org/abs/2406.12276) ![](https://img.shields.io/badge/arXiv-2024.06-red)
- **Coder: Issue resolving with multi-agent and task graphs** [[Paper]](https://arxiv.org/abs/2406.01304) ![](https://img.shields.io/badge/arXiv-2024.06-red)
- **MindAgent: Emergent Gaming Interaction** [[Paper]](https://doi.org/10.18653/v1/2024.findings-naacl.200) ![](https://img.shields.io/badge/ACL_Findings-2024-blue)
- **TextGrad: Automatic "Differentiation" via Text** [[Paper]](https://doi.org/10.48550/arXiv.2406.07496) ![](https://img.shields.io/badge/arXiv-2024.06-red)
- **Agent-E: From Autonomous Web Navigation to Foundational Design Principles in Agentic Systems** [[Paper]](https://doi.org/10.48550/arXiv.2407.13032) ![](https://img.shields.io/badge/arXiv-2024.07-red)
- **Agentless: Demystifying LLM-based Software Engineering Agents** [[Paper]](https://doi.org/10.48550/arXiv.2407.01489) ![](https://img.shields.io/badge/arXiv-2024.07-red)
- **AutoFlow: Automated Workflow Generation for Large Language Model Agents** [[Paper]](https://doi.org/10.48550/arXiv.2407.12821) ![](https://img.shields.io/badge/arXiv-2024.07-red)
- **GPTSwarm: Language Agents as Optimizable Graphs** [[Paper]](https://proceedings.mlr.press/v235/zhuge24a.html) ![](https://img.shields.io/badge/ICML-2024-blue)
- **WebVoyager: Building an End-to-End Web Agent with Large Multimodal Models** [[Paper]](https://doi.org/10.18653/v1/2024.acl-long.371) ![](https://img.shields.io/badge/ACL-2024-blue)
- **AutoCodeRover: Autonomous Program Improvement** [[Paper]](https://doi.org/10.1145/3650212.3680384) ![](https://img.shields.io/badge/ACM-2024-blue)
- **ControlLLM: Augment Language Models with Tools by Searching on Graphs** [[Paper]](https://doi.org/10.1007/978-3-031-73254-6_6) ![](https://img.shields.io/badge/ECCV-2024-blue)
- **Hyperagent: Generalist software engineering agents to solve coding tasks at scale** [[Paper]](https://arxiv.org/abs/2409.16299) ![](https://img.shields.io/badge/arXiv-2024.09-red)
- **See and Think: Embodied Agent in Virtual Environment** [[Paper]](https://doi.org/10.1007/978-3-031-73242-3_11) ![](https://img.shields.io/badge/ECCV-2024-blue)
- **VideoAgent: Long-Form Video Understanding with Large Language Model as Agent** [[Paper]](https://doi.org/10.1007/978-3-031-72989-8_4) ![](https://img.shields.io/badge/ECCV-2024-blue)
- **Swe-search: Enhancing software agents with monte carlo tree search and iterative refinement** [[Paper]](https://arxiv.org/abs/2410.20285) ![](https://img.shields.io/badge/arXiv-2024.10-red)
- **Agent Planning with World Knowledge Model** [[Paper]](http://papers.nips.cc/paper_files/paper/2024/hash/d032263772946dd5026e7f3cd22bce5b-Abstract-Conference.html) ![](https://img.shields.io/badge/NeurIPS-2024-blue)
- **AvaTaR: Optimizing LLM Agents for Tool Usage via Contrastive Reasoning** [[Paper]](http://papers.nips.cc/paper_files/paper/2024/hash/2db8ce969b000fe0b3fb172490c33ce8-Abstract-Conference.html) ![](https://img.shields.io/badge/NeurIPS-2024-blue)
- **Thought of Search: Planning with Language Models Through The Lens of Efficiency** [[Paper]](http://papers.nips.cc/paper_files/paper/2024/hash/fa080fe0f218871faec1d8ba20e491d5-Abstract-Conference.html) ![](https://img.shields.io/badge/NeurIPS-2024-blue)
- **Alibaba LingmaAgent: Improving Automated Issue Resolution via Comprehensive Repository Exploration** [[Paper]](https://arxiv.org/abs/2406.01422) ![](https://img.shields.io/badge/FSE-2025-blue)
- **RepairAgent: An Autonomous, LLM-Based Agent for Program Repair** [[Paper]](https://arxiv.org/abs/2403.17134) ![](https://img.shields.io/badge/ICSE-2025-blue)
- **OctoTools: An Agentic Framework with Extensible Tools for Complex Reasoning** [[Paper]](https://doi.org/10.48550/arXiv.2502.11271) ![](https://img.shields.io/badge/arXiv-2025.02-red)
- **ScoreFlow: Mastering LLM Agent Workflows via Score-based Preference Optimization** [[Paper]](https://doi.org/10.48550/arXiv.2502.04306) ![](https://img.shields.io/badge/arXiv-2025.02-red)
- **WebPilot: A Versatile and Autonomous Multi-Agent System for Web Task Execution with Strategic Exploration** [[Paper]](https://doi.org/10.1609/aaai.v39i22.34505) ![](https://img.shields.io/badge/AAAI-2025-blue)
- **LVAgent: Long Video Understanding by Multi-Round Dynamical Collaboration of MLLM Agents** [[Paper]](https://doi.org/10.48550/arXiv.2503.10200) ![](https://img.shields.io/badge/arXiv-2025.03-red)
- **Open Deep Search: Democratizing Search with Open-source Reasoning Agents** [[Paper]](https://doi.org/10.48550/arXiv.2503.20201) ![](https://img.shields.io/badge/arXiv-2025.03-red)
- **AFlow: Automating Agentic Workflow Generation** [[Paper]](https://openreview.net/forum?id=z5uVAKwmjf) ![](https://img.shields.io/badge/ICLR-2025-blue)
- **AgentSquare: Automatic LLM Agent Search in Modular Design Space** [[Paper]](https://openreview.net/forum?id=mPdmDYIQ7f) ![](https://img.shields.io/badge/ICLR-2025-blue)
- **Automated Design of Agentic Systems** [[Paper]](https://openreview.net/forum?id=t9U3LW7JVX) ![](https://img.shields.io/badge/ICLR-2025-blue)
- **FlowReasoner: Reinforcing Query-Level Meta-Agents** [[Paper]](https://arxiv.org/abs/2504.15257) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **MindSearch: Mimicking Human Minds Elicits Deep AI Searcher** [[Paper]](https://openreview.net/forum?id=xgtXkyqw1f) ![](https://img.shields.io/badge/ICLR-2025-blue)
- **Tool-Planner: Task Planning with Clusters across Multiple Tools** [[Paper]](https://openreview.net/forum?id=dRz3cizftU) ![](https://img.shields.io/badge/ICLR-2025-blue)
- **Demystifying and Enhancing the Efficiency of Large Language Model Based Search Agents** [[Paper]](https://doi.org/10.48550/arXiv.2505.12065) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **Multi-Agent Collaboration via Evolving Orchestration** [[Paper]](https://doi.org/10.48550/arXiv.2505.19591) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **OWL: Optimized Workforce Learning for General Multi-Agent Assistance in Real-World Task Automation** [[Paper]](https://doi.org/10.48550/arXiv.2505.23885) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **Process vs. Outcome Reward: Which is Better for Agentic RAG Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2505.14069) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **Code Researcher: Deep Research Agent for Large Systems Code and Commit History** [[Paper]](https://doi.org/10.48550/arXiv.2506.11060) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **Multimodal DeepResearcher: Generating Text-Chart Interleaved Reports From Scratch with Agentic Framework** [[Paper]](https://doi.org/10.48550/arXiv.2506.02454) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **Explorer: Scaling Exploration-driven Web Trajectory Synthesis for Multimodal Web Agents** [[Paper]](https://aclanthology.org/2025.findings-acl.326/) ![](https://img.shields.io/badge/ACL_Findings-2025-blue)
- **Multi-agent Architecture Search via Agentic Supernet** [[Paper]](https://proceedings.mlr.press/v267/zhang25bi.html) ![](https://img.shields.io/badge/ICML-2025-blue)
- **Plan-and-Act: Improving Planning of Agents for Long-Horizon Tasks** [[Paper]](https://proceedings.mlr.press/v267/erdogan25a.html) ![](https://img.shields.io/badge/ICML-2025-blue)
- **Chain-of-Agents: End-to-End Agent Foundation Models via Multi-Agent Distillation and Agentic RL** [[Paper]](https://doi.org/10.48550/arXiv.2508.13167) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **Cognitive Kernel-Pro: A Framework for Deep Research Agents and Agent Foundation Models Training** [[Paper]](https://doi.org/10.48550/arXiv.2508.00414) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **DyFlow: Dynamic Workflow Framework for Agentic Reasoning** [[Paper]](https://doi.org/10.48550/arXiv.2509.26062) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **RobustFlow: Towards Robust Agentic Workflow Generation** [[Paper]](https://doi.org/10.48550/arXiv.2509.21834) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **Constrained Natural Language Action Planning for Resilient Embodied Systems** [[Paper]](https://doi.org/10.48550/arXiv.2510.06357) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **In-the-Flow Agentic System Optimization for Effective Planning and Tool Use** [[Paper]](https://doi.org/10.48550/arXiv.2510.05592) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **Learning on the Job: An Experience-Driven Self-Evolving Agent for Long-Horizon Tasks** [[Paper]](https://doi.org/10.48550/arXiv.2510.08002) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **MGA: Memory-Driven GUI Agent for Observation-Centric Interaction** [[Paper]](https://doi.org/10.48550/arXiv.2510.24168) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **ManuSearch: Democratizing Deep Search in Large Language Models with a Transparent and Open Multi-Agent Framework** [[Paper]](https://aclanthology.org/2025.findings-emnlp.130/) ![](https://img.shields.io/badge/EMNLP_Findings-2025-blue)
- **Real-Time Reasoning Agents in Evolving Environments** [[Paper]](https://doi.org/10.48550/arXiv.2511.04898) ![](https://img.shields.io/badge/arXiv-2025.11-red)
- **ResearStudio: A Human-intervenable Framework for Building Controllable Deep Research Agents** [[Paper]](https://doi.org/10.18653/v1/2025.emnlp-demos.69) ![](https://img.shields.io/badge/EMNLP-2025-blue)
- **Search-o1: Agentic Search-Enhanced Large Reasoning Models** [[Paper]](https://doi.org/10.18653/v1/2025.emnlp-main.276) ![](https://img.shields.io/badge/EMNLP-2025-blue)
- **The openhands software agent sdk: A composable and extensible foundation for production agents** [[Paper]](https://arxiv.org/abs/2511.03690) ![](https://img.shields.io/badge/arXiv-2025.11-red)
- **CASCADE: Cumulative Agentic Skill Creation through Autonomous Development and Evolution** [[Paper]](https://doi.org/10.48550/arXiv.2512.23880) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **Grammar Search for Multi-Agent Systems** [[Paper]](https://arxiv.org/abs/2512.14079) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **ClinicalReTrial: A Self-Evolving AI Agent for Clinical Trial Protocol Optimization** [[Paper]](https://doi.org/10.48550/arXiv.2601.00290) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **EvoClinician: A Self-Evolving Agent for Multi-Turn Medical Diagnosis via Test-Time Evolutionary Learning** [[Paper]](https://doi.org/10.48550/arXiv.2601.22964) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **ReCreate: Reasoning and Creating Domain Agents Driven by Experience** [[Paper]](https://doi.org/10.48550/arXiv.2601.11100) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **Yunjue Agent Tech Report: A Fully Reproducible, Zero-Start In-Situ Self-Evolving Agent System for Open-Ended Tasks** [[Paper]](https://doi.org/10.48550/arXiv.2601.18226) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **AOrchestra: Automating Sub-Agent Creation for Agentic Orchestration** [[Paper]](https://arxiv.org/abs/2602.03786) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **Dr. MAS: Stable Reinforcement Learning for Multi-Agent LLM Systems** [[Paper]](https://arxiv.org/abs/2602.08847) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **WideSeek-R1: Exploring Width Scaling for Broad Information Seeking via Multi-Agent Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2602.04634) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **Workflow-R1: Group Sub-sequence Policy Optimization for Multi-turn Workflow Construction** [[Paper]](https://doi.org/10.48550/arXiv.2602.01202) ![](https://img.shields.io/badge/arXiv-2026.02-red)

#### Trajectory-Centric Offline Evolution

- **ToolCoder: Teach Code Generation Models to use API search tools** [[Paper]](https://doi.org/10.48550/arXiv.2305.04032) ![](https://img.shields.io/badge/arXiv-2023.05-red)
- **ToolAlpaca: Generalized Tool Learning for Language Models with 3000 Simulated Cases** [[Paper]](https://doi.org/10.48550/arXiv.2306.05301) ![](https://img.shields.io/badge/arXiv-2023.06-red)
- **Toolformer: Language Models Can Teach Themselves to Use Tools** [[Paper]](http://papers.nips.cc/paper_files/paper/2023/hash/d842425e4bf79ba039352da0f658a906-Abstract-Conference.html) ![](https://img.shields.io/badge/NeurIPS-2023-blue)
- **Trial and Error: Exploration-Based Trajectory Optimization for LLM Agents** [[Paper]](https://doi.org/10.48550/arXiv.2403.02502) ![](https://img.shields.io/badge/arXiv-2024.03-red)
- **Large language models can self-improve at web agent tasks** [[Paper]](https://arxiv.org/abs/2405.20309) ![](https://img.shields.io/badge/arXiv-2024.05-red)
- **ToolLLM: Facilitating Large Language Models to Master 16000+ Real-world APIs** [[Paper]](https://openreview.net/forum?id=dHng2O0Jjr) ![](https://img.shields.io/badge/ICLR-2024-blue)
- **BAGEL: Bootstrapping Agents by Guiding Exploration with Language** [[Paper]](https://proceedings.mlr.press/v235/murty24a.html) ![](https://img.shields.io/badge/ICML-2024-blue)
- **Agent-FLAN: Designing Data and Methods of Effective Agent Tuning for Large Language Models** [[Paper]](https://doi.org/10.18653/v1/2024.findings-acl.557) ![](https://img.shields.io/badge/ACL_Findings-2024-blue)
- **AgentTuning: Enabling Generalized Agent Abilities for LLMs** [[Paper]](https://doi.org/10.18653/v1/2024.findings-acl.181) ![](https://img.shields.io/badge/ACL_Findings-2024-blue)
- **Lingma SWE-GPT: An Open Development-Process-Centric Language Model for Automated Software Improvement** [[Paper]](https://doi.org/10.48550/arXiv.2411.00622) ![](https://img.shields.io/badge/arXiv-2024.11-red)
- **Agent-RewardBench: Towards a Unified Benchmark for Reward Modeling across Perception, Planning, and Safety in Real-World Multimodal Agents** [[Paper]](https://arxiv.org/abs/2506.21252) ![](https://img.shields.io/badge/ACL-2025-blue)
- **UI-TARS: Pioneering Automated GUI Interaction with Native Agents** [[Paper]](https://doi.org/10.48550/arXiv.2501.12326) ![](https://img.shields.io/badge/arXiv-2025.01-red)
- **Insta: Towards internet-scale training for agents** [[Paper]](https://arxiv.org/abs/2502.06776) ![](https://img.shields.io/badge/arXiv-2025.02-red)
- **APIGen-MT: Agentic Pipeline for Multi-Turn Data Generation via Simulated Agent-Human Interplay** [[Paper]](https://doi.org/10.48550/arXiv.2504.03601) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **FlowReasoner: Reinforcing Query-Level Meta-Agents** [[Paper]](https://arxiv.org/abs/2504.15257) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **ToolACE: Winning the Points of LLM Function Calling** [[Paper]](https://openreview.net/forum?id=8EB8k6DdCU) ![](https://img.shields.io/badge/ICLR-2025-blue)
- **Dreamgen: Unlocking generalization in robot learning through video world models** [[Paper]](https://arxiv.org/abs/2505.12705) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **MaskSearch: A Universal Pre-Training Framework to Enhance Agentic Search Capability** [[Paper]](https://doi.org/10.48550/arXiv.2505.20285) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **WebDancer: Towards Autonomous Information Seeking Agency** [[Paper]](https://doi.org/10.48550/arXiv.2505.22648) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **GUI-Reflection: Empowering Multimodal GUI Models with Self-Reflection Behavior** [[Paper]](https://doi.org/10.48550/arXiv.2506.08012) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **Aguvis: Unified Pure Vision Agents for Autonomous GUI Interaction** [[Paper]](https://proceedings.mlr.press/v267/xu25ae.html) ![](https://img.shields.io/badge/ICML-2025-blue)
- **Explorer: Scaling Exploration-driven Web Trajectory Synthesis for Multimodal Web Agents** [[Paper]](https://aclanthology.org/2025.findings-acl.326/) ![](https://img.shields.io/badge/ACL_Findings-2025-blue)
- **Multi-Turn Code Generation Through Single-Step Rewards** [[Paper]](https://proceedings.mlr.press/v267/jain25a.html) ![](https://img.shields.io/badge/ICML-2025-blue)
- **OS-Genesis: Automating GUI Agent Trajectory Construction via Reverse Task Synthesis** [[Paper]](https://aclanthology.org/2025.acl-long.277/) ![](https://img.shields.io/badge/ACL-2025-blue)
- **WebSailor: Navigating Super-human Reasoning for Web Agent** [[Paper]](https://doi.org/10.48550/arXiv.2507.02592) ![](https://img.shields.io/badge/arXiv-2025.07-red)
- **WebShaper: Agentically Data Synthesizing via Information-Seeking Formalization** [[Paper]](https://doi.org/10.48550/arXiv.2507.15061) ![](https://img.shields.io/badge/arXiv-2025.07-red)
- **WebSynthesis: World-Model-Guided MCTS for Efficient WebUI-Trajectory Synthesis** [[Paper]](https://doi.org/10.48550/arXiv.2507.04370) ![](https://img.shields.io/badge/arXiv-2025.07-red)
- **Advancing Tool-Augmented Large Language Models via Meta-Verification and Reflection Learning** [[Paper]](https://doi.org/10.1145/3711896.3736835) ![](https://img.shields.io/badge/ACM-2025-blue)
- **Cognitive Kernel-Pro: A Framework for Deep Research Agents and Agent Foundation Models Training** [[Paper]](https://doi.org/10.48550/arXiv.2508.00414) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **Think in Games: Learning to Reason in Games via Reinforcement Learning with Large Language Models** [[Paper]](https://doi.org/10.48550/arXiv.2508.21365) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **WebWatcher: Breaking New Frontier of Vision-Language Deep Research Agent** [[Paper]](https://doi.org/10.48550/arXiv.2508.05748) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **DeepDive: Advancing Deep Search Agents with Knowledge Graphs and Multi-Turn RL** [[Paper]](https://doi.org/10.48550/arXiv.2509.10446) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **Scaling Agents via Continual Pre-training** [[Paper]](https://doi.org/10.48550/arXiv.2509.13310) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **Scaling Synthetic Task Generation for Agents via Exploration** [[Paper]](https://doi.org/10.48550/arXiv.2509.25047) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **ToolRM: Outcome Reward Models for Tool-Calling Large Language Models** [[Paper]](https://doi.org/10.48550/arXiv.2509.11963) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **Towards General Agentic Intelligence via Environment Scaling** [[Paper]](https://doi.org/10.48550/arXiv.2509.13311) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **UI-TARS-2 Technical Report: Advancing GUI Agent with Multi-Turn Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2509.02544) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **WebExplorer: Explore and Evolve for Training Long-Horizon Web Agents** [[Paper]](https://doi.org/10.48550/arXiv.2509.06501) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **WebResearcher: Unleashing unbounded reasoning capability in Long-Horizon Agents** [[Paper]](https://doi.org/10.48550/arXiv.2509.13309) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **WebWeaver: Structuring Web-Scale Evidence with Dynamic Outlines for Open-Ended Deep Research** [[Paper]](https://doi.org/10.48550/arXiv.2509.13312) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **AgentFold: Long-Horizon Web Agents with Proactive Context Management** [[Paper]](https://doi.org/10.48550/arXiv.2510.24699) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **AgentFrontier: Expanding the Capability Frontier of LLM Agents with ZPD-Guided Data Synthesis** [[Paper]](https://doi.org/10.48550/arXiv.2510.24695) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **CRMWeaver: Building Powerful Business Agent via Agentic RL and Shared Memories** [[Paper]](https://doi.org/10.48550/arXiv.2510.25333) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **Explore to Evolve: Scaling Evolved Aggregation Logic via Proactive Online Exploration for Deep Research Agents** [[Paper]](https://doi.org/10.48550/arXiv.2510.14438) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **Tongyi DeepResearch Technical Report** [[Paper]](https://doi.org/10.48550/arXiv.2510.24701) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **WebLeaper: Empowering Efficiency and Efficacy in WebAgent via Enabling Info-Rich Seeking** [[Paper]](https://doi.org/10.48550/arXiv.2510.24697) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **Adapting Web Agents with Synthetic Supervision** [[Paper]](https://doi.org/10.48550/arXiv.2511.06101) ![](https://img.shields.io/badge/arXiv-2025.11-red)
- **AgentEvolver: Towards Efficient Self-Evolving Agent System** [[Paper]](https://doi.org/10.48550/arXiv.2511.10395) ![](https://img.shields.io/badge/arXiv-2025.11-red)
- **EvolveSearch: An Iterative Self-Evolving Search Agent** [[Paper]](https://doi.org/10.18653/v1/2025.emnlp-main.663) ![](https://img.shields.io/badge/EMNLP-2025-blue)
- **SimpleDeepSearcher: Deep Information Seeking via Web-Powered Reasoning Trajectory Synthesis** [[Paper]](https://aclanthology.org/2025.findings-emnlp.739/) ![](https://img.shields.io/badge/EMNLP_Findings-2025-blue)
- **Scalable Data Synthesis for Computer Use Agents with Step-Level Filtering** [[Paper]](https://arxiv.org/abs/2512.10962) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **SIMA 2: A Generalist Embodied Agent for Virtual Worlds** [[Paper]](https://doi.org/10.48550/arXiv.2512.04797) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **O-Researcher: An Open Ended Deep Research Model via Multi-Agent Distillation and Agentic RL** [[Paper]](https://doi.org/10.48550/arXiv.2601.03743) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **Scaling Behavior Cloning Improves Causal Reasoning: An Open Model for Real-Time Video Game Playing** [[Paper]](https://doi.org/10.48550/arXiv.2601.04575) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **SERA: Soft-Verified Efficient Repository Agents** [[Paper]](https://doi.org/10.48550/arXiv.2601.20789) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **ToolACE-MCP: Generalizing History-Aware Routing from MCP Tools to the Agent Web** [[Paper]](https://doi.org/10.48550/arXiv.2601.08276) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **MagicAgent: Towards Generalized Agent Planning** [[Paper]](https://arxiv.org/abs/2602.19000) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **Mobile-Agent-v3.5: Multi-platform Fundamental GUI Agents** [[Paper]](https://arxiv.org/abs/2602.16855) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **ProAct: Agentic Lookahead in Interactive Environments** [[Paper]](https://arxiv.org/abs/2602.05327) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **UI-Venus-1.5 Technical Report** [[Paper]](https://arxiv.org/abs/2602.09082) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **HATS: Hardness-Aware Trajectory Synthesis for GUI Agents** [[Paper]](https://arxiv.org/abs/2603.12138) ![](https://img.shields.io/badge/arXiv-2026.03-red)
- **OpenResearcher: A Fully Open Pipeline for Long-Horizon Deep Research Trajectory Synthesis** [[Paper]](https://arxiv.org/abs/2603.20278) ![](https://img.shields.io/badge/arXiv-2026.03-red)
- **OpenSeeker: Democratizing Frontier Search Agents by Fully Open-Sourcing Training Data** [[Paper]](https://arxiv.org/abs/2603.15594) ![](https://img.shields.io/badge/arXiv-2026.03-red)
- **TopoCurate:Modeling Interaction Topology for Tool-Use Agent Training** [[Paper]](https://doi.org/10.48550/arXiv.2603.01714) ![](https://img.shields.io/badge/arXiv-2026.03-red)
- **VSearcher: Long-Horizon Multimodal Search Agent via Reinforcement Learning** [[Paper]](https://arxiv.org/abs/2603.02795) ![](https://img.shields.io/badge/arXiv-2026.03-red)

#### Exploration-Centric Online Evolution

- **Proximal Policy Optimization Algorithms** [[Paper]](http://arxiv.org/abs/1707.06347) ![](https://img.shields.io/badge/arXiv-2017.07-red)
- **Do As I Can, Not As I Say: Grounding Language in Robotic Affordances** [[Paper]](https://proceedings.mlr.press/v205/ichter23a.html) ![](https://img.shields.io/badge/CoRL-2022-blue)
- **DeepSeekMath: Pushing the Limits of Mathematical Reasoning in Open Language Models** [[Paper]](https://doi.org/10.48550/arXiv.2402.03300) ![](https://img.shields.io/badge/arXiv-2024.02-red)
- **DigiRL: Training In-The-Wild Device-Control Agents with Autonomous Reinforcement Learning** [[Paper]](http://papers.nips.cc/paper_files/paper/2024/hash/1704ddd0bb89f159dfe609b32c889995-Abstract-Conference.html) ![](https://img.shields.io/badge/NeurIPS-2024-blue)
- **DeepSWE: Training a Fully Open-sourced, State-of-the-Art Coding Agent by Scaling RL** [[Paper]](https://www.together.ai/blog/deepswe) ![](https://img.shields.io/badge/Together_AI_Blog-2025-blue)
- **DeepRetrieval: Hacking Real Search Engines and Retrievers with Large Language Models via Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2503.00223) ![](https://img.shields.io/badge/arXiv-2025.03-red)
- **R1-Searcher: Incentivizing the Search Capability in LLMs via Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2503.05592) ![](https://img.shields.io/badge/arXiv-2025.03-red)
- **ReSearch: Learning to Reason with Search for LLMs via Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2503.19470) ![](https://img.shields.io/badge/arXiv-2025.03-red)
- **Search-R1: Training LLMs to Reason and Leverage Search Engines with Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2503.09516) ![](https://img.shields.io/badge/arXiv-2025.03-red)
- **DistRL: An Asynchronous Distributed Reinforcement Learning Framework for On-Device Control Agent** [[Paper]](https://openreview.net/forum?id=LPG8pPSfQD) ![](https://img.shields.io/badge/ICLR-2025-blue)
- **GUI-R1 : A Generalist R1-Style Vision-Language Action Model For GUI Agents** [[Paper]](https://doi.org/10.48550/arXiv.2504.10458) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **OTC: Optimal Tool Calls via Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2504.14870) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **RAGEN: Understanding Self-Evolution in LLM Agents via Multi-Turn Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2504.20073) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **ReTool: Reinforcement Learning for Strategic Tool Use in LLMs** [[Paper]](https://doi.org/10.48550/arXiv.2504.11536) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **ToolRL: Reward is All Tool Learning Needs** [[Paper]](https://doi.org/10.48550/arXiv.2504.13958) ![](https://img.shields.io/badge/arXiv-2025.04-red)
- **WebRL: Training LLM Web Agents via Self-Evolving Online Curriculum Reinforcement Learning** [[Paper]](https://openreview.net/forum?id=oVKEAFjEqv) ![](https://img.shields.io/badge/ICLR-2025-blue)
- **Agentic Reasoning and Tool Integration for LLMs via Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2505.01441) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **Group-in-Group Policy Optimization for LLM Agent Training** [[Paper]](https://doi.org/10.48550/arXiv.2505.10978) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **MaskSearch: A Universal Pre-Training Framework to Enhance Agentic Search Capability** [[Paper]](https://doi.org/10.48550/arXiv.2505.20285) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **Nemotron-Research-Tool-N1: Exploring Tool-Using Language Models with Reinforced Reasoning** [[Paper]](https://doi.org/10.48550/arXiv.2505.00024) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **Process vs. Outcome Reward: Which is Better for Agentic RAG Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2505.14069) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **Search and Refine During Think: Autonomous Retrieval-Augmented Reasoning of LLMs** [[Paper]](https://doi.org/10.48550/arXiv.2505.11277) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **VLA-RL: Towards Masterful and General Robotic Manipulation with Scalable Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2505.18719) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **VRAG-RL: Empower Vision-Perception-Based RAG for Visually Rich Information Understanding via Iterative Reasoning with Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2505.22019) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **ZeroGUI: Automating Online GUI Learning at Zero Human Cost** [[Paper]](https://doi.org/10.48550/arXiv.2505.23762) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **ZeroSearch: Incentivize the Search Capability of LLMs without Searching** [[Paper]](https://doi.org/10.48550/arXiv.2505.04588) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **R-Search: Empowering LLM Reasoning with Search via Multi-Reward Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2506.04185) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **SEEA-R1: Tree-Structured Reinforcement Fine-Tuning for Self-Evolving Embodied Agents** [[Paper]](https://doi.org/10.48550/arXiv.2506.21669) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **SPIRAL: Self-Play on Zero-Sum Games Incentivizes Reasoning via Multi-Agent Multi-Turn Reinforcement Learning** [[Paper]](https://arxiv.org/abs/2506.24119) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **Unleashing Embodied Task Planning Ability in LLMs via Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2506.23127) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **Agentic Reinforced Policy Optimization** [[Paper]](https://doi.org/10.48550/arXiv.2507.19849) ![](https://img.shields.io/badge/arXiv-2025.07-red)
- **Mobilegui-rl: Advancing mobile gui agent through reinforcement learning in online environment** [[Paper]](https://arxiv.org/abs/2507.05720) ![](https://img.shields.io/badge/arXiv-2025.07-red)
- **WebSailor: Navigating Super-human Reasoning for Web Agent** [[Paper]](https://doi.org/10.48550/arXiv.2507.02592) ![](https://img.shields.io/badge/arXiv-2025.07-red)
- **Chain-of-Agents: End-to-End Agent Foundation Models via Multi-Agent Distillation and Agentic RL** [[Paper]](https://doi.org/10.48550/arXiv.2508.13167) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **ComputerRL: Scaling End-to-End Online Reinforcement Learning for Computer Use Agents** [[Paper]](https://doi.org/10.48550/arXiv.2508.14040) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **Seeing, Listening, Remembering, and Reasoning: A Multimodal Agent with Long-Term Memory** [[Paper]](https://doi.org/10.48550/arXiv.2508.09736) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **Thinking With Videos: Multimodal Tool-Augmented Reinforcement Learning for Long Video Reasoning** [[Paper]](https://doi.org/10.48550/arXiv.2508.04416) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **Video-MTR: Reinforced Multi-Turn Reasoning for Long Video Understanding** [[Paper]](https://doi.org/10.48550/arXiv.2508.20478) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **AgentGym-RL: Training LLM Agents for Long-Horizon Decision Making through Multi-Turn Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2509.08755) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **Bootstrapping Task Spaces for Self-Improvement** [[Paper]](https://doi.org/10.48550/arXiv.2509.04575) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **Learn the Ropes, Then Trust the Wins: Self-imitation with Progressive Exploration for Agentic Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2509.22601) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **SimpleTIR: End-to-End Reinforcement Learning for Multi-Turn Tool-Integrated Reasoning** [[Paper]](https://doi.org/10.48550/arXiv.2509.02479) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **UI-S1: Advancing GUI Automation via Semi-online Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2509.11543) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **Agentic Entropy-Balanced Policy Optimization** [[Paper]](https://doi.org/10.48550/arXiv.2510.14545) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **AgentRL: Scaling Agentic Reinforcement Learning with a Multi-Turn, Multi-Task Framework** [[Paper]](https://doi.org/10.48550/arXiv.2510.04206) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **GEM: A Gym for Agentic LLMs** [[Paper]](https://doi.org/10.48550/arXiv.2510.01051) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **Stronger-MAS: Multi-Agent Reinforcement Learning for Collaborative LLMs** [[Paper]](https://arxiv.org/abs/2510.11062) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **VAGEN: Reinforcing World Model Reasoning for Multi-Turn VLM Agents** [[Paper]](https://doi.org/10.48550/arXiv.2510.16907) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **Video-Thinker: Sparking "Thinking with Videos" via Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2510.23473) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **Agent-R1: Training Powerful LLM Agents with End-to-End Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2511.14460) ![](https://img.shields.io/badge/arXiv-2025.11-red)
- **EvolveSearch: An Iterative Self-Evolving Search Agent** [[Paper]](https://doi.org/10.18653/v1/2025.emnlp-main.663) ![](https://img.shields.io/badge/EMNLP-2025-blue)
- **Learning Efficient Communication Protocols for Multi-Agent Reinforcement Learning** [[Paper]](https://arxiv.org/abs/2511.09171) ![](https://img.shields.io/badge/arXiv-2025.11-red)
- **RLVE: Scaling Up Reinforcement Learning for Language Models with Adaptive Verifiable Environments** [[Paper]](https://doi.org/10.48550/arXiv.2511.07317) ![](https://img.shields.io/badge/arXiv-2025.11-red)
- **ToolOrchestra: Elevating Intelligence via Efficient Model and Tool Orchestration** [[Paper]](https://arxiv.org/abs/2511.21689) ![](https://img.shields.io/badge/arXiv-2025.11-red)
- **WebAgent-R1: Training Web Agents via End-to-End Multi-Turn Reinforcement Learning** [[Paper]](https://doi.org/10.18653/v1/2025.emnlp-main.401) ![](https://img.shields.io/badge/EMNLP-2025-blue)
- **GTR-Turbo: Merged Checkpoint is Secretly a Free Teacher for Agentic VLM Training** [[Paper]](https://doi.org/10.48550/arXiv.2512.13043) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **VideoMem: Enhancing Ultra-Long Video Understanding via Adaptive Memory Management** [[Paper]](https://doi.org/10.48550/arXiv.2512.04540) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **Exploring Reasoning Reward Model for Agents** [[Paper]](https://doi.org/10.48550/arXiv.2601.22154) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **GDPO: Group reward-Decoupled Normalization Policy Optimization for Multi-reward RL Optimization** [[Paper]](https://doi.org/10.48550/arXiv.2601.05242) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **Imagine-then-Plan: Agent Learning from Adaptive Lookahead with World Models** [[Paper]](https://doi.org/10.48550/arXiv.2601.08955) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **WebArbiter: A Principle-Guided Reasoning Process Reward Model for Web Agents** [[Paper]](https://doi.org/10.48550/arXiv.2601.21872) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **ARLArena: A Unified Framework for Stable Agentic Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2602.21534) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **CM2: Reinforcement Learning with Checklist Rewards for Multi-Turn and Multi-Step Agentic Tool Use** [[Paper]](https://doi.org/10.48550/arXiv.2602.12268) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **FlowSteer: Interactive Agentic Workflow Orchestration via End-to-End Reinforcement Learning** [[Paper]](https://arxiv.org/abs/2602.01664) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **Hierarchy-of-Groups Policy Optimization for Long-Horizon Agentic Tasks** [[Paper]](https://arxiv.org/abs/2602.22817) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **IntentRL: Training Proactive User-intent Agents for Open-ended Deep Research via Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2602.03468) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **SeeUPO: Sequence-Level Agentic-RL with Convergence Guarantees** [[Paper]](https://arxiv.org/abs/2602.06554) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **Who Deserves the Reward? SHARP: Shapley Credit-based Optimization for Multi-Agent System** [[Paper]](https://arxiv.org/abs/2602.08335) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **MetaClaw: Just Talk-An Agent That Meta-Learns and Evolves in the Wild** [[Paper]](https://arxiv.org/abs/2603.17187) ![](https://img.shields.io/badge/arXiv-2026.03-red)

## Environment Evolution

We focus on how training environments are progressively evolved to support the continuous improvement of agent capability. We identify three complementary paradigms: neural-driven evolution, difficulty-driven evolution, and scaling-driven evolution.

| Direction | Representative mechanisms |
| --- | --- |
| Neural-driven evolution | Self-play and learned world models |
| Difficulty-driven evolution | Explicit curriculum signals and implicit curriculum mechanisms |
| Scaling-driven evolution | Scenario-level scaling and environment-level scaling |

<p align="center">
  <img src="assets/figures/environment-evolution.png" alt="Environment evolution" width="90%">
</p>

### Related Papers

#### Neural-Driven Evolution

- **Is Your LLM Secretly a World Model of the Internet? Model-Based Planning for Web Agents** [[Paper]](https://openreview.net/forum?id=c6l7yA0HSq) ![](https://img.shields.io/badge/TMLR-2025-blue)
- **Absolute zero: Reinforced self-play reasoning with zero data** [[Paper]](https://arxiv.org/abs/2505.03335) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **Self-Challenging Language Model Agents** [[Paper]](https://doi.org/10.48550/arXiv.2506.01716) ![](https://img.shields.io/badge/arXiv-2025.06-red)
- **Vision-zero: Scalable vlm self-improvement via strategic gamified self-play** [[Paper]](https://arxiv.org/abs/2509.25541) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **Llms as scalable, general-purpose simulators for evolving digital agent training** [[Paper]](https://arxiv.org/abs/2510.14969) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **WebEvolver: Enhancing Web Agent Self-Improvement with Co-evolving World Model** [[Paper]](https://doi.org/10.18653/v1/2025.emnlp-main.454) ![](https://img.shields.io/badge/EMNLP-2025-blue)
- **Toward Training Superintelligent Software Agents through Self-Play SWE-RL** [[Paper]](https://doi.org/10.48550/arXiv.2512.18552) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **Active Zero: Self-Evolving Vision-Language Models through Active Environment Exploration** [[Paper]](https://doi.org/10.48550/arXiv.2602.11241) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **Code2World: A GUI World Model via Renderable Code Generation** [[Paper]](https://arxiv.org/abs/2602.09856) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **WebWorld: A Large-Scale World Model for Web Agent Training** [[Paper]](https://arxiv.org/abs/2602.14721) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **World-Model-Augmented Web Agents with Action Correction** [[Paper]](https://arxiv.org/abs/2602.15384) ![](https://img.shields.io/badge/arXiv-2026.02-red)

#### Difficulty-Driven Evolution

- **Paired Open-Ended Trailblazer (POET): Endlessly Generating Increasingly Complex and Diverse Learning Environments and Their Solutions** [[Paper]](http://arxiv.org/abs/1901.01753) ![](https://img.shields.io/badge/arXiv-2019.01-red)
- **Emergent Complexity and Zero-shot Transfer via Unsupervised Environment Design** [[Paper]](https://arxiv.org/abs/2012.02096) ![](https://img.shields.io/badge/arXiv-2020.12-red)
- **Replay-Guided Adversarial Environment Design** [[Paper]](https://proceedings.neurips.cc/paper/2021/hash/0e915db6326b6fb6a3c56546980a8c93-Abstract.html) ![](https://img.shields.io/badge/NeurIPS-2021-blue)
- **Evolving Curricula with Regret-Based Environment Design** [[Paper]](https://proceedings.mlr.press/v162/parker-holder22a.html) ![](https://img.shields.io/badge/ICML-2022-blue)
- **MAESTRO: Open-Ended Environment Design for Multi-Agent Reinforcement Learning** [[Paper]](https://openreview.net/forum?id=sKWlRDzPfd7) ![](https://img.shields.io/badge/ICLR-2023-blue)
- **EnvGen: Generating and Adapting Environments via LLMs for Training Embodied Agents** [[Paper]](https://doi.org/10.48550/arXiv.2403.12014) ![](https://img.shields.io/badge/arXiv-2024.03-red)
- **Refining Minimax Regret for Unsupervised Environment Design** [[Paper]](https://proceedings.mlr.press/v235/beukman24a.html) ![](https://img.shields.io/badge/ICML-2024-blue)
- **AgentGen: Enhancing Planning Abilities for Large Language Model based Agent via Environment and Task Generation** [[Paper]](https://doi.org/10.48550/arXiv.2408.00764) ![](https://img.shields.io/badge/arXiv-2024.08-red)
- **Eurekaverse: Environment curriculum generation via large language models** [[Paper]](https://arxiv.org/abs/2411.01775) ![](https://img.shields.io/badge/arXiv-2024.11-red)
- **DataEnvGym: Data Generation Agents in Teacher Environments with Student Feedback** [[Paper]](https://openreview.net/forum?id=00SnKBGTsz) ![](https://img.shields.io/badge/ICLR-2025-blue)
- **Self-Evolving Curriculum for LLM Reasoning** [[Paper]](https://doi.org/10.48550/arXiv.2505.14970) ![](https://img.shields.io/badge/arXiv-2025.05-red)
- **Reasoning Core: A Scalable RL Environment for LLM Symbolic Reasoning** [[Paper]](https://doi.org/10.48550/arXiv.2509.18083) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **Don't Just Fine-tune the Agent, Tune the Environment** [[Paper]](https://doi.org/10.48550/arXiv.2510.10197) ![](https://img.shields.io/badge/arXiv-2025.10-red)
- **RLVE: Scaling Up Reinforcement Learning for Language Models with Adaptive Verifiable Environments** [[Paper]](https://doi.org/10.48550/arXiv.2511.07317) ![](https://img.shields.io/badge/arXiv-2025.11-red)
- **Scaling Agent Learning via Experience Synthesis** [[Paper]](https://doi.org/10.48550/arXiv.2511.03773) ![](https://img.shields.io/badge/arXiv-2025.11-red)
- **CuES: A Curiosity-driven and Environment-grounded Synthesis Framework for Agentic RL** [[Paper]](https://doi.org/10.48550/arXiv.2512.01311) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **GenEnv: Difficulty-Aligned Co-Evolution Between LLM Agents and Environment Simulators** [[Paper]](https://doi.org/10.48550/arXiv.2512.19682) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **SCALER:Synthetic Scalable Adaptive Learning Environment for Reasoning** [[Paper]](https://doi.org/10.48550/arXiv.2601.04809) ![](https://img.shields.io/badge/arXiv-2026.01-red)

#### Scaling-Driven Evolution

- **Feedback-Driven Tool-Use Improvements in Large Language Models via Automated Build Environments** [[Paper]](https://doi.org/10.48550/arXiv.2508.08791) ![](https://img.shields.io/badge/arXiv-2025.08-red)
- **ARE: Scaling Up Agent Environments and Evaluations** [[Paper]](https://doi.org/10.48550/arXiv.2509.17158) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **Towards General Agentic Intelligence via Environment Scaling** [[Paper]](https://doi.org/10.48550/arXiv.2509.13311) ![](https://img.shields.io/badge/arXiv-2025.09-red)
- **AutoEnv: Automated Environments for Measuring Cross-Environment Agent Learning** [[Paper]](https://doi.org/10.48550/arXiv.2511.19304) ![](https://img.shields.io/badge/arXiv-2025.11-red)
- **AutoForge: Automated Environment Synthesis for Agentic Reinforcement Learning** [[Paper]](https://doi.org/10.48550/arXiv.2512.22857) ![](https://img.shields.io/badge/arXiv-2025.12-red)
- **EnvScaler: Scaling Tool-Interactive Environments for LLM Agent via Programmatic Synthesis** [[Paper]](https://doi.org/10.48550/arXiv.2601.05808) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **InfiniteWeb: Scalable Web Environment Synthesis for GUI Agent Training** [[Paper]](https://doi.org/10.48550/arXiv.2601.04126) ![](https://img.shields.io/badge/arXiv-2026.01-red)
- **Agent world model: Infinity synthetic environments for agentic reinforcement learning** [[Paper]](https://arxiv.org/abs/2602.10090) ![](https://img.shields.io/badge/arXiv-2026.02-red)
- **AutoWebWorld: Synthesizing Infinite Verifiable Web Environments via Finite State Machines** [[Paper]](https://arxiv.org/abs/2602.14296) ![](https://img.shields.io/badge/arXiv-2026.02-red)

## Challenges & Future Directions

We highlight future directions for environment engineering, including standardized environment deployment, richer environment properties, multi-agent interaction, neural-symbolic integration, sim-to-real alignment, agent-environment co-evolution, unified offline-online learning, and a more systematic science of environment engineering.

| Direction | Open questions |
| --- | --- |
| Environment-as-a-Service | How should environments be deployed, versioned, and standardized? |
| Evolving environment properties | How should environments support dynamic, long-horizon, open-ended, and multimodal interaction? |
| Multi-agent environments | How should environments model cooperation, competition, roles, and emergent behavior? |
| Neural-symbolic environments | How can symbolic reliability and neural scalability be combined? |
| Sim-to-real alignment | How can synthetic dynamics transfer to real-world agent behavior? |
| Agent-environment co-evolution | How should agents and environments adapt to each other over time? |
| Unified offline-online learning | How should offline trajectories and online feedback be combined? |
| Science of environment engineering | What environment properties shape specific agent capabilities? |

### Related Papers

#### Offline-Online Learning and Co-Evolution

- **On-Policy Distillation** [[Paper]](https://doi.org/10.64434/tml.20251026) ![](https://img.shields.io/badge/Thinking_Machines_Lab-2025-blue)

## Citation

If you find this survey helpful, please cite our survey:

```bibtex
@article{li2026agenticenvironmentengineering,
  title={Agentic Environment Engineering for Large Language Models: A Survey of Environment Modeling, Synthesis, Evaluation, and Application},
  author={Li, Jiachun and Jin, Zhuoran and Men, Tianyi and Hao, Yupu and Zhu, Kejian and Wang, Lingshuai and Huang, Dongqi and Wang, Longxiang and Hua, Shengjia and Wang, Lu and Gao, Jinshan and Yuan, Hongbang and Xu, Ruilin and Liu, Kang and Zhao, Jun},
  journal={arXiv preprint arXiv:2606.12191},
  year={2026},
  eprint={2606.12191},
  archivePrefix={arXiv},
  primaryClass={cs.CL},
  url={https://arxiv.org/abs/2606.12191}
}
```

## Contact

For any questions or feedback, please reach out to us at jiachun.li@nlpr.ia.ac.cn, zhuoran.jin@nlpr.ia.ac.cn or tianyi.men@nlpr.ia.ac.cn.
