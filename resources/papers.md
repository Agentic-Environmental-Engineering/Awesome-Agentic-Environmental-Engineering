# Curated Papers and Resources

This list follows the taxonomy of **Agentic Environment Engineering for Large Language Models**. It is intentionally curated: each section highlights representative environments, benchmarks, synthesis methods, or evolution methods rather than dumping the full bibliography.

## Environment Domains

### GUI Environments

| Work | Year | Focus |
| --- | --- | --- |
| [WebShop](http://papers.nips.cc/paper_files/paper/2022/hash/82ad13ec01f9fe44c01cb91814fd7b8c-Abstract-Conference.html) | 2022 | Scalable web interaction with grounded language agents |
| [WebArena](https://openreview.net/forum?id=oKn9c6ytLx) | 2024 | Realistic web environments for autonomous agents |
| [VisualWebArena](https://doi.org/10.18653/v1/2024.acl-long.50) | 2024 | Multimodal web agent evaluation |
| [WebVoyager](https://doi.org/10.18653/v1/2024.acl-long.371) | 2024 | End-to-end web agents with large multimodal models |
| [WorkArena](https://proceedings.mlr.press/v235/drouin24a.html) | 2024 | Knowledge work tasks for web agents |
| [OSWorld](http://papers.nips.cc/paper_files/paper/2024/hash/5d413e48f84dc61244b6be550f1cd8f5-Abstract-Datasets_and_Benchmarks_Track.html) | 2024 | Open-ended computer-use tasks in real operating systems |
| [AndroidWorld](https://openreview.net/forum?id=il5yUQsrjC) | 2025 | Dynamic benchmarking for mobile device control |

### Deep Research Environments

| Work | Year | Focus |
| --- | --- | --- |
| [GAIA](https://openreview.net/forum?id=fibxvahvs3) | 2024 | General AI assistant benchmark |
| [SimpleQA](https://arxiv.org/abs/2411.04368) | 2024 | Short-form factuality evaluation |
| [BrowseComp](https://doi.org/10.48550/arXiv.2504.12516) | 2025 | Browsing agents on difficult information-seeking tasks |
| [DeepResearch Bench](https://doi.org/10.48550/arXiv.2506.11763) | 2025 | Deep research agent evaluation |
| [WideSearch](https://doi.org/10.48550/arXiv.2508.07999) | 2025 | Broad agentic information seeking |
| [WebWalker](https://aclanthology.org/2025.acl-long.508/) | 2025 | Web traversal benchmark for LLMs |

### Embodied Environments

| Work | Year | Focus |
| --- | --- | --- |
| [ALFRED](https://openaccess.thecvf.com/content_CVPR_2020/html/Shridhar_ALFRED_A_Benchmark_for_Interpreting_Grounded_Instructions_for_Everyday_Tasks_CVPR_2020_paper.html) | 2020 | Grounded instruction following in household tasks |
| [ALFWorld](https://openreview.net/forum?id=0IOX0YcCdTn) | 2021 | Text and embodied environment alignment |
| [ScienceWorld](https://doi.org/10.18653/v1/2022.emnlp-main.775) | 2022 | Text-based science environments |
| [MineDojo](http://papers.nips.cc/paper_files/paper/2022/hash/74a67268c5cc5910f64938cac4526a90-Abstract-Datasets_and_Benchmarks.html) | 2022 | Open-ended Minecraft agent learning |
| [LEGENT](https://doi.org/10.18653/v1/2024.acl-demos.32) | 2024 | Open platform for embodied agents |
| [DiscoveryWorld](http://papers.nips.cc/paper_files/paper/2024/hash/13836f251823945316ae067350a5c366-Abstract-Datasets_and_Benchmarks_Track.html) | 2024 | Automated scientific discovery in a virtual world |
| [RoboFactory](https://doi.org/10.48550/arXiv.2503.16408) | 2025 | Embodied multi-agent collaboration |

### Game Environments

| Work | Year | Focus |
| --- | --- | --- |
| [Baba Is AI](https://arxiv.org/abs/2407.13729) | 2025 | Rule-based puzzle reasoning for LLM agents |
| [GameArena](https://arxiv.org/abs/2412.06394) | 2025 | Game-based agent evaluation |
| [BALROG](https://arxiv.org/abs/2411.13543) | 2024 | Long-horizon interactive game tasks |
| [GameBench](https://arxiv.org/abs/2406.06613) | 2024 | Broad game-oriented agent evaluation |
| [AI GameStore](https://arxiv.org/abs/2602.17594) | 2026 | Environment collection for game agents |

### Tool Environments

| Work | Year | Focus |
| --- | --- | --- |
| [API-Bank](https://doi.org/10.18653/v1/2023.emnlp-main.187) | 2023 | Tool-augmented LLM benchmark |
| [ToolBench / ToolLLM](https://openreview.net/forum?id=dHng2O0Jjr) | 2024 | Large-scale real-world API use |
| [Toolformer](https://proceedings.neurips.cc/paper_files/paper/2023/hash/d842425e4bf79ba039352da0f658a906-Abstract-Conference.html) | 2023 | Self-supervised tool use |
| [ToolACE](https://openreview.net/forum?id=8EB8k6DdCU) | 2025 | Tool learning and tool-use evaluation |
| [tau-bench](https://arxiv.org/abs/2406.12045) | 2024 | Tool-agent-user interaction benchmark |
| [MCPVerse](https://doi.org/10.48550/arXiv.2508.16260) | 2025 | Real-world MCP tool-use benchmark |

### Code Environments

| Work | Year | Focus |
| --- | --- | --- |
| [MBPP](https://arxiv.org/abs/2108.07732) | 2021 | Basic Python programming problems |
| [SWE-bench](https://openreview.net/forum?id=VTF8yNQM66) | 2024 | Real GitHub issue resolution |
| [LiveCodeBench](https://arxiv.org/abs/2403.07974) | 2024 | Contamination-aware code benchmark |
| [Terminal-Bench](https://doi.org/10.48550/arXiv.2601.11868) | 2026 | Terminal-based agent tasks |
| [KernelBench](https://arxiv.org/abs/2502.10517) | 2025 | Kernel generation and optimization |
| [MLE-bench](https://openreview.net/forum?id=6s5uXNWGIh) | 2025 | Machine learning engineering agents |

### Domain-Specific Environments

| Work | Year | Focus |
| --- | --- | --- |
| [MedAgentBench](https://doi.org/10.48550/arXiv.2501.14654) | 2025 | Medical application agents |
| [ScienceAgentBench](https://openreview.net/forum?id=6z4YKr0GK6) | 2025 | Data-driven scientific discovery agents |
| [DSBench](https://openreview.net/forum?id=DSsSPr0RZJ) | 2025 | Data science agents |
| [StockBench](https://doi.org/10.48550/arXiv.2510.02209) | 2025 | Stock trading agents |
| [FinDeepResearch](https://doi.org/10.48550/arXiv.2510.13936) | 2025 | Financial deep research agents |

### Cross-Domain Environments

| Work | Year | Focus |
| --- | --- | --- |
| [OpenAI Gym](https://arxiv.org/abs/1606.01540) | 2016 | General RL environment interface |
| [AgentBench](https://openreview.net/forum?id=zAdUB0aCTQ) | 2024 | Multi-domain LLM agent evaluation |
| [GEM](https://doi.org/10.48550/arXiv.2510.01051) | 2025 | Gym for agentic LLMs |
| [VitaBench](https://doi.org/10.48550/arXiv.2509.26490) | 2025 | Versatile real-world interactive tasks |
| [DAComp](https://arxiv.org/abs/2512.04324) | 2025 | Data agents across the full data intelligence lifecycle |

## Environment Synthesis and Evaluation

### Symbolic Synthesis

| Work | Year | Focus |
| --- | --- | --- |
| [AgentGen](https://doi.org/10.48550/arXiv.2408.00764) | 2024 | Environment and task generation for planning agents |
| [DreamGym](https://doi.org/10.48550/arXiv.2511.03773) | 2025 | Experience synthesis for scalable agent learning |
| [SCALER](https://doi.org/10.48550/arXiv.2601.04809) | 2026 | Adaptive synthetic learning environments |
| AutoEnv | 2026 | Automated environment construction |
| Scale-SWE | 2026 | Synthetic code environments for software agents |

### Neural Synthesis and World Models

| Work | Year | Focus |
| --- | --- | --- |
| I-JEPA | 2023 | Predictive representation learning |
| RWM | 2023 | Real-world model learning |
| DINO-WM | 2025 | Vision world model learning |
| [WorldGPT](https://doi.org/10.1145/3664647.3681488) | 2024 | Language-based world modeling |
| Agent World Model | 2026 | Infinite synthetic environments for agentic RL |

### Quality Control and Evaluation

| Dimension | Representative concerns |
| --- | --- |
| Correctness | Verifiable rewards, executable checks, consistency of feedback |
| Diversity | Coverage of tasks, domains, trajectories, states, and agent behaviors |
| Complexity | Difficulty calibration, long-horizon structure, compositional tasks |
| Fidelity | Real-world grounding, simulator realism, user and tool behavior fidelity |

Representative works include AgentsCourt, MMR-V, MMR-Life, DAComp, and environment-specific verifiers used in tool, code, and GUI benchmarks.

## Agent and Environment Evolution

### Agent Evolution

| Direction | Representative mechanisms |
| --- | --- |
| Memory-centric experience evolution | Trajectory memory, abstract scripts, reusable skills |
| Orchestration-centric workflow evolution | Fixed workflows, automated workflows, evolving workflows |
| Trajectory-centric offline evolution | Task synthesis, trajectory synthesis, trajectory refinement |
| Exploration-centric online evolution | Reward design, reasoning structure design, RL optimization |

Representative works include ReAct, Self-Refine, TravelPlanner, ToolRL, WebWorld, DreamGym, and SWE-RL.

### Environment Evolution

| Direction | Representative mechanisms |
| --- | --- |
| Neural-driven evolution | Self-play, learned world models, adaptive dynamics |
| Difficulty-driven evolution | Explicit curriculum signals and implicit curriculum mechanisms |
| Scaling-driven evolution | Scenario-level scaling and environment-level scaling |

## Future Directions

| Direction | Open questions |
| --- | --- |
| Environment-as-a-Service | How should environments be deployed, versioned, and standardized? |
| Multi-agent environments | How should environments model roles, institutions, collaboration, and competition? |
| Neural-symbolic environments | How can symbolic reliability and neural scalability be combined? |
| Sim-to-real alignment | How can synthetic dynamics transfer to real-world agent behavior? |
| Science of environment engineering | Are there scaling laws connecting environment properties and agent capabilities? |

## Contributing

To add a paper or benchmark, please open a pull request and follow [CONTRIBUTING.md](../CONTRIBUTING.md).
