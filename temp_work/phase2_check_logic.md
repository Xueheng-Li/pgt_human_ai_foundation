# Phase 2: Logical Dependencies and Definition Chain Check

## Overview

This report analyzes the logical consistency of definitions, theorems, assumptions, and their dependencies across all manuscript sections.

---

## 1. Definition Chain Analysis

### 1.1 Definition Numbering and Sequence

| # | Label | Name | Section | Self-Contained? |
|---|-------|------|---------|-----------------|
| Def 1 | `def:attributed-beliefs` | Attributed Beliefs | sec_framework | Yes (introduces $\tilde{h}_i^{(2,j)}$, $\phi_i$) |
| Def 2 | `def:attribution-function` | Attribution Function | sec_framework | Yes (defines $\phi_i$ formally) |
| Def 3 | `def:indignation` | Indignation with Attenuation | sec_framework | Refs: $h_i^{(2,k)}$, $\tilde{h}_i^{(2,j)}$ (from Def 1) |
| Def 4 | `def:guilt` | Guilt Aversion with Attenuation | sec_framework | Refs: $h_i^{(2,k)}$, $\tilde{h}_i^{(2,j)}$ (from Def 1) |
| Def 5 | `def:game` | Asymmetric Human-AI Psychological Game | sec_framework | Refs: $\phi$ (from Def 2), $U_i^H$, $U_j^A$ |
| Def 6 | `def:ABE` | Attributed Belief Equilibrium | sec_equilibrium | Refs: $U_i^H$, $U_j^A$, $\phi_i$ (all from framework) |

**Status**: Definitions are numbered sequentially (1-6). Each definition either is self-contained or references only prior definitions. **NO ISSUES FOUND**.

### 1.2 Terms Used Before Definition

| Term | First Use | Definition Location | Issue? |
|------|-----------|---------------------|--------|
| $\tilde{h}_i^{(2,j)}$ | sec_framework L19 | Def 1 (L42-49) | **MINOR**: Used in $U_i^H$ before formal definition |
| $\phi_i$ | sec_framework L46 | Def 2 (L59-66) | OK: First appears inside Def 1 |
| $\psi_i$ | sec_framework L19 | Def 3-4 (L89-107) | **MINOR**: Used in payoff equation before formal definition |

**Issues Found**:
- **Minor Issue 1**: $\tilde{h}_i^{(2,j)}$ appears in the human utility equation (L19) before Definition 1 formally defines it (L42-49). Suggestion: Add a forward reference or move the utility equation after Definition 1.
- **Minor Issue 2**: $\psi_i$ is used in L19 but only formally defined in Definitions 3-4 (L89-107). Suggestion: Add brief forward reference.

---

## 2. Assumption Usage Analysis

### 2.1 Assumption Inventory

| Assumption | Label | Content | Location |
|------------|-------|---------|----------|
| A1 | `ass:regularity` | Strategy spaces finite, type spaces compact/convex, payoffs continuous | sec_framework L126-129 |
| A2 | `ass:attribution` | $\phi_i$ continuous in $(\theta_j, x_j)$ for fixed $\omega_i$ | sec_framework L131-134 |
| A3 | `ass:bounded` | $\|\psi_i\| \leq M < \infty$ | sec_framework L136-139 |

### 2.2 Where Assumptions Are Invoked

| Location | Assumption Cited | Context | Correct? |
|----------|-----------------|---------|----------|
| Theorem 1 statement (sec_eq L49) | "A1--A3" | Existence claim | **YES** |
| Proof Step 1 (sec_eq L55) | "A1" | Compactness of $\Sigma$ | **YES** |
| Proof Step 1 (sec_eq L55) | "A2" | Well-defined $\phi_i$ | **YES** |
| Proof Step 2 (sec_eq L65) | "A1" | Compactness for BR | **YES** |
| Proof Step 2 (sec_eq L65) | "A1c" | Continuity for BR | **ISSUE** |
| Proof Remark (sec_eq L78-80) | "A3" | Bounded psychological payoffs | **YES** |

**Issues Found**:
- **Major Issue 1**: The proof uses "A1c" (L65) for continuity, but Assumption A1 in sec_framework does not use subscript notation. A1 is stated as a single assumption with multiple conditions. The proof should say "A1 (continuity)" or the framework should label sub-assumptions as A1a, A1b, A1c.

### 2.3 Unused Assumptions Check

