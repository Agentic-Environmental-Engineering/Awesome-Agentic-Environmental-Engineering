# Agentic Environment Engineering for Large Language Models

<p align="center">
  <b>A survey of environment modeling, synthesis, evaluation, application, and agent-environment co-evolution.</b>
</p>

<p align="center">
  <a href="#introduction"><img alt="Survey" src="https://img.shields.io/badge/Survey-Agentic%20Environment%20Engineering-2F855A"></a>
  <a href="#taxonomy-at-a-glance"><img alt="Taxonomy" src="https://img.shields.io/badge/Taxonomy-Attributes%20%2B%20Domains-2B6CB0"></a>
  <a href="#references"><img alt="References" src="https://img.shields.io/badge/References-582%20Cited%20Works-805AD5"></a>
  <a href="#citation"><img alt="Citation" src="https://img.shields.io/badge/Citation-Cite%20Our%20Survey-D69E2E"></a>
</p>

<p align="center">
  <a href="#news">News</a> |
  <a href="#introduction">Introduction</a> |
  <a href="#table-of-content">Table of Content</a> |
  <a href="#taxonomy-at-a-glance">Taxonomy</a> |
  <a href="#environment-domains">Domains</a> |
  <a href="#environment-synthesis-and-evaluation">Synthesis</a> |
  <a href="#agent-environment-co-evolution">Co-Evolution</a> |
  <a href="#citation">Citation</a> |
  <a href="#contact">Contact</a> |
  <a href="#references">References</a>
</p>

<p align="center">
  <img src="assets/figures/overview.png" alt="Overview of agentic environment engineering" width="96%">
</p>

## News

- 2026-06-05: Initial preview repository created with paper figures, README taxonomy, citation, contact information, and the full cited reference list.

## Introduction

This repository accompanies the survey **Agentic Environment Engineering for Large Language Models**. The survey studies agentic environments as interactive systems for LLM-based agents and organizes the field from the perspective of the environment engineering lifecycle: environment modeling, automated environment synthesis, environment evaluation, and environment applications.

The paper focuses on three research questions: what characteristics and categories define agentic environments, how agentic environments can be constructed and evaluated, and how environments support the closed-loop co-evolution of agents and environments. It reviews environments through eight attributes and eight task domains, then discusses symbolic and neural synthesis, quality evaluation, agent evolution, environment evolution, and future directions.

> Paper status: the public PDF link will be added after the camera-ready PDF or arXiv version is available.

In the paper, agentic environments are defined as dynamic, interactive systems designed for evaluating and training LLM agents. Such environments provide permissible actions, observations, and rewards, enabling iterative interaction between models and environments. The survey also compares traditional data engineering with environment engineering, emphasizing the shift from static corpora and single-turn question answering toward dynamic feedback, multi-turn interaction, and closed-loop control.

| Perspective | Traditional data engineering | Environment engineering |
| --- | --- | --- |
| Learning source | Static corpus or pre-collected trajectories | Dynamic interaction with an environment |
| Interaction pattern | Single-turn question answering | Multi-turn interaction with tools, executors, retrievers, or agents |
| Feedback loop | Open-loop learning against fixed answers | Closed-loop feedback from state changes and rewards |
| Adaptation | Fixed data difficulty | Task complexity can be adjusted with agent capability |

<p align="center">
  <img src="assets/figures/preliminaries.png" alt="From data engineering to environment engineering" width="82%">
</p>

## Table of Content

