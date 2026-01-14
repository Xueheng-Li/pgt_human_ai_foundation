# Phase 3: Specific Actionable Recommendations

**Generated**: 2026-01-12
**Scope**: All 24 identified issues (2 critical, 8 major, 14 minor)

---

## Critical Issues

### Issue C1: Gamma Symbol Collision - Human Guilt vs AI Prosociality

**Problem**: The symbol $\gamma$ is overloaded with two semantically different meanings:
- $\gamma_i$ = human guilt sensitivity (a psychological trait, Definition 4)
- $\gamma_j$/$\gamma_A$ = AI prosociality parameter (a design choice)

This collision appears in framework (L13, L26, L80-82), applications (L11, L15, L19), and welfare (L28-29).

**Recommendation**: Rename AI prosociality parameter to $\rho$ (rho) throughout the manuscript. Keep $\gamma_i$ for human guilt sensitivity.

**Specific Text Changes**:

| File | Line | Current Text | Suggested Text |
|------|------|--------------|----------------|
| sec_framework.tex | L26 | `prosocial ($U_j^A = \pi_j(s) + \gamma_j \sum_{k \in N} \pi_k(s)$)` | `prosocial ($U_j^A = \pi_j(s) + \rho_j \sum_{k \in N} \pi_k(s)$)` |
| sec_framework.tex | L80 | `$\gamma_j \in [0,1]$ is AI's prosociality parameter` | `$\rho_j \in [0,1]$ is AI's prosociality parameter` |
| sec_framework.tex | L82 | `increase with AI prosociality, anthropomorphic signals` | (no change needed - uses prose) |
| sec_applications.tex | L11 | `$\gamma_A$` | `$\rho_A$` |
| sec_applications.tex | L13 | `$U_A(x, y; \gamma_A)$` | `$U_A(x, y; \rho_A)$` |
| sec_applications.tex | L15 | `A prosocial AI ($\gamma_A > 0$)` | `A prosocial AI ($\rho_A > 0$)` |
| sec_applications.tex | L21 | `$\phi_H(\gamma_A, x_A, \omega_H)$` | `$\phi_H(\rho_A, x_A, \omega_H)$` |
| sec_welfare.tex | L28 | `($\gamma_A > 0$)` | `($\rho_A > 0$)` |
| sec_welfare.tex | L29 | `($\gamma_A = 0$)` | `($\rho_A = 0$)` |

**Rationale**:
- $\gamma$ is established in psychological game theory literature for guilt sensitivity
- $\rho$ (rho) is commonly used for correlation or "relatedness" parameters, making it intuitive for prosociality
- Alternative considered: $\eta_j$ (eta) - rejected because $\eta$ appears in L80 for signal sensitivity
- Alternative considered: $\mu_j$ (mu) - acceptable but $\rho$ is more evocative of "prosocial relationship"

---

### Issue C2: Missing Definition - Marginal First-Order Belief $h_i^{(1,k)}$

**Problem**: The equilibrium section (L25-26) uses $h_i^{*(1,k)} = s_k^*$ to express first-order belief consistency about specific player $k$, but the framework (L33) only defines $h_i^{(1)} \in \Delta(S_{-i})$ as a joint distribution over all other players' strategies.

**Recommendation**: Add a clarifying definition of marginal beliefs to the framework's Belief Hierarchies subsection.

**Specific Text Changes**:

**File**: sec_framework.tex
**Location**: After L35 (after the belief hierarchy equations)
**Add new text**:
```latex
For any $k \neq i$, we write $h_i^{(1,k)} \in \Delta(S_k)$ for the marginal of $h_i^{(1)}$ on player $k$'s strategy space. Similarly, $h_i^{(2,k)} \in \Delta(\Delta(S_{-k}))$ denotes $i$'s second-order belief about $k$'s first-order belief.
```

**Rationale**:
- Economic theory papers routinely use marginal notation without explicit definition, so informal usage is acceptable
- However, for a paper defining a new equilibrium concept, explicit definition strengthens the logical foundation
- The added sentence clarifies both first- and second-order marginals in one statement
- This is standard notation in epistemic game theory (cf. Dekel & Siniscalchi, Handbook of Game Theory)

---

## Major Issues

### Issue M1: Missing Definition - Rational Attribution Benchmark $\tilde{h}_i^{(2,j),RAT}$

