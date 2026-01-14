# Phase 2: Proof Notation Consistency Check

**Status**: Analysis complete with **critical findings**

---

## Executive Summary

The 11 proof files in `/drafts/proofs/` are **all empty placeholders** containing only `\textbf{[TODO: Proof to be completed]}`. The actual proofs currently exist as inline content in the main section files (sec_equilibrium.tex, sec_welfare.tex). This check analyzes those inline proofs for notation consistency.

---

## 1. Existence Proof (sec_equilibrium.tex, lines 52-76)

### Notation Consistency Checks

| Element | Used in Proof | Main Text Definition | Status |
|---------|---------------|---------------------|--------|
| $\Sigma = \prod_{i \in N} \Delta(S_i)$ | Line 55 | Not explicitly defined in framework | **Minor** |
| $BR_i^H(h_i, \tilde{h}_i)$ | Lines 57-60 | Consistent with phase1_notation_equilibrium.md | OK |
| $BR_j^A(\sigma_{-j})$ | Lines 61-64 | Consistent with equilibrium notation | OK |
| $\Phi: \Sigma \to \Sigma$ | Line 67 | Consistent with equilibrium notation | OK |
| $\sigma_i$ vs $s_i$ | Mixed usage | Framework uses $s$ for pure, $\sigma$ for mixed | **Minor** |
| A1, A2, A3 | Line 49, 55, 65, 78-80 | Defined in sec_framework.tex lines 126-139 | OK |

### Issues Found

1. **Proof File**: sec_equilibrium.tex (inline proof)
   - **Issue**: Uses "A1c (continuity)" subscript notation (line 65) but A1 in framework (line 126-129) doesn't use sub-assumption labeling
   - **Main Text Reference**: sec_framework.tex, Assumption A1
   - **Severity**: Minor
   - **Suggested Fix**: Either remove the "c" subscript or add explicit sub-assumptions A1a, A1b, A1c to the framework

2. **Proof File**: sec_equilibrium.tex
   - **Issue**: $\Sigma$ used without formal definition in framework section
   - **Main Text Reference**: Not defined
   - **Severity**: Minor
   - **Suggested Fix**: Add $\Sigma = \prod_{i \in N} \Delta(S_i)$ to framework notation

---

## 2. Reduction Proofs (sec_equilibrium.tex, lines 84-100)

### Prop:nesting (Reduction to SPE when $N_A = \emptyset$)

| Element | Used in Proof | Main Text Definition | Status |
|---------|---------------|---------------------|--------|
| $N_A = \emptyset$ | Line 86, 90 | Correctly uses set notation | OK |
| $\tilde{h}$ empty | Line 90 | Logical consequence of $N_A = \emptyset$ | OK |
| SPE reference | Line 86 | citet{battigalli2009dynamic} | OK |

**No issues found.**

### Prop:nash (Reduction to Nash when $\psi_i \equiv 0$)

| Element | Used in Proof | Main Text Definition | Status |
|---------|---------------|---------------------|--------|
| $\psi_i \equiv 0$ | Line 95, 99 | Consistent with framework notation | OK |
| $U_i^H = \pi_i$ | Line 99 | Follows from Definition 1 when $\psi = 0$ | OK |

**No issues found.**

---

## 3. Application Proofs (sec_applications.tex)

The application propositions (Prop. 3.4-3.6) do **not have formal proofs**. They are stated without proof environments. This is acceptable for a journal article where results are "obvious" from the framework, but proofs should be added to the proof files if appendix proofs are planned.

### Notation Consistency in Propositions

| Proposition | Notation Used | Framework Consistency | Status |
|-------------|---------------|----------------------|--------|
| Prop:trust (lines 23-31) | $\tilde{h}_H^{(2,A)}$, $\omega_H$, $y^*$ | Uses subscript "H" for human, "A" for AI | **Minor** |
| Prop:public-goods (lines 48-56) | $\omega$, $c_A$, $\alpha$ | Consistent | OK |
| Prop:coordination (lines 77-85) | $\tilde{h}_i^{(2,j)}$, $x_A$, $\omega$ | Consistent | OK |

### Issues Found

1. **Proof File**: sec_applications.tex
   - **Issue**: Trust game uses $\gamma_A$ for AI prosociality but $\gamma_H$ for human guilt sensitivity - same Greek letter for different concepts
   - **Main Text Reference**: Framework uses $\gamma_i$ for guilt sensitivity (line 13)
   - **Severity**: Major
   - **Suggested Fix**: Use distinct notation: e.g., $\rho_A$ for AI prosociality, $\gamma_H$ for guilt

2. **Proof File**: sec_applications.tex
   - **Issue**: Index convention violation - uses subscript "H" and "A" for player types (e.g., $\tilde{h}_H^{(2,A)}$) but framework uses $i \in N_H$ and $j \in N_A$
   - **Main Text Reference**: Framework consistently uses $i$ for humans, $j$ for AI
   - **Severity**: Minor
   - **Suggested Fix**: Standardize to $\tilde{h}_i^{(2,j)}$ throughout

3. **Proof File**: sec_applications.tex
   - **Issue**: $\lambda_H^{GUILT}$ uses subscript "H" but framework defines $\lambda_i^{GUILT}$ with index $i$
   - **Main Text Reference**: Definition 4, sec_framework.tex line 100-107
   - **Severity**: Minor
   - **Suggested Fix**: Use $\lambda_i^{GUILT}$ consistently

