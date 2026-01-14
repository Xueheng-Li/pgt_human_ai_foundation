# Tennant, Hailes & Musolesi (2023) - Moral Choices in Social Dilemmas with MARL

## Bibliographic Information
- **Title**: Modeling Moral Choices in Social Dilemmas with Multi-Agent Reinforcement Learning
- **Authors**: Elizaveta Tennant, Stephen Hailes, Mirco Musolesi
- **Year**: 2023
- **arXiv ID**: 2301.08491v3
- **PDF**: https://arxiv.org/pdf/2301.08491v3
- **Categories**: cs.MA, cs.AI, cs.LG

---

## Core Contribution

Studies **moral choices in social dilemmas** using Multi-Agent Reinforcement Learning (MARL):
- Bottom-up approach to ethical AI
- Agents learn moral behavior through interaction
- Focuses on emergent cooperation in social dilemmas

---

## Key Concepts

### Bottom-Up vs. Top-Down Ethics
- **Top-down**: Pre-specify ethical rules → risky, inflexible
- **Bottom-up**: Learn ethical behavior → adaptive, emergent
- This paper: Bottom-up MARL approach

### Social Dilemmas as Moral Testbed
- Prisoner's Dilemma
- Public Goods Game
- Commons dilemmas
- Tests cooperation, fairness, punishment

---

## Relevance to Project

### Direct Relevance: ****

Provides MARL framework for studying moral behavior:
- Complements game-theoretic approach
- Shows cooperation can emerge from learning
- Relevant to AI design for prosociality

### Key Questions Raised
1. Does learned cooperation differ from programmed cooperation?
2. How do humans perceive AI that "learned" to cooperate?
3. Can MARL agents develop indignation-like responses?

---

## Technical Details

### MARL Framework
- Multiple agents learning simultaneously
- Environment: Social dilemma games
- Reward structure: Individual + social components
- Learning: Deep RL with various algorithms

### Moral Behavior Metrics
- Cooperation rate
- Punishment patterns
- Reciprocity
- Fairness (distributional outcomes)

---

## Key Results

1. **Cooperation can emerge** from MARL in social dilemmas
2. **Environment structure** affects moral learning
3. **Reward shaping** crucial for desired outcomes
4. **Stable cooperation** requires appropriate mechanisms

---

## Connection to Project Papers

| Project Paper | Connection |
|---------------|------------|
| P1 (Stochastic Stability) | Learning dynamics vs. evolutionary dynamics |
| P2 (Imitation + Spite) | Spite as emergent or programmed? |
| P3 (Attributed Belief EQ) | Do learned agents have "beliefs"? |
| Pilot Experiment | Test human responses to learned vs. programmed AI |

---

## Implications for AI Design

### Design Choice: Programmed vs. Learned Prosociality

| Aspect | Programmed ($\gamma$) | Learned (MARL) |
|--------|---------------------|----------------|
| Predictability | High | Lower |
| Adaptability | Low | High |
| Transparency | Clear | Opaque |
| Human attribution | Design intent | Emergent agency |

### Research Question
Do humans attribute more intentionality to AI that "learned" cooperation vs. AI "programmed" to cooperate?

---

## Methodological Notes

### Applicable Techniques
- MARL training environments
- Social dilemma testbeds
- Metrics for moral behavior
- Comparison frameworks

### Limitations for Our Project
- No belief-dependent preferences
- No explicit psychological game structure
- No human subjects in experiments
- Focus on AI-AI, not human-AI

---

## Quotes

> "Practical uses of Artificial Intelligence (AI) in the real world have demonstrated the importance of embedding moral choices into intelligent agents."

> "A bottom-up learning approach may be more appropriate for studying and developing ethical behavior in AI agents."

---

## Citation

```bibtex
@article{tennant2023modeling,
  title={Modeling Moral Choices in Social Dilemmas with Multi-Agent Reinforcement Learning},
  author={Tennant, Elizaveta and Hailes, Stephen and Musolesi, Mirco},
  journal={arXiv preprint arXiv:2301.08491},
  year={2023}
}
```

---

*Note created: 2026-01-11*
