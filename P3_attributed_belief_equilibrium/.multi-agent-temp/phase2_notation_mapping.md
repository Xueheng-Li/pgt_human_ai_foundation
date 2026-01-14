# Phase 2: Comprehensive Notation Mapping for PGT Human-AI Framework

## Executive Summary

This document provides a complete notation mapping to resolve inconsistencies identified in Phase 1 analysis. It standardizes notation with canonical PGT literature (GPS 1989, BD 2009) while introducing new notation for attributed beliefs in human-AI interactions.

**Key changes**: Replace $E$-notation with standard $h$-notation, formalize all spaces, introduce $\alpha$ for population fractions, align with BD2009 belief hierarchy conventions.

---

## Part I: Current → Standard Notation Mapping

### A. Strategy Notation (s vs a)

**Current usage inconsistency**: Documents use both $s$ and $a$ for strategies without clear convention.

**Standard convention** (adopted from normal-form game theory):
- $a_i \in A_i$: Action set for player $i$
- $a = (a_i, a_{-i}) \in A = \prod_i A_i$: Action profile
- $\sigma_i \in \Delta(A_i)$: Mixed strategy for player $i$
- $\sigma = (\sigma_i, \sigma_{-i}) \in \prod_i \Delta(A_i)$: Mixed strategy profile

**Usage in current documents**:
- ✓ `introduction.md`: Uses $s$ (keep)
- ✓ `framework.md`: Uses $s$ (keep)
- ✗ `applications/trust_game.md`: Uses $s$ (keep)
- ✗ `research_design/P3_*.md`: Uses $s$ (keep)

**Decision**: **Keep $s$ notation** throughout all documents for consistency with current usage.

---

### B. Belief Hierarchy Notation (E vs h)

**Current non-standard notation**:
- $E_i^{(1)}$: First-order beliefs
- $E_i^{(2,k)}$: Second-order beliefs about player $k$
- $\tilde{E}_i^{(2,j)}$: Attributed second-order beliefs about AI $j$

**Standard PGT notation** (BD 2009):
- $h_i^{(1)} \in \Delta(A_{-i})$: First-order beliefs
- $h_i^{(2)} \in \Delta(\Delta(A_{-i}))$: Second-order beliefs
- $\tilde{h}_i^{(2,j)} \in \Delta(A_j)$: Attributed beliefs about AI $j$'s expected action

**Migration path**:

| Current | Standard | Meaning |
|---------|----------|---------|
| $E_i^{(1)}$ | $h_i^{(1)}$ | First-order beliefs about others' actions |
| $E_i^{(2,k)}$ | $h_i^{(2,k)}$ | Second-order beliefs about what $k$ expects |
| $\tilde{E}_i^{(2,j)}$ | $\tilde{h}_i^{(2,j)}$ | Attributed beliefs about AI $j$'s "expectations" |

**Update required in all files**:
- `theory/framework.md`: Lines 19-20, 26, 40-41
- `introduction.md`: Lines 27, 49
- `proofs/existence.md`: Lines 14, 20
- `applications/*.md`: Throughout
- `research_design/P3_*.md`: Lines 29, 77, 99-108

**Recommendation**: Replace ALL $E$-notation with $h$-notation in next revision.

---

### C. Belief Hierarchy Construction

**Missing from current documents**: Universal belief space definition.

**Standard construction** (Mertens-Zamir 1985, BD 2009):