**Problem**: Welfare section (L43-45) uses $\tilde{h}_i^{(2,j),RAT}$ for the "rational benchmark" without formal definition. Proposition 9 (over-anthropomorphism) depends on this undefined object.

**Recommendation**: Define the rational attribution benchmark in the Attribution Function subsection of the framework.

**Specific Text Changes**:

**File**: sec_framework.tex
**Location**: After Definition 2 (Attribution Function), around L66
**Add new definition**:
```latex
\begin{defn}[Rational Attribution Benchmark]
\label{def:rational-benchmark}
The \textbf{rational attribution benchmark} $\tilde{h}_i^{(2,j),RAT}$ is the attributed belief that a fully informed, rational agent would hold:
\begin{equation}
    \tilde{h}_i^{(2,j),RAT} = \lim_{\omega_i \to 0} \phi_i(\theta_j, x_j, \omega_i),
\end{equation}
representing the limiting attributed belief when anthropomorphism tendency approaches zero.
\end{defn}
```

**Alternative formulation** (if zero anthropomorphism is too strong):
```latex
\begin{defn}[Rational Attribution Benchmark]
\label{def:rational-benchmark}
The \textbf{rational attribution benchmark} $\tilde{h}_i^{(2,j),RAT}$ is the attributed belief consistent with AI's actual objective function: the belief that AI $j$ "expects" the strategy profile maximizing $U_j^A(\cdot; \theta_j)$.
\end{defn}
```

**Rationale**: The first formulation ties the benchmark to the anthropomorphism parameter, making it operationally clear. The second formulation is more conceptually accurate but requires specifying how objectives map to "expectations."

---

### Issue M2: Argument Structure Inconsistency - $U_i^H$ Function

**Problem**: Human utility function has three different argument structures:
- Framework L19: $U_i^H(s, h_i, \tilde{h}_i)$ (3 arguments: profile, beliefs, attributed beliefs)
- Equilibrium L15: $U_i^H(s_i, s_{-i}^*, h_i^*, \tilde{h}_i^*)$ (4 arguments: own strategy separated)
- Applications L19: $U_H(y; \tilde{h}_H)$ (2 arguments with semicolon)

**Recommendation**: Clarify that these are equivalent forms used in different contexts.

**Specific Text Changes**:

**File**: sec_framework.tex
**Location**: After equation (1), around L20
**Add clarifying note**:
```latex
When $i$ optimizes, we write $U_i^H(s_i, s_{-i}, h_i, \tilde{h}_i)$ with own strategy $s_i$ as a separate argument. In applications with single human and AI, we abbreviate to $U_H(\cdot; \tilde{h}_H)$, suppressing fixed arguments.
```

**Rationale**: This is standard practice in economics papers - the clarifying note makes the convention explicit without burdening the framework with cumbersome notation.

---

### Issue M3: Attenuation Factor Missing Subscript in Welfare

**Problem**: Welfare section uses $\lambda^{IND}$, $\lambda^{GUILT}$, $\lambda$ without individual subscript $i$, inconsistent with framework's $\lambda_i^{IND}$.

**Recommendation**: Either add subscripts consistently or explicitly state representative-agent assumption.

**Specific Text Changes**:

**File**: sec_welfare.tex
**Location**: L75, before first use of $\lambda$ without subscript
**Add**:
```latex
For the welfare analysis, we focus on a representative human with attenuation factors $\lambda^{IND}$ and $\lambda^{GUILT}$, suppressing the individual subscript.
```

**Rationale**: Representative-agent assumption is standard in welfare economics. Explicit statement prevents confusion while keeping notation clean.

---

### Issue M4: A1c Subscript Reference Without Definition

**Problem**: Existence proof (sec_equilibrium.tex L65) references "A1c (continuity)" but Assumption A1 in the framework has no sub-labels.

**Recommendation**: Change the reference to "A1 (continuity)" since A1 mentions continuity.

**Specific Text Changes**:

**File**: sec_equilibrium.tex
**Line**: L65
**Current**: `By A1 (compactness) and A1c (continuity)`
**Suggested**: `By A1 (compactness and continuity)`

**Alternative**: Add explicit sub-labels to Assumption A1 in framework:
```latex
\begin{assumption}[Regularity]
\label{ass:regularity}
(A1) (a) Strategy spaces $S_i$ are non-empty and finite. (b) Type spaces $T_i$ and $\Theta_j$ are non-empty, convex, and compact. (c) Payoff functions are continuous.
\end{assumption}
```

