# Phase 2: Player and Type Notation Consistency Check

**Checked by**: Agent 2A
**Date**: 2026-01-12
**Files Analyzed**: sec_framework.tex, sec_equilibrium.tex, sec_applications.tex, sec_welfare.tex

---

## Summary

- **Critical Issues**: 2
- **Major Issues**: 3
- **Minor Issues**: 5

---

## 1. Player Set Notation

### 1.1 $N_H$, $N_A$, $N$ Definitions

| Check | Status | Notes |
|-------|--------|-------|
| $N_H$ for humans | **OK** | Defined in framework L9; used consistently |
| $N_A$ for AI | **OK** | Defined in framework L9; used consistently |
| $N = N_H \cup N_A$ | **OK** | Defined in framework L9 |
| $n_H, n_A, n$ for sizes | **OK** | Defined in framework L9; used in applications |
| $\alpha = n_H/n$ | **OK** | Defined in framework L9; used in applications L54 |

### 1.2 Index Conventions

**Issue 1**: Mixed index conventions for AI

- **File**: sec_framework.tex, sec_applications.tex
- **Location**: Framework L13, L26; Applications L11, L19
- **Issue**: AI agents indexed as $j \in N_A$ in most places, but applications use $\gamma_A$, $x_A$, $U_A$ with subscript "A" instead of $j$
- **Severity**: **Major**
- **Details**:
  - Framework uses: $\theta_j$, $\gamma_j$, $U_j^A$ (individual indexing)
  - Applications uses: $\gamma_A$, $U_A$, $x_A$, $\pi_A$ (class indexing)
  - Trust game (L11): $\gamma_A$ instead of $\gamma_j$
  - Trust game (L17): $\pi_A$ instead of $\pi_j$
- **Suggested Fix**:
  - In applications with single AI, add clarifying note: "When $|N_A| = 1$, we write $\gamma_A$ for the unique AI's parameter"
  - OR use $\gamma_1$ for the AI (less readable but consistent)

**Issue 2**: Human indexing inconsistent between $i$ and $H$

- **File**: sec_applications.tex
- **Location**: L17, L19, L21
- **Issue**: Trust game uses $\pi_H$, $U_H$, $\omega_H$ with subscript "H" instead of individual index $i$
- **Severity**: **Minor** (single-human cases)
- **Suggested Fix**: Same as Issue 1 - clarify notation for single-player cases

---

## 2. Type Space Notation

### 2.1 Human Types ($T_i$, $t_i$)

| Check | Status | Notes |
|-------|--------|-------|
| $T_i$ for human type space | **OK** | Framework L13 |
| $t_i \in T_i$ for individual type | **OK** | Framework L13 |
| $t_i = (\beta_i, \gamma_i, \omega_i, \ldots)$ | **OK** | Framework L13 |

### 2.2 AI Design Parameters ($\Theta_j$, $\theta_j$)

| Check | Status | Notes |
|-------|--------|-------|
| $\Theta_j$ for AI parameter space | **OK** | Framework L13 |
| $\theta_j \in \Theta_j$ | **OK** | Framework L13 |

---

## 3. Psychological Parameter Notation

### 3.1 Indignation Sensitivity ($\beta_i$)

| File | Usage | Status |
|------|-------|--------|
| sec_framework.tex | $\beta_i$ (L13, L93, L95) | **OK** |
| sec_applications.tex | $\beta_i$ (L44, L64, L74) | **OK** |

**No issues** with $\beta_i$ - used consistently.

### 3.2 Guilt Sensitivity ($\gamma_i$)

**Issue 3**: $\gamma$ symbol collision between humans and AI

- **File**: sec_framework.tex, sec_applications.tex, sec_welfare.tex
- **Location**:
  - Framework L13: $\gamma_i$ = human guilt sensitivity
  - Framework L26: $\gamma_j$ = AI prosociality parameter
  - Applications L11, L15, L19: $\gamma_A$ = AI prosociality
  - Welfare L28-29: $\gamma_A$ = AI prosociality
- **Issue**: Same base symbol $\gamma$ used for two conceptually different parameters:
  - Human: guilt sensitivity (psychological trait)
  - AI: prosociality parameter (design choice)
