# Project 3: Attributed Belief Equilibrium in Human-AI Games

> Building on: Psychological game theory foundations (GPS 1989, BD 2009)
> Target: Econometrica (if sufficiently general), Journal of Economic Theory

---

## Research Question

What is the appropriate equilibrium concept for games where humans have belief-dependent preferences but AI have design-dependent objectives?

---

## The Foundational Problem

### Classical PGT Assumes Symmetry

Standard psychological game theory:
- All players form belief hierarchies
- All players have belief-dependent utilities
- Beliefs are common knowledge in structure

### Human-AI Asymmetry

| Aspect | Humans | AI |
|--------|--------|-----|
| Mental states | Genuine beliefs | Computational states |
| Utility | Belief-dependent | Design-dependent |
| Belief hierarchy | $E_i^{(1)}, E_i^{(2)}, ...$ | None (or simulated) |
| Attribution | Forms beliefs about AI | Models humans from data |

**Core insight**: Humans form *attributed* beliefs about AI "expectations" even though AI has no genuine expectations.

---

## Formal Framework

### Game Structure

$\Gamma^{asym} = (N_H, N_A, S, U^H, U^A, \phi)$

where:
- $N_H$: set of human players
- $N_A$: set of AI agents
- $S = \prod_i S_i$: strategy space
- $U^H$: human utility functions (belief-dependent)
- $U^A$: AI utility functions (design-dependent)
- $\phi$: attribution function

### Human Utility

For human $i \in N_H$:
$$U_i^H(s, E_i) = \pi_i(s) + \psi_i(s_i, E_i)$$

where $E_i = (E_i^{(1)}, E_i^{(2)}, ...)$ is $i$'s belief hierarchy.

**Examples of $\psi_i$**:
- Guilt: $\psi_i = -\gamma \cdot \mathbf{1}_{s_i \text{ harms } j} \cdot E_i^{(2,j)}(\text{no harm})$
- Indignation: $\psi_i = -\beta \cdot \mathbf{1}_{s_i = D} \cdot E_i^{(2)}(C)$
- Reciprocity: $\psi_i = \kappa \cdot k_i(s_i, E_i^{(1)}) \cdot k_j(E_i^{(1,j)}, E_i^{(2,j)})$

### AI Utility

For AI $j \in N_A$:
$$U_j^A(s; \theta_j) = f_j(s; \theta_j)$$

where $\theta_j$ are design parameters. No belief dependence.

**Examples**:
- Materialist: $U_j^A = \pi_j(s)$
- Prosocial: $U_j^A = \pi_j(s) + \gamma \sum_k \pi_k(s)$
- Conditional: $U_j^A = \pi_j(s) \cdot g(\text{observed human behavior})$

### Attribution Function

Human $i$ facing AI $j$ forms:
$$\tilde{E}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$$

where:
- $\theta_j$: AI design parameters
- $x_j$: observable signals (interface, behavior, framing)
- $\omega_i$: individual characteristics (anthropomorphism tendency)

---

## Equilibrium Definition

**Definition (Attributed Belief Equilibrium - ABE)**

A strategy profile $s^* = (s_H^*, s_A^*)$ and belief system $(E^*, \tilde{E}^*)$ constitute an ABE if:

1. **Human optimality**: $\forall i \in N_H$:
   $$s_i^* \in \arg\max_{s_i} U_i^H(s_i, s_{-i}^*, E_i^*)$$

2. **AI optimality**: $\forall j \in N_A$:
   $$s_j^* \in \arg\max_{s_j} U_j^A(s_j, s_{-j}^*; \theta_j)$$

3. **First-order belief consistency** (H-H):
   $$E_i^{(1,k)} = s_k^* \quad \forall i, k \in N_H$$

4. **First-order belief consistency** (H-A):
   $$\tilde{E}_i^{(1,j)} = s_j^* \quad \forall i \in N_H, j \in N_A$$

5. **Second-order belief consistency** (H-H):
   $$E_i^{(2,k)} = E_k^{(1,i)} \quad \forall i, k \in N_H$$

6. **Attributed second-order beliefs** (H-A):
   $$\tilde{E}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i) \quad \forall i \in N_H, j \in N_A$$

---

## Theoretical Results

### Theorem 1 (Existence)