```latex
\begin{definition}[Universal Belief Hierarchy]
For player $i$, define recursively:
\begin{align}
\mathcal{H}_i^0 &= T_i &&\text{(types)}\\
\mathcal{H}_i^1 &= \Delta\left( \times_{k \neq i} T_k \times A_{-i} \right) &&\text{(first-order)}\\
\mathcal{H}_i^n &= \Delta\left( \times_{k \neq i} \mathcal{H}_k^{n-1} \right) &&\text{($n$-th order)}\\
\mathcal{H}_i &= \prod_{n=0}^\infty \mathcal{H}_i^n &&\text{(full hierarchy)}
\end{align}

A belief system is $h_i = (h_i^{(0)}, h_i^{(1)}, h_i^{(2)}, \ldots) \in \mathcal{H}_i$ where:
- $h_i^{(0)} = t_i \in T_i$ is $i$'s type
- $h_i^{(1)} \in \Delta(\times_{k \neq i} T_k \times A_{-i})$ are first-order beliefs
- $h_i^{(2)} \in \Delta(\times_{k \neq i} \mathcal{H}_k^1)$ are second-order beliefs
- etc.
\end{definition}
```

**Required addition to**: `theory/framework.md` (after line 13)

---

## Part II: Formal Space Definitions

### A. Type Spaces

**Currently missing**: Formal definition of type spaces.

**Definition**:
```latex
\begin{definition}[Type Spaces]
\begin{align}
T_i &\subseteq \mathbb{R}^{m_i} &&\text{Human $i$'s type space} &&\text{(psychological parameters: }\beta, \gamma, \omega_i\text{)}\\
\Theta_j &\subseteq \mathbb{R}^{p_j} &&\text{AI $j$'s design parameter space} &&\text{(prosociality: }\gamma_j\text{, conditionality)}\\
T &= \times_{i \in N_H} T_i \times \times_{j \in N_A} \Theta_j &&\text{Joint type space}
\end{align}
\end{definition}
```

**Human types** $t_i = (\beta_i, \omega_i) \in T_i$ where:
- $\beta_i > 0$: Indignation sensitivity parameter
- $\omega_i \in [0,1]$: Anthropomorphism tendency

**AI types** $\theta_j = (\gamma_j, \tau_j) \in \Theta_j$ where:
- $\gamma_j \in \mathbb{R}$: Programmed prosociality parameter
- $\tau_j$: Behavioral type (materialist, prosocial, conditional)

**Required addition to**: `theory/framework.md` (after line 5)

---

### B. Attribution Function Spaces

**Currently referenced but undefined**: $\Theta$, $X$, $\Omega$.

**Definition**:
```latex
\begin{definition}[Attribution Function Components]
For human $i$ facing AI $j$:

\begin{align}
\Theta_j &\quad\text{AI $j$'s design parameter space} &&(\theta_j \in \Theta_j)\\
X_j &\quad\text{Set of observable signals from AI $j$} &&(x_j \in X_j)\\
\Omega_i &\quad\text{Human $i$'s individual characteristics} &&(\omega_i \in \Omega_i)
\end{align}

The attribution function is:
\[
\phi_i: \Theta_j \times X_j \times \Omega_i \to \Delta(A_j)
\]
mapping AI design and observable signals to attributed beliefs about AI's expected action.
\end{definition}
```

**Specifications**:
- $\Theta_j = \mathbb{R}$ (prosociality parameter $\gamma_j$)
- $X_j = \mathbb{R}^k$ (interface cues, behavioral signals)
- $\Omega_i = [0,1]$ (anthropomorphism tendency $\omega_i$)

**Required addition to**: `theory/framework.md` (lines 28-32)

---

### C. Population Structure (α)

**Mentioned in CLAUDE.md but missing from documents**: Population fraction $\alpha$.

**Definition**:
```latex
\begin{definition}[Population Composition]
Let:
\begin{align}
N_H &= \text{Number of human players}\\
N_A &= \text{Number of AI players}\\
N &= N_H + N_A = \text{Total population size}
\end{align}

Define the human population share:
\[
\alpha = \frac{N_H}{N} \in [0,1]
\]
and AI population share:
\[
1 - \alpha = \frac{N_A}{N}
\]

For large populations, we may write $N_H = \alpha N$, $N_A = (1-\alpha)N$.
\end{definition}
```

**Usage**:
- Used in stochastic stability analysis (P1)
- Appears in welfare comparisons
- Critical for threshold theorems

