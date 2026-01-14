# Application: Public Goods Game with AI

## Setup

- $n-1$ humans, 1 AI agent
- Each player $i$ contributes $c_i \in [0, e]$
- Payoff: $\pi_i = e - c_i + m \sum_j c_j$ where $m \in (1/n, 1)$

## Human Utility (Indignation)

$$U_i^H = \pi_i - \beta \cdot \mathbf{1}_{c_i < \bar{c}} \cdot \left[ \sum_{k \in N_H} E_i^{(2,k)}(c \geq \bar{c}) + \tilde{E}_i^{(2,AI)}(c \geq \bar{c}) \right]$$

where $\bar{c}$ is a norm threshold.

## Key Questions

1. **Norm formation**: Does AI contribution affect the norm threshold $\bar{c}$?
2. **Reference point**: Does AI act as a behavioral reference for humans?
3. **Indignation toward AI**: Do humans feel indignation when defecting against AI's "expectations"?

## Attribution Specifications

**Case 1: AI contribution affects attributed expectations**
$$\tilde{E}_i^{(2,AI)} = g(c_{AI}, \omega_i)$$
Higher $c_{AI}$ → higher perceived norm → more indignation from defection.

**Case 2: AI is excluded from moral consideration**
$$\tilde{E}_i^{(2,AI)} = 0$$
No psychological payoff from violating AI's "expectations."

## Predictions

**H1**: If attribution includes AI, higher AI contribution increases human cooperation.

**H2**: If attribution excludes AI, human cooperation depends only on human share, not AI level.

**H3**: Anthropomorphism moderates the effect of AI contribution on human behavior.

---

*Connect to: P1 stochastic stability analysis with mixed populations*
