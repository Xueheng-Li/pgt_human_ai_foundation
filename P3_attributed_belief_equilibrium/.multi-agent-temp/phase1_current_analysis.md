# Analysis of Introduction.md vs. PGT Standards

## Executive Summary

The current introduction.md provides a good conceptual overview of the attributed belief equilibrium but **lacks the formal rigor and standard terminology expected in PGT literature**. Key gaps include incomplete belief hierarchy formalization, non-standard notation, missing psychological game foundations, and insufficient integration with canonical PGT frameworks (GPS 1989, BD 2009).

---

## 1. Current Notation for Psychological Game Elements

### What's Used (Problems Identified)
- `$E_i^{(1)}$` - Non-standard notation for first-order beliefs
- `$E_i^{(2,k)}$` - Non-standard notation for second-order beliefs
- `$E_i$` - Ambiguous notation for belief systems
- `$\tilde{E}_i^{(2,j)}$` - Novel notation for attributed beliefs (appropriate)

### What's Missing
- **Universal belief spaces**: No definition of $\Omega_i$ or type spaces
- **Belief hierarchies**: Missing standard notation like $H_i^n$ for nth-order beliefs
- **Belief objects**: No notation for actual beliefs (e.g., $b_i^{(n)}$ for nth-order beliefs)
- **Probability measures**: Missing $\Delta(\cdot)$ notation for mixed strategies and beliefs
- **Type notation**: Missing $\theta_i$ for human types and $\tau_j$ for AI types

### PGT Standard Notation (Should Use)
```
From GPS 1989 and BD 2009:
- $T_i$: Player i's type
- $\beta_i$: Beliefs about others' types
- $b_i^{(1)} \in \Delta(S_{-i})$: First-order beliefs
- $b_i^{(2)} \in \Delta(\Delta(S_{-i}))$: Second-order beliefs
- $\Pi_i$: Psychological payoff function
- $\phi_i$: Mapping from beliefs to psychological utility
```

### Required Updates
```latex
% Replace current notation with standard PGT
- Define belief hierarchy: $\mathcal{H}_i^0 = T_i$, $\mathcal{H}_i^{n+1} = \Delta(\prod_{k \neq i} \mathcal{H}_k^n)$
- Define beliefs: $h_i^{(n)} \in \mathcal{H}_i^n$ for nth-order beliefs
- Define extended utility: $U_i(s, h_i^{(1)}, h_i^{(2)}) = \pi_i(s) + \psi_i(h_i^{(2)}, s)$
```

---

## 2. Belief Introduction and Formalization

### Current Approach (Inadequate)
**Line 19-21**: Introduces beliefs too briefly without proper construction:
```
- $E_i^{(1)} \in \Delta(S_{-i})$: first-order beliefs about opponents' play
- $E_i^{(2,k)} \in \Delta(\Delta(S_{-k}))$: second-order beliefs (what $k$ expects)
```

**Issues**:
1. **No belief hierarchy construction**: Missing the recursive definition of infinite hierarchies
2. **No consistency conditions**: No mention of Bayesian consistency or common knowledge
3. **No universal beliefs**: Missing reference to universal belief spaces (Mertens-Zamir)
4. **No Harsanyi framework**: Missing the type space construction

### Standard PGT Approach (Required)
```latex
\begin{definition}[Belief Hierarchy]
For each player i, define the universal belief space:
$\mathcal{H}_i^0 = T_i$ (types)
$\mathcal{H}_i^1 = \Delta(\times_{j \neq i} T_j \times S_{-i})$ (first-order)
$\mathcal{H}_i^2 = \Delta(\times_{j \neq i} \mathcal{H}_j^1)$ (second-order)
...
$\mathcal{H}_i = \prod_{n=0}^\infty \mathcal{H}_i^n$ (full hierarchy)

A belief system is $h_i = (h_i^{(0)}, h_i^{(1)}, h_i^{(2)}, ...) \in \mathcal{H}_i$.
\end{definition}

\begin{definition}[Bayesian Consistency]
Beliefs must satisfy:
1. $h_i^{(1)}(\cdot | t_i) \in \Delta(\times_{j \neq i} T_j \times S_{-i})$
2. $h_i^{(n+1)}(\cdot | t_i, h_i^{(1)}, ..., h_i^{(n)}) \in \Delta(\times_{j \neq i} \mathcal{H}_j^n)$
3. $h_i^{(n)}$ is derived from $h_i^{(n+1)}$ via marginalization (standard consistency)
\end{definition}
```

### Required Updates to Introduction.md
- Add subsection "Belief Hierarchies" (after Line 22)
- Define universal belief spaces properly
- Explain Harsanyi type construction
- Introduce consistency conditions
- Distinguish between "genuine" beliefs (H-H) and "attributed" beliefs (H-A)

