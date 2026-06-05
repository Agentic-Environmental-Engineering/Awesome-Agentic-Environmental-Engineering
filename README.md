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
  <a href="#references">References</a> |
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

## References

<details>
<summary>Show all cited works (582)</summary>

1. Qwen3 Technical Report
2. DeepSeek-R1: Incentivizing Reasoning Capability in LLMs via Reinforcement Learning
3. GEM: A Gym for Agentic LLMs
4. Humanity's Last Code Exam: Can Advanced LLMs Conquer Human's Hardest Code Competition?
5. Introducing GPT-5.4
6. Gemini 3.1 Pro
7. Kimi K2.5: Visual Agentic Intelligence
8. ToolRL: Reward is All Tool Learning Needs
9. TravelPlanner: A Benchmark for Real-World Planning with Language Agents
10. Self-Refine: Iterative Refinement with Self-Feedback
11. Agent world model: Infinity synthetic environments for agentic reinforcement learning
12. Rwku: Benchmarking real-world knowledge unlearning for large language models
13. A Troublemaker with Contagious Jailbreak Makes Chaos in Honest Towns
14. DAComp: Benchmarking Data Agents across the Full Data Intelligence Lifecycle
15. WebShop: Towards Scalable Real-World Web Interaction with Grounded Language Agents
16. SWE-bench: Can Language Models Resolve Real-world Github Issues?
17. ReAct: Synergizing Reasoning and Acting in Language Models
18. Fixing the Broken Compass: Diagnosing and Improving Inference-Time Reward Modeling
19. Omni-Reward: Towards Generalist Omni-Modal Reward Modeling with Free-Form Preferences
20. DeepSeekMath: Pushing the Limits of Mathematical Reasoning in Open Language Models
21. DAPO: An Open-Source LLM Reinforcement Learning System at Scale
22. Reinforced internal-external knowledge synergistic reasoning for efficient adaptive search agent
23. Towards agentic self-learning llms in search environment
24. Agentic Reasoning for Large Language Models
25. Large language models for planning: A comprehensive and systematic survey
26. A survey of recent advances in commonsense knowledge acquisition: Methods and resources
27. WorkArena: How Capable are Web Agents at Solving Common Knowledge Work Tasks?
28. OSWorld: Benchmarking Multimodal Agents for Open-Ended Tasks in Real Computer Environments
29. Measuring short-form factuality in large language models
30. GAIA: a benchmark for General AI Assistants
31. BrowseComp: A Simple Yet Challenging Benchmark for Browsing Agents
32. ALFRED: A Benchmark for Interpreting Grounded Instructions for Everyday Tasks
33. ALFWorld: Aligning Text and Embodied Environments for Interactive Learning
34. ScienceWorld: Is your Agent Smarter than a 5th Grader?
35. GameArena: Evaluating LLM Reasoning through Live Computer Games
36. Baba Is AI: Break the Rules to Beat the Benchmark
37. GameBench: Evaluating Strategic Reasoning Abilities of LLM Agents
38. ToolLLM: Facilitating Large Language Models to Master 16000+ Real-world APIs
39. tau-bench: A Benchmark for Tool-Agent-User Interaction in Real-World Domains
40. API-Bank: A Comprehensive Benchmark for Tool-Augmented LLMs
41. Program synthesis with large language models
42. Terminal-Bench: Benchmarking Agents on Hard, Realistic Tasks in Command Line Interfaces
43. Kernelbench: Can llms write efficient gpu kernels?
44. MedAgentBench: Dataset for Benchmarking LLMs as Agents in Medical Applications
45. ScienceAgentBench: Toward Rigorous Assessment of Language Agents for Data-Driven Scientific Discovery
46. DSBench: How Far Are Data Science Agents from Becoming Data Science Experts?
47. Openai gym
48. AgentBench: Evaluating LLMs as Agents
49. Agentscourt: Building judicial decision-making agents with court debate simulation and legal knowledge augmentation
50. MMR-V: What's Left Unsaid? A Benchmark for Multimodal Deep Reasoning in Videos
51. MMR-Life: Piecing Together Real-life Scenes for Multimodal Multi-image Reasoning
52. MLE-bench: Evaluating Machine Learning Agents on Machine Learning Engineering
53. ToolACE: Winning the Points of LLM Function Calling
54. Toolformer: Language Models Can Teach Themselves to Use Tools
55. Livecodebench: Holistic and contamination free evaluation of large language models for code
56. WebArena: A Realistic Web Environment for Building Autonomous Agents
57. WebVoyager: Building an End-to-End Web Agent with Large Multimodal Models
58. LLMArena: Assessing Capabilities of Large Language Models in Dynamic Multi-Agent Environments
59. Large language models can self-improve at web agent tasks
60. Group-in-Group Policy Optimization for LLM Agent Training
61. Agentic Reinforced Policy Optimization
62. Search-R1: Training LLMs to Reason and Leverage Search Engines with Reinforcement Learning
63. Proximal Policy Optimization Algorithms
64. AgentGen: Enhancing Planning Abilities for Large Language Model based Agent via Environment and Task Generation
65. Scaling Agent Learning via Experience Synthesis
66. SCALER:Synthetic Scalable Adaptive Learning Environment for Reasoning
67. Training Verifiers to Solve Math Word Problems
68. Measuring Massive Multitask Language Understanding
69. MMMU: A Massive Multi-discipline Multimodal Understanding and Reasoning Benchmark for Expert AGI
70. Rag-rewardbench: Benchmarking reward models in retrieval augmented generation for preference alignment
71. IDE-Bench: Evaluating Large Language Models as IDE Agents on Real-World Software Engineering Tasks
72. WideSearch: Benchmarking Agentic Broad Info-Seeking
73. RoboFactory: Exploring Embodied Agent Collaboration with Compositional Constraints
74. Unlocking the future: Exploring look-ahead planning mechanistic interpretability in large language models
75. MCPVerse: An Expansive, Real-World Benchmark for Agentic Tool Use
76. AutoFlow: Automated Workflow Generation for Large Language Model Agents
77. Learning on the Job: An Experience-Driven Self-Evolving Agent for Long-Horizon Tasks
78. In-the-Flow Agentic System Optimization for Effective Planning and Tool Use
79. Adaptation of agentic ai
80. A Comprehensive Survey on Reinforcement Learning-based Agentic Search: Foundations, Roles, Optimizations, Evaluations, and Applications
81. A Comprehensive Survey of Self-Evolving AI Agents: A New Paradigm Bridging Foundation Models and Lifelong Agentic Systems
82. The Landscape of Agentic Reinforcement Learning for LLMs: A Survey
83. Toward Efficient Agents: Memory, Tool learning, and Planning
84. A Survey of Self-Evolving Agents: What, When, How, and Where to Evolve on the Path to Artificial Super Intelligence
85. EnvScaler: Scaling Tool-Interactive Environments for LLM Agent via Programmatic Synthesis
86. AutoEnv: Automated Environments for Measuring Cross-Environment Agent Learning
87. Is Your LLM Secretly a World Model of the Internet? Model-Based Planning for Web Agents
88. Dreamgen: Unlocking generalization in robot learning through video world models
89. WebEvolver: Enhancing Web Agent Self-Improvement with Co-evolving World Model
90. TaskLAMA: Probing the Complex Task Understanding of Language Models
91. HuggingGPT: Solving AI Tasks with ChatGPT and its Friends in Hugging Face
92. TaskBench: Benchmarking Large Language Models for Task Automation
93. Mobile-bench: An evaluation benchmark for llm-based mobile agents
94. WebWalker: Benchmarking LLMs in Web Traversal
95. EmbodiedBench: Comprehensive Benchmarking Multi-modal Large Language Models for Vision-Driven Embodied Agents
96. Mind2Web: Towards a Generalist Agent for the Web
97. On the Effects of Data Scale on UI Control Agents
98. KOR-Bench: Benchmarking Language Models on Knowledge-Orthogonal Reasoning Tasks
99. GVGAI-LLM: Evaluating Large Language Model Agents with Infinite Games
100. V-GameGym: Visual Game Generation for Code Large Language Models
101. GameTraversalBenchmark: Evaluating Planning Abilities Of Large Language Models Through Traversing 2D Game Maps
102. Vsp: Assessing the dual challenges of perception and reasoning in spatial planning tasks for vlms
103. AppWorld: A Controllable World of Apps and People for Benchmarking Interactive Coding Agents
104. Scenario Dreamer: Vectorized Latent Diffusion for Generating Driving Simulation Environments
105. MetaDrive: Composing Diverse Driving Scenarios for Generalizable Reinforcement Learning
106. OSWorld-MCP: Benchmarking MCP Tool Invocation In Computer-Use Agents
107. VisualWebArena: Evaluating Multimodal Agents on Realistic Visual Web Tasks
108. AgentStudio: A Toolkit for Building General Virtual Agents
109. Generative agents: Interactive simulacra of human behavior
110. Collab-overcooked: Benchmarking and evaluating large language models as collaborative agents
111. AvalonBench: Evaluating LLMs Playing the Game of Avalon
112. Mind2Web 2: Evaluating Agentic Search with Agent-as-a-Judge
113. Mobile-env: Building qualified evaluation benchmarks for llm-gui interaction
114. Android in the Wild: A Large-Scale Dataset for Android Device Control
115. AndroidWorld: A Dynamic Benchmarking Environment for Autonomous Agents
116. MobileWorld: Benchmarking Autonomous Mobile Agents in Agent-User Interactive and MCP-Augmented Environments
117. Windows agent arena: Evaluating multi-modal os agents at scale
118. On the Multi-turn Instruction Following for Conversational Web Agents
119. VideoWebArena: Evaluating Long Context Multimodal Agents with Video Understanding Web Tasks
120. WebCanvas: Benchmarking Web Agents in Online Environments
121. An Illusion of Progress? Assessing the Current State of Web Agents
122. MobileAgentBench: An Efficient and User-Friendly Benchmark for Mobile LLM Agents
123. DeepResearch Bench: A Comprehensive Benchmark for Deep Research Agents
124. DRAGged into Conflicts: Detecting and Addressing Conflicting Sources in Search-Augmented LLMs
125. DeepResearchGym: A Free, Transparent, and Reproducible Evaluation Sandbox for Deep Research
126. InfoDeepSeek: Benchmarking Agentic Information Seeking for Retrieval-Augmented Generation
127. Open Data Synthesis For Deep Research
128. BrowseComp-ZH: Benchmarking Web Browsing Ability of Large Language Models in Chinese
129. SurveyGen: Quality-Aware Scientific Survey Generation with Large Language Models
130. ReportBench: Evaluating Deep Research Agents via Academic Survey Tasks
131. Characterizing Deep Research: A Benchmark and Formal Definition
132. OpenScholar: Synthesizing Scientific Literature with Retrieval-augmented LMs
133. ResearcherBench: Evaluating Deep AI Research Systems on the Frontiers of Scientific Inquiry
134. ProxyQA: An Alternative Framework for Evaluating Long-Form Text Generation with Large Language Models
135. AI Idea Bench 2025: AI Research Idea Generation Benchmark
136. DeepReview: Improving LLM-based Paper Review with Human-like Deep Thinking Process
137. PaperBench: Evaluating AI's Ability to Replicate AI Research
138. Multimodal DeepResearcher: Generating Text-Chart Interleaved Reports From Scratch with Agentic Framework
139. Vision-DeepResearch Benchmark: Rethinking Visual and Textual Search for Multimodal Large Language Models
140. MMDeepResearch-Bench: A Benchmark for Multimodal Deep Research Agents
141. OmniGAIA: Towards Native Omni-Modal AI Agents
142. Dr. Bench: A Multidimensional Evaluation for Deep Research Agents, from Answers to Reports
143. Habitat: A Platform for Embodied AI Research
144. Vision-and-Language Navigation: Interpreting Visually-Grounded Navigation Instructions in Real Environments
145. Rlbench: The robot learning benchmark & learning environment
146. Robocasa: Large-scale simulation of everyday tasks for generalist robots
147. BEHAVIOR: Benchmark for Everyday Household Activities in Virtual, Interactive, and Ecological Environments
148. panda-gym: Open-source goal-conditioned environments for robotic learning
149. ET-Plan-Bench: Embodied Task-level Planning Benchmark Towards Spatial-Temporal Cognition with Foundation Models
150. LEGENT: Open Platform for Embodied Agents
151. SimuHome: A Temporal-and Environment-Aware Benchmark for Smart Home LLM Agents
152. Sari Sandbox: A Virtual Retail Store Environment for Embodied AI Agents
153. Decoupled Diffusion Sparks Adaptive Scene Generation
154. MineDojo: Building Open-Ended Embodied Agents with Internet-Scale Knowledge
155. KORGym: A Dynamic Game Platform for LLM Reasoning Evaluation
156. TextArena
157. AI Gamestore: Scalable, Open-Ended Evaluation of Machine General Intelligence with Human Games
158. ING-VP: MLLMs cannot Play Easy Vision-based Games Yet
159. VideoGameBench: Can Vision-Language Models complete popular video games?
160. BALROG: Benchmarking Agentic LLM and VLM Reasoning On Games
161. SmartPlay: A Benchmark for LLMs as Intelligent Agents
162. DSGBench: A Diverse Strategic Game Benchmark for Evaluating LLM-based Agents in Complex Decision-Making Environments
163. GTBench: Uncovering the Strategic Reasoning Limitations of LLMs via Game-Theoretic Evaluations
164. PokeLLMon: A Human-Parity Agent for Pokemon Battles with Large Language Models
165. Describe, Explain, Plan and Select: Interactive Planning with Large Language Models Enables Open-World Multi-Task Agents
166. LMRL Gym: Benchmarks for Multi-Turn Reinforcement Learning with Language Models
167. Clembench: Using Game Play to Evaluate Chat-Optimized Language Models as Conversational Agents
168. LLM-Powered Hierarchical Language Agent for Real-time Human-AI Coordination
169. TextGames: Learning to Self-Play Text-Based Puzzle Games via Language Model Reasoning
170. SPIN-Bench: How Well Do LLMs Plan Strategically and Reason Socially?
171. GAMEBoT: Transparent Assessment of LLM Reasoning in Games
172. MineWorld: a Real-Time and Open-Source Interactive World Model on Minecraft
173. Enhance Reasoning for Large Language Models in the Game Werewolf
174. GameFactory: Creating New Games with Generative Interactive Videos
175. Diffusion Models Are Real-Time Game Engines
176. The Overcooked Generalisation Challenge: Evaluating Cooperation with Novel Partners in Unknown Environments Using Unsupervised Environment Design
177. Minigrid & Miniworld: Modular & Customizable Reinforcement Learning Environments for Goal-Oriented Tasks
178. TEACh: Task-Driven Embodied Agents That Chat
179. Realfred: An embodied instruction following benchmark in photo-realistic environments
180. ToolEyes: Fine-Grained Evaluation for Tool Learning Capabilities of Large Language Models in Real-world Scenarios
181. ACEBench: A Comprehensive Evaluation of LLM Tool Usage
182. FlowBench: Revisiting and Benchmarking Workflow-Guided Planning for LLM-based Agents
183. TRAJECT-Bench:A Trajectory-Aware Benchmark for Evaluating Agentic Tool Use
184. Evaluating Personalized Tool-Augmented LLMs from the Perspectives of Personalization and Proactivity
185. The Berkeley Function Calling Leaderboard (BFCL): From Tool Use to Agentic Evaluation of Large Language Models
186. UserBench: An Interactive Gym Environment for User-Centric Agents
187. tau^2-Bench: Evaluating Conversational Agents in a Dual-Control Environment
188. MCPToolBench++: A Large Scale AI Agent Model Context Protocol MCP Tool Use Benchmark
189. MCP-Universe: Benchmarking Large Language Models with Real-World Model Context Protocol Servers
190. MCP-Bench: Benchmarking Tool-Using LLM Agents with Complex Real-World Tasks via MCP Servers
191. Mcpmark: A benchmark for stress-testing realistic and comprehensive mcp use
192. M^3-Bench: Multi-Modal, Multi-Hop, Multi-Threaded Tool-Using MLLM Agent Benchmark
193. Intercode: Standardizing and benchmarking interactive coding with execution feedback
194. Codeagent: Enhancing code generation with tool-integrated agent systems for real-world repo-level coding challenges
195. BigCodeBench: Benchmarking Code Generation with Diverse Function Calls and Complex Instructions
196. CodeElo: Benchmarking Competition-level Code Generation of LLMs with Human-comparable Elo Ratings
197. Csr-bench: Benchmarking llm agents in deployment of computer science research repositories
198. SWE-Bench Pro: Can AI Agents Solve Long-Horizon Software Engineering Tasks?
199. Swe-bench multimodal: Do ai systems generalize to visual software domains?
200. CRUXEval: A Benchmark for Code Reasoning, Understanding and Execution
201. DebugBench: Evaluating Debugging Capability of Large Language Models
202. CodeRAG-Bench: Can Retrieval Augment Code Generation?
203. SWT-Bench: Testing and Validating Real-World Bug-Fixes with Code Agents
204. FEA-Bench: A Benchmark for Evaluating Repository-Level Code Generation for Feature Implementation
205. Multi-SWE-bench: A Multilingual Benchmark for Issue Resolving
206. NL2Repo-Bench: Towards Long-Horizon Repository Generation Evaluation of Coding Agents
207. WhodunitBench: Evaluating LLMs on Murder Mystery Games
208. FlashAdventure: A Benchmark for GUI Agents Solving Full Story Arcs in Diverse Adventure Games
209. CivRealm: A Learning and Reasoning Odyssey in Civilization for Decision-Making Agents
210. Factorio Learning Environment
211. BioCoder: a benchmark for bioinformatics code generation with large language models
212. Benchmarking Data Science Agents
213. NATURAL PLAN: Benchmarking LLMs on Natural Language Planning
214. DiscoveryWorld: A Virtual Environment for Developing and Evaluating Automated Scientific Discovery Agents
215. StockBench: Can LLM Agents Trade Stocks Profitably In Real-world Markets?
216. Mle-dojo: Interactive environments for empowering llm agents in machine learning engineering
217. FinDeepResearch: Evaluating Deep Research Agents in Rigorous Financial Analysis
218. PaperArena: An Evaluation Benchmark for Tool-Augmented Agentic Reasoning on Scientific Literature
219. BixBench: a Comprehensive Benchmark for LLM-based Agents in Computational Biology
220. CRMArena-Pro: Holistic Assessment of LLM Agents Across Diverse Business Scenarios and Interactions
221. MedAgentGym: A Scalable Agentic Training Environment for Code-Centric Reasoning in Biomedical Data Science
222. Finance Agent Benchmark: Benchmarking LLMs on Real-world Financial Research Tasks
223. EcomBench: Towards Holistic Evaluation of Foundation Agents in E-commerce
224. MedAgentBench v2: Improving Medical LLM Agent Design
225. MedMCP-Calc: Benchmarking LLMs for Realistic Medical Calculator Scenarios via MCP Integration
226. Advancing ESG Intelligence: An Expert-level Agent and Comprehensive Benchmark for Sustainable Finance
227. BioAgent Bench: An AI Agent Evaluation Suite for Bioinformatics
228. World of Workflows: a Benchmark for Bringing World Models to Enterprise Systems
229. EnterpriseOps-Gym: Environments and Evaluations for Stateful Agentic Planning and Tool Use in Enterprise Settings
230. MetaClaw: Just Talk--An Agent That Meta-Learns and Evolves in the Wild
231. Claw-Eval: Toward Trustworthy Evaluation of Autonomous Agents
232. ClawArena: Benchmarking AI Agents in Evolving Information Environments
233. AgentBoard: An Analytical Evaluation Board of Multi-turn LLM Agents
234. AgentGym: Evolving Large Language Model-based Agents across Diverse Environments
235. Benchmarking Agentic Workflow Generation
236. Mlgym: A new framework and benchmark for advancing ai research agents
237. MedBrowseComp: Benchmarking Medical Deep Research and Computer Use
238. WebMMU: A Benchmark for Multimodal Multilingual Website Understanding and Code Generation
239. TPS-Bench: Evaluating AI Agents' Tool Planning & Scheduling Abilities in Compounding Tasks
240. AgencyBench: Benchmarking the Frontiers of Autonomous Agents in 1M-Token Real-World Contexts
241. AgentVista: Evaluating Multimodal Agents in Ultra-Challenging Realistic Visual Scenarios
242. DeepSeek-V3.2: Pushing the Frontier of Open Large Language Models
243. LongCat-Flash-Thinking-2601 Technical Report
244. MiMo-V2-Flash Technical Report
245. Generalized Planning in PDDL Domains with Pretrained Large Language Models
246. Can Language Models Serve as Text-Based World Simulators?
247. Leveraging Environment Interaction for Automated PDDL Translation and Planning with Large Language Models
248. Text2World: Benchmarking Large Language Models for Symbolic World Model Generation
249. WorldCoder, a Model-Based LLM Agent: Building World Models by Writing Code and Interacting with the Environment
250. Towards General Agentic Intelligence via Environment Scaling
251. Scaling Agents via Continual Pre-training
252. On Data Engineering for Scaling LLM Terminal Capabilities
253. LLM-in-Sandbox Elicits General Agentic Intelligence
254. Generalizable End-to-End Tool-Use RL with Synthetic CodeGym
255. Agent2World: Learning to Generate Symbolic World Models via Adaptive Multi-Agent Feedback
256. Training Software Engineering Agents and Verifiers with SWE-Gym
257. R2E-Gym: Procedural Environments and Hybrid Verifiers for Scaling Open-Weights SWE Agents
258. Immersion in the GitHub Universe: Scaling Coding Agents to Mastery
259. SWE-Hub: A Unified Production System for Scalable, Executable Software Engineering Tasks
260. MEnvAgent: Scalable Polyglot Environment Construction for Verifiable Software Engineering
261. SWE-smith: Scaling Data for Software Engineering Agents
262. DockSmith: Scaling Reliable Coding Environments via an Agentic Docker Builder
263. CLI-Gym: Scalable CLI Task Generation via Agentic Environment Inversion
264. SciAgentGym: Benchmarking Multi-Step Scientific Tool-use in LLM Agents
265. FinMTM: A Multi-Turn Multimodal Benchmark for Financial Reasoning and Agent Evaluation
266. AgentSynth: Scalable Task Generation for Generalist Computer-Use Agents
267. lmgame-Bench: How Good are LLMs at Playing Games?
268. GameDevBench: Evaluating Agentic Capabilities Through Game Development
269. Safe and Scalable Web Agent Learning via Recreated Websites
270. AutoWebWorld: Synthesizing Infinite Verifiable Web Environments via Finite State Machines
271. GLM-5: from Vibe Coding to Agentic Engineering
272. DIVE: Scaling Diversity in Agentic Task Synthesis for Generalizable Tool Use
273. KAT-Coder-V2 Technical Report
274. SWE-Universe: Scale Real-World Verifiable Environments to Millions
275. TaskCraft: Automated Generation of Agentic Tasks
276. LOGIGEN: Logic-Driven Generation of Verifiable Agentic Tasks
277. InfiniteWeb: Scalable Web Environment Synthesis for GUI Agent Training
278. NL2Plan: Robust LLM-Driven Planning from Minimal Text Descriptions
279. Procedural Environment Generation for Tool-Use Agents
280. AutoForge: Automated Environment Synthesis for Agentic Reinforcement Learning
281. ScaleEnv: Scaling Environment Synthesis from Scratch for Generalist Interactive Tool-Use Agent Training
282. Training Versatile Coding Agents in Synthetic Environments
283. Endless Terminals: Scaling RL Environments for Terminal Agents
284. Measuring General Intelligence with Generated Games
285. Welcome to the era of experience
286. Planetarium: A Rigorous Benchmark for Translating Text to Structured Planning Languages
287. Generating Symbolic World Models via Test-time Scaling of Large Language Models
288. Synthesizing world models for bilevel planning
289. Hybrid-Gym: Training Coding Agents to Generalize Across Tasks
290. EnvGen: Generating and Adapting Environments via LLMs for Training Embodied Agents
291. Diffusion for World Modeling: Visual Details Matter in Atari
292. Pandora: Towards General World Model with Natural Language Actions and Video States
293. Recurrent World Models Facilitate Policy Evolution
294. Empowering World Models with Reflection for Embodied Video Prediction
295. Vimo: A generative visual gui world model for app agents
296. Matrix-Game: Interactive World Foundation Model
297. Matrix-Game 2.0: An Open-Source, Real-Time, and Streaming Interactive World Model
298. NeuralOS: Towards Simulating Operating Systems via Neural Generative Models
299. GTM: Simulating the World of Tools for AI Agents
300. CWM: An Open-Weights LLM for Research on Code Generation with World Models
301. Imagine-then-Plan: Agent Learning from Adaptive Lookahead with World Models
302. Agent Planning with World Knowledge Model
303. R-WoM: Retrieval-augmented World Model For Computer-use Agents
304. MobileDreamer: Generative Sketch World Model for GUI Agent
305. Code2World: A GUI World Model via Renderable Code Generation
306. Reasoning with Language Model is Planning with World Model
307. Learning and leveraging world models in visual representation learning, 2024
308. Dino-wm: World models on pre-trained visual features enable zero-shot planning
309. Seq-JEPA: Autoregressive Predictive Learning of Invariant-Equivariant World Models
310. Self-supervised learning from images with a joint-embedding predictive architecture
311. Back to the features: Dino as a foundation for video world models
312. Dino-foresight: Looking into the future with dino
313. V-JEPA 2: Self-Supervised Video Models Enable Understanding, Prediction and Planning
314. EnerVerse: Envisioning Embodied Future Space for Robotics Manipulation
315. Genie Envisioner: A Unified World Foundation Platform for Robotic Manipulation
316. KeyWorld: Key Frame Reasoning Enables Effective and Efficient World Models
317. FlowDreamer: A RGB-D World Model With Flow-Based Motion Representations for Robot Manipulation
318. Cosmos Policy: Fine-Tuning Video Models for Visuomotor Control and Planning
319. World action models are zero-shot policies
320. GAIA-2: A Controllable Multi-View Generative World Model for Autonomous Driving
321. Cosmos-Drive-Dreams: Scalable Synthetic Driving Data Generation with World Foundation Models
322. Learning Primitive Embodied World Models: Towards Scalable Robotic Learning
323. AdaWorld: Learning Adaptable World Models with Latent Actions
324. Causal World Modeling for Robot Control
325. Medical World Model: Generative Simulation of Tumor Evolution for Treatment Planning
326. Cosmos World Foundation Model Platform for Physical AI
327. LIVE: Long-horizon Interactive Video World Modeling
328. Dyna-Think: Synergizing Reasoning, Acting, and World Model Simulation in AI Agents
329. Planning with Reasoning using Vision Language World Model
330. Simura: A world-model-driven simulative reasoning architecture for general goal-oriented agents
331. Unlocking Smarter Device Control: Foresighted Planning with a World Model-Driven Code Execution Approach
332. Web World Models
333. World modelling improves language model agents
334. Simulating Environments with Reasoning Models for Agent Training
335. WebWorld: A Large-Scale World Model for Web Agent Training
336. Generative Visual Code Mobile World Models
337. SWE-World: Building Software Engineering Agents in Docker-Free Environments
338. EchoJEPA: A Latent Predictive Foundation Model for Echocardiography
339. Enhancing Open-Domain Task-Solving Capability of LLMs via Autonomous Tool Integration from GitHub
340. CoPS: Empowering LLM Agents with Provable Cross-Task Experience Sharing
341. Embodied large language models enable robots to complete complex tasks in unpredictable environments
342. Memp: Exploring Agent Procedural Memory
343. Synapse: Trajectory-as-Exemplar Prompting with Memory for Computer Control
344. WorldMM: Dynamic Multimodal Memory Agent for Long Video Reasoning
345. Darwin Godel Machine: Open-Ended Evolution of Self-Improving Agents
346. ReasoningBank: Scaling Agent Self-Evolving with Reasoning Memory
347. Agent-Pro: Learning to Evolve via Policy-Level Reflection and Optimization
348. Agent KB: Leveraging Cross-Domain Experience for Agentic Problem Solving
349. DeepAgent: A General Reasoning Agent with Scalable Toolsets
350. FLEX: Continuous Agent Evolution via Forward Learning from Experience
351. O-Mem: Omni Memory System for Personalized, Long Horizon, Self-Evolving Agents
352. Experience-Evolving Multi-Turn Tool-Use Agent with Hybrid Episodic-Procedural Memory
353. Remember Me, Refine Me: A Dynamic Procedural Memory Framework for Experience-Driven Agent Evolution
354. Bifrost: Steering Strategic Trajectories to Bridge Contextual Gaps for Self-Improving Agents
355. Learning Physical Principles from Interaction: Self-Evolving Planning via Test-Time Memory
356. Agent Workflow Memory
357. Reinforcement Learning for Self-Improving Agent with Skill Library
358. Inducing Programmatic Skills for Agentic Tasks
359. SkillWeaver: Web Agents can Self-Improve by Discovering and Honing Skills
360. SkillRL: Evolving Agents via Recursive Skill-Augmented Reinforcement Learning
361. SkillOrchestra: Learning to Route Agents via Skill Transfer
362. Memory in the Age of AI Agents
363. Rethinking Memory in AI: Taxonomy, Operations, Topics, and Future Directions
364. Rethinking Memory Mechanisms of Foundation Agents in the Second Half: A Survey
365. Think While Watching: Online Streaming Segment-Level Memory for Multi-Turn Video Reasoning in Multimodal Large Language Models
366. Learning How to Remember: A Meta-Cognitive Management Method for Structured and Transferable Agent Memory
367. MemGPT: Towards LLMs as Operating Systems
368. Voyager: An Open-Ended Embodied Agent with Large Language Models
369. Training-Free Group Relative Policy Optimization
370. Simulate Before Act: Model-Based Planning for Web Agents
371. ManuSearch: Democratizing Deep Search in Large Language Models with a Transparent and Open Multi-Agent Framework
372. Open Deep Search: Democratizing Search with Open-source Reasoning Agents
373. Search-o1: Agentic Search-Enhanced Large Reasoning Models
374. Demystifying and Enhancing the Efficiency of Large Language Model Based Search Agents
375. Thought of Search: Planning with Language Models Through The Lens of Efficiency
376. Agent hospital: A simulacrum of hospital with evolvable medical agents
377. QuantAgent: Seeking Holy Grail in Trading by Self-Improving Large Language Model
378. Agentless: Demystifying LLM-based Software Engineering Agents
379. AutoCodeRover: Autonomous Program Improvement
380. CodeNav: Beyond tool-use to using real-world codebases with LLM agents
381. Coder: Issue resolving with multi-agent and task graphs
382. Magis: Llm-based multi-agent framework for github issue resolution
383. MetaGPT: Meta Programming for A Multi-Agent Collaborative Framework
384. Swe-agent: Agent-computer interfaces enable automated software engineering
385. VideoAgent: Long-Form Video Understanding with Large Language Model as Agent
386. Real-Time Reasoning Agents in Evolving Environments
387. LVAgent: Long Video Understanding by Multi-Round Dynamical Collaboration of MLLM Agents
388. Explorer: Scaling Exploration-driven Web Trajectory Synthesis for Multimodal Web Agents
389. ScoreFlow: Mastering LLM Agent Workflows via Score-based Preference Optimization
390. RobustFlow: Towards Robust Agentic Workflow Generation
391. DyFlow: Dynamic Workflow Framework for Agentic Reasoning
392. Multi-agent Architecture Search via Agentic Supernet
393. FlowReasoner: Reinforcing Query-Level Meta-Agents
394. MindSearch: Mimicking Human Minds Elicits Deep AI Searcher
395. WideSeek-R1: Exploring Width Scaling for Broad Information Seeking via Multi-Agent Reinforcement Learning
396. Workflow-R1: Group Sub-sequence Policy Optimization for Multi-turn Workflow Construction
397. ResearStudio: A Human-intervenable Framework for Building Controllable Deep Research Agents
398. WebPilot: A Versatile and Autonomous Multi-Agent System for Web Task Execution with Strategic Exploration
399. Plan-and-Act: Improving Planning of Agents for Long-Horizon Tasks
400. AOrchestra: Automating Sub-Agent Creation for Agentic Orchestration
401. Dr. MAS: Stable Reinforcement Learning for Multi-Agent LLM Systems
402. OWL: Optimized Workforce Learning for General Multi-Agent Assistance in Real-World Task Automation
403. ControlLLM: Augment Language Models with Tools by Searching on Graphs
404. Hyperagent: Generalist software engineering agents to solve coding tasks at scale
405. Repairagent: An autonomous, llm-based agent for program repair
406. Swe-search: Enhancing software agents with monte carlo tree search and iterative refinement
407. Alibaba lingmaagent: Improving automated issue resolution via comprehensive repository exploration
408. MindAgent: Emergent Gaming Interaction
409. Code Researcher: Deep Research Agent for Large Systems Code and Commit History
410. Constrained Natural Language Action Planning for Resilient Embodied Systems
411. MGA: Memory-Driven GUI Agent for Observation-Centric Interaction
412. AFlow: Automating Agentic Workflow Generation
413. AgentSquare: Automatic LLM Agent Search in Modular Design Space
414. Multi-Agent Collaboration via Evolving Orchestration
415. Automated Design of Agentic Systems
416. Process vs. Outcome Reward: Which is Better for Agentic RAG Reinforcement Learning
417. AvaTaR: Optimizing LLM Agents for Tool Usage via Contrastive Reasoning
418. ReCreate: Reasoning and Creating Domain Agents Driven by Experience
419. Yunjue Agent Tech Report: A Fully Reproducible, Zero-Start In-Situ Self-Evolving Agent System for Open-Ended Tasks
420. Chain-of-Agents: End-to-End Agent Foundation Models via Multi-Agent Distillation and Agentic RL
421. ClinicalReTrial: A Self-Evolving AI Agent for Clinical Trial Protocol Optimization
422. EvoClinician: A Self-Evolving Agent for Multi-Turn Medical Diagnosis via Test-Time Evolutionary Learning
423. Grammar Search for Multi-Agent Systems
424. CASCADE: Cumulative Agentic Skill Creation through Autonomous Development and Evolution
425. See and Think: Embodied Agent in Virtual Environment
426. Large Language Models as Tool Makers
427. Embodied LLM Agents Learn to Cooperate in Organized Teams
428. Tree of Thoughts: Deliberate Problem Solving with Large Language Models
429. ReWOO: Decoupling Reasoning from Observations for Efficient Augmented Language Models
430. LLM+P: Empowering Large Language Models with Optimal Planning Proficiency
431. AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation Framework
432. The openhands software agent sdk: A composable and extensible foundation for production agents
433. Cognitive Kernel-Pro: A Framework for Deep Research Agents and Agent Foundation Models Training
434. Agent-E: From Autonomous Web Navigation to Foundational Design Principles in Agentic Systems
435. Tool-Planner: Task Planning with Clusters across Multiple Tools
436. ToolChain*: Efficient Action Space Navigation in Large Language Models with A* Search
437. OctoTools: An Agentic Framework with Extensible Tools for Complex Reasoning
438. GPTSwarm: Language Agents as Optimizable Graphs
439. BAGEL: Bootstrapping Agents by Guiding Exploration with Language
440. OS-Genesis: Automating GUI Agent Trajectory Construction via Reverse Task Synthesis
441. Insta: Towards internet-scale training for agents
442. APIGen-MT: Agentic Pipeline for Multi-Turn Data Generation via Simulated Agent-Human Interplay
443. WebSailor: Navigating Super-human Reasoning for Web Agent
444. WebShaper: Agentically Data Synthesizing via Information-Seeking Formalization
445. WebWatcher: Breaking New Frontier of Vision-Language Deep Research Agent
446. Mobile-Agent-v3.5: Multi-platform Fundamental GUI Agents
447. WebExplorer: Explore and Evolve for Training Long-Horizon Web Agents
448. DeepDive: Advancing Deep Search Agents with Knowledge Graphs and Multi-Turn RL
449. Scaling Synthetic Task Generation for Agents via Exploration
450. Scaling Agents via Continual Pre-training
451. Explore to Evolve: Scaling Evolved Aggregation Logic via Proactive Online Exploration for Deep Research Agents
452. CRMWeaver: Building Powerful Business Agent via Agentic RL and Shared Memories
453. WebLeaper: Empowering Efficiency and Efficacy in WebAgent via Enabling Info-Rich Seeking
454. AgentEvolver: Towards Efficient Self-Evolving Agent System
455. VSearcher: Long-Horizon Multimodal Search Agent via Reinforcement Learning
456. OpenSeeker: Democratizing Frontier Search Agents by Fully Open-Sourcing Training Data
457. ToolCoder: Teach Code Generation Models to use API search tools
458. ToolAlpaca: Generalized Tool Learning for Language Models with 3000 Simulated Cases
459. AgentTuning: Enabling Generalized Agent Abilities for LLMs
460. Lingma SWE-GPT: An Open Development-Process-Centric Language Model for Automated Software Improvement
461. Aguvis: Unified Pure Vision Agents for Autonomous GUI Interaction
462. MaskSearch: A Universal Pre-Training Framework to Enhance Agentic Search Capability
463. Tongyi DeepResearch Technical Report
464. AgentFold: Long-Horizon Web Agents with Proactive Context Management
465. SIMA 2: A Generalist Embodied Agent for Virtual Worlds
466. O-Researcher: An Open Ended Deep Research Model via Multi-Agent Distillation and Agentic RL
467. Scaling Behavior Cloning Improves Causal Reasoning: An Open Model for Real-Time Video Game Playing
468. ToolACE-MCP: Generalizing History-Aware Routing from MCP Tools to the Agent Web
469. ProAct: Agentic Lookahead in Interactive Environments
470. OpenResearcher: A Fully Open Pipeline for Long-Horizon Deep Research Trajectory Synthesis
471. HATS: Hardness-Aware Trajectory Synthesis for GUI Agents
472. Trial and Error: Exploration-Based Trajectory Optimization for LLM Agents
473. Agent-FLAN: Designing Data and Methods of Effective Agent Tuning for Large Language Models
474. UI-TARS: Pioneering Automated GUI Interaction with Native Agents
475. Multi-Turn Code Generation Through Single-Step Rewards
476. SimpleDeepSearcher: Deep Information Seeking via Web-Powered Reasoning Trajectory Synthesis
477. EvolveSearch: An Iterative Self-Evolving Search Agent
478. GUI-Reflection: Empowering Multimodal GUI Models with Self-Reflection Behavior
479. Agent-rewardbench: Towards a unified benchmark for reward modeling across perception, planning, and safety in real-world multimodal agents
480. WebSynthesis: World-Model-Guided MCTS for Efficient WebUI-Trajectory Synthesis
481. Think in Games: Learning to Reason in Games via Reinforcement Learning with Large Language Models
482. ToolRM: Outcome Reward Models for Tool-Calling Large Language Models
483. Advancing Tool-Augmented Large Language Models via Meta-Verification and Reflection Learning
484. AgentFrontier: Expanding the Capability Frontier of LLM Agents with ZPD-Guided Data Synthesis
485. Scalable Data Synthesis for Computer Use Agents with Step-Level Filtering
486. Adapting Web Agents with Synthetic Supervision
487. SERA: Soft-Verified Efficient Repository Agents
488. TopoCurate:Modeling Interaction Topology for Tool-Use Agent Training
489. MagicAgent: Towards Generalized Agent Planning
490. WebDancer: Towards Autonomous Information Seeking Agency
491. WebWeaver: Structuring Web-Scale Evidence with Dynamic Outlines for Open-Ended Deep Research
492. WebResearcher: Unleashing unbounded reasoning capability in Long-Horizon Agents
493. UI-Venus-1.5 Technical Report
494. UI-TARS-2 Technical Report: Advancing GUI Agent with Multi-Turn Reinforcement Learning
495. DeepRetrieval: Hacking Real Search Engines and Retrievers with Large Language Models via Reinforcement Learning
496. ReSearch: Learning to Reason with Search for LLMs via Reinforcement Learning
497. Search and Refine During Think: Autonomous Retrieval-Augmented Reasoning of LLMs
498. SEEA-R1: Tree-Structured Reinforcement Fine-Tuning for Self-Evolving Embodied Agents
499. Seeing, Listening, Remembering, and Reasoning: A Multimodal Agent with Long-Term Memory
500. Video-Thinker: Sparking "Thinking with Videos" via Reinforcement Learning
501. R1-Searcher: Incentivizing the Search Capability in LLMs via Reinforcement Learning
502. OTC: Optimal Tool Calls via Reinforcement Learning
503. Nemotron-Research-Tool-N1: Exploring Tool-Using Language Models with Reinforced Reasoning
504. Agentic Reasoning and Tool Integration for LLMs via Reinforcement Learning
505. VLA-RL: Towards Masterful and General Robotic Manipulation with Scalable Reinforcement Learning
506. VRAG-RL: Empower Vision-Perception-Based RAG for Visually Rich Information Understanding via Iterative Reasoning with Reinforcement Learning
507. R-Search: Empowering LLM Reasoning with Search via Multi-Reward Reinforcement Learning
508. Video-MTR: Reinforced Multi-Turn Reasoning for Long Video Understanding
509. Agent-R1: Training Powerful LLM Agents with End-to-End Reinforcement Learning
510. ToolOrchestra: Elevating Intelligence via Efficient Model and Tool Orchestration
511. VideoMem: Enhancing Ultra-Long Video Understanding via Adaptive Memory Management
512. GDPO: Group reward-Decoupled Normalization Policy Optimization for Multi-reward RL Optimization
513. FlowSteer: Interactive Agentic Workflow Orchestration via End-to-End Reinforcement Learning
514. IntentRL: Training Proactive User-intent Agents for Open-ended Deep Research via Reinforcement Learning
515. Who Deserves the Reward? SHARP: Shapley Credit-based Optimization for Multi-Agent System
516. RAGEN: Understanding Self-Evolution in LLM Agents via Multi-Turn Reinforcement Learning
517. ZeroSearch: Incentivize the Search Capability of LLMs without Searching
518. WebAgent-R1: Training Web Agents via End-to-End Multi-Turn Reinforcement Learning
519. Unleashing Embodied Task Planning Ability in LLMs via Reinforcement Learning
520. SPIRAL: Self-Play on Zero-Sum Games Incentivizes Reasoning via Multi-Agent Multi-Turn Reinforcement Learning
521. Mobilegui-rl: Advancing mobile gui agent through reinforcement learning in online environment
522. Thinking With Videos: Multimodal Tool-Augmented Reinforcement Learning for Long Video Reasoning
523. ComputerRL: Scaling End-to-End Online Reinforcement Learning for Computer Use Agents
524. Bootstrapping Task Spaces for Self-Improvement
525. AgentGym-RL: Training LLM Agents for Long-Horizon Decision Making through Multi-Turn Reinforcement Learning
526. UI-S1: Advancing GUI Automation via Semi-online Reinforcement Learning
527. Learn the Ropes, Then Trust the Wins: Self-imitation with Progressive Exploration for Agentic Reinforcement Learning
528. AgentRL: Scaling Agentic Reinforcement Learning with a Multi-Turn, Multi-Task Framework
529. Stronger-MAS: Multi-Agent Reinforcement Learning for Collaborative LLMs
530. VAGEN: Reinforcing World Model Reasoning for Multi-Turn VLM Agents
531. GTR-Turbo: Merged Checkpoint is Secretly a Free Teacher for Agentic VLM Training
532. SeeUPO: Sequence-Level Agentic-RL with Convergence Guarantees
533. Hierarchy-of-Groups Policy Optimization for Long-Horizon Agentic Tasks
534. Deepswe: Training a fully open-sourced, state-of-the-art coding agent by scaling rl, Jul 2025
535. RLVE: Scaling Up Reinforcement Learning for Language Models with Adaptive Verifiable Environments
536. Do As I Can, Not As I Say: Grounding Language in Robotic Affordances
537. ReTool: Reinforcement Learning for Strategic Tool Use in LLMs
538. GUI-R1: A Generalist R1-Style Vision-Language Action Model For GUI Agents
539. ARLArena: A Unified Framework for Stable Agentic Reinforcement Learning
540. CM2: Reinforcement Learning with Checklist Rewards for Multi-Turn and Multi-Step Agentic Tool Use
541. SimpleTIR: End-to-End Reinforcement Learning for Multi-Turn Tool-Integrated Reasoning
542. WebRL: Training LLM Web Agents via Self-Evolving Online Curriculum Reinforcement Learning
543. WebArbiter: A Principle-Guided Reasoning Process Reward Model for Web Agents
544. Exploring Reasoning Reward Model for Agents
545. ZeroGUI: Automating Online GUI Learning at Zero Human Cost
546. DistRL: An Asynchronous Distributed Reinforcement Learning Framework for On-Device Control Agent
547. DigiRL: Training In-The-Wild Device-Control Agents with Autonomous Reinforcement Learning
548. Agentic Entropy-Balanced Policy Optimization
549. Learning Efficient Communication Protocols for Multi-Agent Reinforcement Learning
550. Absolute zero: Reinforced self-play reasoning with zero data
551. Self-Challenging Language Model Agents
552. Vision-zero: Scalable vlm self-improvement via strategic gamified self-play
553. Toward Training Superintelligent Software Agents through Self-Play SWE-RL
554. Active Zero: Self-Evolving Vision-Language Models through Active Environment Exploration
555. Llms as scalable, general-purpose simulators for evolving digital agent training
556. World-Model-Augmented Web Agents with Action Correction
557. Paired Open-Ended Trailblazer (POET): Endlessly Generating Increasingly Complex and Diverse Learning Environments and Their Solutions
558. Emergent Complexity and Zero-shot Transfer via Unsupervised Environment Design
559. Replay-Guided Adversarial Environment Design
560. Evolving Curricula with Regret-Based Environment Design
561. MAESTRO: Open-Ended Environment Design for Multi-Agent Reinforcement Learning
562. Refining Minimax Regret for Unsupervised Environment Design
563. DataEnvGym: Data Generation Agents in Teacher Environments with Student Feedback
564. Eurekaverse: Environment curriculum generation via large language models
565. Don't Just Fine-tune the Agent, Tune the Environment
566. Self-Evolving Curriculum for LLM Reasoning
567. Reasoning Core: A Scalable RL Environment for LLM Symbolic Reasoning
568. CuES: A Curiosity-driven and Environment-grounded Synthesis Framework for Agentic RL
569. GenEnv: Difficulty-Aligned Co-Evolution Between LLM Agents and Environment Simulators
570. Feedback-Driven Tool-Use Improvements in Large Language Models via Automated Build Environments
571. ARE: Scaling Up Agent Environments and Evaluations
572. On-Policy Distillation
573. Room-Across-Room: Multilingual Vision-and-Language Navigation with Dense Spatiotemporal Grounding
574. Beyond the Nav-Graph: Vision-and-Language Navigation in Continuous Environments
575. Avalon's Game of Thoughts: Battle Against Deception through Recursive Contemplation
576. Collab-Overcooked: Benchmarking and Evaluating Large Language Models as Collaborative Agents
577. StableToolBench: Towards Stable Large-Scale Benchmarking on Tool Learning of Large Language Models
578. ToolTalk: Evaluating Tool-Usage in a Conversational Setting
579. MINT: Evaluating LLMs in Multi-turn Interaction with Tools and Language Feedback
580. CAMEL: Communicative Agents for "Mind" Exploration of Large Language Model Society
581. TextGrad: Automatic "Differentiation" via Text
582. DSPy: Compiling Declarative Language Model Calls into State-of-the-Art Pipelines

</details>

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