Under standard regularity conditions on $U^H$, $U^A$, and continuity of $\phi$:
An attributed belief equilibrium exists.

**Proof sketch**: Fixed-point argument similar to Battigalli & Dufwenberg (2009).

### Theorem 2 (Multiplicity)

Different attribution functions $\phi$ can sustain different equilibria.

**Implication**: How humans perceive AI affects equilibrium selection.

### Theorem 3 (Welfare)

Let $W(s) = \sum_i \pi_i(s)$ be social welfare.

If AI is prosocially programmed ($\gamma > 0$) and humans over-anthropomorphize ($\tilde{E}_i^{(2,j)} > $ rational benchmark):

$$W(\text{ABE with over-attribution}) > W(\text{ABE with rational attribution})$$

**Intuition**: Inflated perceived normative pressure sustains more cooperation.

---

## Applications

### Application 1: Trust Game

**Setup**:
- Human trustor, AI trustee
- Trustor sends $x$, AI returns $y(x)$

**Human guilt aversion**:
$$U_H = \pi_H - \gamma \cdot (E_H^{(2)} - y) \cdot \mathbf{1}_{y < E_H^{(2)}}$$

Wait - trustor doesn't have guilt. Let's reverse:

**Setup (reversed)**:
- AI trustor, Human trustee
- AI sends $x$, Human returns $y$

**Human guilt aversion**:
$$U_H^{trustee} = \pi_H(y) - \gamma \cdot \max\{0, \tilde{E}_H^{(2,AI)} - y\}$$

**Question**: How does $\tilde{E}_H^{(2,AI)}$ (what human thinks AI expected) affect return rate?

**Prediction**: Higher anthropomorphism → higher $\tilde{E}_H^{(2,AI)}$ → more guilt from defection → higher return rate.

### Application 2: Public Goods with AI

**Setup**:
- $n-1$ humans, 1 AI
- Linear public goods game

**Human indignation**:
$$U_i^H = \text{payoff} - \beta \cdot \mathbf{1}_{c_i < \bar{c}} \cdot E_i^{(2)}(\text{high contribution})$$

**Questions**:
1. Does AI contribution level $c_A$ affect human $E_i^{(2)}$?
2. Does AI presence change the norm reference point?

### Application 3: Coordination Game

**Setup**:
- 2×2 coordination: $(A,A)$ and $(B,B)$ are equilibria
- 1 human, 1 AI

**Psychological forward induction**:
If AI plays $A$, human may infer AI "intended" coordination on $(A,A)$.

**Question**: Does attributed intent affect human's coordination choice?

---

## Comparison with Existing Concepts

| Concept | Belief Structure | Applicability |
|---------|------------------|---------------|
| Nash Equilibrium | None | All games |
| Psychological Equilibrium (GPS) | Symmetric, genuine | Homogeneous populations |
| Sequential Equilibrium | Probabilistic | Extensive form |
| **Attributed Belief Equilibrium** | Asymmetric, attributed | Human-AI games |

---

## Design Implications

### AI Design Problem

Given attribution function $\phi$:
$$\max_{\theta} W(s^*(\theta, \phi))$$

**Trade-offs**:
- High prosociality ($\gamma$): May be exploited
- Observable signals ($x$): Affect $\tilde{E}^{(2)}$ via attribution
- Conditional behavior: Strategic, but may erode trust

### Interface Design

How to present AI to humans?
- Humanlike appearance → higher anthropomorphism → higher $\tilde{E}^{(2)}$
- Machine-like appearance → lower anthropomorphism → lower psychological pressure

**Optimal design**: Depends on whether over-attribution helps or hurts.

---

## Timeline

| Phase | Task | Duration |
|-------|------|----------|
| 1 | Formal definition and existence proof | 3 weeks |
| 2 | Characterization in canonical games | 4 weeks |
| 3 | Welfare analysis | 3 weeks |
| 4 | Design implications | 2 weeks |
| 5 | Write-up | 3 weeks |
| **Total** | | **15 weeks** |

---

## Open Questions

- [ ] Relationship to Bayesian games with type uncertainty?
- [ ] How to empirically estimate $\phi$?
- [ ] Dynamic extension: learning $\phi$ over time?
- [ ] Multiple AI with different $\theta$?

---

*Draft: 2026-01-11*
