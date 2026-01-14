# Revision Checklist for ABE Paper

**Generated**: 2026-01-12
**Based on**: Phase 3 aggregated issues and recommendations

## Instructions
- [ ] Check box when revision is complete
- Review in order: Critical → Major → Minor
- After completing all revisions, re-compile LaTeX and verify

---

## Critical Revisions (Do First)

### [C1] Gamma Symbol Collision - Human Guilt vs AI Prosociality

**Problem**: $\gamma$ overloaded for both human guilt sensitivity ($\gamma_i$) and AI prosociality ($\gamma_j$/$\gamma_A$).

**Files to modify**: sec_framework.tex, sec_applications.tex, sec_welfare.tex

**sec_framework.tex changes**:
- [ ] **Line 26**: Change `$U_j^A = \pi_j(s) + \gamma_j \sum_{k \in N} \pi_k(s)$` to `$U_j^A = \pi_j(s) + \rho_j \sum_{k \in N} \pi_k(s)$`
- [ ] **Line 80**: Change `$\gamma_j \in [0,1]$ is AI's prosociality parameter` to `$\rho_j \in [0,1]$ is AI's prosociality parameter`

**sec_applications.tex changes**:
- [ ] **Line 11**: Change `$\gamma_A$` to `$\rho_A$` (in "prosociality parameter $\gamma_A$")
- [ ] **Line 13**: Change `$U_A(x, y; \gamma_A)$` to `$U_A(x, y; \rho_A)$`
- [ ] **Line 15**: Change `A prosocial AI ($\gamma_A > 0$)` to `A prosocial AI ($\rho_A > 0$)`
- [ ] **Line 21**: Change `$\phi_H(\gamma_A, x_A, \omega_H)$` to `$\phi_H(\rho_A, x_A, \omega_H)$`

**sec_welfare.tex changes**:
- [ ] **Line 28**: Change `($\gamma_A > 0$)` to `($\rho_A > 0$)`
- [ ] **Line 29**: Change `($\gamma_A = 0$)` to `($\rho_A = 0$)`

**Verification**: After fix, run `grep -r "\\\\gamma_A\|\\\\gamma_j" drafts/` - should return 0 results

---

### [C2] Missing Definition - Marginal First-Order Belief $h_i^{(1,k)}$

**Problem**: Equilibrium uses $h_i^{*(1,k)} = s_k^*$ (Line 25) but framework only defines $h_i^{(1)} \in \Delta(S_{-i})$ (Line 33).

**File to modify**: sec_framework.tex

- [ ] **After Line 35** (after belief hierarchy equations): Add new text:
```latex
For any $k \neq i$, we write $h_i^{(1,k)} \in \Delta(S_k)$ for the marginal of $h_i^{(1)}$ on player $k$'s strategy space. Similarly, $h_i^{(2,k)} \in \Delta(\Delta(S_{-k}))$ denotes $i$'s second-order belief about $k$'s first-order belief.
```

**Verification**: The new definition should appear before Line 36 (the $h_i^{(n)}$ notation remark)

---

## Major Revisions

### [M1] Missing Definition - Rational Attribution Benchmark $\tilde{h}_i^{(2,j),RAT}$

**Problem**: Welfare section (Lines 43-45) uses $\tilde{h}_i^{(2,j),RAT}$ without formal definition.

**File to modify**: sec_framework.tex

- [ ] **After Line 66** (after Definition 2): Add new definition:
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

**Verification**: `\label{def:rational-benchmark}` should be findable in framework section

---

### [M2] Argument Structure Inconsistency - $U_i^H$ Function

**Problem**: Three different argument structures across files.

**File to modify**: sec_framework.tex

- [ ] **After Line 20** (after equation (1)): Add clarifying note:
```latex
When $i$ optimizes, we write $U_i^H(s_i, s_{-i}, h_i, \tilde{h}_i)$ with own strategy $s_i$ as a separate argument. In applications with single human and AI, we abbreviate to $U_H(\cdot; \tilde{h}_H)$, suppressing fixed arguments.
```

---

### [M3] Attenuation Factor Missing Subscript in Welfare

**Problem**: Welfare uses $\lambda^{IND}$, $\lambda^{GUILT}$, $\lambda$ without individual subscript.

**File to modify**: sec_welfare.tex