**Required addition to**: `theory/framework.md` (after line 8)

---

## Part III: Complete Symbol Table

### A. Core Game Structure

| Symbol | Definition | Type | First Use |
|--------|------------|------|-----------|
| $N_H$ | Set of human players | Set | All documents |
| $N_A$ | Set of AI agents | Set | All documents |
| $N$ | $N_H \cup N_A$ | Set | New |
| $n_H = \|N_H\|$ | Number of humans | Integer | New |
| $n_A = \|N_A\|$ | Number of AI | Integer | New |
| $\alpha$ | Human population share | Real $[0,1]$ | New |
| $A_i$ | Human $i$'s action set | Set | All documents |
| $A_j$ | AI $j$'s action set | Set | All documents |
| $A = \prod_{k \in N} A_k$ | Action profile space | Set | All documents |
| $a = (a_i, a_{-i})$ | Action profile | Tuple | All documents |
| $\sigma_i \in \Delta(A_i)$ | Mixed strategy (human) | Probability measure | Standard |
| $\sigma_j \in \Delta(A_j)$ | Mixed strategy (AI) | Probability measure | Standard |
| $\sigma = (\sigma_i, \sigma_{-i})$ | Strategy profile | Tuple | Standard |

### B. Type Spaces and Parameters

| Symbol | Definition | Type | Notes |
|--------|------------|------|-------|
| $T_i$ | Human $i$'s type space | Set | Psychological parameters |
| $\Theta_j$ | AI $j$'s design space | Set | Programmed parameters |
| $t_i \in T_i$ | Human type | Vector | $(\beta_i, \omega_i)$ |
| $\theta_j \in \Theta_j$ | AI design parameters | Vector | $(\gamma_j, \tau_j)$ |
| $\beta_i > 0$ | Indignation sensitivity | Real | Human heterogeneity |
| $\gamma_j \in \mathbb{R}$ | AI prosociality | Real | Design parameter |
| $\omega_i \in [0,1]$ | Anthropomorphism tendency | Real | Human heterogeneity |
| $\tau_j$ | AI behavioral type | Categorical | Materialist/prosocial/conditional |
| $X_j$ | Observable signals from AI $j$ | Set | Interface, behavior |
| $x_j \in X_j$ | Signal realization | Element | May be random |
| $\Omega_i$ | Human $i$'s individual characteristics | Set | $\omega_i \in \Omega_i$ |

### C. Belief Hierarchies

| Symbol | Definition | Type | Consistency |
|--------|------------|------|-------------|
| $h_i^{(0)} = t_i$ | Player $i$'s type | $T_i$ | Trivial |
| $h_i^{(1)} \in \Delta(A_{-i})$ | First-order beliefs | Probability measure | Bayesian |
| $h_i^{(2)} \in \Delta(\Delta(A_{-i}))$ | Second-order beliefs | Probability measure | Bayesian |
| $h_i^{(n)}$ | $n$-th order beliefs | Probability measure | Bayesian |
| $h_i = (h_i^{(0)}, h_i^{(1)}, \ldots)$ | Full belief hierarchy | Tuple | Consistency required |
| $\tilde{h}_i^{(2,j)} \in \Delta(A_j)$ | Attributed beliefs about AI $j$ | Probability measure | Attribution function |
| $\mathcal{H}_i^n$ | $n$-th order belief space | Set | Universal construction |
| $\mathcal{H}_i = \prod_{n=0}^\infty \mathcal{H}_i^n$ | Full hierarchy space | Set | Complete belief system |

**Consistency conditions**:
```latex
\begin{assumption}[Belief Consistency]
For all $i \in N_H$, $n \geq 1$:
\begin{enumerate}
\item $h_i^{(n)} \in \Delta(\times_{k \neq i} \mathcal{H}_k^{n-1})$
\item $h_i^{(n)} = \mu_{\times_{k \neq i} \mathcal{H}_k^{n-1}}(h_i^{(n+1)})$ where $\mu$ is marginalization
\end{enumerate}
\end{assumption}
```

