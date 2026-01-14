# Sun et al. (2025) - Game Theory Meets LLM Survey

## Bibliographic Information
- **Title**: Game Theory Meets Large Language Models: A Systematic Survey with Taxonomy and New Frontiers
- **Authors**: Haoran Sun, Yusen Wu, Peng Wang et al.
- **Year**: 2025
- **arXiv ID**: 2502.09053v2
- **PDF**: https://arxiv.org/pdf/2502.09053v2
- **Categories**: cs.AI, cs.GT, cs.LG

---

## Core Contribution

**First comprehensive survey** of the bidirectional relationship between Game Theory and LLMs:
1. Using game theory to evaluate LLM behavior
2. Using game theory to improve LLM design
3. Using LLMs to solve game-theoretic problems
4. Emerging LLM-game research frontiers

---

## Key Concepts

### Four-Way Taxonomy

| Direction | Description | Examples |
|-----------|-------------|----------|
| GT → Evaluate LLM | Use games to test LLM rationality | Behavioral Turing tests |
| GT → Design LLM | Game-theoretic training objectives | RLHF as principal-agent |
| LLM → Solve GT | LLMs as game players/solvers | Equilibrium computation |
| New Frontiers | Emerging intersections | Multi-agent LLM games |

---

## Relevance to Project

### Direct Relevance: *****

This survey provides **comprehensive context** for the project:
- Documents state of LLM behavioral testing
- Reviews game-theoretic LLM design
- Identifies research gaps we address

### Coverage of Project-Relevant Topics

| Topic | Coverage in Survey | Our Addition |
|-------|-------------------|--------------|
| LLM in strategic games | Extensive | Add psychological games |
| Cooperation/defection | Well-covered | Add belief-dependent preferences |
| Human-AI interaction | Limited | Our main contribution |
| Evolutionary dynamics | Not covered | P1, P2 contributions |
| Stochastic stability | Not covered | P1 methodology |

---

## Key Findings from Survey

### LLM Behavioral Regularities
1. LLMs show **bounded rationality** in games
2. **Context-dependent** behavior (prompt sensitivity)
3. **More cooperative** than human average in many settings
4. **Theory of Mind** capabilities emerging in larger models

### Game-Theoretic LLM Design
1. RLHF as **principal-agent problem**
2. **Mechanism design** for alignment
3. **Multi-objective** optimization challenges

### Open Questions (from survey)
1. How do LLMs form and update beliefs?
2. Can LLMs engage in recursive reasoning?
3. What game-theoretic solution concepts apply?

---

## Connection to Project Papers

| Project Paper | Survey Connection |
|---------------|------------------|
| P1 (Stochastic Stability) | Extends GT→Evaluate with dynamics |
| P2 (Imitation + Spite) | New behavioral mechanism not in survey |
| P3 (Attributed Belief EQ) | Addresses belief formation gap |
| Pilot Experiment | Contributes to GT→Evaluate stream |

---

## Papers Cited We Should Review

The survey cites several papers relevant to our project:

### High Priority
- Akata et al. (2023) - Playing repeated games with LLMs
- Park et al. (2023) - Generative agents simulate human behavior
- Horton (2023) - LLMs as simulated economic agents

### Medium Priority
- Phelps & Russell (2023) - LLMs operationalizing prompts in PD
- Brookins & DeBacker (2023) - LLM decision-making in games

---

## Quotes

> "Game theory is a foundational framework for analyzing strategic interactions, and its intersection with large language models (LLMs) is a rapidly growing field."

> "This paper provides the first comprehensive survey of the bidirectional relationship between Game Theory and LLMs."

---

## Implications for Project Positioning

### Our Contribution Relative to Survey
1. **First** to extend to psychological game theory
2. **First** to analyze evolutionary dynamics with LLM agents
3. **First** to propose equilibrium concept for human-AI psychological games
4. **First** experimental test of belief attribution to AI

### Positioning Statement
"While Sun et al. (2025) comprehensively survey game-theoretic approaches to LLM behavior, they do not address belief-dependent preferences central to psychological game theory. Our project fills this gap..."

---

## Citation

```bibtex
@article{sun2025game,
  title={Game Theory Meets Large Language Models: A Systematic Survey with Taxonomy and New Frontiers},
  author={Sun, Haoran and Wu, Yusen and Wang, Peng and others},
  journal={arXiv preprint arXiv:2502.09053},
  year={2025}
}
```

---

*Note created: 2026-01-11*