4. **Proof File**: sec_applications.tex (Public Goods)
   - **Issue**: Uses $\mathbf{1}_{c_i < c^*}$ but indignation definition uses $\mathbf{1}_{s_i = D}$
   - **Main Text Reference**: Definition 3, sec_framework.tex
   - **Severity**: Minor
   - **Suggested Fix**: Either generalize Definition 3 to allow arbitrary defection indicators or explain the adaptation in context

---

## 4. Welfare Proofs (sec_welfare.tex)

### Prop:welfare-anthro (lines 25-37)

Proof is marked as "Proof Sketch" - acceptable for main text.

| Element | Used in Proof | Main Text Definition | Status |
|---------|---------------|---------------------|--------|
| $\gamma_A$ | Line 28 | AI prosociality - same issue as applications | **Major** |
| $\omega$ | Lines 28-29, 34 | Consistent with $\omega_i$ | OK |
| $W(s^*)$ | Line 28 | Defined line 10-12 | OK |
| $W^{ext}$ | Line 29 | Defined lines 15-18 | OK |

### Prop:over-anthro (lines 47-53)

No formal proof provided - stated without proof environment.

| Element | Used in Proof | Main Text Definition | Status |
|---------|---------------|---------------------|--------|
| $\tilde{h}_i^{(2,j),RAT}$ | Line 43-45 | New notation introduced in welfare section | **Minor** |
| "Over-anthropomorphism" | Line 41 | New concept, defined in place | OK |

### Prop:optimal-design (lines 61-69)

No formal proof provided - stated without proof environment.

| Element | Used in Proof | Main Text Definition | Status |
|---------|---------------|---------------------|--------|
| $x_A^*$ | Line 63 | Uses $x_A$ for anthropomorphic design - potentially conflicts with $x_j$ (signals) | **Major** |

### Issues Found

1. **Proof File**: sec_welfare.tex
   - **Issue**: $\gamma_A$ reused for AI prosociality (same as applications issue)
   - **Main Text Reference**: Framework uses $\gamma_i$ for guilt sensitivity only
   - **Severity**: Major
   - **Suggested Fix**: Introduce distinct notation for AI prosociality

2. **Proof File**: sec_welfare.tex
   - **Issue**: $x_A^*$ for "optimal anthropomorphic design" potentially conflicts with $x_j$ used for "observable signals" in attribution function
   - **Main Text Reference**: Definition 2, line 48
   - **Severity**: Major
   - **Suggested Fix**: Use different notation for design choice variable, e.g., $\xi_A$ or clarify that $x_A$ is the specific signal choice

3. **Proof File**: sec_welfare.tex
   - **Issue**: $\tilde{h}_i^{(2,j),RAT}$ introduces new superscript notation not established in framework
   - **Main Text Reference**: None
   - **Severity**: Minor
   - **Suggested Fix**: Add definition to framework or equilibrium section before use

---

## 5. Empty Proof Files Status

All 11 proof files contain only `\textbf{[TODO: Proof to be completed]}`:

| File | Expected Content | Status |
|------|------------------|--------|
| 01_thm_existence.tex | Full existence proof | Empty |
| 02_prop_reduction_pgt.tex | SPE reduction proof | Empty |
| 03_prop_reduction_nash.tex | Nash reduction proof | Empty |
| 04_prop_rational_attribution.tex | Rational attribution equivalence | Empty |
| 05_prop_multiplicity.tex | Attribution multiplicity proof | Empty |
| 06_prop_trust_game.tex | Trust game equilibrium characterization | Empty |
| 07_prop_public_goods.tex | Public goods equilibrium | Empty |
| 08_prop_coordination.tex | Coordination equilibrium | Empty |
| 09_prop_welfare_anthropomorphism.tex | Welfare-anthropomorphism relationship | Empty |
| 10_prop_welfare_over_anthropomorphism.tex | Over-anthropomorphism effects | Empty |
| 11_prop_optimal_design.tex | Optimal design characterization | Empty |

---

## Summary of Issues

### Critical Issues (0)
None

### Major Issues (3)
1. **$\gamma$ notation conflict**: $\gamma_A$ used for AI prosociality conflicts with $\gamma_i$ for guilt sensitivity
2. **$x_A$ notation conflict**: $x_A^*$ for design variable conflicts with $x_j$ for signals
3. **A1c subscript**: Proof uses "A1c" but framework doesn't define sub-assumptions

### Minor Issues (7)
1. $\Sigma$ used in proof without formal definition
2. Index "H"/"A" used instead of standard $i$/$j$ convention
3. $\lambda_H^{GUILT}$ subscript inconsistency
4. $\mathbf{1}_{c_i < c^*}$ vs $\mathbf{1}_{s_i = D}$ indicator function mismatch
5. $\tilde{h}_i^{(2,j),RAT}$ new notation introduced without prior definition
6. All 11 proof files are empty placeholders
7. No formal proofs for application propositions

---

## Recommended Actions

1. **Immediate**: Resolve $\gamma$ notation conflict by using $\rho_j$ for AI prosociality
2. **Immediate**: Clarify relationship between $x_A$ (design) and $x_j$ (signals)
3. **Before submission**: Complete all proof files or remove the separate proof directory
4. **Before submission**: Standardize index conventions ($i$ for humans, $j$ for AI) throughout
