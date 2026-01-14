# Attributed Belief Equilibrium

> Extending Psychological Game Theory to Human-AI Interactions

---

## Research Question

When humans have belief-dependent preferences (indignation, guilt) but AI agents have design-dependent objectives, what equilibrium concept applies?

## Core Innovation

**Attributed Belief Equilibrium (ABE)** - A new solution concept for games where:
- Humans form genuine belief hierarchies about other humans
- Humans *attribute* beliefs to AI agents (even though AI lack mental states)
- AI optimize design-defined objectives, not belief-dependent utilities

The **attribution function** $\phi_i(\theta_j, x_j, \omega_i)$ captures how human $i$ projects beliefs onto AI $j$ based on:
- AI design parameters $\theta_j$ (e.g., prosociality)
- Observable signals $x_j$ (interface cues, behavioral patterns)
- Human's anthropomorphism tendency $\omega_i$

## Project Structure

```
pgt_human_ai_foundation/
├── drafts/           # Working paper manuscript
├── theory/           # Formal framework (foundations.tex)
├── proofs/           # Existence theorem
├── applications/     # Trust game, public goods
├── literature/       # Key papers (17 annotated)
└── references.bib    # Bibliography
```

## Key Results (In Progress)

| Result | Status |
|--------|--------|
| ABE existence under regularity assumptions | Proof sketch |
| Multiple equilibria sustained by different $\phi$ | Stated |
| Welfare implications of anthropomorphism | Conjectured |

## Building On

- Geanakoplos, Pearce & Stacchetti (1989) - Psychological games
- Battigalli & Dufwenberg (2009) - Dynamic PGT
- Li (2026, GEB) - Indignation and cooperation norms

## Target

Econometrica or Journal of Economic Theory

---

*See `CLAUDE.md` for notation conventions and project details.*
