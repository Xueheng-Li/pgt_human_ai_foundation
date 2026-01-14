# Phase 2: Belief Hierarchy Notation Consistency Check

**Date**: 2026-01-12
**Scope**: All four manuscript sections (framework, equilibrium, applications, welfare)

---

## Executive Summary

The belief hierarchy notation is **largely consistent** across sections. The explicit note about using $h_i^{(n)}$ instead of $\beta_i^{(n)}$ (to avoid confusion with indignation sensitivity $\beta$) is properly implemented. However, several issues require attention, particularly around superscript positioning for equilibrium beliefs and some minor inconsistencies in attributed belief notation.

---

## 1. Basic Hierarchy Notation Check

### Standard Hierarchy Notation

| Notation | Definition | sec_framework | sec_equilibrium | sec_applications | sec_welfare |
|----------|------------|---------------|-----------------|------------------|-------------|
| $h_i^{(0)}$ | type ($= t_i$) | L32: Defined | Not used | Not used | Not used |
| $h_i^{(1)}$ | first-order beliefs | L33: Defined | L25: Used | L70 (implicit) | Not used |
| $h_i^{(2,k)}$ | second-order beliefs | L34: Defined | L26: Used | L44, L47, L74 | Not used |
| $h_i^{(n)}$ | general n-th order | L36: Explicitly noted | Not used | Not used | Not used |

**STATUS**: CONSISTENT - Basic hierarchy properly defined and referenced.

### No Accidental Use of $\beta$ for Beliefs

Searched all sections for $\beta$ usage:
- **sec_framework.tex**: $\beta_i$ = indignation sensitivity (L13, L36, L93, L95) - CORRECT
- **sec_equilibrium.tex**: No $\beta$ usage
- **sec_applications.tex**: $\beta_i$ = indignation/psychological intensity (L44, L64, L74) - CORRECT
- **sec_welfare.tex**: No $\beta$ usage

**STATUS**: CONSISTENT - $\beta$ never used for beliefs (only for indignation sensitivity as intended).

---

## 2. Second-Order Belief Superscripts

### Comma Notation $(2,k)$

| File | Usage Pattern | Consistent? |
|------|---------------|-------------|
| sec_framework.tex | $h_i^{(2,k)}$ (L34, L93, L104) | YES |
| sec_equilibrium.tex | $h_i^{*(2,k)}$ (L26) | YES |
| sec_applications.tex | $h_i^{(2,k)}(c^*)$, $h_i^{(2,k)}(s^{exp})$ (L44, L47, L74) | YES |
| sec_welfare.tex | $h_i$ in $W^{ext}$ (L17) | Uses shorthand |

### Usage of $h_i^{(2)}$ Without Specifying $k$

| File | Line | Context | Issue? |
|------|------|---------|--------|
| sec_framework.tex | L19 | $\psi_i(s, h_i^{(2)}, \tilde{h}_i^{(2)})$ | Collection notation |
| sec_framework.tex | L93-94 | Same collection use | Collection notation |
| sec_framework.tex | L138 | Assumption A3 uses $(h_i^{(2)}, \tilde{h}_i^{(2)})$ | Collection notation |

**FINDING**: The notation $h_i^{(2)}$ (without $k$) is used to denote the **collection** of all second-order beliefs $\{h_i^{(2,k)}\}_{k \in N_H}$. This is an acceptable convention but should be made explicit.

**MINOR ISSUE**: The framework section uses $h_i^{(2)}$ for collections but never explicitly defines this shorthand.

---

## 3. Attributed vs Genuine Beliefs

### Tilde (~) Notation for AI

| Notation | Meaning | Usage Pattern |
|----------|---------|---------------|
| $h_i^{(2,k)}$ | Genuine belief about human $k$ | Always for humans |
| $\tilde{h}_i^{(2,j)}$ | Attributed belief about AI $j$ | Always for AI |

**Verification by File**:

| File | Genuine (humans) | Attributed (AI) | Consistent? |
|------|------------------|-----------------|-------------|
| sec_framework.tex | $h_i^{(2,k)}$ (L34, L93) | $\tilde{h}_i^{(2,j)}$ (L44-46, L93-95) | YES |
| sec_equilibrium.tex | $h_i^{*(2,k)}$ (L26) | $\tilde{h}_i^{*(2,j)}$ (L31) | YES |
| sec_applications.tex | $h_i^{(2,k)}(c^*)$ (L44) | $\tilde{h}_i^{(2,j)}(c^*)$ (L44) | YES |
| sec_welfare.tex | $h$ (L17) | $\tilde{h}$ (L17) | YES (shorthand) |

**STATUS**: CONSISTENT - Tilde notation ONLY used for AI, never for humans.

---

## 4. Equilibrium Belief Notation

### Star (*) Position Issue

This is a **CRITICAL** consistency check. The paper uses equilibrium notation $h^*$, but the position of the star varies:

| File | Line | Notation Used | Pattern |
|------|------|---------------|---------|
| sec_equilibrium.tex | L11 | $h^*$, $\tilde{h}^*$ | System level |
| sec_equilibrium.tex | L25 | $h_i^{*(1,k)} = s_k^*$ | **Star INSIDE superscript** |
| sec_equilibrium.tex | L26 | $h_i^{*(2,k)} = h_k^{*(1,i)}$ | **Star INSIDE superscript** |
| sec_equilibrium.tex | L31 | $\tilde{h}_i^{*(2,j)}$ | **Star INSIDE superscript** |
| sec_equilibrium.tex | L55 | $\tilde{h}_i^{(2,j)}$ (no star) | Non-equilibrium |
| sec_equilibrium.tex | L69-70 | $\tilde{h}_i^{(2,j)}$, $h_i^{(1,k)}$ (no star) | Construction step |

**FINDING**: The equilibrium section uses $h_i^{*(1,k)}$ (star inside superscript) rather than $h_i^{(1,k)*}$ (star outside). This is internally consistent within sec_equilibrium.tex.

**CRITICAL CHECK**: Does the Phase 1 inventory match this?
- Phase 1 inventory (phase1_notation_equilibrium.md) lists: $h_i^{*(1,k)}$, $h_i^{*(2,k)}$, $\tilde{h}_i^{*(2,j)}$
- This matches the source file.

**STATUS**: CONSISTENT - Star position is uniformly INSIDE the superscript for equilibrium beliefs.

---

## 5. Belief Consistency Conditions

### ABE Definition Notation (sec_equilibrium.tex, L23-27)

```latex
h_i^{*(1,k)} &= s_k^* \quad \text{(first-order consistency)}
h_i^{*(2,k)} &= h_k^{*(1,i)} \quad \text{(second-order consistency)}
```

**Analysis**:
- First-order: Human $i$'s belief about $k$'s strategy equals $k$'s actual equilibrium strategy
- Second-order: Human $i$'s second-order belief about $k$ equals $k$'s first-order belief about $i$

**ISSUE FOUND**: The second-order consistency condition uses subscript $(1,i)$ on the RHS, meaning "$k$'s first-order belief about $i$". But the definition at L33 says $h_i^{(1)} \in \Delta(S_{-i})$ - first-order beliefs are about ALL others' play, not about a specific player.

**CRITICAL INCONSISTENCY**:
- **Framework (L33)**: $h_i^{(1)} \in \Delta(S_{-i})$ - beliefs about the entire profile of others
- **Equilibrium (L25-26)**: $h_i^{*(1,k)}$ - beliefs about specific player $k$

This suggests the equilibrium section introduces a REFINED notation $h_i^{(1,k)}$ meaning "player $i$'s belief about what $k$ will do" that is not formally defined in the framework.

**Severity**: MAJOR - requires explicit definition or harmonization.

---

## 6. Additional Findings

### Issue A: First-Order Belief Subscript Inconsistency

| Location | Notation | Interpretation |
|----------|----------|----------------|
| sec_framework.tex L33 | $h_i^{(1)} \in \Delta(S_{-i})$ | Belief about entire opponent profile |
| sec_equilibrium.tex L25 | $h_i^{*(1,k)} = s_k^*$ | Belief about specific player $k$ |
| sec_equilibrium.tex L70 | $h_i^{(1,k)} = \sigma_k$ | Same refined notation |

