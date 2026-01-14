# Notation Inventory: sec_framework.tex

Extracted from `/Users/xueheng/SynologyDrive/Research/pgt_human_ai_foundation/drafts/sec_framework.tex`

---

## 1. Player/Type Notation

| Symbol | Definition | Line |
|--------|------------|------|
| $N$ | Total player set ($N = N_H \cup N_A$) | 9 |
| $N_H$ | Set of human players | 9 |
| $N_A$ | Set of AI agents | 9 |
| $n$ | Total number of players ($\|N\| = n = n_H + n_A$) | 9 |
| $n_H$ | Number of human players ($\|N_H\| = n_H \geq 1$) | 9 |
| $n_A$ | Number of AI agents ($\|N_A\| = n_A \geq 0$) | 9 |
| $\alpha$ | Human population share ($\alpha = n_H / n \in (0, 1]$) | 9 |
| $T_i$ | Type space for human $i \in N_H$ | 13 |
| $t_i$ | Type of human $i$; $t_i = (\beta_i, \gamma_i, \omega_i, \ldots) \in T_i$ | 13 |
| $\beta_i$ | Indignation sensitivity (human type parameter) | 13 |
| $\gamma_i$ | Guilt sensitivity (human type parameter) | 13 |
| $\omega_i$ | Anthropomorphism tendency ($\omega_i \in [0,1]$) | 13 |
| $\Theta_j$ | Design parameter space for AI $j \in N_A$ | 13 |
| $\theta_j$ | Design parameters of AI $j$ ($\theta_j \in \Theta_j$) | 13 |

---

## 2. Strategy Notation

| Symbol | Definition | Line |
|--------|------------|------|
| $S_i$ | Finite strategy set for player $i$ | 11 |
| $\sigma_i$ | Mixed strategy ($\sigma_i \in \Delta(S_i)$) | 11 |
| $S$ | Strategy profile space ($S = \prod_{i \in N} S_i$) | 11 |
| $s$ | Strategy profile ($s \in S$) | 17 |
| $S_{-i}$ | Strategy profile space excluding player $i$ | 33 |
| $S_{-k}$ | Strategy profile space excluding player $k$ | 34 |

---

## 3. Payoff Notation

| Symbol | Definition | Line |
|--------|------------|------|
| $\pi_i(s)$ | Material payoff for player $i$ given strategy profile $s$ | 17 |
| $U_i^H(s, h_i, \tilde{h}_i)$ | Total utility for human $i$ | 18-20 |
| $U_j^A(s; \theta_j)$ | AI utility (design-dependent) | 22-24 |
| $f_j(s; \theta_j)$ | General AI objective function | 23 |
| $\psi_i$ | Psychological payoff for human $i$ | 19 |

**AI Specifications (line 26)**:
- Materialist: $U_j^A = \pi_j(s)$
- Prosocial: $U_j^A = \pi_j(s) + \gamma_j \sum_{k \in N} \pi_k(s)$

---

## 4. Belief Notation

| Symbol | Definition | Line |
|--------|------------|------|
| $h_i^{(0)}$ | Type (zeroth-order belief); $h_i^{(0)} = t_i \in T_i$ | 32 |
| $h_i^{(1)}$ | First-order beliefs about others' play; $h_i^{(1)} \in \Delta(S_{-i})$ | 33 |
| $h_i^{(2,k)}$ | Second-order beliefs: what player $k$ expects from others; $h_i^{(2,k)} \in \Delta(\Delta(S_{-k}))$ | 34 |
| $h_i^{(2)}$ | Collection of second-order beliefs | 19, 93-94 |
| $h_i^{(n)}$ | General $n$-th order belief (replaces $\beta_i^{(n)}$ from B&D 2009) | 36 |

---

## 5. Attributed Belief Notation

| Symbol | Definition | Line |
|--------|------------|------|
| $\tilde{h}_i^{(2,j)}$ | Attributed second-order belief: what human $i$ believes AI $j$ expected | 44-48 |
| $\tilde{h}_i^{(2)}$ | Collection of attributed second-order beliefs | 19 |
| $\tilde{h}_i^{(2,j)}(C)$ | Attributed probability that AI $j$ expected cooperation | 80-82, 95 |

---

## 6. Attribution Function Notation

| Symbol | Definition | Line |
|--------|------------|------|
| $\phi_i$ | Attribution function for human $i$; $\phi_i: \Theta_j \times X \times \Omega_i \to \Delta(S_i)$ | 61-65 |
| $\phi$ | Collection of attribution functions $\{\phi_i\}_{i \in N_H}$ | 117 |
| $X$ | Signal space | 48 |
| $x_j$ | Observable signals for AI $j$ ($x_j \in X$) | 48 |
| $\Omega_i$ | Anthropomorphism tendency space for human $i$ | 63 |

**Attribution Function Variants (lines 72-75)**:
- $\phi_i^{beh}$ — Behavioural attribution: $g(s_j^{obs}, \omega_i)$
- $\phi_i^{sig}$ — Signal-based attribution: $g(x_j, \omega_i)$
- $\phi_i^{disp}$ — Dispositional attribution: $\omega_i \cdot \bar{h} + (1 - \omega_i) \cdot \underline{h}$