- [News](#news)
- [Introduction](#introduction)
- [Table of Content](#table-of-content)
- [Taxonomy at a Glance](#taxonomy-at-a-glance)
- [Environment Domains](#environment-domains)
- [Environment Synthesis and Evaluation](#environment-synthesis-and-evaluation)
- [Agent-Environment Co-Evolution](#agent-environment-co-evolution)
- [Citation](#citation)
- [Contact](#contact)
- [References](#references)

## Taxonomy at a Glance

The survey characterizes agentic environments through eight attributes: representation, feedback, timing, observability, stochasticity, continuity, modality, and cardinality. These attributes correspond to symbolic or neural environments, open-loop or closed-loop environments, online or offline environments, MDP or POMDP settings, deterministic or nondeterministic dynamics, discrete or continuous spaces, unimodal or multimodal interfaces, and single-agent or multi-agent environments.

| View | Core question | Categories used in the survey |
| --- | --- | --- |
| Environment attributes | What properties define an environment? | symbolic/neural, open/closed loop, online/offline, MDP/POMDP, deterministic/nondeterministic, discrete/continuous, unimodal/multimodal, single/multi-agent |
| Environment domains | What task worlds do agents operate in? | GUI, Deep Research, Embodied, Game, Tool, Code, Domain-Specific, Cross-Domain |
| Environment lifecycle | How are environments built and used? | modeling, synthesis, evaluation, agent evolution, environment evolution |

<p align="center">
  <img src="assets/figures/environment-attributes.png" alt="Environment attributes" width="86%">
</p>

## Environment Domains

The survey groups representative agentic environments into eight domains: GUI, Deep Research, Embodied, Game, Tool, Code, Domain-Specific, and Cross-Domain. These domains are used to describe the development paths of current benchmarks and environments as well as the core capabilities they evaluate or support.

<p align="center">
  <img src="assets/figures/environment-domains.png" alt="Environment domains" width="96%">
</p>

| Domain | Representative focus in the survey |
| --- | --- |
| GUI | Desktop, mobile, and web GUI environments |
| Deep Research | Browsing, information seeking, long-form research, and report-generation environments |
| Embodied | Household, robotics, navigation, science, and virtual embodied environments |
| Game | Open-world, puzzle reasoning, social deduction, adventure quest, and strategy management games |
| Tool | Conventional tool use, user-simulated tool use, and MCP-based tool use |
| Code | Code generation, understanding, verification, debugging, and repository-level tasks |
| Domain-Specific | Environments for specialized fields such as medicine, science, finance, law, business, and biology |
| Cross-Domain | General-purpose environments and benchmarks spanning multiple task worlds |

## Environment Synthesis and Evaluation

The survey divides automated environment synthesis into symbolic synthesis and neural synthesis. Symbolic synthesis uses explicit structures such as code, rules, simulators, tools, or verifiers to construct environments and provide reliable feedback. Neural synthesis parameterizes environment dynamics with neural models, especially world models, and is discussed through pixel-level, word-level, and latent-level modeling.

For environment evaluation, the paper discusses quality control through four dimensions: correctness, diversity, complexity, and fidelity. Correctness is often supported by execution, verifiers, constraints, or task completion signals, while diversity, complexity, and fidelity measure whether synthesized environments are varied, challenging, and faithful to target systems or real-world dynamics.

| Direction | Scope in the survey | Quality dimensions |
| --- | --- | --- |
| Symbolic synthesis | Rule-, code-, simulator-, tool-, and verifier-based environment construction | correctness, diversity, complexity, fidelity |
| Neural synthesis | Pixel-level, word-level, and latent-level world modeling | correctness, diversity, complexity, fidelity |
| Quality evaluation | Environment reliability and usefulness for agent learning or evaluation | correctness, diversity, complexity, fidelity |

<p align="center">
  <img src="assets/figures/symbolic-synthesis.png" alt="Symbolic environment synthesis" width="88%">
</p>

<p align="center">
  <img src="assets/figures/neural-world-model.png" alt="Neural environment synthesis and world models" width="88%">
</p>

## Agent-Environment Co-Evolution

The survey treats environments not only as benchmarks, but also as mechanisms that support agent evolution and can themselves evolve. Agent evolution is discussed through memory-centric experience evolution, orchestration-centric workflow evolution, trajectory-centric offline evolution, and exploration-centric online evolution. Environment evolution is discussed through neural-driven, difficulty-driven, and scaling-driven approaches.

| Track | Categories used in the survey |
| --- | --- |
| Agent evolution | memory-centric experience evolution, orchestration-centric workflow evolution, trajectory-centric offline evolution, exploration-centric online evolution |
| Environment evolution | neural-driven evolution, difficulty-driven evolution, scaling-driven evolution |
| Future directions | Environment-as-a-Service, Multi-agent Environments, Neural-Symbolic Environments, sim-to-real alignment, and agent-environment co-evolution |

<p align="center">
  <img src="assets/figures/agent-evolution.png" alt="Agent evolution in environments" width="90%">
</p>

<p align="center">
  <img src="assets/figures/environment-evolution.png" alt="Environment evolution" width="90%">
</p>

## Citation

If you find this survey helpful, please cite our survey:

```bibtex
@article{li2026agenticenvironmentengineering,
  title={Agentic Environment Engineering for Large Language Models},
  author={Li, Jiachun and Jin, Zhuoran and Men, Tianyi and Hao, Yupu and Zhu, Kejian and Wang, Lingshuai and Huang, Dongqi and Wang, Longxiang and Hua, Shengjia and Wang, Lu and Gao, Jinshan and Yuan, Hongbang and Xu, Ruilin and Liu, Kang and Zhao, Jun},
  year={2026},
  note={Version v1, major update on May 19, 2026}
}
```

## Contact

For any questions or feedback, please reach out to us at jiachun.li@nlpr.ia.ac.cn, zhuoran.jin@nlpr.ia.ac.cn or tianyi.men@nlpr.ia.ac.cn

## References

1. **Qwen3 Technical Report**, *Qwen Team et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.09388)
2. **DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning**, *DeepSeek-AI et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2501.12948)
3. **GEM: A Gym for Agentic LLMs**, *Liu et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.01051)
4. **Humanity's Last Code Exam: Can Advanced LLMs Conquer Human's Hardest Code Competition?**, *Li et al.*, Findings of EMNLP 2025. [Paper](https://aclanthology.org/2025.findings-emnlp.1152/)
5. **Introducing GPT-5.4**, *OpenAI et al.*, OpenAI 2025. [Paper](https://openai.com/index/introducing-gpt-5-4/)
6. **Gemini 3.1 Pro**, *Google DeepMind et al.*, Google DeepMind 2025. [Paper](https://deepmind.google/models/gemini/pro/)
7. **Kimi K2.5: Visual Agentic Intelligence**, *Kimi Team et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2602.02276)
8. **ToolRL: Reward is All Tool Learning Needs**, *Qian et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2504.13958)
9. **TravelPlanner: A Benchmark for Real-World Planning with Language Agents**, *Xie et al.*, ICML 2024. [Paper](https://proceedings.mlr.press/v235/xie24j.html)
10. **Self-Refine: Iterative Refinement with Self-Feedback**, *Madaan et al.*, NeurIPS 2023. [Paper](http://papers.nips.cc/paper_files/paper/2023/hash/91edff07232fb1b55a505a9e9f6c0ff3-Abstract-Conference.html)
11. **Agent world model: Infinity synthetic environments for agentic reinforcement learning**, *Wang et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.10090)
12. **RWKU: Benchmarking Real-World Knowledge Unlearning for Large Language Models**, *Jin et al.*, NeurIPS 2024. [Paper](https://arxiv.org/abs/2406.10890)
13. **A Troublemaker with Contagious Jailbreak Makes Chaos in Honest Towns**, *Men et al.*, ACL 2025. [Paper](https://aclanthology.org/2025.acl-long.859/)
14. **DAComp: Benchmarking Data Agents across the Full Data Intelligence Lifecycle**, *Lei et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2512.04324)
15. **WebShop: Towards Scalable Real-World Web Interaction with Grounded Language Agents**, *Yao et al.*, NeurIPS 2022. [Paper](http://papers.nips.cc/paper_files/paper/2022/hash/82ad13ec01f9fe44c01cb91814fd7b8c-Abstract-Conference.html)
16. **SWE-bench: Can Language Models Resolve Real-world Github Issues?**, *Jimenez et al.*, ICLR 2024. [Paper](https://openreview.net/forum?id=VTF8yNQM66)
17. **ReAct: Synergizing Reasoning and Acting in Language Models**, *Yao et al.*, ICLR 2023. [Paper](https://openreview.net/forum?id=WE_vluYUL-X)
18. **Fixing the Broken Compass: Diagnosing and Improving Inference-Time Reward Modeling**, *Li et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2503.05188)
19. **Omni-Reward: Towards Generalist Omni-Modal Reward Modeling with Free-Form Preferences**, *Jin et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2510.23451)
20. **DeepSeekMath: Pushing the Limits of Mathematical Reasoning in Open Language Models**, *Shao et al.*, arXiv 2024. [Paper](https://doi.org/10.48550/arXiv.2402.03300)
21. **DAPO: An Open-Source LLM Reinforcement Learning System at Scale**, *Yu et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2503.14476)
22. **Reinforced internal-external knowledge synergistic reasoning for efficient adaptive search agent**, *Huang et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2505.07596)
23. **Towards agentic self-learning llms in search environment**, *Sun et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2510.14253)
24. **Agentic Reasoning for Large Language Models**, *Wei et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.12538)
25. **Large language models for planning: A comprehensive and systematic survey**, *Cao et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2505.19683)
26. **A Survey of Recent Advances in Commonsense Knowledge Acquisition: Methods and Resources**, *Wang et al.*, Machine Intelligence Research 2025. [Paper](https://doi.org/10.1007/s11633-023-1471-3)
27. **WorkArena: How Capable are Web Agents at Solving Common Knowledge Work Tasks?**, *Drouin et al.*, ICML 2024. [Paper](https://proceedings.mlr.press/v235/drouin24a.html)
28. **OSWorld: Benchmarking Multimodal Agents for Open-Ended Tasks in Real Computer Environments**, *Xie et al.*, NeurIPS 2024. [Paper](http://papers.nips.cc/paper_files/paper/2024/hash/5d413e48f84dc61244b6be550f1cd8f5-Abstract-Datasets_and_Benchmarks_Track.html)
29. **Measuring short-form factuality in large language models**, *Wei et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2411.04368)
30. **GAIA: a benchmark for General AI Assistants**, *Mialon et al.*, ICLR 2024. [Paper](https://openreview.net/forum?id=fibxvahvs3)
31. **BrowseComp: A Simple Yet Challenging Benchmark for Browsing Agents**, *Wei et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2504.12516)
32. **ALFRED: A Benchmark for Interpreting Grounded Instructions for Everyday Tasks**, *Shridhar et al.*, CVPR 2020. [Paper](https://openaccess.thecvf.com/content_CVPR_2020/html/Shridhar_ALFRED_A_Benchmark_for_Interpreting_Grounded_Instructions_for_Everyday_Tasks_CVPR_2020_paper.html)
33. **ALFWorld: Aligning Text and Embodied Environments for Interactive Learning**, *Shridhar et al.*, ICLR 2021. [Paper](https://openreview.net/forum?id=0IOX0YcCdTn)
34. **ScienceWorld: Is your Agent Smarter than a 5th Grader?**, *Wang et al.*, EMNLP 2022. [Paper](https://doi.org/10.18653/v1/2022.emnlp-main.775)
35. **GameArena: Evaluating LLM Reasoning through Live Computer Games**, *Hu et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2412.06394)
36. **Baba Is AI: Break the Rules to Beat the Benchmark**, *Cloos et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2407.13729)
37. **GameBench: Evaluating Strategic Reasoning Abilities of LLM Agents**, *Costarelli et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2406.06613)
38. **ToolLLM: Facilitating Large Language Models to Master 16000+ Real-world APIs**, *Qin et al.*, ICLR 2024. [Paper](https://openreview.net/forum?id=dHng2O0Jjr)
39. **tau-bench: A Benchmark for Tool-Agent-User Interaction in Real-World Domains**, *Yao et al.*, arXiv 2024. [Paper](https://doi.org/10.48550/arXiv.2406.12045)
40. **API-Bank: A Comprehensive Benchmark for Tool-Augmented LLMs**, *Li et al.*, EMNLP 2023. [Paper](https://doi.org/10.18653/v1/2023.emnlp-main.187)
41. **Program synthesis with large language models**, *Austin et al.*, arXiv 2021. [Paper](https://arxiv.org/abs/2108.07732)
42. **Terminal-Bench: Benchmarking Agents on Hard, Realistic Tasks in Command Line Interfaces**, *Merrill et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.11868)
43. **Kernelbench: Can llms write efficient gpu kernels?**, *Ouyang et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2502.10517)
44. **MedAgentBench: Dataset for Benchmarking LLMs as Agents in Medical Applications**, *Jiang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2501.14654)
45. **ScienceAgentBench: Toward Rigorous Assessment of Language Agents for Data-Driven Scientific Discovery**, *Chen et al.*, ICLR 2025. [Paper](https://openreview.net/forum?id=6z4YKr0GK6)
46. **DSBench: How Far Are Data Science Agents from Becoming Data Science Experts?**, *Jing et al.*, ICLR 2025. [Paper](https://openreview.net/forum?id=DSsSPr0RZJ)
47. **Openai gym**, *Brockman et al.*, arXiv 2016. [Paper](https://arxiv.org/abs/1606.01540)
48. **AgentBench: Evaluating LLMs as Agents**, *Liu et al.*, ICLR 2024. [Paper](https://openreview.net/forum?id=zAdUB0aCTQ)
49. **AgentsCourt: Building Judicial Decision-Making Agents with Court Debate Simulation and Legal Knowledge Augmentation**, *He et al.*, Findings of EMNLP 2024. [Paper](https://arxiv.org/abs/2403.02959)
50. **MMR-V: What's Left Unsaid? A Benchmark for Multimodal Deep Reasoning in Videos**, *Zhu et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2506.04141)
51. **MMR-Life: Piecing Together Real-life Scenes for Multimodal Multi-image Reasoning**, *Li et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2603.02024)
52. **MLE-bench: Evaluating Machine Learning Agents on Machine Learning Engineering**, *Chan et al.*, ICLR 2025. [Paper](https://openreview.net/forum?id=6s5uXNWGIh)
53. **ToolACE: Winning the Points of LLM Function Calling**, *Liu et al.*, ICLR 2025. [Paper](https://openreview.net/forum?id=8EB8k6DdCU)
54. **Toolformer: Language Models Can Teach Themselves to Use Tools**, *Schick et al.*, NeurIPS 2023. [Paper](http://papers.nips.cc/paper_files/paper/2023/hash/d842425e4bf79ba039352da0f658a906-Abstract-Conference.html)
55. **Livecodebench: Holistic and contamination free evaluation of large language models for code**, *Jain et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2403.07974)
56. **WebArena: A Realistic Web Environment for Building Autonomous Agents**, *Zhou et al.*, ICLR 2024. [Paper](https://openreview.net/forum?id=oKn9c6ytLx)
57. **WebVoyager: Building an End-to-End Web Agent with Large Multimodal Models**, *He et al.*, ACL 2024. [Paper](https://doi.org/10.18653/v1/2024.acl-long.371)
58. **LLMArena: Assessing Capabilities of Large Language Models in Dynamic Multi-Agent Environments**, *Chen et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2402.16499)
59. **Large language models can self-improve at web agent tasks**, *Patel et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2405.20309)
60. **Group-in-Group Policy Optimization for LLM Agent Training**, *Feng et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.10978)
61. **Agentic Reinforced Policy Optimization**, *Dong et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2507.19849)
62. **Search-R1: Training LLMs to Reason and Leverage Search Engines with Reinforcement Learning**, *Jin et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2503.09516)
63. **Proximal Policy Optimization Algorithms**, *Schulman et al.*, arXiv 2017. [Paper](http://arxiv.org/abs/1707.06347)
64. **AgentGen: Enhancing Planning Abilities for Large Language Model based Agent via Environment and Task Generation**, *Hu et al.*, arXiv 2024. [Paper](https://doi.org/10.48550/arXiv.2408.00764)
65. **Scaling Agent Learning via Experience Synthesis**, *Chen et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2511.03773)
66. **SCALER:Synthetic Scalable Adaptive Learning Environment for Reasoning**, *Xu et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.04809)
67. **Training Verifiers to Solve Math Word Problems**, *Cobbe et al.*, arXiv 2021. [Paper](https://arxiv.org/abs/2110.14168)
68. **Measuring Massive Multitask Language Understanding**, *Hendrycks et al.*, ICLR 2021. [Paper](https://openreview.net/forum?id=d7KBjmI3GmQ)
69. **MMMU: A Massive Multi-discipline Multimodal Understanding and Reasoning Benchmark for Expert AGI**, *Yue et al.*, arXiv 2023. [Paper](https://doi.org/10.48550/arXiv.2311.16502)
70. **RAG-RewardBench: Benchmarking Reward Models in Retrieval Augmented Generation for Preference Alignment**, *Jin et al.*, Findings of ACL 2025. [Paper](https://arxiv.org/abs/2412.13746)
71. **IDE-Bench: Evaluating Large Language Models as IDE Agents on Real-World Software Engineering Tasks**, *Mateega et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2601.20886)
72. **WideSearch: Benchmarking Agentic Broad Info-Seeking**, *Wong et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.07999)
73. **RoboFactory: Exploring Embodied Agent Collaboration with Compositional Constraints**, *Qin et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2503.16408)
74. **Unlocking the Future: Exploring Look-Ahead Planning Mechanistic Interpretability in Large Language Models**, *Men et al.*, EMNLP 2024. [Paper](https://aclanthology.org/2024.emnlp-main.440/)
75. **MCPVerse: An Expansive, Real-World Benchmark for Agentic Tool Use**, *Lei et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.16260)
76. **AutoFlow: Automated Workflow Generation for Large Language Model Agents**, *Li et al.*, arXiv 2024. [Paper](https://doi.org/10.48550/arXiv.2407.12821)
77. **Learning on the Job: An Experience-Driven Self-Evolving Agent for Long-Horizon Tasks**, *Yang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.08002)
78. **In-the-Flow Agentic System Optimization for Effective Planning and Tool Use**, *Li et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.05592)
79. **Adaptation of agentic ai**, *Jiang et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2512.16301)
80. **A Comprehensive Survey on Reinforcement Learning-based Agentic Search: Foundations, Roles, Optimizations, Evaluations, and Applications**, *Lin et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.16724)
81. **A Comprehensive Survey of Self-Evolving AI Agents: A New Paradigm Bridging Foundation Models and Lifelong Agentic Systems**, *Fang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.07407)
82. **The Landscape of Agentic Reinforcement Learning for LLMs: A Survey**, *Zhang et al.*, Trans. Mach. Learn. Res 2026. [Paper](https://openreview.net/forum?id=RY19y2RI1O)
83. **Toward Efficient Agents: Memory, Tool learning, and Planning**, *Yang et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2601.14192)
84. **A Survey of Self-Evolving Agents: What, When, How, and Where to Evolve on the Path to Artificial Super Intelligence**, *Gao et al.*, Trans. Mach. Learn. Res 2026. [Paper](https://openreview.net/forum?id=CTr3bovS5F)
85. **EnvScaler: Scaling Tool-Interactive Environments for LLM Agent via Programmatic Synthesis**, *Song et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.05808)
86. **AutoEnv: Automated Environments for Measuring Cross-Environment Agent Learning**, *Zhang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2511.19304)
87. **Is Your LLM Secretly a World Model of the Internet? Model-Based Planning for Web Agents**, *Gu et al.*, Trans. Mach. Learn. Res 2025. [Paper](https://openreview.net/forum?id=c6l7yA0HSq)
88. **Dreamgen: Unlocking generalization in robot learning through video world models**, *Jang et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2505.12705)
89. **WebEvolver: Enhancing Web Agent Self-Improvement with Co-evolving World Model**, *Fang et al.*, EMNLP 2025. [Paper](https://doi.org/10.18653/v1/2025.emnlp-main.454)
90. **TaskLAMA: Probing the Complex Task Understanding of Language Models**, *Yuan et al.*, AAAI 2024. [Paper](https://doi.org/10.1609/aaai.v38i17.29918)
91. **HuggingGPT: Solving AI Tasks with ChatGPT and its Friends in Hugging Face**, *Shen et al.*, NeurIPS 2023. [Paper](http://papers.nips.cc/paper_files/paper/2023/hash/77c33e6a367922d003ff102ffb92b658-Abstract-Conference.html)
92. **TaskBench: Benchmarking Large Language Models for Task Automation**, *Shen et al.*, NeurIPS 2024. [Paper](http://papers.nips.cc/paper_files/paper/2024/hash/085185ea97db31ae6dcac7497616fd3e-Abstract-Datasets_and_Benchmarks_Track.html)
93. **Mobile-Bench: An Evaluation Benchmark for LLM-based Mobile Agents**, *Deng et al.*, ACL 2024. [Paper](https://aclanthology.org/2024.acl-long.478/)
94. **WebWalker: Benchmarking LLMs in Web Traversal**, *Wu et al.*, ACL 2025. [Paper](https://aclanthology.org/2025.acl-long.508/)
95. **EmbodiedBench: Comprehensive Benchmarking Multi-modal Large Language Models for Vision-Driven Embodied Agents**, *Yang et al.*, ICML 2025. [Paper](https://proceedings.mlr.press/v267/yang25f.html)
96. **Mind2Web: Towards a Generalist Agent for the Web**, *Deng et al.*, NeurIPS 2023. [Paper](http://papers.nips.cc/paper_files/paper/2023/hash/5950bf290a1570ea401bf98882128160-Abstract-Datasets_and_Benchmarks.html)
97. **On the Effects of Data Scale on UI Control Agents**, *Li et al.*, NeurIPS 2024. [Paper](http://papers.nips.cc/paper_files/paper/2024/hash/a79f3ef3b445fd4659f44648f7ea8ffd-Abstract-Datasets_and_Benchmarks_Track.html)
98. **KOR-Bench: Benchmarking Language Models on Knowledge-Orthogonal Reasoning Tasks**, *Ma et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2410.06526)
99. **GVGAI-LLM: Evaluating Large Language Model Agents with Infinite Games**, *Li et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2508.08501)
100. **V-GameGym: Visual Game Generation for Code Large Language Models**, *Zhang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.20136)
101. **GameTraversalBenchmark: Evaluating Planning Abilities Of Large Language Models Through Traversing 2D Game Maps**, *Nasir et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2410.07765)
102. **Vsp: Assessing the dual challenges of perception and reasoning in spatial planning tasks for vlms**, *Wu et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2407.01863)
103. **AppWorld: A Controllable World of Apps and People for Benchmarking Interactive Coding Agents**, *Trivedi et al.*, ACL 2024. [Paper](https://doi.org/10.18653/v1/2024.acl-long.850)
104. **Scenario Dreamer: Vectorized Latent Diffusion for Generating Driving Simulation Environments**, *Rowe et al.*, CVPR 2025. [Paper](https://openaccess.thecvf.com/content/CVPR2025/html/Rowe_Scenario_Dreamer_Vectorized_Latent_Diffusion_for_Generating_Driving_Simulation_Environments_CVPR_2025_paper.html)
105. **MetaDrive: Composing Diverse Driving Scenarios for Generalizable Reinforcement Learning**, *Li et al.*, IEEE Trans. Pattern Anal. Mach. Intell 2023. [Paper](https://doi.org/10.1109/TPAMI.2022.3190471)
106. **OSWorld-MCP: Benchmarking MCP Tool Invocation In Computer-Use Agents**, *Jia et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.24563)
107. **VisualWebArena: Evaluating Multimodal Agents on Realistic Visual Web Tasks**, *Koh et al.*, ACL 2024. [Paper](https://doi.org/10.18653/v1/2024.acl-long.50)
108. **AgentStudio: A Toolkit for Building General Virtual Agents**, *Zheng et al.*, ICLR 2025. [Paper](https://openreview.net/forum?id=axUf8BOjnH)
109. **Generative Agents: Interactive Simulacra of Human Behavior**, *Park et al.*, UIST 2023. [Paper](https://arxiv.org/abs/2304.03442)
110. **Collab-Overcooked: Benchmarking and Evaluating Large Language Models as Collaborative Agents**, *Sun et al.*, EMNLP 2025. [Paper](https://aclanthology.org/2025.emnlp-main.249/)
111. **AvalonBench: Evaluating LLMs Playing the Game of Avalon**, *Light et al.*, arXiv 2023. [Paper](https://arxiv.org/abs/2310.05036)
112. **Mind2Web 2: Evaluating Agentic Search with Agent-as-a-Judge**, *Gou et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2506.21506)
113. **Mobile-env: Building qualified evaluation benchmarks for llm-gui interaction**, *Zhang et al.*, arXiv 2023. [Paper](https://arxiv.org/abs/2305.08144)
114. **Android in the Wild: A Large-Scale Dataset for Android Device Control**, *Rawles et al.*, arXiv 2023. [Paper](https://doi.org/10.48550/arXiv.2307.10088)
115. **AndroidWorld: A Dynamic Benchmarking Environment for Autonomous Agents**, *Rawles et al.*, ICLR 2025. [Paper](https://openreview.net/forum?id=il5yUQsrjC)
116. **MobileWorld: Benchmarking Autonomous Mobile Agents in Agent-User Interactive and MCP-Augmented Environments**, *Kong et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2512.19432)
117. **Windows agent arena: Evaluating multi-modal os agents at scale**, *Bonatti et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2409.08264)
118. **On the Multi-turn Instruction Following for Conversational Web Agents**, *Deng et al.*, ACL 2024. [Paper](https://doi.org/10.18653/v1/2024.acl-long.477)
119. **VideoWebArena: Evaluating Long Context Multimodal Agents with Video Understanding Web Tasks**, *Jang et al.*, ICLR 2025. [Paper](https://openreview.net/forum?id=unDQOUah0F)
120. **WebCanvas: Benchmarking Web Agents in Online Environments**, *Pan et al.*, arXiv 2024. [Paper](https://doi.org/10.48550/arXiv.2406.12373)
121. **An Illusion of Progress? Assessing the Current State of Web Agents**, *Xue et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2504.01382)
122. **MobileAgentBench: An Efficient and User-Friendly Benchmark for Mobile LLM Agents**, *Wang et al.*, arXiv 2024. [Paper](https://doi.org/10.48550/arXiv.2406.08184)
123. **DeepResearch Bench: A Comprehensive Benchmark for Deep Research Agents**, *Du et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2506.11763)
124. **DRAGged into Conflicts: Detecting and Addressing Conflicting Sources in Search-Augmented LLMs**, *Cattan et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2506.08500)
125. **DeepResearchGym: A Free, Transparent, and Reproducible Evaluation Sandbox for Deep Research**, *Coelho et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.19253)
126. **InfoDeepSeek: Benchmarking Agentic Information Seeking for Retrieval-Augmented Generation**, *Xi et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.15872)
127. **Open Data Synthesis For Deep Research**, *Xia et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.00375)
128. **BrowseComp-ZH: Benchmarking Web Browsing Ability of Large Language Models in Chinese**, *Zhou et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2504.19314)
129. **SurveyGen: Quality-Aware Scientific Survey Generation with Large Language Models**, *Bao et al.*, EMNLP 2025. [Paper](https://doi.org/10.18653/v1/2025.emnlp-main.136)
130. **ReportBench: Evaluating Deep Research Agents via Academic Survey Tasks**, *Li et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.15804)
131. **Characterizing Deep Research: A Benchmark and Formal Definition**, *Java et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.04183)
132. **OpenScholar: Synthesizing Scientific Literature with Retrieval-augmented LMs**, *Asai et al.*, arXiv 2024. [Paper](https://doi.org/10.48550/arXiv.2411.14199)
133. **ResearcherBench: Evaluating Deep AI Research Systems on the Frontiers of Scientific Inquiry**, *Xu et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2507.16280)
134. **ProxyQA: An Alternative Framework for Evaluating Long-Form Text Generation with Large Language Models**, *Tan et al.*, ACL 2024. [Paper](https://doi.org/10.18653/v1/2024.acl-long.368)
135. **AI Idea Bench 2025: AI Research Idea Generation Benchmark**, *Qiu et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2504.14191)
136. **DeepReview: Improving LLM-based Paper Review with Human-like Deep Thinking Process**, *Zhu et al.*, ACL 2025. [Paper](https://aclanthology.org/2025.acl-long.1420/)
137. **PaperBench: Evaluating AI's Ability to Replicate AI Research**, *Starace et al.*, ICML 2025. [Paper](https://proceedings.mlr.press/v267/starace25a.html)
138. **Multimodal DeepResearcher: Generating Text-Chart Interleaved Reports From Scratch with Agentic Framework**, *Yang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2506.02454)
139. **Vision-DeepResearch Benchmark: Rethinking Visual and Textual Search for Multimodal Large Language Models**, *Zeng et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.02185)
140. **MMDeepResearch-Bench: A Benchmark for Multimodal Deep Research Agents**, *Huang et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.12346)
141. **OmniGAIA: Towards Native Omni-Modal AI Agents**, *Li et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2602.22897)
142. **Dr. Bench: A Multidimensional Evaluation for Deep Research Agents, from Answers to Reports**, *Yao et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2510.02190)
143. **Habitat: A Platform for Embodied AI Research**, *Savva et al.*, ICCV 2019. [Paper](https://doi.org/10.1109/ICCV.2019.00943)
144. **Vision-and-Language Navigation: Interpreting Visually-Grounded Navigation Instructions in Real Environments**, *Anderson et al.*, CVPR 2018. [Paper](http://openaccess.thecvf.com/content_cvpr_2018/html/Anderson_Vision-and-Language_Navigation_Interpreting_CVPR_2018_paper.html)
145. **RLBench: The Robot Learning Benchmark & Learning Environment**, *James et al.*, IEEE RA-L 2020. [Paper](https://arxiv.org/abs/1909.12271)
146. **Robocasa: Large-scale simulation of everyday tasks for generalist robots**, *Nasiriany et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2406.02523)
147. **BEHAVIOR: Benchmark for Everyday Household Activities in Virtual, Interactive, and Ecological Environments**, *Srivastava et al.*, CoRL 2021. [Paper](https://proceedings.mlr.press/v164/srivastava22a.html)
148. **panda-gym: Open-source goal-conditioned environments for robotic learning**, *Gallou'edec et al.*, arXiv 2021. [Paper](https://arxiv.org/abs/2106.13687)
149. **ET-Plan-Bench: Embodied Task-level Planning Benchmark Towards Spatial-Temporal Cognition with Foundation Models**, *Zhang et al.*, IROS 2025. [Paper](https://doi.org/10.1109/IROS60139.2025.11246658)
150. **LEGENT: Open Platform for Embodied Agents**, *Cheng et al.*, ACL 2024. [Paper](https://doi.org/10.18653/v1/2024.acl-demos.32)
151. **SimuHome: A Temporal-and Environment-Aware Benchmark for Smart Home LLM Agents**, *Seo et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2509.24282)
152. **Sari Sandbox: A Virtual Retail Store Environment for Embodied AI Agents**, *Gajo et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.00400)
153. **Decoupled Diffusion Sparks Adaptive Scene Generation**, *Zhou et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2504.10485)
154. **MineDojo: Building Open-Ended Embodied Agents with Internet-Scale Knowledge**, *Fan et al.*, NeurIPS 2022. [Paper](http://papers.nips.cc/paper_files/paper/2022/hash/74a67268c5cc5910f64938cac4526a90-Abstract-Datasets_and_Benchmarks.html)
155. **KORGym: A Dynamic Game Platform for LLM Reasoning Evaluation**, *Shi et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2505.14552)
156. **TextArena**, *Guertler et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2504.11442)
157. **AI Gamestore: Scalable, Open-Ended Evaluation of Machine General Intelligence with Human Games**, *Ying et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.17594)
158. **ING-VP: MLLMs cannot Play Easy Vision-based Games Yet**, *Zhang et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2410.06555)
159. **VideoGameBench: Can Vision-Language Models complete popular video games?**, *Zhang et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2505.18134)
160. **BALROG: Benchmarking Agentic LLM and VLM Reasoning On Games**, *Paglieri et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2411.13543)
161. **SmartPlay: A Benchmark for LLMs as Intelligent Agents**, *Wu et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2310.01557)
162. **DSGBench: A Diverse Strategic Game Benchmark for Evaluating LLM-based Agents in Complex Decision-Making Environments**, *Tang et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2503.06047)
163. **GTBench: Uncovering the Strategic Reasoning Limitations of LLMs via Game-Theoretic Evaluations**, *Duan et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2402.12348)
164. **PokeLLMon: A Human-Parity Agent for Pokemon Battles with Large Language Models**, *Hu et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2402.01118)
165. **Describe, Explain, Plan and Select: Interactive Planning with Large Language Models Enables Open-World Multi-Task Agents**, *Wang et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2302.01560)
166. **LMRL Gym: Benchmarks for Multi-Turn Reinforcement Learning with Language Models**, *Abdulhai et al.*, arXiv 2023. [Paper](https://arxiv.org/abs/2311.18232)
167. **Clembench: Using Game Play to Evaluate Chat-Optimized Language Models as Conversational Agents**, *Chalamalasetti et al.*, arXiv 2023. [Paper](https://arxiv.org/abs/2305.13455)
168. **LLM-Powered Hierarchical Language Agent for Real-time Human-AI Coordination**, *Liu et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2312.15224)
169. **TextGames: Learning to Self-Play Text-Based Puzzle Games via Language Model Reasoning**, *Hudi et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2502.18431)
170. **SPIN-Bench: How Well Do LLMs Plan Strategically and Reason Socially?**, *Yao et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2503.12349)
171. **GAMEBoT: Transparent Assessment of LLM Reasoning in Games**, *Lin et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2412.13602)
172. **MineWorld: a Real-Time and Open-Source Interactive World Model on Minecraft**, *Guo et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2504.08388)
173. **Enhance Reasoning for Large Language Models in the Game Werewolf**, *Wu et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2402.02330)
174. **GameFactory: Creating New Games with Generative Interactive Videos**, *Yu et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2501.08325)
175. **Diffusion Models Are Real-Time Game Engines**, *Valevski et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2408.14837)
176. **The Overcooked Generalisation Challenge: Evaluating Cooperation with Novel Partners in Unknown Environments Using Unsupervised Environment Design**, *Ruhdorfer et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2406.17949)
177. **Minigrid & Miniworld: Modular & Customizable Reinforcement Learning Environments for Goal-Oriented Tasks**, *Chevalier-Boisvert et al.*, arXiv 2023. [Paper](https://arxiv.org/abs/2306.13831)
178. **TEACh: Task-Driven Embodied Agents That Chat**, *Padmakumar et al.*, AAAI 2022. [Paper](https://ojs.aaai.org/index.php/AAAI/article/view/20097)
179. **ReALFRED: An Embodied Instruction Following Benchmark in Photo-Realistic Environments**, *Kim et al.*, ECCV 2024. [Paper](https://arxiv.org/abs/2407.18550)
180. **ToolEyes: Fine-Grained Evaluation for Tool Learning Capabilities of Large Language Models in Real-world Scenarios**, *Ye et al.*, COLING 2025. [Paper](https://aclanthology.org/2025.coling-main.12/)
181. **ACEBench: A Comprehensive Evaluation of LLM Tool Usage**, *Chen et al.*, Findings of EMNLP 2025. [Paper](https://aclanthology.org/2025.findings-emnlp.697/)
182. **FlowBench: Revisiting and Benchmarking Workflow-Guided Planning for LLM-based Agents**, *Xiao et al.*, Findings of EMNLP 2024. [Paper](https://doi.org/10.18653/v1/2024.findings-emnlp.638)
183. **TRAJECT-Bench:A Trajectory-Aware Benchmark for Evaluating Agentic Tool Use**, *He et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.04550)
184. **Evaluating Personalized Tool-Augmented LLMs from the Perspectives of Personalization and Proactivity**, *Hao et al.*, ACL 2025. [Paper](https://aclanthology.org/2025.acl-long.1064/)
185. **The Berkeley Function Calling Leaderboard (BFCL): From Tool Use to Agentic Evaluation of Large Language Models**, *Patil et al.*, ICML 2025. [Paper](https://proceedings.mlr.press/v267/patil25a.html)
186. **UserBench: An Interactive Gym Environment for User-Centric Agents**, *Qian et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2507.22034)
187. **tau^2-Bench: Evaluating Conversational Agents in a Dual-Control Environment**, *Barres et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2506.07982)
188. **MCPToolBench++: A Large Scale AI Agent Model Context Protocol MCP Tool Use Benchmark**, *Fan et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.07575)
189. **MCP-Universe: Benchmarking Large Language Models with Real-World Model Context Protocol Servers**, *Luo et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.14704)
190. **MCP-Bench: Benchmarking Tool-Using LLM Agents with Complex Real-World Tasks via MCP Servers**, *Wang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.20453)
191. **Mcpmark: A benchmark for stress-testing realistic and comprehensive mcp use**, *Wu et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2509.24002)
192. **M^3-Bench: Multi-Modal, Multi-Hop, Multi-Threaded Tool-Using MLLM Agent Benchmark**, *Zhou et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2511.17729)
193. **InterCode: Standardizing and Benchmarking Interactive Coding with Execution Feedback**, *Yang et al.*, NeurIPS 2023. [Paper](https://arxiv.org/abs/2306.14898)
194. **CodeAgent: Enhancing Code Generation with Tool-Integrated Agent Systems for Real-World Repo-level Coding Challenges**, *Zhang et al.*, ACL 2024. [Paper](https://aclanthology.org/2024.acl-long.737/)
195. **BigCodeBench: Benchmarking Code Generation with Diverse Function Calls and Complex Instructions**, *Zhuo et al.*, ICLR 2025. [Paper](https://openreview.net/forum?id=YrycTjllL0)
196. **CodeElo: Benchmarking Competition-level Code Generation of LLMs with Human-comparable Elo Ratings**, *Quan et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2501.01257)
197. **CSR-Bench: Benchmarking LLM Agents in Deployment of Computer Science Research Repositories**, *Xiao et al.*, NAACL 2025. [Paper](https://aclanthology.org/2025.naacl-long.633/)
198. **SWE-Bench Pro: Can AI Agents Solve Long-Horizon Software Engineering Tasks?**, *Deng et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.16941)
199. **Swe-bench multimodal: Do ai systems generalize to visual software domains?**, *Yang et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2410.03859)
200. **CRUXEval: A Benchmark for Code Reasoning, Understanding and Execution**, *Gu et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2401.03065)
201. **DebugBench: Evaluating Debugging Capability of Large Language Models**, *Tian et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2401.04621)
202. **CodeRAG-Bench: Can Retrieval Augment Code Generation?**, *Wang et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2406.14497)
203. **SWT-Bench: Testing and Validating Real-World Bug-Fixes with Code Agents**, *Mündler et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2406.12952)
204. **FEA-Bench: A Benchmark for Evaluating Repository-Level Code Generation for Feature Implementation**, *Li et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2503.06680)
205. **Multi-SWE-bench: A Multilingual Benchmark for Issue Resolving**, *Zan et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2504.02605)
206. **NL2Repo-Bench: Towards Long-Horizon Repository Generation Evaluation of Coding Agents**, *Ding et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2512.12730)
207. **WhodunitBench: Evaluating Large Multimodal Agents via Murder Mystery Games**, *Xie et al.*, NeurIPS 2024. [Paper](https://proceedings.neurips.cc/paper_files/paper/2024/hash/9dd4533e7e4e5ed809344280609c5b05-Abstract-Datasets_and_Benchmarks_Track.html)
208. **FlashAdventure: A Benchmark for GUI Agents Solving Full Story Arcs in Diverse Adventure Games**, *Ahn et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2509.01052)
209. **CivRealm: A Learning and Reasoning Odyssey in Civilization for Decision-Making Agents**, *Qi et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2401.10568)
210. **Factorio Learning Environment**, *Hopkins et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2503.09617)
211. **BioCoder: a benchmark for bioinformatics code generation with large language models**, *Tang et al.*, Bioinform 2024. [Paper](https://doi.org/10.1093/bioinformatics/btae230)
212. **Benchmarking Data Science Agents**, *Zhang et al.*, ACL 2024. [Paper](https://doi.org/10.18653/v1/2024.acl-long.308)
213. **NATURAL PLAN: Benchmarking LLMs on Natural Language Planning**, *Zheng et al.*, arXiv 2024. [Paper](https://doi.org/10.48550/arXiv.2406.04520)
214. **DiscoveryWorld: A Virtual Environment for Developing and Evaluating Automated Scientific Discovery Agents**, *Jansen et al.*, NeurIPS 2024. [Paper](http://papers.nips.cc/paper_files/paper/2024/hash/13836f251823945316ae067350a5c366-Abstract-Datasets_and_Benchmarks_Track.html)
215. **StockBench: Can LLM Agents Trade Stocks Profitably In Real-world Markets?**, *Chen et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.02209)
216. **Mle-dojo: Interactive environments for empowering llm agents in machine learning engineering**, *Qiang et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2505.07782)
217. **FinDeepResearch: Evaluating Deep Research Agents in Rigorous Financial Analysis**, *Zhu et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.13936)
218. **PaperArena: An Evaluation Benchmark for Tool-Augmented Agentic Reasoning on Scientific Literature**, *Wang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.10909)
219. **BixBench: a Comprehensive Benchmark for LLM-based Agents in Computational Biology**, *Mitchener et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2503.00096)
220. **CRMArena-Pro: Holistic Assessment of LLM Agents Across Diverse Business Scenarios and Interactions**, *Huang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.18878)
221. **MedAgentGym: A Scalable Agentic Training Environment for Code-Centric Reasoning in Biomedical Data Science**, *Xu et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2506.04405)
222. **Finance Agent Benchmark: Benchmarking LLMs on Real-world Financial Research Tasks**, *Bigeard et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.00828)
223. **EcomBench: Towards Holistic Evaluation of Foundation Agents in E-commerce**, *Min et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2512.08868)
224. **MedAgentBench v2: Improving Medical LLM Agent Design**, *Chen et al.*, PSB 2026. [Paper](https://doi.org/10.1142/9789819824755_0025)
225. **MedMCP-Calc: Benchmarking LLMs for Realistic Medical Calculator Scenarios via MCP Integration**, *Zhu et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.23049)
226. **Advancing ESG Intelligence: An Expert-level Agent and Comprehensive Benchmark for Sustainable Finance**, *Zhao et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2601.08676)
227. **BioAgent Bench: An AI Agent Evaluation Suite for Bioinformatics**, *Fa et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.21800)
228. **World of Workflows: a Benchmark for Bringing World Models to Enterprise Systems**, *Gupta et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.22130)
229. **EnterpriseOps-Gym: Environments and Evaluations for Stateful Agentic Planning and Tool Use in Enterprise Settings**, *Malay et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2603.13594)
230. **MetaClaw: Just Talk-An Agent That Meta-Learns and Evolves in the Wild**, *Xia et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2603.17187)
231. **Claw-Eval: Toward Trustworthy Evaluation of Autonomous Agents**, *Ye et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2604.06132)
232. **ClawArena: Benchmarking AI Agents in Evolving Information Environments**, *Ji et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2604.04202)
233. **AgentBoard: An Analytical Evaluation Board of Multi-turn LLM Agents**, *Ma et al.*, NeurIPS 2024. [Paper](http://papers.nips.cc/paper_files/paper/2024/hash/877b40688e330a0e2a3fc24084208dfa-Abstract-Datasets_and_Benchmarks_Track.html)
234. **AgentGym: Evolving Large Language Model-based Agents across Diverse Environments**, *Xi et al.*, arXiv 2024. [Paper](https://doi.org/10.48550/arXiv.2406.04151)
235. **Benchmarking Agentic Workflow Generation**, *Qiao et al.*, ICLR 2025. [Paper](https://openreview.net/forum?id=vunPXOFmoi)
236. **Mlgym: A new framework and benchmark for advancing ai research agents**, *Nathani et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2502.14499)
237. **MedBrowseComp: Benchmarking Medical Deep Research and Computer Use**, *Chen et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.14963)
238. **WebMMU: A Benchmark for Multimodal Multilingual Website Understanding and Code Generation**, *Awal et al.*, EMNLP 2025. [Paper](https://doi.org/10.18653/v1/2025.emnlp-main.1276)
239. **TPS-Bench: Evaluating AI Agents' Tool Planning & Scheduling Abilities in Compounding Tasks**, *Xu et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2511.01527)
240. **AgencyBench: Benchmarking the Frontiers of Autonomous Agents in 1M-Token Real-World Contexts**, *Li et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.11044)
241. **AgentVista: Evaluating Multimodal Agents in Ultra-Challenging Realistic Visual Scenarios**, *Su et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2602.23166)
242. **DeepSeek-V3.2: Pushing the Frontier of Open Large Language Models**, *DeepSeek-AI et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2512.02556)
243. **LongCat-Flash-Thinking-2601 Technical Report**, *Meituan LongCat Team et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.16725)
244. **MiMo-V2-Flash Technical Report**, *Xiaomi et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.02780)
245. **Generalized Planning in PDDL Domains with Pretrained Large Language Models**, *Silver et al.*, AAAI 2024. [Paper](https://doi.org/10.1609/aaai.v38i18.30006)
246. **Can Language Models Serve as Text-Based World Simulators?**, *Wang et al.*, ACL 2024. [Paper](https://doi.org/10.18653/v1/2024.acl-short.1)
247. **Leveraging Environment Interaction for Automated PDDL Translation and Planning with Large Language Models**, *Mahdavi et al.*, NeurIPS 2024. [Paper](http://papers.nips.cc/paper_files/paper/2024/hash/44af065477781e7f8a8589b14a62c489-Abstract-Conference.html)
248. **Text2World: Benchmarking Large Language Models for Symbolic World Model Generation**, *Hu et al.*, Findings of ACL 2025. [Paper](https://aclanthology.org/2025.findings-acl.1337/)
249. **WorldCoder, a Model-Based LLM Agent: Building World Models by Writing Code and Interacting with the Environment**, *Tang et al.*, NeurIPS 2024. [Paper](http://papers.nips.cc/paper_files/paper/2024/hash/820c61a0cd419163ccbd2c33b268816e-Abstract-Conference.html)
250. **Towards General Agentic Intelligence via Environment Scaling**, *Fang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.13311)
251. **Scaling Agents via Continual Pre-training**, *Su et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.13310)
252. **On Data Engineering for Scaling LLM Terminal Capabilities**, *Pi et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.21193)
253. **LLM-in-Sandbox Elicits General Agentic Intelligence**, *Cheng et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.16206)
254. **Generalizable End-to-End Tool-Use RL with Synthetic CodeGym**, *Du et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.17325)
255. **Agent2World: Learning to Generate Symbolic World Models via Adaptive Multi-Agent Feedback**, *Hu et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2512.22336)
256. **Training Software Engineering Agents and Verifiers with SWE-Gym**, *Pan et al.*, ICML 2025. [Paper](https://proceedings.mlr.press/v267/pan25g.html)
257. **R2E-Gym: Procedural Environments and Hybrid Verifiers for Scaling Open-Weights SWE Agents**, *Jain et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2504.07164)
258. **Immersion in the GitHub Universe: Scaling Coding Agents to Mastery**, *Zhao et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.09892)
259. **SWE-Hub: A Unified Production System for Scalable, Executable Software Engineering Tasks**, *Zeng et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2603.00575)
260. **MEnvAgent: Scalable Polyglot Environment Construction for Verifiable Software Engineering**, *Guo et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.22859)
261. **SWE-smith: Scaling Data for Software Engineering Agents**, *Yang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2504.21798)
262. **DockSmith: Scaling Reliable Coding Environments via an Agentic Docker Builder**, *Zhang et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2602.00592)
263. **CLI-Gym: Scalable CLI Task Generation via Agentic Environment Inversion**, *Lin et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.10999)
264. **SciAgentGym: Benchmarking Multi-Step Scientific Tool-use in LLM Agents**, *Shen et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.12984)
265. **FinMTM: A Multi-Turn Multimodal Benchmark for Financial Reasoning and Agent Evaluation**, *Zhang et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2602.03130)
266. **AgentSynth: Scalable Task Generation for Generalist Computer-Use Agents**, *Xie et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2506.14205)
267. **lmgame-Bench: How Good are LLMs at Playing Games?**, *Li et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2505.15146)
268. **GameDevBench: Evaluating Agentic Capabilities Through Game Development**, *Chi et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.11103)
269. **Safe and Scalable Web Agent Learning via Recreated Websites**, *Chae et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2603.10505)
270. **AutoWebWorld: Synthesizing Infinite Verifiable Web Environments via Finite State Machines**, *Wu et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.14296)
271. **GLM-5: from Vibe Coding to Agentic Engineering**, *GLM et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2602.15763)
272. **DIVE: Scaling Diversity in Agentic Task Synthesis for Generalizable Tool Use**, *Chen et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2603.11076)
273. **KAT-Coder-V2 Technical Report**, *Li et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2603.27703)
274. **SWE-Universe: Scale Real-World Verifiable Environments to Millions**, *Chen et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2602.02361)
275. **TaskCraft: Automated Generation of Agentic Tasks**, *Shi et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2506.10055)
276. **LOGIGEN: Logic-Driven Generation of Verifiable Agentic Tasks**, *Zeng et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2603.00540)
277. **InfiniteWeb: Scalable Web Environment Synthesis for GUI Agent Training**, *Zhang et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.04126)
278. **NL2Plan: Robust LLM-Driven Planning from Minimal Text Descriptions**, *Gestrin et al.*, arXiv 2024. [Paper](https://doi.org/10.48550/arXiv.2405.04215)
279. **Procedural Environment Generation for Tool-Use Agents**, *Sullivan et al.*, EMNLP 2025. [Paper](https://doi.org/10.18653/v1/2025.emnlp-main.936)
280. **AutoForge: Automated Environment Synthesis for Agentic Reinforcement Learning**, *Cai et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2512.22857)
281. **ScaleEnv: Scaling Environment Synthesis from Scratch for Generalist Interactive Tool-Use Agent Training**, *Tu et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.06820)
282. **Training Versatile Coding Agents in Synthetic Environments**, *Zhu et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2512.12216)
283. **Endless Terminals: Scaling RL Environments for Terminal Agents**, *Gandhi et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.16443)
284. **Measuring General Intelligence with Generated Games**, *Verma et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.07215)
285. **Welcome to the Era of Experience**, *Silver et al.*, Google AI 2025. [Paper](https://storage.googleapis.com/deepmind-media/Era-of-Experience%20/The%20Era%20of%20Experience%20Paper.pdf)
286. **Planetarium: A Rigorous Benchmark for Translating Text to Structured Planning Languages**, *Zuo et al.*, NAACL 2025. [Paper](https://doi.org/10.18653/v1/2025.naacl-long.560)
287. **Generating Symbolic World Models via Test-time Scaling of Large Language Models**, *Yu et al.*, Trans. Mach. Learn. Res 2025. [Paper](https://openreview.net/forum?id=zVo6PfBa0K)
288. **Synthesizing world models for bilevel planning**, *Ahmed et al.*, Trans. Mach. Learn. Res 2025. [Paper](https://openreview.net/forum?id=m9V4JHLJrD)
289. **Hybrid-Gym: Training Coding Agents to Generalize Across Tasks**, *Xie et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.16819)
290. **EnvGen: Generating and Adapting Environments via LLMs for Training Embodied Agents**, *Zala et al.*, arXiv 2024. [Paper](https://doi.org/10.48550/arXiv.2403.12014)
291. **Diffusion for World Modeling: Visual Details Matter in Atari**, *Alonso et al.*, NeurIPS 2024. [Paper](http://papers.nips.cc/paper_files/paper/2024/hash/6bdde0373d53d4a501249547084bed43-Abstract-Conference.html)
292. **Pandora: Towards General World Model with Natural Language Actions and Video States**, *Xiang et al.*, arXiv 2024. [Paper](https://doi.org/10.48550/arXiv.2406.09455)
293. **Recurrent World Models Facilitate Policy Evolution**, *Ha et al.*, NeurIPS 2018. [Paper](https://proceedings.neurips.cc/paper/2018/hash/2de5d16682c3c35007e4e92982f1a2ba-Abstract.html)
294. **Empowering World Models with Reflection for Embodied Video Prediction**, *Chi et al.*, ICML 2025. [Paper](https://proceedings.mlr.press/v267/chi25b.html)
295. **Vimo: A generative visual gui world model for app agents**, *Luo et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2504.13936)
296. **Matrix-Game: Interactive World Foundation Model**, *Zhang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2506.18701)
297. **Matrix-Game 2.0: An Open-Source, Real-Time, and Streaming Interactive World Model**, *He et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.13009)
298. **NeuralOS: Towards Simulating Operating Systems via Neural Generative Models**, *Rivard et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2507.08800)
299. **GTM: Simulating the World of Tools for AI Agents**, *Ren et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2512.04535)
300. **CWM: An Open-Weights LLM for Research on Code Generation with World Models**, *team et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.02387)
301. **Imagine-then-Plan: Agent Learning from Adaptive Lookahead with World Models**, *Liu et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.08955)
302. **Agent Planning with World Knowledge Model**, *Qiao et al.*, NeurIPS 2024. [Paper](http://papers.nips.cc/paper_files/paper/2024/hash/d032263772946dd5026e7f3cd22bce5b-Abstract-Conference.html)
303. **R-WoM: Retrieval-augmented World Model For Computer-use Agents**, *Mei et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.11892)
304. **MobileDreamer: Generative Sketch World Model for GUI Agent**, *Cao et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.04035)
305. **Code2World: A GUI World Model via Renderable Code Generation**, *Zheng et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.09856)
306. **Reasoning with Language Model is Planning with World Model**, *Hao et al.*, EMNLP 2023. [Paper](https://doi.org/10.18653/v1/2023.emnlp-main.507)
307. **Learning and Leveraging World Models in Visual Representation Learning**, *Garrido et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2403.00504)
308. **Dino-wm: World models on pre-trained visual features enable zero-shot planning**, *Zhou et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2411.04983)
309. **Seq-JEPA: Autoregressive Predictive Learning of Invariant-Equivariant World Models**, *Ghaemi et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2505.03176)
310. **Self-Supervised Learning from Images with a Joint-Embedding Predictive Architecture**, *Assran et al.*, CVPR 2023. [Paper](https://arxiv.org/abs/2301.08243)
311. **Back to the features: Dino as a foundation for video world models**, *Baldassarre et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2507.19468)
312. **Dino-foresight: Looking into the future with dino**, *Karypidis et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2412.11673)
313. **V-JEPA 2: Self-Supervised Video Models Enable Understanding, Prediction and Planning**, *Assran et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2506.09985)
314. **EnerVerse: Envisioning Embodied Future Space for Robotics Manipulation**, *Huang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2501.01895)
315. **Genie Envisioner: A Unified World Foundation Platform for Robotic Manipulation**, *Liao et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.05635)
316. **KeyWorld: Key Frame Reasoning Enables Effective and Efficient World Models**, *Li et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.21027)
317. **FlowDreamer: A RGB-D World Model With Flow-Based Motion Representations for Robot Manipulation**, *Guo et al.*, IEEE Robotics Autom. Lett 2026. [Paper](https://doi.org/10.1109/LRA.2026.3653273)
318. **Cosmos Policy: Fine-Tuning Video Models for Visuomotor Control and Planning**, *Kim et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.16163)
319. **World action models are zero-shot policies**, *Ye et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.15922)
320. **GAIA-2: A Controllable Multi-View Generative World Model for Autonomous Driving**, *Russell et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2503.20523)
321. **Cosmos-Drive-Dreams: Scalable Synthetic Driving Data Generation with World Foundation Models**, *Ren et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2506.09042)
322. **Learning Primitive Embodied World Models: Towards Scalable Robotic Learning**, *Sun et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.20840)
323. **AdaWorld: Learning Adaptable World Models with Latent Actions**, *Gao et al.*, ICML 2025. [Paper](https://proceedings.mlr.press/v267/gao25u.html)
324. **Causal World Modeling for Robot Control**, *Li et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.21998)
325. **Medical World Model: Generative Simulation of Tumor Evolution for Treatment Planning**, *Yang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2506.02327)
326. **Cosmos World Foundation Model Platform for Physical AI**, *Agarwal et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2501.03575)
327. **LIVE: Long-horizon Interactive Video World Modeling**, *Huang et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2602.03747)
328. **Dyna-Think: Synergizing Reasoning, Acting, and World Model Simulation in AI Agents**, *Yu et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2506.00320)
329. **Planning with Reasoning using Vision Language World Model**, *Chen et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.02722)
330. **Simura: A world-model-driven simulative reasoning architecture for general goal-oriented agents**, *Deng et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2507.23773)
331. **Unlocking Smarter Device Control: Foresighted Planning with a World Model-Driven Code Execution Approach**, *Yin et al.*, Findings of EMNLP 2025. [Paper](https://aclanthology.org/2025.findings-emnlp.213/)
332. **Web World Models**, *Feng et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2512.23676)
333. **World modelling improves language model agents**, *Guo et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2506.02918)
334. **Simulating Environments with Reasoning Models for Agent Training**, *Li et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2511.01824)
335. **WebWorld: A Large-Scale World Model for Web Agent Training**, *Xiao et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.14721)
336. **Generative Visual Code Mobile World Models**, *Koh et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2602.01576)
337. **SWE-World: Building Software Engineering Agents in Docker-Free Environments**, *Sun et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2602.03419)
338. **EchoJEPA: A Latent Predictive Foundation Model for Echocardiography**, *Munim et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.02603)
339. **Enhancing Open-Domain Task-Solving Capability of LLMs via Autonomous Tool Integration from GitHub**, *Lyu et al.*, ACL 2025. [Paper](https://aclanthology.org/2025.acl-long.845/)
340. **CoPS: Empowering LLM Agents with Provable Cross-Task Experience Sharing**, *Yang et al.*, arXiv 2024. [Paper](https://doi.org/10.48550/arXiv.2410.16670)
341. **Embodied large language models enable robots to complete complex tasks in unpredictable environments**, *Mon-Williams et al.*, Nat. Mac. Intell 2025. [Paper](https://doi.org/10.1038/s42256-025-01005-x)
342. **Memp: Exploring Agent Procedural Memory**, *Fang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.06433)
343. **Synapse: Trajectory-as-Exemplar Prompting with Memory for Computer Control**, *Zheng et al.*, ICLR 2024. [Paper](https://openreview.net/forum?id=Pc8AU1aF5e)
344. **WorldMM: Dynamic Multimodal Memory Agent for Long Video Reasoning**, *Yeo et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2512.02425)
345. **Darwin Godel Machine: Open-Ended Evolution of Self-Improving Agents**, *Zhang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.22954)
346. **ReasoningBank: Scaling Agent Self-Evolving with Reasoning Memory**, *Ouyang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.25140)
347. **Agent-Pro: Learning to Evolve via Policy-Level Reflection and Optimization**, *Zhang et al.*, ACL 2024. [Paper](https://doi.org/10.18653/v1/2024.acl-long.292)
348. **Agent KB: Leveraging Cross-Domain Experience for Agentic Problem Solving**, *Tang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2507.06229)
349. **DeepAgent: A General Reasoning Agent with Scalable Toolsets**, *Li et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.21618)
350. **FLEX: Continuous Agent Evolution via Forward Learning from Experience**, *Cai et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2511.06449)
351. **O-Mem: Omni Memory System for Personalized, Long Horizon, Self-Evolving Agents**, *Wang et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2511.13593)
352. **Experience-Evolving Multi-Turn Tool-Use Agent with Hybrid Episodic-Procedural Memory**, *Li et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2512.07287)
353. **Remember Me, Refine Me: A Dynamic Procedural Memory Framework for Experience-Driven Agent Evolution**, *Cao et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2512.10696)
354. **Bifrost: Steering Strategic Trajectories to Bridge Contextual Gaps for Self-Improving Agents**, *Tran et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.05810)
355. **Learning Physical Principles from Interaction: Self-Evolving Planning via Test-Time Memory**, *Li et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.20323)
356. **Agent Workflow Memory**, *Wang et al.*, arXiv 2024. [Paper](https://doi.org/10.48550/arXiv.2409.07429)
357. **Reinforcement Learning for Self-Improving Agent with Skill Library**, *Wang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2512.17102)
358. **Inducing Programmatic Skills for Agentic Tasks**, *Wang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2504.06821)
359. **SkillWeaver: Web Agents can Self-Improve by Discovering and Honing Skills**, *Zheng et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2504.07079)
360. **SkillRL: Evolving Agents via Recursive Skill-Augmented Reinforcement Learning**, *Xia et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.08234)
361. **SkillOrchestra: Learning to Route Agents via Skill Transfer**, *Wang et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.19672)
362. **Memory in the Age of AI Agents**, *Hu et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2512.13564)
363. **Rethinking Memory in AI: Taxonomy, Operations, Topics, and Future Directions**, *Du et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.00675)
364. **Rethinking Memory Mechanisms of Foundation Agents in the Second Half: A Survey**, *Huang et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2602.06052)
365. **Think While Watching: Online Streaming Segment-Level Memory for Multi-Turn Video Reasoning in Multimodal Large Language Models**, *Wang et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2603.11896)
366. **Learning How to Remember: A Meta-Cognitive Management Method for Structured and Transferable Agent Memory**, *Liang et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2601.07470)
367. **MemGPT: Towards LLMs as Operating Systems**, *Packer et al.*, arXiv 2023. [Paper](https://doi.org/10.48550/arXiv.2310.08560)
368. **Voyager: An Open-Ended Embodied Agent with Large Language Models**, *Wang et al.*, Trans. Mach. Learn. Res 2024. [Paper](https://openreview.net/forum?id=ehfRiF0R3a)
369. **Training-Free Group Relative Policy Optimization**, *Cai et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.08191)
370. **Simulate Before Act: Model-Based Planning for Web Agents**, *Gu et al.*, OpenReview 2024. [Paper](https://openreview.net/forum?id=JDa5RiTIC7)
371. **ManuSearch: Democratizing Deep Search in Large Language Models with a Transparent and Open Multi-Agent Framework**, *Huang et al.*, Findings of EMNLP 2025. [Paper](https://aclanthology.org/2025.findings-emnlp.130/)
372. **Open Deep Search: Democratizing Search with Open-source Reasoning Agents**, *Alzubi et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2503.20201)
373. **Search-o1: Agentic Search-Enhanced Large Reasoning Models**, *Li et al.*, EMNLP 2025. [Paper](https://doi.org/10.18653/v1/2025.emnlp-main.276)
374. **Demystifying and Enhancing the Efficiency of Large Language Model Based Search Agents**, *Yang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.12065)
375. **Thought of Search: Planning with Language Models Through The Lens of Efficiency**, *Katz et al.*, NeurIPS 2024. [Paper](http://papers.nips.cc/paper_files/paper/2024/hash/fa080fe0f218871faec1d8ba20e491d5-Abstract-Conference.html)
376. **Agent hospital: A simulacrum of hospital with evolvable medical agents**, *Li et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2405.02957)
377. **QuantAgent: Seeking Holy Grail in Trading by Self-Improving Large Language Model**, *Wang et al.*, arXiv 2024. [Paper](https://doi.org/10.48550/arXiv.2402.03755)
378. **Agentless: Demystifying LLM-based Software Engineering Agents**, *Xia et al.*, arXiv 2024. [Paper](https://doi.org/10.48550/arXiv.2407.01489)
379. **AutoCodeRover: Autonomous Program Improvement**, *Zhang et al.*, ACM 2024. [Paper](https://doi.org/10.1145/3650212.3680384)
380. **CodeNav: Beyond tool-use to using real-world codebases with LLM agents**, *Gupta et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2406.12276)
381. **Coder: Issue resolving with multi-agent and task graphs**, *Chen et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2406.01304)
382. **MAGIS: LLM-Based Multi-Agent Framework for GitHub Issue Resolution**, *Tao et al.*, NeurIPS 2024. [Paper](https://arxiv.org/abs/2403.17927)
383. **MetaGPT: Meta Programming for A Multi-Agent Collaborative Framework**, *Hong et al.*, ICLR 2024. [Paper](https://openreview.net/forum?id=VtmBAGCN7o)
384. **SWE-agent: Agent-Computer Interfaces Enable Automated Software Engineering**, *Yang et al.*, NeurIPS 2024. [Paper](https://arxiv.org/abs/2405.15793)
385. **VideoAgent: Long-Form Video Understanding with Large Language Model as Agent**, *Wang et al.*, ECCV 2024. [Paper](https://doi.org/10.1007/978-3-031-72989-8_4)
386. **Real-Time Reasoning Agents in Evolving Environments**, *Wen et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2511.04898)
387. **LVAgent: Long Video Understanding by Multi-Round Dynamical Collaboration of MLLM Agents**, *Chen et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2503.10200)
388. **Explorer: Scaling Exploration-driven Web Trajectory Synthesis for Multimodal Web Agents**, *Pahuja et al.*, Findings of ACL 2025. [Paper](https://aclanthology.org/2025.findings-acl.326/)
389. **ScoreFlow: Mastering LLM Agent Workflows via Score-based Preference Optimization**, *Wang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2502.04306)
390. **RobustFlow: Towards Robust Agentic Workflow Generation**, *Xu et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.21834)
391. **DyFlow: Dynamic Workflow Framework for Agentic Reasoning**, *Wang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.26062)
392. **Multi-agent Architecture Search via Agentic Supernet**, *Zhang et al.*, ICML 2025. [Paper](https://proceedings.mlr.press/v267/zhang25bi.html)
393. **FlowReasoner: Reinforcing Query-Level Meta-Agents**, *Gao et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2504.15257)
394. **MindSearch: Mimicking Human Minds Elicits Deep AI Searcher**, *Chen et al.*, ICLR 2025. [Paper](https://openreview.net/forum?id=xgtXkyqw1f)
395. **WideSeek-R1: Exploring Width Scaling for Broad Information Seeking via Multi-Agent Reinforcement Learning**, *Xu et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2602.04634)
396. **Workflow-R1: Group Sub-sequence Policy Optimization for Multi-turn Workflow Construction**, *Kong et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2602.01202)
397. **ResearStudio: A Human-intervenable Framework for Building Controllable Deep Research Agents**, *Yang et al.*, EMNLP 2025. [Paper](https://doi.org/10.18653/v1/2025.emnlp-demos.69)
398. **WebPilot: A Versatile and Autonomous Multi-Agent System for Web Task Execution with Strategic Exploration**, *Zhang et al.*, AAAI 2025. [Paper](https://doi.org/10.1609/aaai.v39i22.34505)
399. **Plan-and-Act: Improving Planning of Agents for Long-Horizon Tasks**, *Erdogan et al.*, ICML 2025. [Paper](https://proceedings.mlr.press/v267/erdogan25a.html)
400. **AOrchestra: Automating Sub-Agent Creation for Agentic Orchestration**, *Ruan et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.03786)
401. **Dr. MAS: Stable Reinforcement Learning for Multi-Agent LLM Systems**, *Lang et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.08847)
402. **OWL: Optimized Workforce Learning for General Multi-Agent Assistance in Real-World Task Automation**, *Hu et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.23885)
403. **ControlLLM: Augment Language Models with Tools by Searching on Graphs**, *Liu et al.*, ECCV 2024. [Paper](https://doi.org/10.1007/978-3-031-73254-6_6)
404. **Hyperagent: Generalist software engineering agents to solve coding tasks at scale**, *Phan et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2409.16299)
405. **RepairAgent: An Autonomous, LLM-Based Agent for Program Repair**, *Bouzenia et al.*, ICSE 2025. [Paper](https://arxiv.org/abs/2403.17134)
406. **Swe-search: Enhancing software agents with monte carlo tree search and iterative refinement**, *Antoniades et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2410.20285)
407. **Alibaba LingmaAgent: Improving Automated Issue Resolution via Comprehensive Repository Exploration**, *Ma et al.*, FSE 2025. [Paper](https://arxiv.org/abs/2406.01422)
408. **MindAgent: Emergent Gaming Interaction**, *Gong et al.*, Findings of ACL 2024. [Paper](https://doi.org/10.18653/v1/2024.findings-naacl.200)
409. **Code Researcher: Deep Research Agent for Large Systems Code and Commit History**, *Singh et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2506.11060)
410. **Constrained Natural Language Action Planning for Resilient Embodied Systems**, *Byrd et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.06357)
411. **MGA: Memory-Driven GUI Agent for Observation-Centric Interaction**, *Cheng et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.24168)
412. **AFlow: Automating Agentic Workflow Generation**, *Zhang et al.*, ICLR 2025. [Paper](https://openreview.net/forum?id=z5uVAKwmjf)
413. **AgentSquare: Automatic LLM Agent Search in Modular Design Space**, *Shang et al.*, ICLR 2025. [Paper](https://openreview.net/forum?id=mPdmDYIQ7f)
414. **Multi-Agent Collaboration via Evolving Orchestration**, *Dang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.19591)
415. **Automated Design of Agentic Systems**, *Hu et al.*, ICLR 2025. [Paper](https://openreview.net/forum?id=t9U3LW7JVX)
416. **Process vs. Outcome Reward: Which is Better for Agentic RAG Reinforcement Learning**, *Zhang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.14069)
417. **AvaTaR: Optimizing LLM Agents for Tool Usage via Contrastive Reasoning**, *Wu et al.*, NeurIPS 2024. [Paper](http://papers.nips.cc/paper_files/paper/2024/hash/2db8ce969b000fe0b3fb172490c33ce8-Abstract-Conference.html)
418. **ReCreate: Reasoning and Creating Domain Agents Driven by Experience**, *Hao et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.11100)
419. **Yunjue Agent Tech Report: A Fully Reproducible, Zero-Start In-Situ Self-Evolving Agent System for Open-Ended Tasks**, *Li et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.18226)
420. **Chain-of-Agents: End-to-End Agent Foundation Models via Multi-Agent Distillation and Agentic RL**, *Li et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.13167)
421. **ClinicalReTrial: A Self-Evolving AI Agent for Clinical Trial Protocol Optimization**, *Xing et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.00290)
422. **EvoClinician: A Self-Evolving Agent for Multi-Turn Medical Diagnosis via Test-Time Evolutionary Learning**, *He et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.22964)
423. **Grammar Search for Multi-Agent Systems**, *Singh et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2512.14079)
424. **CASCADE: Cumulative Agentic Skill Creation through Autonomous Development and Evolution**, *Huang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2512.23880)
425. **See and Think: Embodied Agent in Virtual Environment**, *Zhao et al.*, ECCV 2024. [Paper](https://doi.org/10.1007/978-3-031-73242-3_11)
426. **Large Language Models as Tool Makers**, *Cai et al.*, ICLR 2024. [Paper](https://openreview.net/forum?id=qV83K9d5WB)
427. **Embodied LLM Agents Learn to Cooperate in Organized Teams**, *Guo et al.*, arXiv 2024. [Paper](https://doi.org/10.48550/arXiv.2403.12482)
428. **Tree of Thoughts: Deliberate Problem Solving with Large Language Models**, *Yao et al.*, NeurIPS 2023. [Paper](http://papers.nips.cc/paper_files/paper/2023/hash/271db9922b8d1f4dd7aaef84ed5ac703-Abstract-Conference.html)
429. **ReWOO: Decoupling Reasoning from Observations for Efficient Augmented Language Models**, *Xu et al.*, arXiv 2023. [Paper](https://arxiv.org/abs/2305.18323)
430. **LLM+P: Empowering Large Language Models with Optimal Planning Proficiency**, *Liu et al.*, arXiv 2023. [Paper](https://doi.org/10.48550/arXiv.2304.11477)
431. **AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation Framework**, *Wu et al.*, arXiv 2023. [Paper](https://doi.org/10.48550/arXiv.2308.08155)
432. **The openhands software agent sdk: A composable and extensible foundation for production agents**, *Wang et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2511.03690)
433. **Cognitive Kernel-Pro: A Framework for Deep Research Agents and Agent Foundation Models Training**, *Fang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.00414)
434. **Agent-E: From Autonomous Web Navigation to Foundational Design Principles in Agentic Systems**, *Abuelsaad et al.*, arXiv 2024. [Paper](https://doi.org/10.48550/arXiv.2407.13032)
435. **Tool-Planner: Task Planning with Clusters across Multiple Tools**, *Liu et al.*, ICLR 2025. [Paper](https://openreview.net/forum?id=dRz3cizftU)
436. **ToolChain: Efficient Action Space Navigation in Large Language Models with A Search**, *Zhuang et al.*, ICLR 2024. [Paper](https://openreview.net/forum?id=B6pQxqUcT8)
437. **OctoTools: An Agentic Framework with Extensible Tools for Complex Reasoning**, *Lu et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2502.11271)
438. **GPTSwarm: Language Agents as Optimizable Graphs**, *Zhuge et al.*, ICML 2024. [Paper](https://proceedings.mlr.press/v235/zhuge24a.html)
439. **BAGEL: Bootstrapping Agents by Guiding Exploration with Language**, *Murty et al.*, ICML 2024. [Paper](https://proceedings.mlr.press/v235/murty24a.html)
440. **OS-Genesis: Automating GUI Agent Trajectory Construction via Reverse Task Synthesis**, *Sun et al.*, ACL 2025. [Paper](https://aclanthology.org/2025.acl-long.277/)
441. **Insta: Towards internet-scale training for agents**, *Trabucco et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2502.06776)
442. **APIGen-MT: Agentic Pipeline for Multi-Turn Data Generation via Simulated Agent-Human Interplay**, *Prabhakar et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2504.03601)
443. **WebSailor: Navigating Super-human Reasoning for Web Agent**, *Li et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2507.02592)
444. **WebShaper: Agentically Data Synthesizing via Information-Seeking Formalization**, *Tao et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2507.15061)
445. **WebWatcher: Breaking New Frontier of Vision-Language Deep Research Agent**, *Geng et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.05748)
446. **Mobile-Agent-v3.5: Multi-platform Fundamental GUI Agents**, *Xu et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.16855)
447. **WebExplorer: Explore and Evolve for Training Long-Horizon Web Agents**, *Liu et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.06501)
448. **DeepDive: Advancing Deep Search Agents with Knowledge Graphs and Multi-Turn RL**, *Lu et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.10446)
449. **Scaling Synthetic Task Generation for Agents via Exploration**, *Ramrakhya et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.25047)
450. **Scaling Agents via Continual Pre-training**, *Su et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.13310)
451. **Explore to Evolve: Scaling Evolved Aggregation Logic via Proactive Online Exploration for Deep Research Agents**, *Wang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.14438)
452. **CRMWeaver: Building Powerful Business Agent via Agentic RL and Shared Memories**, *Lai et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.25333)
453. **WebLeaper: Empowering Efficiency and Efficacy in WebAgent via Enabling Info-Rich Seeking**, *Tao et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.24697)
454. **AgentEvolver: Towards Efficient Self-Evolving Agent System**, *Zhai et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2511.10395)
455. **VSearcher: Long-Horizon Multimodal Search Agent via Reinforcement Learning**, *Zhang et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2603.02795)
456. **OpenSeeker: Democratizing Frontier Search Agents by Fully Open-Sourcing Training Data**, *Du et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2603.15594)
457. **ToolCoder: Teach Code Generation Models to use API search tools**, *Zhang et al.*, arXiv 2023. [Paper](https://doi.org/10.48550/arXiv.2305.04032)
458. **ToolAlpaca: Generalized Tool Learning for Language Models with 3000 Simulated Cases**, *Tang et al.*, arXiv 2023. [Paper](https://doi.org/10.48550/arXiv.2306.05301)
459. **AgentTuning: Enabling Generalized Agent Abilities for LLMs**, *Zeng et al.*, Findings of ACL 2024. [Paper](https://doi.org/10.18653/v1/2024.findings-acl.181)
460. **Lingma SWE-GPT: An Open Development-Process-Centric Language Model for Automated Software Improvement**, *Ma et al.*, arXiv 2024. [Paper](https://doi.org/10.48550/arXiv.2411.00622)
461. **Aguvis: Unified Pure Vision Agents for Autonomous GUI Interaction**, *Xu et al.*, ICML 2025. [Paper](https://proceedings.mlr.press/v267/xu25ae.html)
462. **MaskSearch: A Universal Pre-Training Framework to Enhance Agentic Search Capability**, *Wu et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.20285)
463. **Tongyi DeepResearch Technical Report**, *Li et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.24701)
464. **AgentFold: Long-Horizon Web Agents with Proactive Context Management**, *Ye et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.24699)
465. **SIMA 2: A Generalist Embodied Agent for Virtual Worlds**, *SIMA Team et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2512.04797)
466. **O-Researcher: An Open Ended Deep Research Model via Multi-Agent Distillation and Agentic RL**, *Yao et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.03743)
467. **Scaling Behavior Cloning Improves Causal Reasoning: An Open Model for Real-Time Video Game Playing**, *Yue et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.04575)
468. **ToolACE-MCP: Generalizing History-Aware Routing from MCP Tools to the Agent Web**, *Yao et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.08276)
469. **ProAct: Agentic Lookahead in Interactive Environments**, *Yu et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.05327)
470. **OpenResearcher: A Fully Open Pipeline for Long-Horizon Deep Research Trajectory Synthesis**, *Li et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2603.20278)
471. **HATS: Hardness-Aware Trajectory Synthesis for GUI Agents**, *Shao et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2603.12138)
472. **Trial and Error: Exploration-Based Trajectory Optimization for LLM Agents**, *Song et al.*, arXiv 2024. [Paper](https://doi.org/10.48550/arXiv.2403.02502)
473. **Agent-FLAN: Designing Data and Methods of Effective Agent Tuning for Large Language Models**, *Chen et al.*, Findings of ACL 2024. [Paper](https://doi.org/10.18653/v1/2024.findings-acl.557)
474. **UI-TARS: Pioneering Automated GUI Interaction with Native Agents**, *Qin et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2501.12326)
475. **Multi-Turn Code Generation Through Single-Step Rewards**, *Jain et al.*, ICML 2025. [Paper](https://proceedings.mlr.press/v267/jain25a.html)
476. **SimpleDeepSearcher: Deep Information Seeking via Web-Powered Reasoning Trajectory Synthesis**, *Sun et al.*, Findings of EMNLP 2025. [Paper](https://aclanthology.org/2025.findings-emnlp.739/)
477. **EvolveSearch: An Iterative Self-Evolving Search Agent**, *Zhang et al.*, EMNLP 2025. [Paper](https://doi.org/10.18653/v1/2025.emnlp-main.663)
478. **GUI-Reflection: Empowering Multimodal GUI Models with Self-Reflection Behavior**, *Wu et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2506.08012)
479. **Agent-RewardBench: Towards a Unified Benchmark for Reward Modeling across Perception, Planning, and Safety in Real-World Multimodal Agents**, *Men et al.*, ACL 2025. [Paper](https://arxiv.org/abs/2506.21252)
480. **WebSynthesis: World-Model-Guided MCTS for Efficient WebUI-Trajectory Synthesis**, *Gao et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2507.04370)
481. **Think in Games: Learning to Reason in Games via Reinforcement Learning with Large Language Models**, *Liao et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.21365)
482. **ToolRM: Outcome Reward Models for Tool-Calling Large Language Models**, *Agarwal et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.11963)
483. **Advancing Tool-Augmented Large Language Models via Meta-Verification and Reflection Learning**, *Ma et al.*, ACM 2025. [Paper](https://doi.org/10.1145/3711896.3736835)
484. **AgentFrontier: Expanding the Capability Frontier of LLM Agents with ZPD-Guided Data Synthesis**, *Chen et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.24695)
485. **Scalable Data Synthesis for Computer Use Agents with Step-Level Filtering**, *He et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2512.10962)
486. **Adapting Web Agents with Synthetic Supervision**, *Wang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2511.06101)
487. **SERA: Soft-Verified Efficient Repository Agents**, *Shen et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.20789)
488. **TopoCurate:Modeling Interaction Topology for Tool-Use Agent Training**, *Yang et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2603.01714)
489. **MagicAgent: Towards Generalized Agent Planning**, *Ren et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.19000)
490. **WebDancer: Towards Autonomous Information Seeking Agency**, *Wu et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.22648)
491. **WebWeaver: Structuring Web-Scale Evidence with Dynamic Outlines for Open-Ended Deep Research**, *Li et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.13312)
492. **WebResearcher: Unleashing unbounded reasoning capability in Long-Horizon Agents**, *Qiao et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.13309)
493. **UI-Venus-1.5 Technical Report**, *Gao et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.09082)
494. **UI-TARS-2 Technical Report: Advancing GUI Agent with Multi-Turn Reinforcement Learning**, *Seed et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.02544)
495. **DeepRetrieval: Hacking Real Search Engines and Retrievers with Large Language Models via Reinforcement Learning**, *Jiang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2503.00223)
496. **ReSearch: Learning to Reason with Search for LLMs via Reinforcement Learning**, *Chen et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2503.19470)
497. **Search and Refine During Think: Autonomous Retrieval-Augmented Reasoning of LLMs**, *Shi et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.11277)
498. **SEEA-R1: Tree-Structured Reinforcement Fine-Tuning for Self-Evolving Embodied Agents**, *Tian et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2506.21669)
499. **Seeing, Listening, Remembering, and Reasoning: A Multimodal Agent with Long-Term Memory**, *Long et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.09736)
500. **Video-Thinker: Sparking "Thinking with Videos" via Reinforcement Learning**, *Wang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.23473)
501. **R1-Searcher: Incentivizing the Search Capability in LLMs via Reinforcement Learning**, *Song et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2503.05592)
502. **OTC: Optimal Tool Calls via Reinforcement Learning**, *Wang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2504.14870)
503. **Nemotron-Research-Tool-N1: Exploring Tool-Using Language Models with Reinforced Reasoning**, *Zhang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.00024)
504. **Agentic Reasoning and Tool Integration for LLMs via Reinforcement Learning**, *Singh et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.01441)
505. **VLA-RL: Towards Masterful and General Robotic Manipulation with Scalable Reinforcement Learning**, *Lu et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.18719)
506. **VRAG-RL: Empower Vision-Perception-Based RAG for Visually Rich Information Understanding via Iterative Reasoning with Reinforcement Learning**, *Wang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.22019)
507. **R-Search: Empowering LLM Reasoning with Search via Multi-Reward Reinforcement Learning**, *Zhao et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2506.04185)
508. **Video-MTR: Reinforced Multi-Turn Reasoning for Long Video Understanding**, *Xie et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.20478)
509. **Agent-R1: Training Powerful LLM Agents with End-to-End Reinforcement Learning**, *Cheng et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2511.14460)
510. **ToolOrchestra: Elevating Intelligence via Efficient Model and Tool Orchestration**, *Su et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2511.21689)
511. **VideoMem: Enhancing Ultra-Long Video Understanding via Adaptive Memory Management**, *Jin et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2512.04540)
512. **GDPO: Group reward-Decoupled Normalization Policy Optimization for Multi-reward RL Optimization**, *Liu et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.05242)
513. **FlowSteer: Interactive Agentic Workflow Orchestration via End-to-End Reinforcement Learning**, *Zhang et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.01664)
514. **IntentRL: Training Proactive User-intent Agents for Open-ended Deep Research via Reinforcement Learning**, *Luo et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2602.03468)
515. **Who Deserves the Reward? SHARP: Shapley Credit-based Optimization for Multi-Agent System**, *Li et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.08335)
516. **RAGEN: Understanding Self-Evolution in LLM Agents via Multi-Turn Reinforcement Learning**, *Wang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2504.20073)
517. **ZeroSearch: Incentivize the Search Capability of LLMs without Searching**, *Sun et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.04588)
518. **WebAgent-R1: Training Web Agents via End-to-End Multi-Turn Reinforcement Learning**, *Wei et al.*, EMNLP 2025. [Paper](https://doi.org/10.18653/v1/2025.emnlp-main.401)
519. **Unleashing Embodied Task Planning Ability in LLMs via Reinforcement Learning**, *Fei et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2506.23127)
520. **SPIRAL: Self-Play on Zero-Sum Games Incentivizes Reasoning via Multi-Agent Multi-Turn Reinforcement Learning**, *Liu et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2506.24119)
521. **Mobilegui-rl: Advancing mobile gui agent through reinforcement learning in online environment**, *Shi et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2507.05720)
522. **Thinking With Videos: Multimodal Tool-Augmented Reinforcement Learning for Long Video Reasoning**, *Zhang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.04416)
523. **ComputerRL: Scaling End-to-End Online Reinforcement Learning for Computer Use Agents**, *Lai et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.14040)
524. **Bootstrapping Task Spaces for Self-Improvement**, *Jiang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.04575)
525. **AgentGym-RL: Training LLM Agents for Long-Horizon Decision Making through Multi-Turn Reinforcement Learning**, *Xi et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.08755)
526. **UI-S1: Advancing GUI Automation via Semi-online Reinforcement Learning**, *Lu et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.11543)
527. **Learn the Ropes, Then Trust the Wins: Self-imitation with Progressive Exploration for Agentic Reinforcement Learning**, *Qin et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.22601)
528. **AgentRL: Scaling Agentic Reinforcement Learning with a Multi-Turn, Multi-Task Framework**, *Zhang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.04206)
529. **Stronger-MAS: Multi-Agent Reinforcement Learning for Collaborative LLMs**, *Zhao et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2510.11062)
530. **VAGEN: Reinforcing World Model Reasoning for Multi-Turn VLM Agents**, *Wang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.16907)
531. **GTR-Turbo: Merged Checkpoint is Secretly a Free Teacher for Agentic VLM Training**, *Wei et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2512.13043)
532. **SeeUPO: Sequence-Level Agentic-RL with Convergence Guarantees**, *Hu et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.06554)
533. **Hierarchy-of-Groups Policy Optimization for Long-Horizon Agentic Tasks**, *He et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.22817)
534. **DeepSWE: Training a Fully Open-sourced, State-of-the-Art Coding Agent by Scaling RL**, *Luo et al.*, Together AI Blog 2025. [Paper](https://www.together.ai/blog/deepswe)
535. **RLVE: Scaling Up Reinforcement Learning for Language Models with Adaptive Verifiable Environments**, *Zeng et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2511.07317)
536. **Do As I Can, Not As I Say: Grounding Language in Robotic Affordances**, *Ichter et al.*, CoRL 2022. [Paper](https://proceedings.mlr.press/v205/ichter23a.html)
537. **ReTool: Reinforcement Learning for Strategic Tool Use in LLMs**, *Feng et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2504.11536)
538. **GUI-R1 : A Generalist R1-Style Vision-Language Action Model For GUI Agents**, *Luo et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2504.10458)
539. **ARLArena: A Unified Framework for Stable Agentic Reinforcement Learning**, *Wang et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2602.21534)
540. **CM2: Reinforcement Learning with Checklist Rewards for Multi-Turn and Multi-Step Agentic Tool Use**, *Zhang et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2602.12268)
541. **SimpleTIR: End-to-End Reinforcement Learning for Multi-Turn Tool-Integrated Reasoning**, *Xue et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.02479)
542. **WebRL: Training LLM Web Agents via Self-Evolving Online Curriculum Reinforcement Learning**, *Qi et al.*, ICLR 2025. [Paper](https://openreview.net/forum?id=oVKEAFjEqv)
543. **WebArbiter: A Principle-Guided Reasoning Process Reward Model for Web Agents**, *Zhang et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.21872)
544. **Exploring Reasoning Reward Model for Agents**, *Fan et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2601.22154)
545. **ZeroGUI: Automating Online GUI Learning at Zero Human Cost**, *Yang et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.23762)
546. **DistRL: An Asynchronous Distributed Reinforcement Learning Framework for On-Device Control Agent**, *Wang et al.*, ICLR 2025. [Paper](https://openreview.net/forum?id=LPG8pPSfQD)
547. **DigiRL: Training In-The-Wild Device-Control Agents with Autonomous Reinforcement Learning**, *Bai et al.*, NeurIPS 2024. [Paper](http://papers.nips.cc/paper_files/paper/2024/hash/1704ddd0bb89f159dfe609b32c889995-Abstract-Conference.html)
548. **Agentic Entropy-Balanced Policy Optimization**, *Dong et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.14545)
549. **Learning Efficient Communication Protocols for Multi-Agent Reinforcement Learning**, *Zhang et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2511.09171)
550. **Absolute zero: Reinforced self-play reasoning with zero data**, *Zhao et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2505.03335)
551. **Self-Challenging Language Model Agents**, *Zhou et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2506.01716)
552. **Vision-zero: Scalable vlm self-improvement via strategic gamified self-play**, *Wang et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2509.25541)
553. **Toward Training Superintelligent Software Agents through Self-Play SWE-RL**, *Wei et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2512.18552)
554. **Active Zero: Self-Evolving Vision-Language Models through Active Environment Exploration**, *He et al.*, arXiv 2026. [Paper](https://doi.org/10.48550/arXiv.2602.11241)
555. **Llms as scalable, general-purpose simulators for evolving digital agent training**, *Wang et al.*, arXiv 2025. [Paper](https://arxiv.org/abs/2510.14969)
556. **World-Model-Augmented Web Agents with Action Correction**, *Shen et al.*, arXiv 2026. [Paper](https://arxiv.org/abs/2602.15384)
557. **Paired Open-Ended Trailblazer (POET): Endlessly Generating Increasingly Complex and Diverse Learning Environments and Their Solutions**, *Wang et al.*, arXiv 2019. [Paper](http://arxiv.org/abs/1901.01753)
558. **Emergent Complexity and Zero-shot Transfer via Unsupervised Environment Design**, *Dennis et al.*, arXiv 2020. [Paper](https://arxiv.org/abs/2012.02096)
559. **Replay-Guided Adversarial Environment Design**, *Jiang et al.*, NeurIPS 2021. [Paper](https://proceedings.neurips.cc/paper/2021/hash/0e915db6326b6fb6a3c56546980a8c93-Abstract.html)
560. **Evolving Curricula with Regret-Based Environment Design**, *Parker-Holder et al.*, ICML 2022. [Paper](https://proceedings.mlr.press/v162/parker-holder22a.html)
561. **MAESTRO: Open-Ended Environment Design for Multi-Agent Reinforcement Learning**, *Samvelyan et al.*, ICLR 2023. [Paper](https://openreview.net/forum?id=sKWlRDzPfd7)
562. **Refining Minimax Regret for Unsupervised Environment Design**, *Beukman et al.*, ICML 2024. [Paper](https://proceedings.mlr.press/v235/beukman24a.html)
563. **DataEnvGym: Data Generation Agents in Teacher Environments with Student Feedback**, *Khan et al.*, ICLR 2025. [Paper](https://openreview.net/forum?id=00SnKBGTsz)
564. **Eurekaverse: Environment curriculum generation via large language models**, *Liang et al.*, arXiv 2024. [Paper](https://arxiv.org/abs/2411.01775)
565. **Don't Just Fine-tune the Agent, Tune the Environment**, *Lu et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2510.10197)
566. **Self-Evolving Curriculum for LLM Reasoning**, *Chen et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2505.14970)
567. **Reasoning Core: A Scalable RL Environment for LLM Symbolic Reasoning**, *Lacombe et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.18083)
568. **CuES: A Curiosity-driven and Environment-grounded Synthesis Framework for Agentic RL**, *Mai et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2512.01311)
569. **GenEnv: Difficulty-Aligned Co-Evolution Between LLM Agents and Environment Simulators**, *Guo et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2512.19682)
570. **Feedback-Driven Tool-Use Improvements in Large Language Models via Automated Build Environments**, *Ye et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2508.08791)
571. **ARE: Scaling Up Agent Environments and Evaluations**, *Andrews et al.*, arXiv 2025. [Paper](https://doi.org/10.48550/arXiv.2509.17158)
572. **On-Policy Distillation**, *Lu et al.*, Thinking Machines Lab: Connectionism 2025. [Paper](https://doi.org/10.64434/tml.20251026)
573. **Room-Across-Room: Multilingual Vision-and-Language Navigation with Dense Spatiotemporal Grounding**, *Ku et al.*, EMNLP 2020. [Paper](https://doi.org/10.18653/v1/2020.emnlp-main.356)
574. **Beyond the Nav-Graph: Vision-and-Language Navigation in Continuous Environments**, *Krantz et al.*, ECCV 2020. [Paper](https://doi.org/10.1007/978-3-030-58604-1_7)
575. **Avalon's Game of Thoughts: Battle Against Deception through Recursive Contemplation**, *Wang et al.*, arXiv 2023. [Paper](https://arxiv.org/abs/2310.01320)
576. **Collab-Overcooked: Benchmarking and Evaluating Large Language Models as Collaborative Agents**, *Sun et al.*, EMNLP 2025. [Paper](http://dx.doi.org/10.18653/v1/2025.emnlp-main.249)
577. **StableToolBench: Towards Stable Large-Scale Benchmarking on Tool Learning of Large Language Models**, *Guo et al.*, Findings of ACL 2024. [Paper](https://doi.org/10.18653/v1/2024.findings-acl.664)
578. **ToolTalk: Evaluating Tool-Usage in a Conversational Setting**, *Farn et al.*, arXiv 2023. [Paper](https://doi.org/10.48550/arXiv.2311.10775)
579. **MINT: Evaluating LLMs in Multi-turn Interaction with Tools and Language Feedback**, *Wang et al.*, ICLR 2024. [Paper](https://openreview.net/forum?id=jp3gWrMuIZ)
580. **CAMEL: Communicative Agents for "Mind" Exploration of Large Language Model Society**, *Li et al.*, NeurIPS 2023. [Paper](http://papers.nips.cc/paper_files/paper/2023/hash/a3621ee907def47c1b952ade25c67698-Abstract-Conference.html)
581. **TextGrad: Automatic "Differentiation" via Text**, *Yuksekgonul et al.*, arXiv 2024. [Paper](https://doi.org/10.48550/arXiv.2406.07496)
582. **DSPy: Compiling Declarative Language Model Calls into State-of-the-Art Pipelines**, *Khattab et al.*, ICLR 2024. [Paper](https://openreview.net/forum?id=sY5N0zY5Od)