- **Severity**: **Critical**
- **Suggested Fix**:
  - Keep $\gamma_i$ for human guilt sensitivity
  - Change AI prosociality to $\rho_j$ or $\kappa_j$ to avoid confusion
  - Alternative: Use $\gamma_i^{guilt}$ for humans explicitly

### 3.3 Anthropomorphism ($\omega_i$)

**Issue 4**: Inconsistent subscripting of $\omega$

- **File**: sec_applications.tex, sec_welfare.tex
- **Location**:
  - Applications L27: $\omega_H$ (single-human)
  - Applications L52: $\omega$ (no subscript)
  - Welfare L28, L29, L52: $\omega$ (no subscript throughout)
- **Issue**: Sometimes $\omega_i$ (individual), sometimes $\omega$ (population/representative)
- **Severity**: **Minor**
- **Suggested Fix**:
  - Use $\omega_i$ consistently for individual-level
  - In welfare section, add note that $\omega$ denotes common anthropomorphism for simplicity

---

## 4. Attenuation Factor Notation

### 4.1 Indignation Attenuation ($\lambda_i^{IND}$)

| File | Location | Usage | Status |
|------|----------|-------|--------|
| sec_framework.tex | L93, L95 | $\lambda_i^{IND}$ | **OK** |
| sec_applications.tex | L44, L49, L60 | $\lambda_i^{IND}$ | **OK** |
| sec_welfare.tex | L75 | $\lambda^{IND}$ (no subscript) | Minor inconsistency |

### 4.2 Guilt Attenuation ($\lambda_i^{GUILT}$)

| File | Location | Usage | Status |
|------|----------|-------|--------|
| sec_framework.tex | L104, L106 | $\lambda_i^{GUILT}$ | **OK** |
| sec_applications.tex | L19, L24 | $\lambda_H^{GUILT}$ | Minor (single human case) |
| sec_welfare.tex | L75 | $\lambda^{GUILT}$ (no subscript) | Minor inconsistency |

### 4.3 Generic Attenuation ($\lambda_i$)

**Issue 5**: Generic $\lambda_i$ without emotion superscript

- **File**: sec_applications.tex
- **Location**: L69, L74
- **Issue**: Coordination game uses $\lambda_i$ without specifying IND or GUILT
- **Severity**: **Major**
- **Details**: The psychological mechanism in coordination is matching expectations (neither indignation nor guilt as defined), so a generic $\lambda_i$ may be intentional but needs clarification
- **Suggested Fix**: Either:
  - Define a third mechanism (expectation-matching) with its own attenuation
  - Specify which mechanism applies and use appropriate superscript
  - Add footnote explaining the generic use

---

## 5. Second-Order Belief Notation

### 5.1 Genuine Second-Order Beliefs ($h_i^{(2,k)}$)

| File | Usage | Status |
|------|-------|--------|
| sec_framework.tex | L34, L93-94, L104 | $h_i^{(2,k)}$ | **OK** |
| sec_equilibrium.tex | L11, L23, L26, L70 | $h_i^{*(2,k)}$ (starred for equilibrium) | **OK** |
| sec_applications.tex | L44, L47, L67, L74 | $h_i^{(2,k)}(\cdot)$ with argument | See Issue 6 |

**Issue 6**: Functional notation for beliefs

- **File**: sec_applications.tex
- **Location**: L44, L47, L67, L74
- **Issue**: Uses $h_i^{(2,k)}(c^*)$ or $h_i^{(2,k)}(s^{exp})$ with argument, suggesting probability of specific action
- **Severity**: **Minor**
- **Details**: Framework defines $h_i^{(2,k)} \in \Delta(\Delta(S_{-k}))$ (distribution over distributions), but applications use it as probability mass function
- **Suggested Fix**: Clarify in framework that $h_i^{(2,k)}(a)$ denotes the probability human $i$ believes $k$ assigned to action $a$

### 5.2 Attributed Second-Order Beliefs ($\tilde{h}_i^{(2,j)}$)

