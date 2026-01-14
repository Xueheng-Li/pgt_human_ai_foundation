# Formal Framework for Attributed Belief Equilibrium

## Game Structure

Define the asymmetric game $\Gamma^{asym} = (N_H, N_A, S, U^H, U^A, \phi)$ where:

- $N_H = \{1, \ldots, n_H\}$: set of human players
- $N_A = \{1, \ldots, n_A\}$: set of AI agents
- $S = \prod_{i \in N_H \cup N_A} S_i$: strategy space
- $U^H = \{U_i^H\}_{i \in N_H}$: human utility functions
- $U^A = \{U_j^A\}_{j \in N_A}$: AI utility functions
- $\phi = \{\phi_i\}_{i \in N_H}$: attribution functions

## Belief Hierarchies

### Human Beliefs (Standard PGT)

For $i \in N_H$, define:
- $E_i^{(1)} \in \Delta(S_{-i})$: first-order beliefs about opponents' play
- $E_i^{(2,k)} \in \Delta(\Delta(S_{-k}))$: second-order beliefs (what $k$ expects)
- Higher orders as needed

### Attributed Beliefs (Novel)

For $i \in N_H$ facing $j \in N_A$:
$$\tilde{E}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$$

where:
- $\theta_j \in \Theta$: AI design parameters (prosociality, conditionality)
- $x_j \in X$: observable signals (interface design, behavioral cues)
- $\omega_i \in \Omega$: individual heterogeneity (anthropomorphism tendency)

## Utility Specifications

### Human Utility

$$U_i^H(s, E_i) = \pi_i(s) + \psi_i(s_i, E_i, \tilde{E}_i)$$

where $\psi_i$ captures psychological payoffs:
- Indignation toward humans: $-\beta \cdot \mathbf{1}_{s_i = D} \cdot E_i^{(2,k)}(C)$ for $k \in N_H$
- Indignation toward AI: $-\beta \cdot \mathbf{1}_{s_i = D} \cdot \tilde{E}_i^{(2,j)}(C)$ for $j \in N_A$

### AI Utility

$$U_j^A(s; \theta_j) = f_j(s; \theta_j)$$

No belief dependence. Examples:
- Materialist: $U_j^A = \pi_j(s)$
- Prosocial: $U_j^A = \pi_j(s) + \gamma \sum_k \pi_k(s)$

## Assumptions

**A1 (Regularity)**: $U_i^H$ is continuous in all arguments; $S_i$ compact for all $i$.

**A2 (Attribution Continuity)**: $\phi_i$ is continuous in $(\theta_j, x_j)$.

**A3 (Bounded Psychological Payoffs)**: $|\psi_i| \leq M$ for some $M < \infty$.

---

*To develop: Formal definition of belief consistency conditions*
