# Guo (2023) - GPT in Game Theory Experiments

## Bibliographic Information
- **Title**: GPT in Game Theory Experiments
- **Authors**: Fulin Guo
- **Year**: 2023
- **arXiv ID**: 2305.05516v2
- **PDF**: https://arxiv.org/pdf/2305.05516v2
- **Categories**: econ.GN

---

## Core Contribution

Explores using GPT in strategic game experiments:
- **Ultimatum Game**: Tests fairness and rejection behavior
- **Prisoner's Dilemma**: Tests cooperation and reciprocity

Designs prompts to enable GPT to understand game rules and generate both choices and reasoning.

---

## Key Concepts

### Prompt Engineering for Games
- Clear game rule specification
- Role assignment (proposer/responder)
- Reasoning elicitation
- Strategy verbalization

### GPT Behavioral Patterns
- Makes positive offers (ultimatum game)
- Rejects unfair offers
- Conditional cooperation (PD)
- Reasoning resembles human justifications

---

## Relevance to Project

### Direct Relevance: ****

Complements Mei et al. (2024) with:
- Earlier publication (GPT-3.5 era)
- Focus on reasoning, not just behavior
- Simpler experimental design
- More accessible replication

### Key Findings for Project

| Finding | Implication |
|---------|-------------|
| GPT offers fair splits | Supports prosociality assumption |
| GPT rejects unfair offers | Has "indignation-like" behavior |
| GPT cooperates conditionally | Strategy-dependent cooperation |
| GPT articulates reasons | May enable belief attribution |

---

## Technical Details

### Experimental Design
- Single-shot games
- Multiple prompt variations
- Temperature settings tested
- Response parsing methodology

### Ultimatum Game Results
- GPT typically offers 40-50%
- Rejects offers below 20-30%
- Reasoning cites "fairness" concepts

### Prisoner's Dilemma Results
- Conditional cooperation observed
- Responds to partner's history
- Articulates reciprocity logic

---

## Key Results

1. **GPT exhibits human-like behavior** in strategic games
2. **Reasoning is articulable** and often coherent
3. **Prompt sensitivity** affects behavior significantly
4. **Context matters**: Framing changes responses

---

## Connection to Project Papers

| Project Paper | Connection |
|---------------|------------|
| P1 (Stochastic Stability) | GPT as potential AI agent type |
| P2 (Imitation + Spite) | GPT's rejection behavior relates to spite |
| P3 (Attributed Belief EQ) | GPT reasoning as basis for attribution |
| Pilot Experiment | Methodological guidance |

---

## Methodological Implications

### For Our Pilot Experiment
1. **Prompt design matters**: Need standardized prompts
2. **Reasoning elicitation**: Can probe AI "intentions"
3. **Replication**: Single-shot vs. repeated games differ
4. **Temperature**: Affects variability of responses

### Human Attribution Questions
- Does seeing GPT's reasoning affect human attribution?
- Do humans interpret GPT reasoning as "genuine beliefs"?
- Can reasoning transparency increase/decrease cooperation?

---

## Comparison with Later Work

| Aspect | Guo (2023) | Mei et al. (2024) |
|--------|-----------|------------------|
| Model | GPT-3.5 | GPT-4 |
| Games | UG, PD | Trust, DG, risk, Big-5 |
| Focus | Reasoning | Behavioral equivalence |
| Sample | Small | Large, systematic |
| Finding | Human-like | Indistinguishable |

Evolution from "human-like" to "indistinguishable" over one year.

---

## Limitations

1. **Single model tested** (GPT-3.5)
2. **Limited game repertoire**
3. **No human comparison sample**
4. **Prompt-dependent results**

### Our Extensions
- Test with human partners
- Include belief measures
- Add punishment options
- Measure attribution explicitly

---

## Quotes

> "GPT exhibits behaviours similar to human responses, such as making positive offers and rejecting unfair ones in the ultimatum game."

> "Conditional cooperation in the prisoner's dilemma... GPT responds to the other player's previous choices."

---

## Citation

```bibtex
@article{guo2023gpt,
  title={GPT in Game Theory Experiments},
  author={Guo, Fulin},
  journal={arXiv preprint arXiv:2305.05516},
  year={2023}
}
```

---

*Note created: 2026-01-11*