All three assumptions (A1, A2, A3) are used in the existence proof. **No orphan assumptions**.

---

## 3. Theorem-Proposition Numbering Analysis

### 3.1 Complete List of Results

| Result | Label | Section | Number in Sequence |
|--------|-------|---------|-------------------|
| Theorem 1 | `thm:existence` | sec_equilibrium | 1 |
| Proposition 1 | `prop:nesting` | sec_equilibrium | 1 |
| Proposition 2 | `prop:nash` | sec_equilibrium | 2 |
| Proposition 3 | `prop:rational-attribution` | sec_equilibrium | 3 |
| Proposition 4 | `prop:multiplicity` | sec_equilibrium | 4 |
| Proposition 5 | `prop:trust` | sec_applications | 5 |
| Proposition 6 | `prop:public-goods` | sec_applications | 6 |
| Proposition 7 | `prop:coordination` | sec_applications | 7 |
| Proposition 8 | `prop:welfare-anthro` | sec_welfare | 8 |
| Proposition 9 | `prop:over-anthro` | sec_welfare | 9 |
| Proposition 10 | `prop:optimal-design` | sec_welfare | 10 |

**Status**: 1 Theorem + 10 Propositions. Numbers are sequential with no gaps or duplicates. **NO ISSUES FOUND**.

### 3.2 Proposition Dependencies

| Proposition | Depends On | Assumptions Used | Status |
|-------------|------------|------------------|--------|
| Prop 1 (nesting) | ABE Definition | None | OK |
| Prop 2 (nash) | ABE Definition | None | OK |
| Prop 3 (rational-attr) | ABE Definition | None | OK |
| Prop 4 (multiplicity) | ABE Definition | None | OK |
| Prop 5 (trust) | Defs 1-4, ABE | Implicit A1-A3 | OK |
| Prop 6 (public-goods) | Defs 1-4, ABE | Implicit A1-A3 | OK |
| Prop 7 (coordination) | Defs 1-4, ABE | Implicit A1-A3 | OK |
| Prop 8 (welfare-anthro) | ABE, Welfare defs | None stated | **MINOR**: Should cite A1-A3 |
| Prop 9 (over-anthro) | ABE, $\tilde{h}^{RAT}$ | None stated | **MINOR**: $\tilde{h}^{RAT}$ not formally defined |
| Prop 10 (optimal-design) | Props 8-9 | None stated | OK |

---

## 4. Reference Consistency Analysis

### 4.1 Assumption References

| Reference | Location | Correct? | Issue |
|-----------|----------|----------|-------|
| "Assumptions A1--A3" | Theorem 1 | YES | - |
| "A1" | Proof Step 1 | YES | - |
| "A2" | Proof Step 1 | YES | - |
| "A1c" | Proof Step 2 | **NO** | Sub-label not defined |
| "A3" | Proof Remark | YES | - |

### 4.2 Definition References

All cross-references to definitions in the equilibrium section correctly point to framework definitions. **NO ISSUES FOUND**.

### 4.3 Forward References

| Forward Reference | Location | Target | Issue |
|-------------------|----------|--------|-------|
| SPE reference | Prop 1 (sec_eq L86) | Not defined | **MINOR**: "Sequential Psychological Equilibrium" is cited but not formally defined |
| $\tilde{h}^{(2,j),RAT}$ | Prop 9 (sec_welfare L44) | Not in framework | **MAJOR**: Used but not defined in sec_framework |

---

## 5. Special Case Logic Analysis

### 5.1 Proposition 1: $N_A = \emptyset$ reduces to SPE

**Logic Check**:
- When $N_A = \emptyset$: attributed belief system $\tilde{h}$ is empty (correct)
- All beliefs become genuine beliefs (correct)
- ABE conditions reduce to: human optimality + genuine belief consistency (correct)
- These are "exactly the SPE conditions" (claim)

**Issue**: SPE (Sequential Psychological Equilibrium) is cited from \citet{battigalli2009dynamic} but not formally stated. The reader must trust this equivalence.

**Severity**: Minor - citation is sufficient for journal standards.

### 5.2 Proposition 2: $\psi_i \equiv 0$ reduces to Nash

**Logic Check**:
- When $\psi_i \equiv 0$: $U_i^H = \pi_i$ (correct)
- Beliefs no longer affect payoffs (correct)
- Human optimality becomes: $s_i^* \in \arg\max \pi_i(s_i, s_{-i}^*)$ (correct)
- AI optimality unchanged: $s_j^* \in \arg\max U_j^A$ (correct)
- Combined: Nash equilibrium conditions (correct)

