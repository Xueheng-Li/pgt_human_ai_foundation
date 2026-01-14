# Project 1: Stochastic Stability in Mixed Human-AI Populations

> Building on: Li (2026) GEB - Indignation and Cooperation
> Target: Journal of Economic Theory, Games and Economic Behavior

---

## Research Question

What is the stochastically stable distribution of cooperation in a population with fraction $\alpha$ humans (with indignation preferences) and fraction $(1-\alpha)$ AI agents (with programmed prosociality)?

---

## Model Setup

### Population Structure

- Total population: $N$ agents
- Humans: $N_H = \alpha N$ with indignation preferences
- AI agents: $N_A = (1-\alpha)N$ with design-dependent utilities

### Stage Game

Prisoner's Dilemma with standard payoffs:

|   | C | D |
|---|---|---|
| C | R, R | S, T |
| D | T, S | P, P |

where $T > R > P > S$ and $2R > T + S$.

### Human Utility

For human $i$:
$$U_i^H(a_i, a_{-i}, E_i) = \pi_i(a_i, a_{-i}) - \beta \cdot \mathbf{1}_{a_i=D} \cdot E_i^{(2)}(C)$$

where:
- $\pi_i$: material payoff
- $\beta > 0$: indignation intensity
- $E_i^{(2)}(C)$: $i$'s belief about what others expected $i$ to play

### AI Utility

For AI $j$:
$$U_j^A(a_j, a_{-j}; \gamma) = \pi_j(a_j, a_{-j}) + \gamma \cdot \mathbf{1}_{a_j=C}$$

where $\gamma \geq 0$ is the programmed prosociality parameter.

Alternative: Conditional AI
$$U_j^{A,cond} = \pi_j + \gamma \cdot \mathbf{1}_{a_j=C} \cdot \mathbf{1}_{\sigma_{-j} > \bar{\sigma}}$$

---

## Dynamics

### Human Learning

Noisy best response with logit rule:
$$\Pr(a_i = C) = \frac{\exp(\tau^{-1} U_i^H(C))}{\exp(\tau^{-1} U_i^H(C)) + \exp(\tau^{-1} U_i^H(D))}$$

where $\tau > 0$ is noise/temperature parameter.

### AI Behavior

**Case A: Fixed AI**
- AI plays fixed strategy $\sigma_A \in [0,1]$ (exogenous)
- Simplest case for initial analysis

**Case B: Slow-updating AI**
- AI updates via gradient descent on designer's objective
- Much slower than human learning: $\epsilon_A \ll \epsilon_H$

### Mutation Process

- Human mutation rate: $\epsilon_H$ (experimentation, error)
- AI mutation rate: $\epsilon_A$ (retraining, version updates)

---

## Key Technical Challenges

### Challenge 1: Heterogeneous Mutation Rates

Standard stochastic stability takes $\epsilon \to 0$ uniformly. With $\epsilon_H \neq \epsilon_A$:

$$\lim_{\epsilon_H \to 0} \lim_{\epsilon_A \to 0} \mu^{\epsilon_H, \epsilon_A} \quad \text{vs} \quad \lim_{\epsilon_A \to 0} \lim_{\epsilon_H \to 0} \mu^{\epsilon_H, \epsilon_A}$$

**Conjecture:** Order of limits matters when types have different learning speeds.

### Challenge 2: Belief Formation Toward AI

Human $i$ facing AI $j$ forms attributed belief $\tilde{E}_i^{(2,j)}$.

Need to specify:
- How does $\tilde{E}_i^{(2,j)}$ relate to AI's actual programming?
- Does it differ systematically from $E_i^{(2,k)}$ for human $k$?

### Challenge 3: Type-Dependent Resistance

Resistance of equilibrium $E$ = minimum mutations to escape basin.

With heterogeneous types:
$$R(E \to E') = \min\{r_H + \lambda r_A : \text{transition possible}\}$$

where $\lambda = \epsilon_A/\epsilon_H$ captures relative mutation costs.

---

## Conjectured Results

### Proposition 1 (Critical Threshold)

There exists $\alpha^* \in (0,1)$ such that:
- For $\alpha > \alpha^*$: Full cooperation is stochastically stable
- For $\alpha < \alpha^*$: Full defection is stochastically stable

The threshold $\alpha^*$ depends on:
- Indignation intensity $\beta$
- AI prosociality $\gamma$
- Attribution bias (over/under-anthropomorphism)

### Proposition 2 (Order of Limits)

When $\epsilon_A/\epsilon_H \to 0$ (AI adapts faster):
- Stochastically stable outcome depends primarily on AI programming
- Human adaptation is secondary for equilibrium selection

When $\epsilon_H/\epsilon_A \to 0$ (humans adapt faster):
- Opposite: human indignation mechanism dominates selection

### Proposition 3 (Non-monotonicity)

AI cooperation level $\sigma_A$ has non-monotonic effect on human cooperation:
- Low $\sigma_A$: Humans cooperate (avoid indignation from defecting against cooperators)
- Moderate $\sigma_A$: Mixed
- High $\sigma_A$: Humans may defect (exploit prosocial AI without indignation cost)

---

## Proof Strategy

1. **State space**: $\Omega = \{0, 1, ..., N_H\} \times \{0, 1, ..., N_A\}$ (number of cooperators by type)

2. **Transition probabilities**: Derive from logit dynamics + matching

3. **Stationary distribution**: Characterize $\mu^\epsilon$ for small $\epsilon$

4. **Resistance tree**: Construct minimum-resistance spanning tree

5. **Stochastically stable states**: States in root of minimum-resistance tree

---

## Extensions

### Extension A: Local Interaction

Replace random matching with network structure. Use Li (2026) mobility extension.

### Extension B: Multiple AI Types

Different AI agents with different $\gamma$ values. Heterogeneity within AI population.

### Extension C: Endogenous AI Design

AI designer chooses $\gamma$ to maximize social welfare. Mechanism design perspective.

---

## Timeline

| Phase | Task | Duration |
|-------|------|----------|
| 1 | Formalize model, define equilibrium | 2 weeks |
| 2 | Prove existence, characterize stationary dist | 4 weeks |
| 3 | Derive stochastically stable states | 4 weeks |
| 4 | Write up, simulations | 4 weeks |
| **Total** | | **14 weeks** |

---

## Open Questions

- [ ] Does Sandholm (2010) order-of-limits result extend to heterogeneous types?
- [ ] What is the right specification for $\tilde{E}_i^{(2,j)}$?
- [ ] Can we get closed-form $\alpha^*$ for 2×2 case?
- [ ] How does network structure interact with AI introduction?

---

*Draft: 2026-01-11*