- [ ] **Before Line 75** (before first use of $\lambda$ without subscript): Add:
```latex
For the welfare analysis, we focus on a representative human with attenuation factors $\lambda^{IND}$ and $\lambda^{GUILT}$, suppressing the individual subscript.
```

---

### [M4] A1c Subscript Reference Without Definition

**Problem**: Existence proof (Line 65) references "A1c (continuity)" but Assumption A1 has no sub-labels.

**File to modify**: sec_equilibrium.tex

- [ ] **Line 65**: Change `By A1 (compactness) and A1c (continuity)` to `By A1 (compactness and continuity)`

**Alternative** (if preferred): Add explicit sub-labels to Assumption A1 in sec_framework.tex Lines 126-129.

---

### [M5] Generic $\lambda_i$ Without Emotion Superscript in Coordination

**Problem**: Coordination game (Line 74) uses $\lambda_i$ without IND or GUILT superscript.

**File to modify**: sec_applications.tex

- [ ] **Lines 72-74**: Change `$\lambda_i \sum_{j \in N_A}$` to `$\lambda_i^{COORD} \sum_{j \in N_A}$`
- [ ] **After Line 75**: Add explanation:
```latex
where $\lambda_i^{COORD}$ is the coordination-specific attenuation factor (analogous to $\lambda_i^{IND}$).
```

---

### [M6] Psychological Payoff Missing Second-Order Superscript in Welfare

**Problem**: Welfare (Line 17) uses $\psi_i(s, h_i, \tilde{h}_i)$ but framework uses $\psi_i(s, h_i^{(2)}, \tilde{h}_i^{(2)})$.

**File to modify**: sec_welfare.tex

- [ ] **Line 17**: After the equation, add parenthetical:
```latex
(where $h_i$ and $\tilde{h}_i$ abbreviate the second-order belief structures $h_i^{(2)}$ and $\tilde{h}_i^{(2)}$)
```

---

### [M7] $x_A^*$ Design Variable Clarification

**Problem**: Welfare uses $x_A^*$ for "optimal anthropomorphic design" but $x_j$ denotes "observable signals" in Definition 2.

**File to modify**: sec_welfare.tex

- [ ] **Line 63**: Change `The optimal level of anthropomorphic design $x_A^*$ satisfies` to `The optimal anthropomorphic signal $x_A^* \in X$ satisfies`

---

### [M8] Proposition 3 Precision Issue

**Problem**: "consistent with AI's actual objective function" is vague.

**File to modify**: sec_equilibrium.tex

- [ ] **Lines 102-105** (Proposition 3): Change `If the attribution function $\phi_i$ maps to beliefs consistent with AI's actual objective function` to:
```latex
If the attribution function satisfies $\phi_i(\theta_j, x_j, \omega_i) = \mathbb{E}[s_i^* \mid \theta_j]$ for all $\omega_i$---that is, attributed beliefs equal the AI's rational expectation given its objective
```

OR add definition before Proposition:
```latex
Say that $\phi_i$ is \textbf{objective-aligned} if $\phi_i(\theta_j, x_j, \omega_i)$ coincides with the belief that AI $j$ would hold if it could form genuine beliefs given objective $\theta_j$.
```

---

## Minor Revisions

### Batch A: Index Convention (m1, m2)

**File to modify**: sec_applications.tex

- [ ] **After Line 5** (opening paragraph): Add notation note:
```latex
\textit{Notation.} In two-player games with one human and one AI, we use subscripts $H$ and $A$ (rather than indexed $i$ and $j$) for clarity.
```

---

### Batch B: Functional Arguments (m4, m5)

**File to modify**: sec_framework.tex

- [ ] **After the new marginal belief definition (see C2)**: Add:
```latex
We write $h_i^{(2,k)}(a)$ for the probability that $i$ assigns to $k$'s first-order belief placing probability 1 on action $a$.
```

---

### Batch C: Collection Notation (m6)

**File to modify**: sec_framework.tex

- [ ] **After the marginal belief definition (see C2)**: Add:
```latex
We write $h_i^{(2)} = \{h_i^{(2,k)}\}_{k \in N_H \setminus \{i\}}$ for the collection of $i$'s second-order beliefs about all other humans.
```

---

### Batch D: Forward References (m7)

