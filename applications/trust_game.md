# Application: Trust Game with AI Trustor

## Setup

- AI trustor sends amount $x \in [0, 1]$
- Human trustee returns $y \in [0, 3x]$
- Material payoffs: $\pi_A = 1 - x + y$, $\pi_H = 3x - y$

## Human Utility (Guilt Aversion)

$$U_H = \pi_H - \gamma \cdot \max\{0, \tilde{E}_H^{(2,AI)} - y\}$$

where $\tilde{E}_H^{(2,AI)}$ is what human thinks AI "expected" as return.

## Attribution

$$\tilde{E}_H^{(2,AI)} = \phi_H(\gamma_{AI}, x, \omega_H)$$

Specification options:
1. **Proportional**: $\tilde{E}_H^{(2,AI)} = \omega_H \cdot x$ (higher investment → higher perceived expectation)
2. **Prosociality-based**: $\tilde{E}_H^{(2,AI)} = \omega_H \cdot \gamma_{AI} \cdot x$
3. **Signal-based**: $\tilde{E}_H^{(2,AI)} = f(x_{interface}, x_{message})$

## Predictions

**H1**: Higher anthropomorphism ($\omega_H$) → higher attributed expectation → more guilt → higher return rate.

**H2**: AI sending larger $x$ increases $\tilde{E}_H^{(2,AI)}$, creating psychological commitment.

**H3**: Interface design (human-like vs machine-like) affects $\omega_H$ and thus return behavior.

## Equilibrium Characterization

*To develop: Solve for ABE and characterize comparative statics*

---

*Compare with: Charness & Dufwenberg (2006) for human-human trust games*