### D. Utility Functions

| Symbol | Definition | Type | Notes |
|--------|------------|------|-------|
| $\pi_i(a)$ | Material payoff to $i$ | Real | Standard |
| $\psi_i(a, h_i)$ | Psychological payoff to human $i$ | Real | Belief-dependent |
| $U_i^H(a, h_i, \tilde{h}_i)$ | Human $i$'s total utility | Real | $\pi_i + \psi_i$ |
| $U_j^A(a; \theta_j)$ | AI $j$'s utility | Real | Design-dependent |
| $\beta_i > 0$ | Indignation parameter | Real | From type $t_i$ |
| $\gamma_j \in \mathbb{R}$ | AI prosociality parameter | Real | From design $\theta_j$ |

**Human utility decomposition**:
```latex
\begin{definition}[Human Utility]
For human $i \in N_H$:
\[
U_i^H(a, h_i, \tilde{h}_i) = \pi_i(a) + \psi_i^{IND}(a, h_i^{(2)}, \tilde{h}_i^{(2)})
\]
where indignation is:
\[
\psi_i^{IND}(a, h_i^{(2)}, \tilde{h}_i^{(2)}) = -\beta_i \cdot \mathbf{1}_{a_i = D} \cdot \left[ \sum_{k \in N_H} h_i^{(2,k)}(C) + \sum_{j \in N_A} \tilde{h}_i^{(2,j)}(C) \right]
\]
\end{definition}
```

### E. Attribution Function

| Symbol | Definition | Type | Domain/Codomain |
|--------|------------|------|-----------------|
| $\phi_i$ | Human $i$'s attribution function | Function | $\Theta_j \times X_j \times \Omega_i \to \Delta(A_j)$ |
| $\tilde{h}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$ | Attributed beliefs | Probability measure | $\Delta(A_j)$ |

**Assumption on attribution function**:
```latex
\begin{assumption}[Attribution]
For each $i \in N_H$, $j \in N_A$:
\begin{enumerate}
\item $\phi_i(\theta_j, x_j, \omega_i) \in \Delta(A_j)$
\item $\phi_i$ is continuous in $(\theta_j, x_j)$
\item $\tilde{h}_i^{(2,j)}$ is interpreted as "what $i$ believes $j$ expected $i$ to do"
\end{enumerate}
\end{assumption}
```

---

## Part IV: Alignment with BD2009 Conventions

### A. Belief Hierarchy Notation

**Standard BD2009 notation** (from "Dynamic psychological games"):

| BD2009 | Our Framework | Notes |
|--------|---------------|-------|
| $\beta_i$ | $h_i^{(1)}$ | First-order beliefs (we use $h$ not $\beta$) |
| $\beta_i^2$ | $h_i^{(2)}$ | Second-order beliefs |
| $\mu_i$ | $h_i$ | Full hierarchy |
| $u_i(s, \mu_i)$ | $U_i^H(a, h_i, \tilde{h}_i)$ | Extended utility |
| $\psi_i(s, \mu_i)$ | $\psi_i(a, h_i^{(2)}, \tilde{h}_i^{(2)})$ | Psychological payoff |

**Departure from BD2009**: We use $h$ instead of $\beta$ for beliefs to avoid confusion with indignation parameter $\beta$.

**Justification**: $\beta$ is standard for indignation sensitivity in PGT literature (GPS 1989, Li 2026). Using different symbol for beliefs reduces cognitive load.

---

### B. Extended Utility Function

**BD2009 format**:
```latex
U_i(s, h_i) = u_i(s, t_i) + \psi_i(s, h_i^{(2)}, h_i^{(3)}, \ldots)
```