---

## 3. Missing Standard PGT Terminology

### Not Used (But Should Be)
1. **"Psychological Games"** - Never explicitly stated
2. **"Belief-Dependent Preferences"** - Used informally, not as formal term
3. **"Psychological Payoffs"** - Not defined
4. **"Extended Utility Function"** - Missing concept
5. **"Guilt Aversion"** - Mentioned but not defined as PGT mechanism
6. **"Indignation"** - Used but not linked to standard PGT literature
7. **"Sequential Psychological Equilibrium"** - Not mentioned
8. **"Type-Continuum Model"** - Missing framework reference
9. **"Higher-Order Beliefs"** - Too brief treatment

### Required Terminology Additions
```latex
% After Line 79 (Related Literature), add subsection:

\subsection{Psychological Game Theory Foundations}

\begin{definition}[Psychological Game]
A psychological game (GPS 1989) is defined by:
1. A Bayesian game $(N, \{T_i\}, \{S_i\}, \{u_i\}, p)$ with type space $T_i$
2. Belief hierarchies $\{h_i^{(n)}\}_{n=1}^\infty$ for each player i
3. Extended utility functions $U_i: S \times \prod_{n=1}^\infty \mathcal{H}_i^n \to \mathbb{R}$
   such that $U_i(s, h_i) = u_i(s, t_i) + \psi_i(s, h_i^{(2)}, h_i^{(3)}, ...)$

The term $\psi_i$ captures belief-dependent payoffs (psychological payoffs).
\end{definition}

\begin{example}[Indignation]
Following Battigalli \& Dufwenberg (2009), indignation is:
$\psi_i^{IND}(s_i, s_{-i}, h_i^{(2)}) = -\beta \cdot \mathbf{1}_{s_i = D} \cdot h_i^{(2)}(C)$
where $\beta > 0$ is the indignation sensitivity parameter.
\end{example}
```

---

## 4. Gaps in Psychological Game Framework Definition

### Current Definition (Line 38-41)
```
We define an asymmetric game $\Gamma^{asym} = (N_H, N_A, S, U^H, U^A, \phi)$ where:
- Human utility $U_i^H(s, E_i)$ depends on beliefs (standard PGT)
- AI utility $U_j^A(s; \theta_j)$ depends only on outcomes and design parameters
- Attribution function $\phi$ bridges the asymmetry
```

**Major Issues**:
1. **No explicit psychological game definition**: Doesn't reference GPS 1989 or BD 2009
2. **Missing type spaces**: No $T_H$, $T_A$ specification
3. **Incomplete utility structure**: No decomposition into material + psychological components
4. **No prior distribution**: Missing common prior over types
5. **No strategy spaces**: $S_i$ not defined for humans vs. AI
6. **Attribution function ad hoc**: No theoretical foundation for $\phi$

### Required Framework Definition
```latex
\begin{definition}[Asymmetric Human-AI Psychological Game]
An asymmetric psychological game with human-AI interaction is:
$\Gamma = (N_H, N_A, \{T_i\}_{i \in N_H}, \{T_j\}_{j \in N_A}, \{S_i\}_{i \in N_H \cup N_A}, \{U_i\}_{i \in N_H}, \{U_j\}_{j \in N_A}, \phi, p)$

Where:
1. $N_H, N_A$ are finite sets of humans and AI agents
2. $T_i$ for $i \in N_H$ are human type spaces (heterogeneity in psychological parameters)
3. $T_j$ for $j \in N_A$ are AI design parameter spaces
4. $S_i$ are finite strategy sets
5. Human utility: $U_i(s, h_i) = \pi_i(s) + \psi_i(s, h_i^{(2)}, \tilde{h}_i^{(2)})$
   where $\psi_i$ captures indignation, guilt, reciprocity
6. AI utility: $U_j(s; \theta_j) = f_j(s; \theta_j)$ (no belief dependence)
7. Attribution function: $\phi: T_j \times X \times \Omega_i \to \Delta(\Delta(S_j))$
   maps AI design to attributed beliefs
8. $p \in \Delta(\times_{i \in N_H} T_i \times \times_{j \in N_A} T_j)$ is common prior
\end{definition}
```

---

## 5. Alignment with PGT Literature Conventions

### Current Gaps vs. Canon

| **PGT Element** | **Standard Reference** | **Current Status** | **Required Update** |
|-----------------|------------------------|-------------------|---------------------|
| Belief hierarchies | GPS 1989, BD 2009 | Too brief, non-standard notation | Define universal belief spaces, consistency |
| Psychological payoffs | GPS 1989 | Implicit, not formalized | Define $\psi_i$ function explicitly |
| Extended utility | BD 2009 | Missing decomposition | Show $U_i = \pi_i + \psi_i$ |
| Equilibrium concept | BD 2009,2016 | ABE is novel but undefined formally | Define ABE with sequential rationality |
| Types | Harsanyi 1968 | Missing human types | Define $T_i$ for psychological heterogeneity |
| Consistency | Mertens-Zamir 1985 | Not discussed | Add Bayesian consistency conditions |
| Examples | BD 2009 trust game | Mentioned but not formalized | Reference canonical trust game setup |

