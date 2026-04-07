# Awesome Multi-Agent Systems

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

A curated, **annotated** list of resources for the Multi-Agent Systems (MAS) research community—spanning **classic milestone work** and **recent advances (2021–2026)** across coordination, game theory, negotiation, planning, multi-agent learning, robotics, and simulation.

*Star counts below are **live badges** pulled from GitHub in real time via [shields.io](https://shields.io/).*

## Executive summary

Multi-Agent Systems research sits at the intersection of **(i) decision-making**, **(ii) interaction** (cooperation/competition/negotiation), and **(iii) evaluation** in realistic multi-entity environments (games, markets, robots, social settings). This README is designed to help you:
- Build **foundational literacy** (agent models, architectures, coordination, decentralised decision-making, DCOPs, negotiation).
- Track **high-impact modern directions** (benchmarking + reproducibility in MARL; scalable simulators; and LLM-based multi-agent "agentic systems" and evaluation).
- Choose **tools responsibly** (licensing, maturity signals like release activity/archival status, community adoption).

If any detail below is not reliably available from primary/official sources at authoring time, it is explicitly marked **unspecified**.

## Table of contents

- [How this repo is organised](#how-this-repo-is-organised)
- [MAS taxonomy and milestone timeline](#mas-taxonomy-and-milestone-timeline)
- [Curated resources](#curated-resources)
  - [Classic books (pre-2024)](#classic-books-pre-2024)
  - [Recent books (2024–)](#recent-books-2024)
  - [Tutorials and courses](#tutorials-and-courses)
  - [Tutorials and how-to guides](#tutorials-and-how-to-guides)
  - [Seminal papers and milestone work](#seminal-papers-and-milestone-work)
  - [Recent high-impact papers and surveys](#recent-high-impact-papers-and-surveys)
  - [Datasets and benchmarks](#datasets-and-benchmarks)
  - [Frameworks, libraries, and tools](#frameworks-libraries-and-tools)
  - [Competitions and challenges](#competitions-and-challenges)
  - [Agent interoperability protocols](#agent-interoperability-protocols)
- [Reproducibility and community](#reproducibility-and-community)
  - [Reproducibility resources and code](#reproducibility-resources-and-code)
  - [Community resources](#community-resources)
- [Contribution guidelines and curation criteria](#contribution-guidelines-and-curation-criteria)

## How this repo is organised

This repository treats MAS as a **family of research problems** rather than a single subfield. Resources are navigable via:
- **Topic tags** (e.g., `MARL`, `game-theory`, `negotiation`, `planning`, `robotics`, `simulation`, `DCOP`, `LLM-agents`).
- **Two-tier curation**:
  - **Milestones**: conceptual foundations and widely-cited "shape-of-the-field" work (often older).
  - **Recent**: last 5 years (2021–2026) emphasising robust benchmarks, reproducibility, and new agent paradigms (including LLM-based multi-agent evaluation and orchestration).

Entry format used below:

```
- [**Title**](Link) (Year) by Authors/Maintainers
  Annotation. Tags
```

## MAS taxonomy and milestone timeline

### MAS topic taxonomy

```mermaid
graph TD
  MAS[Multi-Agent Systems] --> Models[Agent Models & Architectures]
  MAS --> Interaction[Interaction & Coordination]
  MAS --> Learning[Learning in Multi-Agent Settings]
  MAS --> Eval[Benchmarks, Evaluation, Reproducibility]
  MAS --> Simulation[Agent-Based Modelling & Simulation]

  Models --> BDI[BDI / deliberative agents]
  Models --> DecDP[Decentralised decision processes - Dec-POMDP/DEC-MDP]
  Interaction --> GameTheory[Game theory & mechanism design]
  Interaction --> Negotiation[Automated negotiation]
  Interaction --> DCOP[Distributed constraint optimisation - DCOP]
  Interaction --> MAPF[Multi-agent path finding]

  Learning --> MARL[Multi-Agent Reinforcement Learning]
  Learning --> Comm[Emergent communication / coordination learning]
  Learning --> LLM[LLM-based agents & multi-agent teams]

  MAS --> Protocols[Agent Interoperability Protocols]
  Protocols --> ToolProto[Tool/context protocols - MCP]
  Protocols --> A2AProto[Agent-to-agent protocols - A2A]
  Protocols --> UIProto[Agent-to-user protocols - AG-UI]

  Eval --> Bench[Benchmarks & task suites]
  Eval --> Artifacts[Artifacts, checklists, code release norms]
  Simulation --> ABM[ABM toolchains - social/eco/epi]
  Simulation --> RoboticsSim[Robotics-focused multi-agent simulation]
```

### Milestone timeline

```mermaid
timeline
  title MAS milestones (selected)
  1980 : Contract Net Protocol (task allocation/coordination)
  1993 : Agent-Oriented Programming
  1995 : BDI Agents (theory to practice)
  2001 : Agent-based software engineering (agent paradigm)
  2002 : Decentralised control complexity (Dec-POMDP/DEC-MDP)
  2005 : ADOPT (DCOP optimality + async execution)
  2009 : Max-Sum in decentralised coordination (factor graphs)
  2021 : MAPPO (strong cooperative MARL baseline)
  2021 : Melting Pot (social/generalisation evaluation)
  2022 : VMAS (vectorised multi-robot MARL sim)
  2022 : SMACv2 (harder cooperative MARL benchmark)
  2023 : MARLlib (standardised MARL training library)
  2024 : BenchMARL (reproducible benchmarking pipeline)
  2024 : Magentic-One (generalist multi-agent LLM system)
  2024 : MCP - Model Context Protocol (tool/context interop standard)
  2025 : A2A - Agent2Agent Protocol (agent-to-agent interop standard)
  2025 : OpenAI Agents SDK / Google ADK (production multi-agent frameworks)
  2025 : Survey on evaluating/benchmarking LLM agents
  2026 : General AgentBench (unified LLM-agent evaluation)
```

## Curated resources

### Classic books (pre-2024)

- [*An Introduction to MultiAgent Systems* (2nd ed.)](https://www.wiley.com/en-us/An+Introduction+to+MultiAgent+Systems%2C+2nd+Edition-p-9780470519462) (2009) by Michael Wooldridge
  A widely used MAS textbook covering agent concepts, interaction, coordination, and foundational theory; a solid "first principles" entry point for the broader MAS canon beyond MARL. `foundations`, `agents`, `coordination`

- [**Multiagent Systems: Algorithmic, Game-Theoretic, and Logical Foundations**](http://www.masfoundations.org/) (2009) by Yoav Shoham, Kevin Leyton-Brown
  Core reference connecting MAS with game theory, mechanism design, and computational foundations; also supported by a freely accessible "rough version" linked from a canonical course page. `game-theory`, `mechanism-design`, `foundations`

- [**Multi-Agent Systems: A Modern Approach to Distributed Artificial Intelligence**](https://mitpress.mit.edu/9780262731317/multi-agent-systems/) (1999) by Gerhard Weiss (editor)
  Classic edited volume spanning early MAS themes (coordination, communication, architectures) from distributed AI roots; useful for historical depth and breadth. `distributed-ai`, `foundations`, `architectures`


### Recent books (2024–)

- [**Agents and Multi-Agent Systems Development: Platforms, Toolkits, Technologies**](https://link.springer.com/book/10.1007/978-3-032-01082-7) (2026) by R. Collier, V. Mascardi, A. Ricci (editors)
  A snapshot of the current state of the art in tools, frameworks, and techniques for designing and implementing multi-agent systems; includes a chapter on "Agent Toolkits Anno 2025." `MAS-engineering`, `platforms`, `toolkits`

- [**Design Multi-Agent AI Systems Using MCP and A2A**](https://www.packtpub.com/en-sg/product/design-multi-agent-ai-systems-using-mcp-and-a2a-9781806116461) (2026) by Gigi Sayfan
  Hands-on guide to building a production-ready multi-agent AI framework from scratch in Python; covers tool use, memory via MCP, collaborative agent workflows with A2A, observability, and human-in-the-loop patterns. Companion code on GitHub. `LLM-agents`, `MCP`, `A2A`, `practice`

- [**Agentic AI: Theories and Practices**](https://link.springer.com/book/10.1007/978-3-031-90026-6) (2025) by Ken Huang (editor)
  Analyses the rise of generative AI agents (agentic AI) across industries, covering development, applications, and implications from finance to healthcare. `agentic-ai`, `LLM-agents`, `applications`

- [**AI Agents in Action**](https://www.manning.com/books/ai-agents-in-action) (2025) by Micheal Lanham
  Practitioner guide to building multi-agent AI systems using modern frameworks (LangChain, AutoGen, CrewAI); covers knowledge management, memory systems, and collaborative multi-agent architectures. `LLM-agents`, `multi-agent`, `practice`

- [**Building Applications with AI Agents**](https://www.oreilly.com/library/view/building-applications-with/9781098176495/) (2025) by Michael Albada
  A practical, research-based approach to designing and implementing single- and multi-agent systems, covering coordination techniques and communication methods for agent systems. `LLM-agents`, `multi-agent`, `practice`

- [**Designing Multi-Agent Systems: Principles, Patterns, and Implementation for AI Agents**](https://multiagentbook.com/) (2025) by Victor Dibia
  A first-principles guide to designing multi-agent applications, walking through building a feature-complete framework from scratch; by a core AutoGen contributor at Microsoft Research. Companion code on GitHub. `LLM-agents`, `multi-agent`, `practice`

- [**Multi-Agent Reinforcement Learning: Foundations and Modern Approaches**](https://www.marl-book.com/) (2024) by Stefano V. Albrecht, Filippos Christianos, Lukas Schäfer
  A modern MARL textbook focusing on models, solution concepts, algorithms, and practical challenges; associated with a companion website and learning materials (slides/code). `MARL`, `RL`, `game-theory`, `reproducibility`, `code`


### Tutorials and courses

- [**European Agent Systems Summer School (EASSS)**](https://easss.upb.ro/) (2025) by EURAMAS community
  Long-running summer school (since 1999) offering introductory and advanced courses across autonomous agents and MAS, aimed at researchers and students. `community`, `tutorials`, `foundations`

- [**AAMAS tutorials programme**](https://aamas2025.org/index.php/conference/program/tutorials/) (2025) by AAMAS organisers
  Tutorials highlight evolving MAS topics; the official programme page provides titles/abstracts and can seed curated "learning pathways" each year. `community`, `tutorials`, `MAS`

- [**Cooperative AI Summer School**](https://www.cooperativeai.com/summer-school/summer-school-2025) (2025) by Cooperative AI community
  A summer school aimed at grounding participants in cooperative AI (overlapping with MAS/MARL, incentives, and human/agent cooperation). `cooperative-ai`, `MARL`, `incentives`

- [AAMAS 2025 tutorial: **RL in Automated Negotiation (T1)**](https://github.com/yasserfarouk/aamas2025rlneg) (2025) by Yasser Farouk
  A concrete tutorial artefact (slides/code) framing negotiation as a multi-agent RL problem; useful for bridging MAS negotiation and learning-based approaches. `negotiation`, `MARL`, `tutorial`

- [Stanford **CS 224M: Multi Agent Systems**](https://web.stanford.edu/class/cs224m/) (2014) by Stanford course staff; Instructor: Yoav Shoham
  A game-theory-and-mechanism-design-heavy MAS course page with structured readings, lecture materials via edX links, and a direct tie-in to the Shoham & Leyton-Brown textbook. `game-theory`, `mechanism-design`, `foundations`


### Tutorials and how-to guides

- [**LangGraph documentation pointers**](https://github.com/langchain-ai/langgraph) (2026) by LangChain/LangGraph maintainers
  README positions LangGraph for durable execution, memory, and human-in-the-loop agent workflows—useful for building multi-agent graphs. `LLM-agents`, `orchestration`, `graphs`

- [**NegMAS tutorials**](https://negmas.readthedocs.io/en/latest/tutorials.html) (2026) by NegMAS maintainers
  The repo links to tutorials and API references; also documents an ecosystem of competition frameworks and agents. `negotiation`, `how-to`, `simulation`

- [**AutoGen README (multi-agent orchestration examples)**](https://github.com/microsoft/autogen) (2025) by Microsoft
  Includes code examples for multi-agent orchestration and notes on maintenance mode considerations for new users. `LLM-agents`, `orchestration`, `framework`

- [**pyDCOP documentation**](https://pydcop.readthedocs.io/) (2022) by Orange Open Source (archived)
  Despite archival status, the repo points to hosted documentation and provides a practical entry to DCOP modelling and algorithm experimentation. `DCOP`, `coordination`, `how-to`

- [**Swarm README and examples**](https://github.com/openai/swarm) (unspecified) by OpenAI
  The README describes the two primitives (agents + handoffs), provides examples, and frames Swarm as a lightweight, testable educational resource for multi-agent orchestration. `LLM-agents`, `orchestration`, `tutorial`


### Seminal papers and milestone work

- [**Decentralised Coordination of Continuously Valued Control Parameters using the Max-Sum Algorithm**](https://eprints.soton.ac.uk/267314/1/main-maxsumcont.pdf) (2009) by Stranders et al.
  Demonstrates the Max-Sum message-passing approach for decentralised coordination via factor-graph representations, influential in MAS coordination and resource allocation formulations. `DCOP`, `message-passing`, `coordination`

- [**ADOPT: Asynchronous Distributed Constraint Optimization with Quality Guarantees**](https://www.sciencedirect.com/science/article/pii/S0004370204001511) (2005) by Modi et al.
  A key DCOP algorithm: asynchronous, parallel execution with guarantees on solution quality (optimality), strongly influencing DCOP as a MAS coordination formalism. `DCOP`, `coordination`, `optimization`

- [**The Complexity of Decentralized Control of Markov Decision Processes**](https://pubsonline.informs.org/doi/abs/10.1287/moor.27.4.819.297) (2002) by Bernstein et al.
  Formalises decentralised decision-making models and proves strong complexity results, grounding Dec-POMDP/DEC-MDP research in computational limits. `Dec-POMDP`, `planning`, `theory`

- [**An agent-based approach for building complex software systems**](https://dl.acm.org/doi/10.1145/367211.367250) (2001) by Nicholas R. Jennings
  A landmark argument for agent-based decomposition in complex software systems (autonomy, interaction, emergent system behaviour), shaping MAS engineering practice. `agent-oriented-software`, `engineering`

- [**BDI Agents: From Theory to Practice**](https://cdn.aaai.org/ICMAS/1995/ICMAS95-042.pdf) (1995) by Anand S. Rao, Michael P. Georgeff
  A classic bridge from formal BDI logics to implemented agent systems; foundational to deliberative agent architectures and practical rational agency discussions. `BDI`, `agent-architectures`, `foundations`

- [**Agent-oriented programming**](https://www.sciencedirect.com/science/article/pii/0004370293900349) (1993) by Yoav Shoham
  Establishes "agent-oriented programming" as a computational paradigm and helped catalyse agent-based approaches and mental-state abstractions in AI. `agent-architectures`, `foundations`

- [**The Contract Net Protocol: High-Level Communication and Control in a Distributed Problem Solver**](https://dl.acm.org/doi/10.1109/TC.1980.1675516) (1980) by Reid G. Smith
  Introduces a negotiation-inspired protocol for distributed task allocation—one of the earliest and most influential coordination mechanisms in distributed AI/MAS. `coordination`, `task-allocation`, `distributed-ai`


### Recent high-impact papers and surveys

Items are chosen for (a) field-shaping benchmarks/tooling, (b) reproducibility/evaluation influence, or (c) representing a major new direction (e.g., LLM-based multi-agent systems).

- [**General AgentBench**](https://arxiv.org/html/2602.18998v1) (2026) by —
  Introduces a unified benchmark framework for evaluating general LLM agents across search/coding/reasoning/tool-use; relevant for assessing generality claims. `LLM-agents`, `benchmark`, `evaluation`

- [**The Orchestration of Multi-Agent Systems: Architectures, Protocols, and Enterprise Adoption**](https://arxiv.org/abs/2601.13671) (2026) by —
  Discusses MCP and A2A as emerging standards for structured, interoperable multi-agent communication in enterprise settings. `protocols`, `orchestration`, `survey`

- [**Evaluation and Benchmarking of LLM Agents: A Survey**](https://dl.acm.org/doi/10.1145/3711896.3736570) (2025) by Mohammadi et al.
  A survey aiming to clarify the evaluation landscape for LLM agents; useful when designing benchmarks, metrics, and reporting practices. `LLM-agents`, `survey`, `evaluation`

- [**LLM Multi-Agent Systems: Challenges and Open Problems**](https://arxiv.org/abs/2502.12668) (2025) by Tran et al.
  Explicitly focuses on challenges/open problems for LLM multi-agent systems, helping turn "framework hacking" into research questions. `LLM-agents`, `multi-agent`, `survey`

- [**A Survey of Agent Interoperability Protocols: MCP, ACP, A2A, and ANP**](https://arxiv.org/abs/2505.02279) (2025) by Ehtesham et al.
  Comparative survey of four emerging agent communication/interoperability protocols across architecture, transport, security, and deployment dimensions. `protocols`, `interoperability`, `survey`

- [**Advancing Multi-Agent Systems Through Model Context Protocol**](https://arxiv.org/abs/2504.21030) (2025) by —
  Examines MCP's role in MAS with case studies in enterprise knowledge management, collaborative research, and distributed problem-solving. `MCP`, `multi-agent`, `protocols`

- [**BenchMARL: Benchmarking Multi-Agent Reinforcement Learning**](https://github.com/facebookresearch/BenchMARL) (2024) by Bettini, Prorok, Moens
  A benchmarking/training pipeline focused on **standardised configuration and reproducible comparisons** across algorithms, environments, and models (TorchRL backend). `MARL`, `benchmarking`, `reproducibility`

- [**MLE-bench: Evaluating Machine Learning Agents on ML Engineering**](https://arxiv.org/abs/2410.07095) (2024) by Chan et al.
  Curates ML engineering tasks (from Kaggle competitions) to measure agent performance on real-world ML engineering workflows. `LLM-agents`, `benchmark`, `ML-engineering`

- [**Magentic-One: A Generalist Multi-Agent System for Solving Complex Tasks**](https://arxiv.org/abs/2411.04468) (2024) by Fourney et al.
  A generalist multi-agent architecture with an Orchestrator coordinating specialised agents (web/file/code) to complete complex tasks; a representative "agentic systems" direction. `LLM-agents`, `multi-agent`, `tool-use`

- [**Large Language Model based Multi-Agents: A Survey of Progress and Challenges**](https://arxiv.org/abs/2402.01680) (2024) by Guo et al.
  Aggregates methods, patterns, and open problems for LLM-based multi-agent systems; a practical map of a fast-moving space. `LLM-agents`, `multi-agent`, `survey`

- [**MLAgentBench: Evaluating Language Agents on ML Experimentation**](https://arxiv.org/abs/2310.03302) (2023–2024) by Huang et al.
  Focuses evaluation on agents performing end-to-end ML experimentation tasks; useful for connecting agentic systems to scientific workflows. `LLM-agents`, `benchmark`, `ML-engineering`

- [**AgentBench: Evaluating LLMs as Agents**](https://arxiv.org/abs/2308.03688) (2023) by Liu et al.
  A multi-dimensional benchmark of interactive environments to evaluate "LLM-as-agent" behaviour, helping structure evaluation beyond static QA. `LLM-agents`, `benchmark`, `evaluation`

- [**Multi-Agent Reinforcement Learning: Foundations and Modern Approaches**](https://arxiv.org/abs/2306.08502) (2023) by Wang et al.
  A broad MARL survey spanning foundations, algorithms, and challenges; good for "state of the field" grounding alongside textbooks. `MARL`, `survey`, `foundations`

- [**MARLlib: A Scalable and Efficient Multi-agent RL Library**](https://www.jmlr.org/papers/volume24/23-0378/23-0378.pdf) (2022–2023) by Hu et al.
  Standardises MARL training across tasks/algorithms via wrappers + policy mapping; positioned as a scalable library building on Ray/RLlib infrastructure. `MARL`, `library`, `reproducibility`

- [**Melting Pot 2.0**](https://arxiv.org/abs/2211.13746) (2022) by Agapiou et al.
  Expands and revises Melting Pot, including more scenarios and details intended as a sustained reference for future work using the Melting Pot protocol. `MARL`, `evaluation`, `social`

- [**SMACv2: A New Benchmark for Cooperative Multi-Agent RL**](https://arxiv.org/abs/2212.07489) (2022) by Ellis et al.
  Updates the StarCraft cooperative benchmark to address "solved" aspects of SMAC via added randomisation and diversity; widely used for evaluating cooperative MARL scalability and robustness. `MARL`, `benchmark`, `StarCraft`

- [**VMAS: A Vectorized Multi-Agent Simulator for Collective Robot Learning**](https://arxiv.org/abs/2207.03530) (2022) by Bettini et al.
  Provides a vectorised, differentiable multi-agent simulator for scalable multi-robot MARL benchmarking; targets high-throughput training and multi-robot scenarios. `robotics`, `simulation`, `MARL`

- [**Problem Compilation for Multi-Agent Path Finding: a Survey**](https://www.ijcai.org/proceedings/2022/0783) (2022) by Pavel Surynek
  A survey view of MAPF research directions and problem formulations; useful for MAS planning/coordination beyond learning-based methods. `planning`, `MAPF`, `survey`

- [**The Surprising Effectiveness of PPO in Cooperative, Multi-Agent Games**](https://arxiv.org/abs/2103.01955) (2021) by Yu et al.
  Reassesses on-policy PPO in cooperative MARL and popularises MAPPO-style baselines; widely used as a strong, practical reference point for cooperative MARL comparisons. `MARL`, `CTDE`, `baselines`

- [**Scalable Evaluation of Multi-Agent Reinforcement Learning with Melting Pot**](https://arxiv.org/abs/2107.06857) (2021) by Leibo et al.
  Proposes **Melting Pot** as an evaluation suite emphasising generalisation to new social partners and social scenarios, broadening MARL evaluation beyond narrow task overfitting. `MARL`, `evaluation`, `social`


### Datasets and benchmarks

- [**OpenSpiel**](https://github.com/google-deepmind/open_spiel) (2019–) by DeepMind
  A widely used suite of games for reinforcement learning and game-theoretic research (C++/Python). `game-theory`, `RL`, `benchmark` · ![Stars](https://img.shields.io/github/stars/google-deepmind/open_spiel.svg?style=social&label=Star)

- [**PettingZoo**](https://github.com/Farama-Foundation/PettingZoo) (2020–) by Farama Foundation
  A standardised Python API + environment collection for MARL; paired with an academic paper describing the API model (AEC) and design choices. `MARL`, `benchmarks`, `simulation` · ![Stars](https://img.shields.io/github/stars/Farama-Foundation/PettingZoo.svg?style=social&label=Star)

- [**Multi-Agent Particle Environment (MPE)**](https://github.com/openai/multiagent-particle-envs) (2017) by OpenAI (archived)
  Classic particle-world MARL environment used in multiple seminal MARL/communication papers; archived "as-is" and the repo points to maintained variants in PettingZoo. `MARL`, `continuous`, `benchmark` · ![Stars](https://img.shields.io/github/stars/openai/multiagent-particle-envs.svg?style=social&label=Star)

- [**Overcooked-AI**](https://github.com/HumanCompatibleAI/overcooked_ai) (2019–) by HumanCompatibleAI
  Benchmark environment for cooperative coordination (human-AI and AI-AI); includes data links and references to research using the environment. `cooperation`, `human-ai`, `coordination` · ![Stars](https://img.shields.io/github/stars/HumanCompatibleAI/overcooked_ai.svg?style=social&label=Star)

- [**Melting Pot**](https://github.com/google-deepmind/meltingpot) (2021–) by DeepMind
  Multi-agent evaluation suite focused on social interactions and generalisation; repo includes evaluation tooling and documentation. `MARL`, `social`, `evaluation` · ![Stars](https://img.shields.io/github/stars/google-deepmind/meltingpot.svg?style=social&label=Star)

- [**Hanabi Learning Environment**](https://github.com/google-deepmind/hanabi-learning-environment) (2018–2024) by DeepMind (archived)
  Research platform implementing the cooperative game Hanabi as an RL environment; repo is archived (read-only) as of 2024-04-18. `cooperative`, `partial-obs`, `benchmark` · ![Stars](https://img.shields.io/github/stars/google-deepmind/hanabi-learning-environment.svg?style=social&label=Star)

- [**VMAS environments**](https://github.com/proroklab/VectorizedMultiAgentSimulator) (2022–) by Prorok Lab
  A simulator plus a set of multi-robot scenarios; supports vectorised execution for throughput. `robotics`, `simulation`, `MARL` · ![Stars](https://img.shields.io/github/stars/proroklab/VectorizedMultiAgentSimulator.svg?style=social&label=Star)

- [**MAgent2**](https://github.com/Farama-Foundation/MAgent2) (2020–) by Farama Foundation
  Engine for gridworld-like many-agent environments; positioned as maintained fork + separate home for earlier PettingZoo environments. `many-agents`, `simulation`, `MARL` · ![Stars](https://img.shields.io/github/stars/Farama-Foundation/MAgent2.svg?style=social&label=Star)

- [**SMACv2**](https://github.com/oxwhirl/smacv2) (2019–) by WhiRL / Oxford
  Cooperative MARL benchmark in StarCraft II micromanagement scenarios; designed to be API-compatible with SMAC while adding more challenging diversity. `MARL`, `StarCraft`, `benchmark` · ![Stars](https://img.shields.io/github/stars/oxwhirl/smacv2.svg?style=social&label=Star)

- [**SMAC (original)**](https://github.com/oxwhirl/smac) (unspecified) by WhiRL / Oxford
  Predecessor benchmark; useful for historical consistency with older baselines and for papers reporting SMAC results. `MARL`, `StarCraft`, `benchmark`

- [**Hanabi Challenge paper**](https://research.google/pubs/the-hanabi-challenge-a-new-frontier-for-ai-research/) (2020) by Bard et al.
  Introduces Hanabi as an AI challenge domain and a learning environment/framework for research evaluation. `cooperative`, `communication`, `benchmark`

- [**MAPF community + resources**](https://mapf.info/) (unspecified) by MAPF community
  Central community hub for Multi-Agent Path Finding (definitions, materials, publications). `MAPF`, `planning`, `community`

- [**League of Robot Runners / MAPF code archive**](https://github.com/MAPF-Competition/Code-Archive) (unspecified) by MAPF-Competition
  A code archive of competition solutions, explicitly intended to reduce barriers of entry and improve reproducibility for MAPF. `MAPF`, `competition`, `reproducibility`


### Frameworks, libraries, and tools

Framework selection is often the biggest "time sink" decision in MAS work. The list below emphasises language, license, adoption (stars), and maturity signals (active vs archived, release cadence, explicit "beta" disclaimers).

- [**AutoGen**](https://github.com/microsoft/autogen) — Python · MIT (code) + CC-BY-4.0 (docs) · Maintenance mode (succeeded by Agent Framework)
  Multi-agent LLM application framework. ![Stars](https://img.shields.io/github/stars/microsoft/autogen.svg?style=social&label=Star)

- [**CrewAI**](https://github.com/crewAIInc/crewAI) — Python · MIT · Mature/active (industry-oriented)
  Multi-agent workflow orchestration; native MCP and A2A support. ![Stars](https://img.shields.io/github/stars/crewAIInc/crewAI.svg?style=social&label=Star)

- [**Ray**](https://github.com/ray-project/ray) (incl. RLlib) — Python/C++ · Apache-2.0 · Production/active
  Distributed RL training; practical multi-agent RL at scale. ![Stars](https://img.shields.io/github/stars/ray-project/ray.svg?style=social&label=Star)

- [**LangGraph**](https://github.com/langchain-ai/langgraph) — Python · MIT · Mature/active
  Graph-based orchestration for long-running/stateful agents. ![Stars](https://img.shields.io/github/stars/langchain-ai/langgraph.svg?style=social&label=Star)

- [**Swarm**](https://github.com/openai/swarm) — Python · MIT · Experimental/educational
  Lightweight educational framework for multi-agent orchestration (handoffs/tools). ![Stars](https://img.shields.io/github/stars/openai/swarm.svg?style=social&label=Star)

- [**OpenAI Agents SDK**](https://github.com/openai/openai-agents-python) — Python · MIT · Active
  Production multi-agent orchestration with handoffs, guardrails, tracing; successor to Swarm. ![Stars](https://img.shields.io/github/stars/openai/openai-agents-python.svg?style=social&label=Star)

- [**Google ADK**](https://github.com/google/adk-python) — Python/Go/TS/Java · Apache-2.0 · Active
  Code-first toolkit for building, evaluating, and deploying AI agents; MCP tool support. ![Stars](https://img.shields.io/github/stars/google/adk-python.svg?style=social&label=Star)

- [**Microsoft Agent Framework**](https://github.com/microsoft/agent-framework) — Python/.NET · MIT · Active
  Unified multi-agent framework merging AutoGen + Semantic Kernel; graph-based workflows, multi-LLM, OpenTelemetry. ![Stars](https://img.shields.io/github/stars/microsoft/agent-framework.svg?style=social&label=Star)

- [**OpenSpiel**](https://github.com/google-deepmind/open_spiel) — C++/Python · Apache-2.0 · Mature/active
  Games for RL + game theory research. ![Stars](https://img.shields.io/github/stars/google-deepmind/open_spiel.svg?style=social&label=Star)

- [**Mesa**](https://github.com/projectmesa/mesa) — Python · Apache-2.0 · Mature/active
  Agent-based modelling (ABM) in Python; JOSS paper for Mesa 3 (2025). ![Stars](https://img.shields.io/github/stars/projectmesa/mesa.svg?style=social&label=Star)

- [**PettingZoo**](https://github.com/Farama-Foundation/PettingZoo) — Python · MIT · Mature/active
  Standardised MARL environments + API. ![Stars](https://img.shields.io/github/stars/Farama-Foundation/PettingZoo.svg?style=social&label=Star)

- [**TorchRL**](https://github.com/pytorch/rl) — Python · MIT · Active; "beta" disclaimer
  RL library (includes MARL-relevant utilities; used by BenchMARL/VMAS). ![Stars](https://img.shields.io/github/stars/pytorch/rl.svg?style=social&label=Star)

- [**MPE**](https://github.com/openai/multiagent-particle-envs) — Python · MIT · Archived
  Classic particle-world benchmark. ![Stars](https://img.shields.io/github/stars/openai/multiagent-particle-envs.svg?style=social&label=Star)

- [**PyMARL**](https://github.com/oxwhirl/pymarl) — Python · Apache-2.0 · Mature (research)
  Research codebase for cooperative MARL baselines. ![Stars](https://img.shields.io/github/stars/oxwhirl/pymarl.svg?style=social&label=Star)

- [**MARLlib**](https://github.com/Replicable-MARL/MARLlib) — Python/C++ · MIT · Mature (research)
  Unified MARL training across tasks/algorithms (built on Ray/RLlib). ![Stars](https://img.shields.io/github/stars/Replicable-MARL/MARLlib.svg?style=social&label=Star)

- [**NetLogo**](https://github.com/NetLogo/NetLogo) — Scala/Java · GPL-2.0 · Mature/active
  ABM language + modelling environment (strong education + research footprint). ![Stars](https://img.shields.io/github/stars/NetLogo/NetLogo.svg?style=social&label=Star)

- [**BenchMARL**](https://github.com/facebookresearch/BenchMARL) — Python · MIT · Active (research)
  Standardised MARL benchmarking + reporting pipeline. ![Stars](https://img.shields.io/github/stars/facebookresearch/BenchMARL.svg?style=social&label=Star)

- [**VMAS**](https://github.com/proroklab/VectorizedMultiAgentSimulator) — Python · GPL-3.0 · Active (research)
  Vectorised multi-agent robotics simulation for MARL benchmarking. ![Stars](https://img.shields.io/github/stars/proroklab/VectorizedMultiAgentSimulator.svg?style=social&label=Star)

- [**SPADE**](https://github.com/javipalanca/spade) — Python · MIT · Active (niche)
  XMPP-based multi-agent platform. ![Stars](https://img.shields.io/github/stars/javipalanca/spade.svg?style=social&label=Star)

- [**Jason**](https://github.com/jason-lang/jason) — Java · LGPL-3.0 · Active (niche)
  BDI/AgentSpeak interpreter and MAS platform. ![Stars](https://img.shields.io/github/stars/jason-lang/jason.svg?style=social&label=Star)

- [**MASON**](https://github.com/eclab/mason) — Java · View license · Mature (research/edu)
  Multi-agent simulation toolkit. ![Stars](https://img.shields.io/github/stars/eclab/mason.svg?style=social&label=Star)

- [**GAMA Platform**](https://github.com/gama-platform/gama) — Java · GPL-3.0 · Active (niche)
  Spatially explicit ABM simulation environment. ![Stars](https://img.shields.io/github/stars/gama-platform/gama.svg?style=social&label=Star)

- [**NegMAS**](https://github.com/yasserfarouk/negmas) — Python · BSD-3-Clause · Active (niche)
  Automated negotiation library + ecosystem (ANL/SCML agents, bridges). ![Stars](https://img.shields.io/github/stars/yasserfarouk/negmas.svg?style=social&label=Star)

- [**Jadex**](https://github.com/actoron/jadex) — Java · GPL-3.0 · Niche/low activity
  BDI agent platform. ![Stars](https://img.shields.io/github/stars/actoron/jadex.svg?style=social&label=Star)

- [**pyDCOP**](https://github.com/Orange-OpenSource/pyDCOP) — Python · BSD-3-Clause · Archived (2022-10-20)
  DCOP algorithms + experimentation tooling. ![Stars](https://img.shields.io/github/stars/Orange-OpenSource/pyDCOP.svg?style=social&label=Star)


### Competitions and challenges

- [**ANAC leagues listing (ANL, SCML)**](https://scml.cs.brown.edu/) (2026) by Brown University site
  Shows the league structure (Automated Negotiation League; Supply Chain Management League) for ANAC 2026. `negotiation`, `benchmark`

- [**Hanabi Challenge**](https://research.google/pubs/the-hanabi-challenge-a-new-frontier-for-ai-research/) (2020–) by Google Research / community
  A cooperative imperfect-information game used as an AI challenge; the paper introduces an open-source learning environment and evaluation framing. `cooperation`, `communication`, `benchmark`

- [**Automated Negotiating Agents Competition (ANAC)**](https://scml.cs.brown.edu/anac2025) (2010–) by ANAC organisers
  Tournament series for benchmarking automated negotiation strategies; ANAC 2025 page summarises aims and positioning as a practical benchmark. `negotiation`, `competition`, `benchmark`

- [**RoboCup Soccer Simulation League**](https://www.robocup.org/leagues/23) (ongoing) by RoboCup
  Multi-agent team strategy competition in a simulated soccer environment; official page highlights "independently moving software players (agents)". `robotics`, `multi-agent`, `competition`

- [**League of Robot Runners (MAPF competition)**](https://github.com/MAPF-Competition/Code-Archive) (ongoing) by MAPF-Competition
  Competition solution archive intended to lower barrier of entry and support reproducibility for MAPF. `MAPF`, `planning`, `competition`

- [**RoboCup Rescue Simulation "Agent Simulation"**](https://rescuesim.robocup.org/research/publications/agent-competition/) (ongoing) by RoboCup Rescue Simulation
  "Agent Simulation" competition track with publications list curated by organisers; useful for multi-agent disaster response and coordination research context. `robotics`, `simulation`, `coordination`

- [**Supply Chain Management League (SCML)**](https://scml.cs.brown.edu/scml) (unspecified) by SCML organisers
  A negotiation-centric simulation: build an agent negotiating trades for a factory manager in a supply chain setting. `negotiation`, `simulation`, `markets`

- [**Multi-Agent Programming Contest (MAPC)**](https://multiagentcontest.org/) (unspecified) by MAPC organisers
  Long-running contest emphasising engineering of MAS that coordinate in a shared environment (often used in agent programming education/research). `MAS-engineering`, `coordination`, `competition`


### Agent interoperability protocols

A fast-emerging layer in LLM-based multi-agent systems: open protocols standardising how agents connect to tools, communicate with each other, and interact with users. Governance is converging under the **Agentic AI Foundation (AAIF)**, a Linux Foundation directed fund co-founded by Anthropic, Block, Google, Microsoft, and OpenAI (formed December 2025).

- [**Model Context Protocol (MCP)**](https://github.com/modelcontextprotocol) — Tool/context access · Anthropic / AAIF (2024) · MIT
  An open standard providing a universal JSON-RPC interface for AI applications to connect to external tools, data sources, and services — "USB-C for AI." Adopted by OpenAI, Google, Microsoft, and 10,000+ production servers. Donated to the Linux Foundation (AAIF) in Dec 2025. [Spec](https://modelcontextprotocol.io) · ![Stars](https://img.shields.io/github/stars/modelcontextprotocol/servers.svg?style=social&label=Star)

- [**Agent2Agent Protocol (A2A)**](https://github.com/a2aproject/A2A) — Agent-to-agent · Google / AAIF (2025) · Apache-2.0
  An open protocol for cross-framework agent-to-agent communication: discovery via Agent Cards, task negotiation, and multimodal collaboration without exposing internal logic. 150+ partner organisations; donated to Linux Foundation in June 2025. Absorbed IBM's ACP. [Spec](https://a2a-protocol.org/latest/) · ![Stars](https://img.shields.io/github/stars/a2aproject/A2A.svg?style=social&label=Star)

- [**AGENTS.md**](https://github.com/agentsmd/agents.md) — Agent instructions · OpenAI / AAIF (2025) · MIT
  A simple, open markdown convention providing AI coding agents with project-specific instructions (build commands, code style, testing rules); adopted by 60,000+ repositories and supported by all major AI coding tools. ![Stars](https://img.shields.io/github/stars/agentsmd/agents.md.svg?style=social&label=Star)

- [**AG-UI (Agent-User Interaction Protocol)**](https://github.com/ag-ui-protocol/ag-ui) — Agent-to-user · CopilotKit (2025) · MIT
  An open, event-based protocol standardising real-time bidirectional communication between AI agent backends and frontend applications; enables generative UI, state synchronisation, and human-in-the-loop collaboration. ![Stars](https://img.shields.io/github/stars/ag-ui-protocol/ag-ui.svg?style=social&label=Star)

- [**Agent Network Protocol (ANP)**](https://github.com/agent-network-protocol/AgentNetworkProtocol) — Decentralised networking · ANP community (2024) · MIT
  A W3C-aligned protocol for decentralised agent identity, discovery, and communication using a three-layer architecture built on DIDs and Verifiable Credentials; aims to be the networking layer for the "Agentic Web." ![Stars](https://img.shields.io/github/stars/agent-network-protocol/AgentNetworkProtocol.svg?style=social&label=Star)


## Reproducibility and community

### Reproducibility resources and code

- [**NeurIPS Paper Checklist (reproducibility + transparency)**](https://neurips.cc/public/guides/PaperChecklist) (2025) by NeurIPS
  The checklist is explicitly described as encouraging best practices for reproducibility, transparency, ethics, and societal impact, and is part of submission requirements. `reproducibility`, `reporting`, `community`

- [**BenchMARL**](https://github.com/facebookresearch/BenchMARL) (2024) by Facebook Research
  Explicitly designed around reproducibility and standardisation of MARL experiments; includes configuration discipline and benchmarking abstractions. `MARL`, `reproducibility`, `benchmarking`

- [**MARLlib**](https://github.com/Replicable-MARL/MARLlib) (2022–2023) by Replicable-MARL
  Emphasises standardised wrappers and policy mapping to reduce compatibility friction; provides a codebase associated with both arXiv and JMLR versions. `MARL`, `reproducibility`, `library`

- [**MAPF competition code archive**](https://github.com/MAPF-Competition/Code-Archive) (ongoing) by MAPF-Competition
  Reproducibility mechanism in a competition context (collects top implementations yearly) to help newcomers and facilitate comparisons. `MAPF`, `reproducibility`, `competition`

- [**OpenReview**](https://openreview.net/about) (ongoing) by OpenReview (nonprofit)
  A peer review + publishing infrastructure used by major ML venues; useful for reading reviews, comparing revisions, and tracking reproducibility discussions. `peer-review`, `reproducibility`, `community`

- [**MARL papers with code (curated)**](https://github.com/TimeBreaker/MARL-papers-with-code) (unspecified) by TimeBreaker (community)
  A community-maintained catalogue of MARL papers with code; useful as a quick "code exists?" discovery layer (not a primary source for claims). `MARL`, `code`, `index`


### Community resources

- [**AAMAS conference**](https://cyprusconferences.org/aamas2026/) (2026) by AAMAS organisers
  Flagship MAS venue; AAMAS 2026 dates are 25–29 May 2026 in Paphos, Cyprus. `conference`, `MAS`, `community`

- [**Agentic AI Foundation (AAIF)**](https://aaif.io/) (2025) by Linux Foundation
  Industry governance body for open agentic standards (stewards MCP, A2A, AGENTS.md); platinum members include AWS, Anthropic, Block, Google, Microsoft, and OpenAI. `standards`, `governance`, `LLM-agents`

- [**EUMAS (European Conference on MAS)**](https://euramas.github.io/eumas2025/) (2025) by EUMAS organisers
  European venue specifically focused on MAS research, complementary to broader AI conferences. `conference`, `MAS`

- [**AAMAS workshops**](https://aamas2025.org/index.php/conference/program/accepted-workshops/) (2025) by AAMAS organisers
  Workshops pages are useful for tracking subcommunity focus areas (emerging topics, nascent benchmarks). `workshops`, `community`

- [**IFAAMAS (organising association)**](https://www.ifaamas.org/) (ongoing) by IFAAMAS
  Association representing autonomous agents and MAS, distributing knowledge through conferences and related activities. `community`, `MAS`

- [**EURAMAS**](https://sites.google.com/view/euramas/) (ongoing) by European Association for Multi-Agent Systems
  Community hub for European MAS activities (EASSS, EUMAS, etc.). `community`, `Europe`, `MAS`

- [**RoboCup Soccer Simulation League + mailing list**](https://www.robocup.org/leagues/23) (ongoing) by RoboCup
  Official league page describes the simulation league and points to an official mailing list. `robotics`, `simulation`, `community`

- [**NetLogo community channels**](https://github.com/NetLogo/NetLogo) (ongoing) by NetLogo maintainers
  The NetLogo repo points to a user group, forum, and a developer list (`netlogo-devel`), supporting community troubleshooting and extension. `ABM`, `simulation`, `community`

- [**MAPF community portal**](https://mapf.info/) (unspecified) by MAPF community
  Centralised MAPF info and materials; useful for MAS planning researchers and competition participants. `MAPF`, `planning`, `community`


## Contribution guidelines and curation criteria

### Contribution guidelines

Contributions are welcome via pull requests. Aim to keep entries **curated, not exhaustive**.

Recommended workflow:
1. Add a single item to the appropriate list (or propose a new subcategory if clearly necessary).
2. Ensure each entry includes all required metadata:
   - **Title**
   - **Authors/Maintainers**
   - **Year** (or `unspecified`)
   - **Annotation** (1–3 sentences; focus on significance and appropriate use)
   - **Link** (prefer official/publisher/proceedings/arXiv/GitHub)
   - **Tags**
3. For tools, include **language + license + maturity + stars** (or mark unknown values as `unspecified`).
4. Prefer one strong primary source over multiple secondary blog posts.

### Curation criteria

An entry is likely to be accepted if it satisfies most of:
- **Primary/official source**: original paper (arXiv/DOI/proceedings) or official repository/organisation page.
- **Research relevance**: directly informs MAS theory, algorithms, evaluation protocols, or reproducible tooling.
- **Demonstrated impact**: strong citations, adoption, or clear "milestone" status (historical shaping).
- **Reproducibility**: code, data, benchmarks, or explicit evaluation methodology where applicable.
- **Clarity and neutrality**: annotation states what it is good for, limitations, and typical use contexts.