**Rationale**: Simple fix requires minimal change. Alternative is more precise but adds complexity.

---

### Issue M5: Generic $\lambda_i$ Without Emotion Superscript in Coordination

**Problem**: Coordination game (sec_applications.tex L74) uses $\lambda_i$ without specifying IND or GUILT superscript.

**Recommendation**: Define "expectation-matching" as a third psychological mechanism, or clarify this is indignation-like.

**Specific Text Changes**:

**File**: sec_applications.tex
**Line**: L72-74
**Current**:
```latex
\psi_i = -\beta_i \cdot \mathbf{1}_{s_i \neq s^{exp}} \cdot \left[ \sum_{k \in N_H} h_i^{(2,k)}(s^{exp}) + \lambda_i \sum_{j \in N_A} \tilde{h}_i^{(2,j)}(s^{exp}) \right].
```
**Suggested**:
```latex
\psi_i^{COORD} = -\beta_i \cdot \mathbf{1}_{s_i \neq s^{exp}} \cdot \left[ \sum_{k \in N_H} h_i^{(2,k)}(s^{exp}) + \lambda_i^{COORD} \sum_{j \in N_A} \tilde{h}_i^{(2,j)}(s^{exp}) \right],
```
And add after equation: `where $\lambda_i^{COORD}$ is the coordination-specific attenuation factor (analogous to $\lambda_i^{IND}$).`

**Alternative**: Change $\lambda_i$ to $\lambda_i^{IND}$ if coordination disappointment is treated as indignation.

**Rationale**: Explicit labeling clarifies which psychological mechanism is operating.

---

### Issue M6: Psychological Payoff Missing Second-Order Superscript in Welfare

**Problem**: Welfare (L17) uses $\psi_i(s, h_i, \tilde{h}_i)$ but framework (L19) uses $\psi_i(s, h_i^{(2)}, \tilde{h}_i^{(2)})$.

**Recommendation**: Add note that $h_i$ abbreviates $h_i^{(2)}$ in welfare context.

**Specific Text Changes**:

**File**: sec_welfare.tex
**Line**: Around L17
**Add footnote or parenthetical**: `(where $h_i$ and $\tilde{h}_i$ abbreviate the second-order belief structures $h_i^{(2)}$ and $\tilde{h}_i^{(2)}$)`

**Rationale**: Minor clarification maintains consistency without cluttering equations.

---

### Issue M7: $x_A^*$ Design Variable Conflicts with Signal Notation

**Problem**: Welfare uses $x_A^*$ for "optimal anthropomorphic design" but $x_j$ denotes "observable signals" in Definition 2.

**Recommendation**: Clarify that $x_A^*$ is the optimal choice of the signal $x_A$.

**Specific Text Changes**:

**File**: sec_welfare.tex
**Line**: L63
**Current**: `The optimal level of anthropomorphic design $x_A^*$ satisfies`
**Suggested**: `The optimal anthropomorphic signal $x_A^* \in X$ satisfies`

**Rationale**: Makes clear that $x_A^*$ is an optimized value of the signal variable $x_A$, not a new notation.

---

### Issue M8: Proposition 3 Precision Issue - "Consistent with AI's Objective"

**Problem**: Proposition 3 (rational attribution) uses imprecise phrase "consistent with AI's actual objective function."

**Recommendation**: Define precisely what "consistent" means.

**Specific Text Changes**:

**File**: sec_equilibrium.tex
**Location**: Proposition 3 statement (around L102-105)
**Current**: `If the attribution function $\phi_i$ maps to beliefs consistent with AI's actual objective function`
**Suggested**: `If the attribution function satisfies $\phi_i(\theta_j, x_j, \omega_i) = \mathbb{E}[s_i^* \mid \theta_j]$ for all $\omega_i$---that is, attributed beliefs equal the AI's rational expectation given its objective`

**Alternative** (simpler): Add definition before Proposition:
```latex
Say that $\phi_i$ is \textbf{objective-aligned} if $\phi_i(\theta_j, x_j, \omega_i)$ coincides with the belief that AI $j$ would hold if it could form genuine beliefs given objective $\theta_j$.
```

**Rationale**: Precision is essential for a reduction theorem.

---

## Minor Issues - Batch Recommendations

### Category: Index Convention (m1, m2, m10)

**Problem**: Applications use $H$, $A$ subscripts instead of $i$, $j$ for single-player cases.

**Recommendation**: Add a standardizing note at the start of Applications section:

**File**: sec_applications.tex
**Location**: After L5 (opening paragraph)
**Add**:
```latex
\textit{Notation.} In two-player games with one human and one AI, we use subscripts $H$ and $A$ (rather than indexed $i$ and $j$) for clarity.
```

---

### Category: Representative Agent Notation (m3)

**Problem**: $\omega$ vs $\omega_i$ inconsistent across sections.

**Recommendation**: Already addressed in M3 recommendation (representative-agent statement).

---

### Category: Functional Arguments (m4, m5)

**Problem**: $\pi$ written without $(s)$ argument; belief functions like $h_i^{(2,k)}(c^*)$ use argument notation without definition.

**Recommendation**: Add to framework notation:

**File**: sec_framework.tex
**Location**: After L35 (belief section)
**Add**:
```latex
We write $h_i^{(2,k)}(a)$ for the probability that $i$ assigns to $k$'s first-order belief placing probability 1 on action $a$.
```

---

### Category: Collection Notation (m6)

**Problem**: $h_i^{(2)}$ used for collection $\{h_i^{(2,k)}\}$ without definition.

**Recommendation**: Define explicitly.

**File**: sec_framework.tex
**Location**: After the marginal belief definition (see C2)
**Add**:
```latex
We write $h_i^{(2)} = \{h_i^{(2,k)}\}_{k \in N_H \setminus \{i\}}$ for the collection of $i$'s second-order beliefs about all other humans.
```

---

### Category: Forward References (m7)

**Problem**: $\tilde{h}_i^{(2,j)}$ and $\psi_i$ used before formal definition.

**Recommendation**: Add forward reference in L19.

**File**: sec_framework.tex
**Line**: L19-21
**Add parenthetical**: `(defined formally in Definition 1 and Definitions 3--4 below)`

---

### Category: Equilibrium Definitions (m8, m9, m12)

**Problem**: SPE not defined; $\Sigma$ mixed strategy space not defined; pure vs mixed unclear.

**Recommendations**:
- For m8: Change `reduces to Sequential Psychological Equilibrium as in \citet{battigalli2009dynamic}` to include brief inline definition or add `(see their Definition X)`.
- For m9: Add to proof beginning: `Let $\Sigma = \prod_{i \in N} \Delta(S_i)$ denote the space of mixed strategy profiles.`
- For m12: Add to ABE definition: `The definition extends naturally to mixed strategies $\sigma_i^* \in \Delta(S_i)$ by replacing point expectations with expectations over randomizations.`

---

### Category: Indicator Function Adaptation (m11)

**Problem**: Public goods uses $\mathbf{1}_{c_i < c^*}$ but indignation definition uses $\mathbf{1}_{s_i = D}$.

**Recommendation**: Add note in applications that the indicator adapts to the game context, or generalize Definition 3.

**File**: sec_applications.tex
**Line**: After L44
**Add**: `The indicator $\mathbf{1}_{c_i < c^*}$ generalizes the defection indicator in Definition 3 to the continuous contribution setting.`

---

### Category: Assumption Citations (m13)

**Problem**: Propositions 8-9 don't cite A1-A3.

**Recommendation**: Add assumption citations.

**File**: sec_welfare.tex
**Propositions 8-9 statements**:
**Add**: `Under Assumptions A1--A3,` at the beginning of each proposition statement.

---

### Category: Empty Proof Files (m14)

**Problem**: All 11 proof files contain only placeholder text.

**Recommendation**: Either complete proofs or consolidate into main text.

**Options**:
1. Complete proofs in `/drafts/proofs/` directory
2. Remove proof directory and include all proofs in main document
3. Mark as "Proofs available upon request" for working paper version

**Rationale**: For journal submission, proofs must be available. Decision depends on document length constraints.

---

## Summary Priority Matrix

| Priority | Issue IDs | Est. Effort | Dependency |
|----------|-----------|-------------|------------|
| **Immediate** | C1 (gamma), C2 (marginal) | 30 min | None |
| **Before Submission** | M1 (RAT def), M4 (A1c ref) | 15 min | C1 |
| **Before Submission** | M2-M3 (arguments) | 20 min | None |
| **Before Submission** | M5-M8 (precision) | 30 min | M1 |
| **Polish** | m1-m14 (minor) | 45 min | All major |

**Total estimated revision time**: 2.5-3 hours

---

*Report generated by Phase 3 Agent B. Recommendations are specific and actionable with exact text replacements provided.*