### Missing Canonical References
- **Geanakoplos, Pearce & Stacchetti (1989)**: "Psychological games and dynamic games"
- **Battigalli & Dufwenberg (2009)**: "Dynamic psychological games"
- **Battigalli & Dufwenberg (2016)**: "Partially specified dynamic psychological games"
- **Mertens & Zamir (1985)**: Universal belief spaces
- **Harsanyi (1968)**: Games with incomplete information
- **Brandenburger & Dekel (1993)**: Rationalizability and beliefs

---

## 6. Specific Line-by-Line Issues in Introduction.md

### Line 27-28
```latex
% Current:
\tilde{E}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)

% Should be:
\tilde{e}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i) \quad \text{where} \quad \tilde{e}_i^{(2,j)} \in \Delta(S_j)
% Need to specify what the belief is about (AI's expected action)
```

### Line 37-41
```latex
% Current (too vague):
\Gamma^{asym} = (N_H, N_A, S, U^H, U^A, \phi)

% Should specify:
\Gamma^{asym} = (N_H, N_A, \{T_i\}_{i \in N_H}, \{T_j\}_{j \in N_A}, \{S_i\}_{i \in N_H \cup N_A}, \{U_i\}_{i \in N_H}, \{U_j\}_{j \in N_A}, \phi, p)
```

### Line 40
```latex
% Current:
U_i^H(s, E_i) depends on beliefs (standard PGT)

% Should be:
U_i^H(s, h_i, \tilde{h}_i) = \pi_i(s) - \beta \cdot \mathbf{1}_{s_i=D} \cdot [h_i^{(2)}(C) + \tilde{h}_i^{(2)}(C)]
% Show explicit form of psychological payoff
```

---

## 7. Missing Mathematical Formalism

### Need to Add
1. **Belief space construction**:
```latex
\forall i \in N_H, \quad \mathcal{H}_i = \prod_{n=0}^\infty \Delta(\mathcal{H}_{-i}^n)
```

2. **Attribution function domain/codomain**:
```latex
\phi_i: \Theta_j \times X \times \Omega_i \to \Delta(\Delta(S_j))
```
Notationally, need to specify that $\tilde{E}_i^{(2,j)}$ is a belief about what AI $j$ expected.

3. **Psychological payoff function**:
```latex
\psi_i^H(s, h_i, \tilde{h}_i) = -\beta^H \cdot \mathbf{1}_{s_i=D} \cdot h_i^{(2)}(C) - \beta^A \cdot \mathbf{1}_{s_i=D} \cdot \tilde{h}_i^{(2)}(C)
```

4. **Consistency conditions**:
```latex
\text{(C1) H-H consistency: } h_i^{(n+1)} \text{ marginalizes to } h_i^{(n)}
\text{(C2) Attribution: } \tilde{h}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)
```

---

## 8. Framework.md Issues

### Current Problems
- **Line 19-21**: Non-standard belief notation
- **Line 37**: Utility decomposition missing $\psi_i$ explicitly
- **Line 40-41**: Indignation specification too ad hoc
- **Line 61**: "To develop" - belief consistency conditions not defined

### Required Additions
```latex
\section{Belief Consistency}

\begin{assumption}[Consistency]
The belief hierarchy $(h_i^{(1)}, h_i^{(2)}, ...)$ satisfies:
\begin{enumerate}
\item $h_i^{(n)} \in \Delta(\mathcal{H}_{-i}^{n-1})$ for all $n \geq 1$
\item $h_i^{(n)} = \mu_{\mathcal{H}_{-i}^{n-1}}(h_i^{(n+1)})$ where $\mu$ is marginalization
\end{enumerate}
\end{assumption}

\begin{assumption}[Attribution]
For each $i \in N_H$ and $j \in N_A$:
$\tilde{h}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$
where $\phi_i$ is continuous in $(\theta_j, x_j)$.
\end{assumption}
```

---

## 9. Existence.md Issues

### Current Problems
- **Line 9**: "Follows BD 2009" - but doesn't specify which theorem
- **Line 14**: Strategy spaces not properly defined (humans vs. AI different)
- **Line 20-23**: Missing psychological payoff in utility specification
- **Line 27**: "Belief consistency mapping" - not defined
- **Line 35**: "Key challenge" - but no solution approach specified

