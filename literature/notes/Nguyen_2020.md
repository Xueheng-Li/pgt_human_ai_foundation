# Nguyen et al. (2020) - Theory of Mind with Guilt Aversion in RL

## Bibliographic Information
- **Title**: Theory of Mind with Guilt Aversion Facilitates Cooperative Reinforcement Learning
- **Authors**: Dung Nguyen, Svetha Venkatesh, Phuoc Nguyen et al.
- **Year**: 2020
- **arXiv ID**: 2009.07445v1
- **PDF**: https://arxiv.org/pdf/2009.07445v1
- **Categories**: cs.AI

---

## Core Contribution

Introduces **ToMAGA (Theory of Mind Agents with Guilt Aversion)** - RL agents equipped with:
1. Theory of Mind capability
2. Guilt aversion mechanism

Shows that guilt aversion (from psychological game theory) can be operationalized in artificial agents to enhance cooperation.

---

## Key Concepts

### Guilt Aversion in AI
- Agents experience utility loss when they believe they disappointed others
- Requires modeling what other agents expect (second-order beliefs)
- Promotes cooperative behavior similar to humans

### Theory of Mind Implementation
- Agents maintain beliefs about other agents' beliefs
- Recursive reasoning about expectations
- Computational implementation of belief hierarchies

---

## Relevance to Project

### Direct Relevance: *****

This paper is **critical** for P3 (Attributed Belief Equilibrium):
- Demonstrates guilt aversion can be implemented in artificial agents
- Provides computational framework for belief hierarchies in AI
- Shows cooperation enhancement through psychological mechanisms

### Key Questions Raised
1. Can indignation (not just guilt) be similarly implemented?
2. How do humans perceive AI with ToM vs. without?
3. What happens when AI's guilt parameter is transparent to humans?

---

## Technical Details

### Agent Architecture
- ToM module: Models other agents' beliefs and expectations
- Guilt module: Computes disutility from expectation violations
- RL backbone: Standard policy optimization with modified reward

### Experimental Setup
- Multi-agent cooperation games
- Comparison: Standard RL vs. ToMAGA
- Metrics: Cooperation rate, social welfare

---

## Key Results

1. **ToMAGA agents cooperate more** than standard RL agents
2. **Guilt mechanism is essential** - ToM alone insufficient
3. **Scalability**: Works in complex multi-agent settings

---

## Connection to Project Papers

| Project Paper | Connection |
|---------------|------------|
| P1 (Stochastic Stability) | Provides AI agent specification with belief-dependent utility |
| P2 (Imitation + Spite) | ToMAGA as alternative to prosocial AI specification |
| P3 (Attributed Belief EQ) | Computational foundation for AI belief structures |

---

## Limitations and Extensions

### Limitations
- Assumes AI can accurately model human beliefs
- Doesn't address human attribution of beliefs to AI
- Symmetric treatment (both players are AI)

### Extensions Needed for Project
- Asymmetric case: Human with genuine beliefs + AI with simulated beliefs
- Attribution function: How humans construct $\tilde{E}_i^{(2,j)}$ for AI
- Heterogeneous populations with mixed human-AI

---

## Quotes

> "Guilt aversion induces experience of a utility loss in people if they believe they have disappointed others, and this promotes cooperative behaviour in human."

> "We aim to build a new kind of affective reinforcement learning agents...equipped with an ability to think about other agents' mental states."

---

## Citation

```bibtex
@article{nguyen2020theory,
  title={Theory of Mind with Guilt Aversion Facilitates Cooperative Reinforcement Learning},
  author={Nguyen, Dung and Venkatesh, Svetha and Nguyen, Phuoc and others},
  journal={arXiv preprint arXiv:2009.07445},
  year={2020}
}
```

---

*Note created: 2026-01-11*
