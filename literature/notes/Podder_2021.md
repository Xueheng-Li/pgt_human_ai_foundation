# Podder, Righi & Pancotto (2021) - Reputation and Punishment in Optional PGG

## Bibliographic Information
- **Title**: Reputation and Punishment sustain cooperation in the Optional Public Goods Game
- **Authors**: Shirsendu Podder, Simone Righi, Francesca Pancotto
- **Year**: 2021
- **arXiv ID**: 2110.02031v1
- **PDF**: https://arxiv.org/pdf/2110.02031v1
- **Categories**: q-bio.PE

---

## Core Contribution

Studies the **Optional Public Goods Game** with:
1. **Loner strategy**: Option to not participate
2. **Reputation system**: Tracks past behavior
3. **Punishment**: Both prosocial and antisocial

Shows how reputation and punishment interact to sustain cooperation.

---

## Key Concepts

### Three-Strategy Cycle
Without punishment: Cooperator → Defector → Loner → Cooperator
- C beats L (cooperation payoff > loner payoff)
- D beats C (defection exploits cooperation)
- L beats D (loners avoid exploitation)

### Prosocial vs. Antisocial Punishment
- **Prosocial**: Cooperators punish defectors
- **Antisocial**: Defectors punish cooperators
- Both affect evolution of strategies

### Reputation
- Tracks cooperation history
- Affects who gets punished
- May affect willingness to punish

---

## Relevance to Project

### Direct Relevance: ****

Provides framework for experimental design:
- Optional participation (abstention)
- Reputation effects
- Punishment mechanisms
- Cyclic dynamics

### Implications for AI in Social Dilemmas
- AI could be perceived as "always participating" (no loner option)
- AI reputation may be transparent (programmed)
- Human punishment of AI: prosocial or antisocial?

---

## Technical Details

### Model Setup
- Optional Public Goods Game
- Four strategies: C (cooperate), D (defect), L (loner), P (punishing cooperator)
- Evolutionary dynamics on networks
- Reputation updating rules

### Key Parameters
- Punishment cost and fine
- Reputation threshold
- Network structure
- Multiplication factor

---

## Key Results

1. **Reputation + Punishment** together sustain cooperation
2. **Antisocial punishment** undermines cooperation significantly
3. **Loner option** provides escape from defector dominance
4. **Network structure** affects reputation efficacy

---

## Connection to Project Papers

| Project Paper | Connection |
|---------------|------------|
| P1 (Stochastic Stability) | Stability with abstention option |
| P2 (Imitation + Spite) | Spite as antisocial punishment |
| P3 (Attributed Belief EQ) | Reputation as observable belief proxy |
| Pilot Experiment | Design with optional participation |

---

## Experimental Design Implications

### For Pilot Experiment

| Feature | Implementation |
|---------|---------------|
| Abstention | Allow "sit out" option |
| Reputation | Display past behavior |
| Punishment | Costly punishment stage |
| AI reputation | Transparent vs. hidden |

### Treatment Variations
1. AI reputation visible vs. hidden
2. AI behavior history shown vs. not shown
3. Human punishment of AI allowed vs. not

---

## Theoretical Extensions Needed

### For Human-AI Settings
1. How does AI "reputation" form when behavior is deterministic?
2. Does transparent AI design ($\gamma$) substitute for reputation?
3. Is human punishment of AI "prosocial" or "misplaced"?

### Mathematical Framework
Extend their model:
$$U_i = \pi_i(a) - c \cdot \text{punish}_i - \beta \cdot \mathbb{1}_{a_i=D} \cdot E_i^{(2)}$$

Add indignation to punishment decision.

---

## Quotes

> "While prosocial punishment can help increase cooperation, anti-social punishment -- where defectors punish cooperators -- can hamper cooperation substantially."

> "The introduction of the 'Loner' strategy allows players to withdraw from the game, which leads to a cooperator-defector-loner cycle."

---

## Citation

```bibtex
@article{podder2021reputation,
  title={Reputation and Punishment sustain cooperation in the Optional Public Goods Game},
  author={Podder, Shirsendu and Righi, Simone and Pancotto, Francesca},
  journal={arXiv preprint arXiv:2110.02031},
  year={2021}
}
```

---

*Note created: 2026-01-11*
