# Phase 1: Notation Inventory - Equilibrium Section

## 1. Equilibrium Notation

| Symbol | Definition | Context |
|--------|------------|---------|
| $s^* = (s_H^*, s_A^*)$ | Equilibrium strategy profile | ABE Definition |
| $h^*$ | Equilibrium genuine belief system | ABE Definition |
| $\tilde{h}^*$ | Equilibrium attributed belief system | ABE Definition |
| $h_i^{*(1,k)}$ | Human i's equilibrium first-order belief about k | Genuine belief consistency |
| $h_i^{*(2,k)}$ | Human i's equilibrium second-order belief about k | Genuine belief consistency |
| $\tilde{h}_i^{*(2,j)}$ | Human i's equilibrium attributed belief about AI j | Attribution consistency |
| $BR_i^H(h_i, \tilde{h}_i)$ | Human i's best response correspondence | Existence proof |
| $BR_j^A(\sigma_{-j})$ | AI j's best response correspondence | Existence proof |
| $\Phi: \Sigma \to \Sigma$ | Fixed-point mapping | Existence proof |

## 2. New Definitions

### Definition: Attributed Belief Equilibrium (def:ABE)
Four conditions:
1. **Human Optimality**: $s_i^* \in \arg\max_{s_i \in S_i} U_i^H(s_i, s_{-i}^*, h_i^*, \tilde{h}_i^*)$
2. **AI Optimality**: $s_j^* \in \arg\max_{s_j \in S_j} U_j^A(s_j, s_{-j}^*; \theta_j)$
3. **Genuine Belief Consistency**: $h_i^{*(1,k)} = s_k^*$ and $h_i^{*(2,k)} = h_k^{*(1,i)}$
4. **Attribution Consistency**: $\tilde{h}_i^{*(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$

### Key Concepts
- **Dual consistency**: H-H beliefs Bayesian; H-A beliefs attribution-based
- **Asymmetric rationality**: Humans psychologically rational; AI design-rational
- **No cognizability for attributed beliefs**: AI lacks genuine beliefs

## 3. Theorems and Propositions

| Result | Statement | Assumptions Used |
|--------|-----------|------------------|
| Theorem 1 (thm:existence) | ABE exists | A1, A2, A3 |
| Prop. (prop:nesting) | Reduction to SPE when $N_A = \emptyset$ | None beyond ABE def |
| Prop. (prop:nash) | Reduction to Nash when $\psi_i \equiv 0$ | None beyond ABE def |
| Prop. (prop:rational-attribution) | Equivalence to Bayesian game with type uncertainty | Rational attribution |
| Prop. (prop:multiplicity) | Different $\phi, \phi'$ yield different $s^*$ | Fixed material game |

## 4. Proof Notation

| Symbol | Definition | Location |
|--------|------------|----------|
| $\Sigma = \prod_{i \in N} \Delta(S_i)$ | Space of mixed strategy profiles | Proof Step 1 |
| $\sigma_i \in \Delta(S_i)$ | Mixed strategy for player i | Best response def |
| $\mathbb{E}[\cdot]$ | Expectation operator | Best response def |
| $BR^H(h, \tilde{h}) \times BR^A(\sigma)$ | Joint best response | Fixed-point mapping |

## 5. Cross-References to Framework

### Assumptions Referenced
- **A1**: Compactness of strategy space (Step 1, Step 2)
- **A1c**: Continuity of utility (Step 2) - NOTE: Subscript notation
- **A2**: Well-defined and continuous attribution function (Step 1)
- **A3**: Bounded psychological payoffs (Remark after proof)

### Definitions Referenced
- $U_i^H$: Human utility function
- $U_j^A$: AI utility function
- $\phi_i$: Attribution function
- $\theta_j$: AI design parameters
- $x_j$: AI behavioral cues
- $\omega_i$: Human anthropomorphism tendency
- $N_H, N_A$: Human and AI player sets
- $\psi_i$: Psychological payoff function
- $\pi_i$: Material payoff function

## 6. Potential Inconsistencies

1. **A1c notation**: Uses subscript "c" in "A1c (continuity)" - need to verify if framework section uses same sub-assumption labeling
2. **Sigma vs s notation**: Proof uses $\sigma$ for mixed strategies but definition uses $s$ - may need clarification if $s$ includes mixed
3. **Sequential Psychological Equilibrium (SPE)**: Referenced as reduction case - need to verify this is defined/cited properly in framework
4. **$h_i^{(2,k)}$ vs $h_i^{*(2,k)}$**: Equilibrium uses starred superscripts; verify framework uses unstarred for general beliefs