**RECOMMENDATION**: Add to framework section:
> "For notational convenience, we write $h_i^{(1,k)}$ for the marginal of $h_i^{(1)}$ on player $k$'s strategy."

### Issue B: Argument Notation in Applications

In sec_applications.tex, beliefs take arguments:
- $h_i^{(2,k)}(C)$ - probability human $k$ expected **C**ooperation (L93, framework)
- $h_i^{(2,k)}(c^*)$ - probability human $k$ expected contribution level $c^*$ (L44, applications)
- $h_i^{(2,k)}(s^{exp})$ - probability human $k$ expected technology $s^{exp}$ (L74, applications)

**STATUS**: CONSISTENT - The argument notation $(C)$, $(c^*)$, $(s^{exp})$ represents "belief that player expected this action/level."

### Issue C: Collection vs Individual Notation

The paper sometimes uses:
- $h_i^{(2)}$ for the collection $\{h_i^{(2,k)}\}_{k \neq i}$
- $\tilde{h}_i^{(2)}$ for the collection $\{\tilde{h}_i^{(2,j)}\}_{j \in N_A}$

This is implicit in:
- sec_framework.tex L19: $\psi_i(s, h_i^{(2)}, \tilde{h}_i^{(2)})$
- sec_welfare.tex L17: $\psi_i(s, h_i, \tilde{h}_i)$ (even more abbreviated)

**RECOMMENDATION**: Add explicit definition:
> "We write $h_i^{(2)} = \{h_i^{(2,k)}\}_{k \in N_H \setminus \{i\}}$ for the collection of second-order beliefs."

---

## Summary of Issues

### Critical Issues (Must Fix)

| # | File | Location | Issue | Suggested Fix |
|---|------|----------|-------|---------------|
| 1 | sec_equilibrium.tex | L25-26 | $h_i^{(1,k)}$ notation used but not defined in framework | Add marginal belief definition to sec_framework.tex |

### Major Issues (Should Fix)

| # | File | Location | Issue | Suggested Fix |
|---|------|----------|-------|---------------|
| 2 | sec_framework.tex | L19, L138 | $h_i^{(2)}$ collection notation used but not defined | Add explicit collection notation definition |

### Minor Issues (Consider Fixing)

| # | File | Location | Issue | Suggested Fix |
|---|------|----------|-------|---------------|
| 3 | sec_welfare.tex | L17 | Uses $h_i$ without superscript (shorthand) | Accept as stylistic; welfare uses aggregate notation |
| 4 | All | Various | Argument notation $(C)$, $(c^*)$ used without formal definition | Add clarifying footnote |

---

## Verification: Key Claim from Paper

The paper states (sec_framework.tex L36):
> "We use $h_i^{(n)}$ instead of the $\beta_i^{(n)}$ notation from Battigalli & Dufwenberg (2009) to avoid confusion with the indignation sensitivity parameter $\beta$."

**VERIFIED**: This claim is correctly implemented throughout. No instances of $\beta_i^{(n)}$ for beliefs found in any section.

---

## Recommended Fixes

### Fix 1: Add Marginal Belief Definition (CRITICAL)

Add to sec_framework.tex after L33:
```latex
For notational convenience, we write $h_i^{(1,k)}$ for the marginal of $h_i^{(1)}$
on player $k$'s strategy, i.e., $i$'s belief about what $k$ will play.
```

### Fix 2: Add Collection Notation Definition (MAJOR)

Add to sec_framework.tex after L34:
```latex
We write $h_i^{(2)} = \{h_i^{(2,k)}\}_{k \in N_H \setminus \{i\}}$ for the collection
of second-order beliefs about all other humans, and similarly
$\tilde{h}_i^{(2)} = \{\tilde{h}_i^{(2,j)}\}_{j \in N_A}$ for attributed beliefs about all AI agents.
```

---

*Analysis complete. 2 critical/major issues identified, both resolvable with notation clarifications.*
