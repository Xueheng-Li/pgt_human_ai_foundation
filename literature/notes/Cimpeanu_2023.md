# Cimpeanu, Pereira & Han (2023) - Guilt Evolution

## Bibliographic Information
- **Title**: The evolutionary advantage of guilt: co-evolution of social and non-social guilt in structured populations
- **Authors**: Theodor Cimpeanu, Luis Moniz Pereira, The Anh Han
- **Year**: 2023
- **arXiv ID**: 2302.09859v2
- **PDF**: https://arxiv.org/pdf/2302.09859v2
- **Categories**: cs.MA, cs.AI, cs.CY, math.DS, nlin.AO

---

## Core Contribution

Studies the **co-evolution of two forms of guilt**:
1. **Social guilt**: Requires understanding others' internal states (costly)
2. **Non-social guilt**: Self-referential, only involves own actions (cheaper)

Investigates how both evolve in structured populations and their effects on cooperation.

---

## Key Concepts

### Two Types of Guilt

| Type | Definition | Cost | ToM Required? |
|------|------------|------|---------------|
| Social | Disutility from disappointing others' expectations | High | Yes |
| Non-social | Disutility from violating own standards | Low | No |

### Evolutionary Dynamics
- Population structure affects which guilt type dominates
- Network effects on guilt evolution
- Co-evolution with cooperation strategies

---

## Relevance to Project

### Direct Relevance: *****

This paper is **essential** for understanding AI design choices in P1-P3:
- AI could be programmed with social guilt (requires ToM) vs. non-social guilt (simpler)
- Design choice affects human attribution of intentionality
- Provides framework for heterogeneous guilt in populations

### Key Implications for Project
1. AI with social guilt may be perceived differently than AI with non-social guilt
2. Co-evolution framework applicable to mixed human-AI populations
3. Cost of ToM matters for AI design and scalability

---

## Technical Details

### Model Structure
- Agents on networks (structured populations)
- Strategy space: Cooperate/Defect + Guilt type
- Payoff modified by guilt experience
- Evolutionary dynamics with imitation

### Key Parameters
- Guilt intensity (similar to indignation intensity $\beta$ in Li 2026)
- Network structure (degree, clustering)
- Cost of social vs. non-social guilt

---

## Key Results

1. **Social guilt can evolve** despite higher cost when network structure supports it
2. **Non-social guilt dominates** in well-mixed populations
3. **Both types coexist** in certain parameter regimes
4. **Cooperation increases** with either guilt type, but social guilt more effective

---

## Connection to Project Papers

| Project Paper | Connection |
|---------------|------------|
| P1 (Stochastic Stability) | Guilt type affects resistance calculations |
| P2 (Imitation + Spite) | Guilt mechanisms interact with spite |
| P3 (Attributed Belief EQ) | Social guilt requires belief attribution |
| Pilot Experiment | Test human punishment of AI with/without social guilt |

---

## Design Implications for AI

### Option 1: AI with Social Guilt
- Pro: More human-like, potentially better cooperation
- Con: Requires ToM capability, computationally expensive
- Human perception: May attribute more intentionality

### Option 2: AI with Non-Social Guilt
- Pro: Simpler, scalable
- Con: May appear mechanical, less effective cooperation
- Human perception: May see as mere rule-following

### Option 3: AI without Guilt (Pure Prosociality γ)
- Pro: Simplest design, transparent
- Con: Misses psychological mechanisms
- Human perception: Clearly artificial

---

## Quotes

> "Building ethical machines may involve bestowing upon them the emotional capacity to self-evaluate and repent on their actions."

> "Social guilt entails a cost, requiring agents to exert efforts to understand others' internal states and behaviours."

---

## Citation

```bibtex
@article{cimpeanu2023evolutionary,
  title={The evolutionary advantage of guilt: co-evolution of social and non-social guilt in structured populations},
  author={Cimpeanu, Theodor and Pereira, Luis Moniz and Han, The Anh},
  journal={arXiv preprint arXiv:2302.09859},
  year={2023}
}
```

---

*Note created: 2026-01-11*
