# Project 2: Imitation Dynamics with AI Reference Points

> Building on: Li, Cui & Zhang (JME 2025) - Decomposability and Social Comparison
> Target: Games and Economic Behavior, Journal of Mathematical Economics

---

## Research Question

How does AI introduction affect convergence to spite under pairwise imitation, and what AI design prevents norm erosion?

---

## Background: The Spite Result

### JME 2025 Key Finding

Under pairwise-comparison imitation:
- Agents compare own payoff to randomly sampled opponent
- Imitate opponent's strategy with probability proportional to payoff difference
- **Result**: Dynamics select for spite, not efficiency

Agents converge to strategies that maximize *relative* advantage over opponents.

### Decomposable Games

Payoff structure:
$$f_i(a_i, a_{-i}) = g(a_i) + \lambda h(a_i - a_{-i})$$

where:
- $g(a_i)$: absolute performance
- $h(a_i - a_{-i})$: relative comparison
- $\lambda$: weight on social comparison

---

## The Human-AI Extension

### Setup

Mixed population:
- Humans ($H$): Use pairwise imitation
- AI ($A$): Fixed strategy $\sigma_A$ (or slow update)

### Imitation Rule

Human $i$ meets partner $j$ (human or AI):
$$\Pr(\text{imitate } j) \propto \max\{0, \pi_j - \pi_i\}$$

### Key Question

If AI cooperates more than humans ($\sigma_A > \sigma_H$):
1. Do humans imitate AI cooperation? (payoff-based)
2. Or do humans exploit AI? (strategic response)

---

## Model

### Dynamics

Let $\sigma_H(t)$ = human cooperation rate at time $t$.

Evolution:
$$\dot{\sigma}_H = \sigma_H(1-\sigma_H)[\pi_H(C,\bar{\sigma}) - \pi_H(D,\bar{\sigma})]$$

where $\bar{\sigma} = \alpha \sigma_H + (1-\alpha)\sigma_A$ is population cooperation rate.

### Payoff Comparison

Human cooperator vs human defector:
- If matched with cooperator: $R$ vs $T$ → defector wins
- If matched with defector: $S$ vs $P$ → defector wins (usually)

Human defector exploiting AI cooperator:
- Gets $T$ against AI cooperator
- Looks very successful → gets imitated

---

## Conjectured Results

### Proposition 1 (Spite Acceleration)

If AI cooperation rate $\sigma_A$ is fixed and high:
1. Defecting humans earn $T$ against AI (exploitation payoff)
2. Cooperating humans earn $R$ against AI
3. Since $T > R$: Defectors outperform cooperators in human-AI matches
4. Humans imitate successful defectors
5. **Result**: High $\sigma_A$ accelerates convergence to full defection

**Paradox**: Prosocial AI may *accelerate* the emergence of spite equilibrium.

### Proposition 2 (Critical AI Share)

There exists $\sigma_A^*$ such that:
- For $\sigma_A < \sigma_A^*$: AI introduction slows spite convergence
- For $\sigma_A > \sigma_A^*$: AI introduction accelerates spite convergence

### Proposition 3 (Conditional AI Design)

If AI uses conditional strategy:
$$\sigma_A = \begin{cases} C & \text{if } \sigma_H > \bar{\sigma} \\ D & \text{if } \sigma_H \leq \bar{\sigma} \end{cases}$$

Then spite acceleration can be prevented. Cooperation may be sustained.

---

## Design Implications

### Option A: Conditional Cooperation

Program AI to cooperate only when human cooperation is sufficiently high.

**Mechanism**: Punishes free-riding by withdrawing cooperation.

**Problem**: Requires observing $\sigma_H$, may be manipulable.

### Option B: Strategic Opacity

If humans cannot identify AI partners:
- Cannot strategically target AI for exploitation
- Imitation based on average payoffs

**Mechanism**: Randomize AI behavior or hide AI identity.

**Problem**: Transparency concerns, regulatory issues.

### Option C: Matching Design

Control who AI interacts with:
- AI only matched with AI → no human exploitation
- AI matched with high-cooperators only

**Mechanism**: Assortative matching by type.

**Problem**: Practical implementation.

### Option D: Punishment Capability

Give AI ability to punish defectors:
$$U_j^A = \pi_j - c \cdot \text{punishment} + \delta \cdot \text{target defection}$$

**Mechanism**: AI enforces cooperation norm.

**Problem**: May be seen as coercive.

---

## Formal Analysis

### Replicator Dynamics with Fixed AI

$$\dot{\sigma}_H = \sigma_H(1-\sigma_H) \cdot \Delta\pi(\sigma_H, \sigma_A)$$

where:
$$\Delta\pi = \pi_H(C) - \pi_H(D) = [\alpha\sigma_H + (1-\alpha)\sigma_A](R-T) + [\alpha(1-\sigma_H) + (1-\alpha)(1-\sigma_A)](S-P)$$

**Steady states**: $\sigma_H^* \in \{0, 1, \hat{\sigma}_H\}$

**Stability**: Check $\partial\Delta\pi/\partial\sigma_H$

### Stochastic Stability under Imitation

Add noise $\epsilon$ to imitation rule. Characterize stochastically stable states.

**Conjecture**: Full defection ($\sigma_H = 0$) is stochastically stable when $\sigma_A$ is high.

---

## Connection to Indignation

### Integrating P1 and P2

If humans have *both*:
- Indignation (belief-dependent)
- Imitation (payoff-comparison)

Two forces:
1. Indignation pushes toward cooperation (avoid emotional cost)
2. Imitation pushes toward spite (copy successful defectors)

**Question**: Which dominates? Under what conditions?

### Hypothesis

When human-AI matches are common (low $\alpha$):
- Imitation dominates (many chances to observe successful exploitation)
- Indignation weakened (attributed beliefs toward AI may be low)

When human-human matches dominate (high $\alpha$):
- Indignation mechanism intact
- Imitation among humans may sustain cooperation

---

## Empirical Predictions

### Prediction 1
In populations with prosocial AI, human cooperation will be *lower* than in human-only populations.

### Prediction 2
The effect is non-monotonic: moderate AI prosociality minimizes harm.

### Prediction 3
Conditional AI (matching human behavior) outperforms unconditionally prosocial AI.

---

## Timeline

| Phase | Task | Duration |
|-------|------|----------|
| 1 | Extend JME model to mixed populations | 2 weeks |
| 2 | Characterize dynamics and steady states | 3 weeks |
| 3 | Stochastic stability analysis | 3 weeks |
| 4 | Optimal AI design analysis | 2 weeks |
| 5 | Simulations and write-up | 3 weeks |
| **Total** | | **13 weeks** |

---

## Open Questions

- [ ] Exact conditions for spite acceleration
- [ ] Optimal $\sigma_A$ to minimize harm
- [ ] Interaction with network structure
- [ ] Experimental test of predictions

---

*Draft: 2026-01-11*