**Linear Attribution Example (lines 78-83)**:
- $\gamma_j$ — AI's prosociality parameter ($\gamma_j \in [0,1]$)
- $\eta$ — Signal sensitivity ($\eta > 0$)
- Formula: $\tilde{h}_i^{(2,j)}(C) = \omega_i \cdot ( \gamma_j + \eta \cdot x_j )$

---

## 7. Psychological Payoff Notation

### Indignation (Definition 3, lines 89-96)

| Symbol | Definition |
|--------|------------|
| $\psi_i^{IND}$ | Indignation payoff |
| $\beta_i$ | Indignation sensitivity ($\beta_i > 0$) |
| $\lambda_i^{IND}$ | Indignation attenuation factor toward AI ($\lambda_i^{IND} \in [0,1]$) |
| $h_i^{(2,k)}(C)$ | Probability that human $k$ expected cooperation |
| $\mathbf{1}_{s_i = D}$ | Indicator for defection |

**Formula**:
$$\psi_i^{IND}(s, h_i^{(2)}, \tilde{h}_i^{(2)}) = -\beta_i \cdot \mathbf{1}_{s_i = D} \cdot \left[ \sum_{k \in N_H} h_i^{(2,k)}(C) + \lambda_i^{IND} \sum_{j \in N_A} \tilde{h}_i^{(2,j)}(C) \right]$$

### Guilt Aversion (Definition 4, lines 100-107)

| Symbol | Definition |
|--------|------------|
| $\psi_i^{GUILT}$ | Guilt payoff |
| $\gamma_i$ | Guilt sensitivity ($\gamma_i > 0$) |
| $\lambda_i^{GUILT}$ | Guilt attenuation factor toward AI ($\lambda_i^{GUILT} \in [0,1]$) |

**Formula**:
$$\psi_i^{GUILT}(s, h_i^{(2)}, \tilde{h}_i^{(2)}) = -\gamma_i \cdot \left[ \sum_{k \in N_H} \max\{0, h_i^{(2,k)} - \pi_k(s)\} + \lambda_i^{GUILT} \sum_{j \in N_A} \max\{0, \tilde{h}_i^{(2,j)} - \pi_j(s)\} \right]$$

---

## 8. Formal Definitions

| Number | Label | Name | Line |
|--------|-------|------|------|
| Definition 1 | `def:attributed-beliefs` | Attributed Beliefs | 42-49 |
| Definition 2 | `def:attribution-function` | Attribution Function | 59-66 |
| Definition 3 | `def:indignation` | Indignation with Attenuation | 89-96 |
| Definition 4 | `def:guilt` | Guilt Aversion with Attenuation | 100-107 |
| Definition 5 | `def:game` | Asymmetric Human-AI Psychological Game | 113-120 |

---

## 9. Assumptions

| Number | Label | Name | Content | Line |
|--------|-------|------|---------|------|
| A1 | `ass:regularity` | Regularity | Strategy spaces finite, type spaces compact/convex, payoffs continuous | 126-129 |
| A2 | `ass:attribution` | Attribution Continuity | $\phi_i$ continuous in $(\theta_j, x_j)$ for fixed $\omega_i$ | 131-134 |
| A3 | `ass:bounded` | Bounded Psychological Payoffs | $\|\psi_i\| \leq M < \infty$ for all players, strategies, beliefs | 136-139 |

---

## 10. Game Tuple Components

The game $\Gamma$ (Definition 5, line 117) contains:
$$\Gamma = (N_H, N_A, \{T_i\}_{i \in N_H}, \{\Theta_j\}_{j \in N_A}, \{S_i\}_{i \in N}, \{U_i^H\}_{i \in N_H}, \{U_j^A\}_{j \in N_A}, \phi, p)$$

| Component | Description |
|-----------|-------------|
| $N_H, N_A$ | Human and AI player sets |
| $\{T_i\}_{i \in N_H}$ | Human type spaces |
| $\{\Theta_j\}_{j \in N_A}$ | AI design parameter spaces |
| $\{S_i\}_{i \in N}$ | Strategy sets |
| $\{U_i^H\}_{i \in N_H}$ | Human utility functions |
| $\{U_j^A\}_{j \in N_A}$ | AI utility functions |
| $\phi$ | Attribution functions |
| $p$ | Common prior over types |

---

## 11. Additional Notation

| Symbol | Definition | Line |
|--------|------------|------|
| $\Delta(\cdot)$ | Probability simplex over a set | 11, 33, etc. |
| $C$ | Cooperate action | 51, 80, 93-95 |
| $D$ | Defect action | 93 |
| $\bar{h}$ | Upper bound belief (in dispositional attribution) | 74 |
| $\underline{h}$ | Lower bound belief (in dispositional attribution) | 74 |
| $s_j^{obs}$ | Observed AI behaviour | 72 |
| $g(\cdot)$ | Generic function in attribution specifications | 72-73 |
| $M$ | Bound on psychological payoffs | 138 |

---

*Inventory complete. 140 lines analyzed.*