### Required Additions
```latex
\subsection{Extended Game Construction}

Define the extended game $\Gamma^e$ with:
- Human strategies: $\sigma_i: \mathcal{H}_i \to \Delta(S_i)$ (belief-contingent)
- AI strategies: $\tau_j: \Theta_j \to \Delta(S_j)$ (design-contingent)

Human i's expected utility given $\sigma, \tau, h_i$:
\[
EU_i(\sigma_i, \sigma_{-i}, \tau, h_i) = \sum_{s \in S} U_i(s, h_i, \phi_i(\theta_j, x_j, \omega_i)) \prod_{k \neq i} \sigma_k(h_k)(s_k) \prod_{\ell \in N_A} \tau_\ell(\theta_\ell)(s_\ell)
\]

Where $U_i(s, h_i, \tilde{h}_i) = \pi_i(s) + \psi_i(s, h_i^{(2)}, \tilde{h}_i^{(2)})$.

\subsection{Best Response Correspondence}

Human i's best response:
\[
BR_i^H(\sigma_{-i}, \tau, h_i) = \arg\max_{\sigma_i} EU_i(\sigma_i, \sigma_{-i}, \tau, h_i)
\]

AI j's best response:
\[
BR_j^A(\sigma, \tau_{-j}, \theta_j) = \arg\max_{\tau_j} \sum_{s \in S} U_j(s; \theta_j) \prod_{k \in N_H} \sigma_k(h_k)(s_k) \prod_{\ell \neq j} \tau_\ell(\theta_\ell)(s_\ell)
\]

\subsection{Fixed Point Mapping}

Define $\Phi: \prod_{i \in N_H} \Delta(S_i)^{\mathcal{H}_i} \times \prod_{j \in N_A} \Delta(S_j)^{\Theta_j} \to \prod_{i \in N_H} \Delta(S_i)^{\mathcal{H}_i} \times \prod_{j \in N_A} \Delta(S_j)^{\Theta_j}$ by:
\[
\Phi(\sigma, \tau) = (BR^H(\sigma, \tau), BR^A(\sigma, \tau))
\]

\begin{theorem}[Kakutani Fixed Point]
Under assumptions A1-A3, $\Phi$ has a fixed point $(\sigma^*, \tau^*)$.
\end{theorem}
```

---

## 10. Priority Updates for PGT Alignment

### Phase 1: Critical (Must Fix)
1. **Add proper belief hierarchy construction** (introduce universal belief spaces)
2. **Replace notation** with standard PGT notation ($h_i^{(n)}$ instead of $E_i^{(n)}$)
3. **Define psychological payoff function** $\psi_i$ explicitly
4. **Add consistency conditions** for both genuine and attributed beliefs
5. **Reference canonical PGT papers** explicitly in introduction

### Phase 2: Important (Should Fix)
1. **Formal equilibrium definition** with sequential rationality
2. **Type space construction** for human heterogeneity
3. **Examples** referencing canonical BD 2009 games
4. **Complete existence proof** with fixed point argument

### Phase 3: Nice to Have (Could Fix)
1. **Welfare analysis** section
2. **Comparative statics** with attribution parameters
3. **Dynamic extensions** (learning, reputation)

---

## 11. Recommended Revision Strategy

### Step 1: Restructure Introduction
```latex
1. Motivation (keep current)
2. Psychological Game Theory Background (ADD - 2 pages)
   - Define psychological games (GPS 1989)
   - Belief hierarchies and consistency
   - Extended utility functions
   - Examples: indignation, guilt
3. Asymmetric Human-AI Games (MODIFY - 2 pages)
   - New framework definition
   - Attribution function theory
   - Attributed Belief Equilibrium
4. Related Literature (keep current)
5. Contributions (keep current)
```

### Step 2: Fix Theory/Framework.md
- Replace all $E_i^{(n)}$ notation with standard $h_i^{(n)}$
- Add belief hierarchy construction
- Define $\psi_i$ function explicitly
- Add consistency assumptions

### Step 3: Complete Proofs/Existence.md
- Add detailed Kakutani fixed point proof
- Show continuity of best response correspondences
- Prove existence of ABE

---

## 12. Conclusion

The current introduction.md has **strong conceptual novelty** (attributed beliefs) but **lacks the formal mathematical rigor** expected in top-tier PGT papers. The primary issues are:

1. **Notation**: Non-standard, confusing notation throughout
2. **Formalism**: Missing belief hierarchy construction and consistency
3. **Literature**: Insufficient integration with canonical PGT
4. **Framework**: Incomplete game definition

**Recommended action**: Completely revise Sections 2-3 (Core Ideas and Methodology) to align with PGT standards before proceeding to applications or extensions. The attributed belief concept is valuable, but it must be built on solid PGT foundations.

**Estimated revision time**: 1-2 weeks for full alignment with PGT standards.
