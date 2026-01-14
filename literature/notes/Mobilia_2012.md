# Mobilia (2012) - Stochastic Dynamics with Cooperation Facilitators

## Bibliographic Information
- **Title**: Stochastic dynamics of the prisoner's dilemma with cooperation facilitators
- **Authors**: Mauro Mobilia
- **Year**: 2012
- **arXiv ID**: 1207.2072v2
- **PDF**: https://arxiv.org/pdf/1207.2072v2
- **Categories**: q-bio.PE, cond-mat.stat-mech, nlin.AO, physics.soc-ph

---

## Core Contribution

Analyzes **stochastic evolutionary dynamics** in the Prisoner's Dilemma with a special class of agents: **cooperation facilitators**.

Key mechanism: Facilitators enhance cooperator fitness without affecting defector fitness.

---

## Key Concepts

### Cooperation Facilitators
- Small number of agents who boost cooperator payoffs
- Do not play the game directly
- Enhance the environment for cooperation
- Analogous to AI that provides "cooperation subsidy"

### Stochastic Dynamics
- Finite population analysis
- Birth-death process
- Fixation probabilities
- Mean fixation times

### Selection and Drift
- Weak selection limit analyzed
- Interplay of selection and genetic drift
- Size effects on cooperation survival

---

## Relevance to Project

### Direct Relevance: ****

Provides **stochastic analysis template** for P1:
- Finite population methods
- Facilitator as AI analog
- Fixation probability calculations

### Key Mapping

| Their Concept | Our Concept |
|---------------|-------------|
| Cooperation facilitator | Prosocial AI ($\gamma > 0$) |
| Facilitator number | AI population share $(1-\alpha)$ |
| Enhanced cooperator fitness | Interaction with AI |
| Stochastic dynamics | Evolutionary learning with errors |

---

## Technical Details

### Model Setup
- Prisoner's Dilemma: C vs D
- Population size $N$
- $n_F$ cooperation facilitators (fixed)
- Moran process dynamics

### Fitness Functions
Without facilitators:
$$f_C = 1 + w(Rc - Sc')$$
$$f_D = 1 + w(Tc - Pc')$$

With facilitators (boost to cooperators):
$$f_C' = f_C + \delta \cdot n_F$$

### Key Results
- Fixation probability of cooperation: $\rho_C(n_F)$
- Critical facilitator number for $\rho_C > 1/N$
- Mean time to fixation

---

## Key Results

1. **Facilitators promote cooperation** even in small numbers
2. **Critical threshold** exists for cooperation to be favored
3. **Population size matters**: Larger populations need more facilitators
4. **Stochastic effects** can help or hurt cooperation

---

## Connection to Project Papers

| Project Paper | Connection |
|---------------|------------|
| P1 (Stochastic Stability) | Methods for finite population analysis |
| P2 (Imitation + Spite) | Alternative mechanism to spite |
| P3 (Attributed Belief EQ) | Facilitators don't need beliefs |
| Pilot Experiment | Test facilitator interpretation of AI |

---

## Mathematical Framework

### Fixation Probability
For Moran process:
$$\rho_C = \frac{1}{1 + \sum_{k=1}^{N-1} \prod_{j=1}^{k} \frac{T_j^-}{T_j^+}}$$

where $T_j^+$ and $T_j^-$ are transition rates.

### With Facilitators
Transition rates modified:
$$T_j^+ = \frac{j(N-j)}{N} \cdot \frac{f_C'}{j \cdot f_C' + (N-j) \cdot f_D}$$

### Weak Selection Expansion
$$\rho_C \approx \frac{1}{N} + \frac{w}{N} \cdot g(n_F, N, \text{payoffs})$$

---

## Implications for P1 Analysis

### Extension Needed
Replace facilitators with strategic AI agents:
- AI plays the game (not just facilitates)
- AI has own payoff structure
- AI strategy affects human fitness directly

### Type-Dependent Analysis
- Distinguish human-human, human-AI, AI-AI interactions
- Different payoff modifications for each
- Aggregate to population dynamics

---

## Quotes

> "The presence of a small number of cooperation facilitators enhances the fitness (reproductive potential) of cooperators, while it does not alter that of defectors."

> "In a finite population of size N, we analyze the stochastic evolutionary dynamics of this system."

---

## Citation

```bibtex
@article{mobilia2012stochastic,
  title={Stochastic dynamics of the prisoner's dilemma with cooperation facilitators},
  author={Mobilia, Mauro},
  journal={arXiv preprint arXiv:1207.2072},
  year={2012}
}
```

---

*Note created: 2026-01-11*