**File to modify**: sec_framework.tex

- [ ] **Lines 19-21** (after utility equation): Add parenthetical:
```latex
(defined formally in Definition 1 and Definitions 3--4 below)
```

---

### Batch E: Equilibrium Definitions (m8, m9, m12)

**File to modify**: sec_equilibrium.tex

- [ ] **m8 - Line 86**: Change `reduces to Sequential Psychological Equilibrium as in \citet{battigalli2009dynamic}` to `reduces to Sequential Psychological Equilibrium (Definition X in \citealt{battigalli2009dynamic})`

- [ ] **m9 - Line 55**: The line already defines $\Sigma$. Verify it appears before first use:
```latex
Let $\Sigma = \prod_{i \in N} \Delta(S_i)$ denote the space of mixed strategy profiles.
```

- [ ] **m12 - After Definition 6**: Add note:
```latex
The definition extends naturally to mixed strategies $\sigma_i^* \in \Delta(S_i)$ by replacing point expectations with expectations over randomizations.
```

---

### Batch F: Indicator Function Adaptation (m11)

**File to modify**: sec_applications.tex

- [ ] **After Line 44**: Add:
```latex
The indicator $\mathbf{1}_{c_i < c^*}$ generalizes the defection indicator in Definition 3 to the continuous contribution setting.
```

---

### Batch G: Assumption Citations (m13)

**File to modify**: sec_welfare.tex

- [ ] **Proposition 8 statement** (around Line 25): Add `Under Assumptions A1--A3,` at beginning
- [ ] **Proposition 9 statement** (around Line 47): Add `Under Assumptions A1--A3,` at beginning

---

### Batch H: Subscript Standardization (m10)

**File to modify**: sec_applications.tex

- [ ] **Lines 19, 24**: Verify $\lambda_H^{GUILT}$ is acceptable given the H/A notation clarification in Batch A. If not, change to $\lambda_i^{GUILT}$.

---

### Batch I: Empty Proof Files (m14)

**Directory**: `/Users/xueheng/SynologyDrive/Research/pgt_human_ai_foundation/drafts/proofs/`

- [ ] **Decision needed**: Either:
  1. Complete all 11 proofs
  2. Remove proof directory and include proofs in main document
  3. Add note: "Proofs available upon request" for working paper

---

## Post-Revision Verification Checklist

### Compilation
- [ ] Run `cd drafts && pdflatex main.tex` - compiles without errors
- [ ] Run `bibtex main` - no undefined reference warnings
- [ ] Run `pdflatex main.tex` twice more for cross-references

### Symbol Consistency
- [ ] Search for `\gamma_A` and `\gamma_j` - should return 0 results (C1 fixed)
- [ ] Search for `h_i^{(1,k)}` - verify definition exists before first use
- [ ] Search for `\tilde{h}_i^{(2,j),RAT}` - verify definition exists in framework
- [ ] Search for `A1c` - should return 0 results (M4 fixed)

### Cross-Reference Integrity
- [ ] All `\ref{def:*}` resolve correctly
- [ ] All `\ref{prop:*}` resolve correctly
- [ ] All `\citet{}` and `\citep{}` resolve correctly

---

## Notation Consistency Final Check

After all revisions, verify:
- [ ] All $\rho_j$ (new AI prosociality symbol) used consistently throughout
- [ ] All belief hierarchies use $h$ notation (not $\beta$)
- [ ] All attributed beliefs have tilde: $\tilde{h}$
- [ ] All equilibrium objects have star: $s^*, h^*, \tilde{h}^*$
- [ ] Subscripts: $i$ for humans, $j$ for AI (general); $H$, $A$ for single-player cases (applications only)
- [ ] Superscripts for emotions: IND, GUILT, COORD clearly labeled
- [ ] Attenuation factors: $\lambda_i^{TYPE}$ with both subscript and superscript

---

## Summary Statistics

| Category | Count | Estimated Time |
|----------|-------|----------------|
| Critical | 2 (C1, C2) | 30 min |
| Major | 8 (M1-M8) | 45 min |
| Minor | 9 batches | 45 min |
| Verification | 15 checks | 20 min |
| **Total** | | **~2.5 hours** |

---

*Checklist generated by Phase 4 Agent A. Each item includes file, line number, and specific text changes.*