**Our format** (extended for attributed beliefs):
```latex
U_i^H(a, h_i, \tilde{h}_i) = \pi_i(a) + \psi_i^{IND}(a, h_i^{(2)}, \tilde{h}_i^{(2)})
```

**Key differences**:
1. Separate notation for genuine ($h_i$) vs attributed ($\tilde{h}_i$) beliefs
2. Psychological payoff only depends on second-order beliefs (standard in indignation models)
3. Different notation for material payoff ($\pi_i$ vs $u_i$)

**Rationale**:
- $\pi_i$ is more intuitive for "material" or " pecuniary" payoff
- Separate notation for attributed beliefs clarifies the asymmetry

---

### C. Equilibrium Concept Alignment

**BD2009 Sequential Psychological Equilibrium (SPE)**:
1. Sequential rationality given beliefs
2. Belief consistency via Bayes' rule
3. Common knowledge of rationality

**Our Attributed Belief Equilibrium (ABE)**:
1. Sequential rationality for humans (given genuine + attributed beliefs)
2. Sequential rationality for AI (given design)
3. Belief consistency for H-H interactions (Bayes' rule)
4. Attribution consistency for H-A interactions ($\tilde{h}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$)

**Key innovation**: Condition 4 replaces BD2009's common knowledge assumption with asymmetric attribution.

---

## Part V: Undefined Symbols Requiring Definition

### A. High Priority (Must Define)

1. **$\mathcal{E}$** (existence.md line 27)
   - Used for "belief consistency mapping"
   - Should be $\mathcal{H} = \prod_i \mathcal{H}_i$ (full hierarchy space)

2. **$\bar{c}$** (public_goods.md line 11)
   - Norm threshold in public goods game
   - Define as endogenously determined or exogenous parameter

3. **$E_k^{(1,i)}$** (research_design/P3_*.md line 105)
   - First-order beliefs about what $k$ thinks about $i$
   - Should be $h_k^{(1,i)}$ with standard notation

4. **$\mu$** (existence.md line 28)
   - Marginalization operator
   - Define explicitly: $\mu_{\mathcal{X}}(p)$ for $p \in \Delta(\mathcal{X} \times \mathcal{Y})$

### B. Medium Priority (Should Define)

1. **$\kappa$** (research_design/P3_*.md line 60)
   - Reciprocity parameter
   - Add to type space $T_i$

2. **$m$** (public_goods.md line 7)
   - Multiplier in public goods game
   - Define: $m \in (1/n, 1)$

3. **$g(\cdot)$** (applications/trust_game.md line 17)
   - Interface function
   - Specify functional form

### C. Low Priority (Could Define)

1. **$\lambda$** (mentioned in CLAUDE.md)
   - Ratio of mutation rates $\epsilon_A/\epsilon_H$
   - Used in P1, not P3

---

## Part VI: New Symbols for Attributed Beliefs

### A. Core Attributed Belief Notation

| Symbol | Definition | Rationale |
|--------|------------|-----------|
| $\tilde{h}_i^{(2,j)}$ | Attributed second-order beliefs about AI $j$ | Novel extension of BD2009 |
| $\tilde{h}_i^{(1,j)}$ | Attributed first-order beliefs about AI $j$ | What $i$ thinks $j$ will do |
| $\tilde{\mathcal{H}}_i$ | Space of attributed beliefs | New concept |
| $\phi_i$ | Attribution function | Maps AI design to attributed beliefs |

### B. Extended Notation (Future Use)

| Symbol | Definition | Use Case |
|--------|------------|----------|
| $\tilde{h}_i^{(3,j,k)}$ | Attributed third-order beliefs | What $i$ thinks $j$ thinks $k$ expects |
| $\hat{h}_i^{(2,j)}$ | "Meta-attributed" beliefs | What $i$ thinks $j$ thinks $i$ thinks... |
| $\phi_i^{(n)}$ | Higher-order attribution | For complex belief hierarchies |

**Note**: These extensions may be needed for more sophisticated models but are not required for core ABE definition.

---

## Part VII: Recommendations for Introduction Updates

### A. Section 2: Core Ideas (Replace Lines 23-41)

**Current text** (problematic):
```
When human i interacts with AI j, the human forms attributed second-order beliefs:
$\tilde{E}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$

This attribution function $\phi_i$ maps:
- $\theta_j$: AI's design parameters
- $x_j$: Observable signals
- $\omega_i$: Individual characteristics
```

**Recommended replacement**:
```latex
\subsection{Attributed Beliefs in Human-AI Interaction}

When human $i$ interacts with AI $j$, the human forms \emph{attributed} beliefs about the AI's "expectations"—even though AI has no genuine beliefs. Formally:

\[
\tilde{h}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)
\]

where:
\begin{itemize}
\item $\theta_j \in \Theta_j$ are AI $j$'s design parameters (e.g., prosociality level $\gamma_j$)
\item $x_j \in X_j$ are observable signals (interface design, behavioral cues)
\item $\omega_i \in \Omega_i$ is human $i$'s anthropomorphism tendency
\item $\tilde{h}_i^{(2,j)} \in \Delta(A_j)$ represents what human $i$ believes AI $j$ expected $i$ to do
\end{itemize}

The key insight: humans psychologically project mental states onto AI, creating asymmetric belief structures central to our equilibrium concept.
```

**Benefits**:
1. Uses standard $h$-notation
2. Formally defines spaces $\Theta_j$, $X_j$, $\Omega_i$
3. Clarifies what attributed beliefs represent
4. Connects to psychological evidence on anthropomorphism

### B. Section 3: Asymmetric Game Structure (Replace Lines 38-50)

**Current text** (incomplete):
```
We define an asymmetric game $\Gamma^{asym} = (N_H, N_A, S, U^H, U^A, \phi)$ where:
- Human utility $U_i^H(s, E_i)$ depends on beliefs (standard PGT)
- AI utility $U_j^A(s; \theta_j)$ depends only on outcomes and design parameters
- Attribution function $\phi$ bridges the asymmetry
```

**Recommended replacement**:
```latex
\subsection{Asymmetric Human-AI Games}

We define a psychological game with asymmetric player types:

\[
\Gamma^{asym} = (N_H, N_A, \{T_i\}_{i \in N_H}, \{\Theta_j\}_{j \in N_A}, \{A_i\}_{i \in N_H \cup N_A}, \{U_i^H\}_{i \in N_H}, \{U_j^A\}_{j \in N_A}, \{\phi_i\}_{i \in N_H}, p)
\]

\begin{itemize}
\item $N_H, N_A$ are finite sets of humans and AI agents
\item $T_i \subseteq \mathbb{R}^{m_i}$ are human type spaces capturing psychological heterogeneity
\item $\Theta_j \subseteq \mathbb{R}^{p_j}$ are AI design parameter spaces
\item $A_k$ are finite action sets for all players
\item Human utility: $U_i^H(a, h_i, \tilde{h}_i) = \pi_i(a) + \psi_i(a, h_i^{(2)}, \tilde{h}_i^{(2)})$ where $\psi_i$ captures indignation and guilt
\item AI utility: $U_j^A(a; \theta_j) = f_j(a; \theta_j)$ with no belief dependence
\item Attribution functions: $\phi_i: \Theta_j \times X_j \times \Omega_i \to \Delta(A_j)$ for each human $i$
\item $p \in \Delta(\times_{i \in N_H} T_i \times \times_{j \in N_A} \Theta_j)$ is common prior over types
\end{itemize}
```

**Benefits**:
1. Complete game definition with all components
2. Uses standard PGT notation
3. Explicitly shows utility decomposition ($\pi_i + \psi_i$)
4. References canonical psychological game literature

---

## Part VIII: Implementation Timeline

### Phase 1: Critical Updates (Week 1)

**Files to modify**:
1. `theory/framework.md` - Add all space definitions, belief hierarchy construction
2. `introduction.md` - Replace notation, add formal definitions
3. `research_design/P3_*.md` - Update notation throughout

**Key changes**:
- Replace ALL $E$-notation with $h$-notation
- Define $\Theta$, $X$, $\Omega$ spaces
- Add $\alpha$ for population fraction
- Add belief hierarchy construction

### Phase 2: Important Updates (Week 2)

**Files to modify**:
1. `proofs/existence.md` - Update with standard notation
2. `applications/trust_game.md` - Replace notation, define $\bar{c}$
3. `applications/public_goods.md` - Replace notation, define $m$

**Key changes**:
- Use $h$-notation in proofs
- Define all parameters explicitly
- Add consistency conditions

### Phase 3: Cleanup (Week 3)

**Tasks**:
- Scan all documents for undefined symbols
- Ensure consistency across all files
- Add LaTeX formatting where missing
- Update CLAUDE.md with new notation

---

## Part IX: LaTeX Formatting Standards

### A. Mathematical Notation

**Use**:
- `$h_i^{(n)}$` for inline math
- `$$h_i^{(n)} \in \Delta(A_{-i})$$` for display math
- `\begin{definition}...\end{definition}` for formal definitions
- `\begin{assumption}...\end{assumption}` for assumptions

**Avoid**:
- `\text{}` inside math mode (use `\mathrm{}` or `\operatorname{}`)
- Inconsistent spacing around operators
- Mixing text and math without proper commands

### B. Cross-References

**Use**:
- `\label{def:belief-hierarchy}` for definitions
- `\autoref{def:belief-hierarchy}` for references
- `\nameref{def:belief-hierarchy}` for names

**Example**:
```latex
\begin{definition}[Belief Hierarchy]
\label{def:belief-hierarchy}
...
\end{definition}

See \autoref{def:belief-hierarchy} for the formal construction.
```

### C. Symbol Consistency

**Create a symbol list** at the beginning of each major document:

```latex
\section*{Notation}

\subsection*{Players and Population}
\begin{tabbing}
$N_H$ \quad \= Set of humans \\
$N_A$ \> Set of AI agents \\
$\alpha$ \> Human population share
\end{tabbing}

\subsection*{Types and Beliefs}
\begin{tabbing}
$T_i$ \quad \= Human $i$'s type space \\
$h_i^{(1)}$ \> First-order beliefs \\
$\tilde{h}_i^{(2,j)}$ \> Attributed beliefs about AI $j$
\end{tabbing}
```

---

## Part X: Quality Checklist

Before finalizing notation:

- [ ] All $E$-notation replaced with $h$-notation
- [ ] All spaces ($\Theta$, $X$, $\Omega$) formally defined
- [ ] $\alpha$ introduced and used consistently
- [ ] Belief hierarchy construction added to framework
- [ ] Consistency conditions explicitly stated
- [ ] Psychological payoff function $\psi_i$ defined
- [ ] Attribution function $\phi_i$ domain/codomain specified
- [ ] All undefined symbols (marked in Part V) given definitions
- [ ] Cross-references working properly
- [ ] LaTeX formatting consistent
- [ ] Symbol table included in each major document

---

## Conclusion

This mapping provides a complete standardization of notation aligned with canonical PGT literature while introducing the novel concept of attributed beliefs. The key innovation—extending BD2009's symmetric belief hierarchies to asymmetric H-A interactions—requires careful notation to maintain rigor.

**Priority 1**: Replace $E$-notation with $h$-notation throughout
**Priority 2**: Add formal definitions of all spaces
**Priority 3**: Introduce belief hierarchy construction
**Priority 4**: Ensure consistency across all documents

The attributed belief equilibrium is conceptually novel but must be built on solid mathematical foundations. This notation mapping ensures that foundation is in place.

---

*Phase 2 completion: 2026-01-11*
*Next: Implementation in all P3 documents*