| File | Usage | Status |
|------|-------|--------|
| sec_framework.tex | L44, L46, L51, L80, L93-95, L104 | $\tilde{h}_i^{(2,j)}$ | **OK** |
| sec_equilibrium.tex | L12, L24, L31, L55, L69 | $\tilde{h}_i^{*(2,j)}$ | **OK** |
| sec_applications.tex | L19, L21, L25, L44, L48, L68, L74 | $\tilde{h}_H^{(2,A)}$ or $\tilde{h}_i^{(2,j)}$ | **OK** |
| sec_welfare.tex | L17, L32, L43-45 | $\tilde{h}_i^{(2,j)}$, $\tilde{h}_i^{(2,j),RAT}$ | **OK** |

**Issue 7**: RAT superscript undefined in framework

- **File**: sec_welfare.tex
- **Location**: L43-45
- **Issue**: Uses $\tilde{h}_i^{(2,j),RAT}$ for rational benchmark, but this is not defined in framework
- **Severity**: **Major**
- **Suggested Fix**: Add definition of rational attribution benchmark in framework section

---

## 6. Equilibrium Notation Issues

### 6.1 A1c Subscript

- **File**: sec_equilibrium.tex
- **Location**: L65
- **Issue**: Uses "A1c (continuity)" suggesting sub-assumption, but framework A1 includes continuity without subscript
- **Severity**: **Minor**
- **Suggested Fix**: Remove subscript or add explicit sub-assumptions A1a, A1b, A1c in framework

---

## 7. Missing Definitions

| Symbol | Used In | Missing From | Severity |
|--------|---------|--------------|----------|
| $\tilde{h}_i^{(2,j),RAT}$ | sec_welfare L43-45 | sec_framework | Major |
| $W(s)$, $W^{ext}$ | sec_welfare L11, L17 | sec_framework | Minor (welfare-specific) |
| $x_A^*$ | sec_welfare L63 | sec_framework | Minor (welfare-specific) |

---

## Issues Summary Table

| # | File | Location | Issue | Severity | Fix |
|---|------|----------|-------|----------|-----|
| 1 | Applications | L11, L17 | AI indexed as $A$ not $j$ | Major | Add clarifying note for single-AI cases |
| 2 | Applications | L17-21 | Human indexed as $H$ not $i$ | Minor | Add clarifying note for single-human cases |
| 3 | Framework, Apps, Welfare | Multiple | $\gamma$ collision (human guilt vs AI prosociality) | **Critical** | Use $\rho_j$ for AI prosociality |
| 4 | Apps, Welfare | Multiple | $\omega$ vs $\omega_i$ subscripting | Minor | Use $\omega_i$ consistently or clarify |
| 5 | Applications | L69, L74 | Generic $\lambda_i$ without emotion superscript | Major | Specify mechanism or define new one |
| 6 | Applications | L44, L67 | $h_i^{(2,k)}(\cdot)$ functional notation | Minor | Clarify in framework |
| 7 | Welfare | L43-45 | $\tilde{h}_i^{(2,j),RAT}$ undefined | Major | Add definition to framework |
| 8 | Equilibrium | L65 | A1c subscript notation | Minor | Align with framework |
| 9 | Welfare | L75, L78 | $\lambda$ without subscript $i$ | Minor | Add subscript or clarify representative agent |
| 10 | Welfare | L28-29 | $\gamma_A$ vs $\gamma_j$ | **Critical** | Standardize (same as Issue 3) |

---

## Recommendations by Priority

### Critical (Must Fix)
1. **Resolve $\gamma$ collision**: Human guilt sensitivity ($\gamma_i$) and AI prosociality ($\gamma_j$/$\gamma_A$) use the same base symbol. Recommend renaming AI prosociality to $\rho_j$.

### Major (Should Fix)
2. **Define rational benchmark**: Add $\tilde{h}_i^{(2,j),RAT}$ definition to framework.
3. **Clarify single-agent notation**: Add note explaining that $A$/$H$ subscripts are used when $|N_A|=1$ or $|N_H|=1$.
4. **Specify coordination mechanism**: Either define expectation-matching as distinct mechanism or use existing IND/GUILT.

### Minor (Consider Fixing)
5. Standardize $\omega_i$ vs $\omega$ (always use subscript or explain)
6. Standardize $\lambda_i$ vs $\lambda$ (always use subscript or explain representative agent)
7. Clarify functional notation for beliefs
8. Align A1c reference with framework

---

*Check complete. 10 issues identified across 4 files.*