**Status**: Logic is sound. **NO ISSUES**.

### 5.3 Proposition 3: Rational Attribution implies Bayesian Game

**Logic Check**:
- If $\phi_i$ maps to beliefs consistent with AI's actual objective (stated)
- Then attributed beliefs = rational inference about AI type
- This is equivalent to a Bayesian game with type uncertainty

**Issue**: "Consistent with AI's actual objective function" is vague. What does it mean for an attributed belief (about AI expectations) to be "consistent" with an objective function?

**Severity**: Major - the statement needs more precision to be logically complete.

**Suggested Fix**: Define precisely: $\phi_i(\theta_j, x_j, \omega_i) = \hat{h}^{RAT}(\theta_j)$ where $\hat{h}^{RAT}$ is the rational inference operator.

---

## 6. ABE Definition Completeness Analysis

### 6.1 Four Conditions Check

| Condition | Well-Defined? | Notation Complete? |
|-----------|---------------|-------------------|
| Human Optimality | YES | Uses $U_i^H$, $s_i$, $h_i^*$, $\tilde{h}_i^*$ - all defined |
| AI Optimality | YES | Uses $U_j^A$, $s_j$, $\theta_j$ - all defined |
| Genuine Belief Consistency | YES | Uses $h_i^{*(1,k)}$, $h_i^{*(2,k)}$, $s_k^*$ - all defined |
| Attribution Consistency | YES | Uses $\tilde{h}_i^{*(2,j)}$, $\phi_i$, $\theta_j$, $x_j$, $\omega_i$ - all defined |

**Status**: All four ABE conditions are well-defined and reference properly defined notation. **NO ISSUES**.

### 6.2 Missing Elements in ABE Definition

- **Mixed strategies**: ABE definition uses $s_i^*$ (pure strategy) but Theorem 1 proof uses $\sigma_i$ (mixed). The definition should clarify whether equilibrium is in pure or mixed strategies.

**Severity**: Minor - context makes it clear that mixed strategies are allowed.

---

## 7. Summary of Issues

### Critical Issues (Must Fix)

None found.

### Major Issues (Should Fix)

| # | Section | Issue | Suggested Fix |
|---|---------|-------|---------------|
| 1 | sec_equilibrium L65 | Uses "A1c" but A1 has no sub-labels | Change to "A1 (continuity)" or add sub-labels A1a-A1c to framework |
| 2 | sec_welfare L44 | $\tilde{h}_i^{(2,j),RAT}$ not defined in framework | Add definition to sec_framework or sec_welfare |
| 3 | Prop 3 | "Consistent with AI's objective" is imprecise | Define rational attribution formally |

### Minor Issues (Consider Fixing)

| # | Section | Issue | Suggested Fix |
|---|---------|-------|---------------|
| 1 | sec_framework L19 | $\tilde{h}_i^{(2,j)}$ used before Def 1 | Add forward reference |
| 2 | sec_framework L19 | $\psi_i$ used before Defs 3-4 | Add forward reference |
| 3 | Prop 1 | SPE not formally defined | Add brief definition or explicit citation |
| 4 | Props 8-9 | Assumptions not cited | Add "Under A1-A3" to statements |
| 5 | ABE Definition | Pure vs mixed strategies unclear | Add clarifying note |

---

## 8. Logical Consistency Summary

### Definition Chain: **SOUND**
- All 6 definitions are properly sequenced
- Dependencies flow correctly (Def 1 -> Def 2 -> Defs 3-4 -> Def 5 -> Def 6)
- Minor forward reference issues only

### Assumption Structure: **MOSTLY SOUND**
- A1, A2, A3 are clearly stated
- Issue with A1c sub-label in proof

### Theorem-Proposition Sequence: **SOUND**
- 1 Theorem + 10 Propositions correctly numbered
- No gaps or duplicates

### Special Case Reductions: **MOSTLY SOUND**
- Prop 1 (SPE reduction): Logic correct
- Prop 2 (Nash reduction): Logic correct
- Prop 3 (Bayesian game): Needs precision

### ABE Definition: **COMPLETE**
- All 4 conditions well-defined
- All notation properly referenced

---

*Report generated: Phase 2 Logical Dependency Check*
*Files analyzed: 6 source files + 4 Phase 1 notation inventories*
