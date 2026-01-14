# Notation Inventory: Welfare Section + Cross-Reference Analysis

## Part A: Welfare Section Notation (sec_welfare.tex)

### A1. Welfare Functions

| Symbol | Definition | Source Line |
|--------|------------|-------------|
| `W(s)` | Social welfare (material): $W(s) = \sum_{i \in N} \pi_i(s)$ | L11-12 |
| `W^{ext}(s, h, \tilde{h})` | Extended welfare: $W^{ext}(s, h, \tilde{h}) = \sum_{i \in N} \pi_i(s) + \sum_{i \in N_H} \psi_i(s, h_i, \tilde{h}_i)$ | L16-18 |

### A2. Anthropomorphism and Design Parameters

| Symbol | Meaning | Context |
|--------|---------|---------|
| `\omega` | Anthropomorphism level | Propositions 8-9 |
| `\gamma_A` | AI prosociality parameter | Props 8-9 (>0 = prosocial, =0 = materialist) |
| `x_A^*` | Optimal anthropomorphic design level | Proposition 10 |

### A3. Attenuation Factors

| Symbol | Meaning | Context |
|--------|---------|---------|
| `\lambda^{IND}` | Indignation attenuation toward AI | L75, Remark on welfare buffer |
| `\lambda^{GUILT}` | Guilt attenuation toward AI | L75, Remark on welfare buffer |
| `\lambda` | Generic attenuation (when IND/GUILT not distinguished) | L78-81 |

### A4. Over-Anthropomorphism Notation

| Symbol | Meaning | Source Line |
|--------|---------|-------------|
| `\tilde{h}_i^{(2,j)}` | Attributed second-order belief | L43 |
| `\tilde{h}_i^{(2,j),RAT}` | Rational benchmark for attributed beliefs | L44-45 |

### A5. Propositions in Welfare Section

| Label | Title | Key Variables |
|-------|-------|---------------|
| `prop:welfare-anthro` | Welfare Effects of Anthropomorphism | $\omega$, $\gamma_A$, $W(s^*)$, $W^{ext}$ |
| `prop:over-anthro` | Welfare Effects of Over-Anthropomorphism | $\tilde{h}_i^{(2,j)}$, $\tilde{h}_i^{(2,j),RAT}$ |
| `prop:optimal-design` | Optimal AI Design | $x_A^*$ |

### A6. Other Variables

| Symbol | Meaning | Context |
|--------|---------|---------|
| `m` | Public goods multiplier | Proof sketch L34 |
| `s^*` | Equilibrium strategy profile | Throughout |
| `h^*`, `\tilde{h}^*` | Equilibrium belief systems | W^{ext} definition |

---

## Part B: Cross-Reference with Foundations (theory/foundations.tex)

### B1. Notation Alignment Check

#### Consistent Notation (No Issues)

| Symbol | Foundations Definition | Welfare Usage | Status |
|--------|----------------------|---------------|--------|
| `N` | Total player set (L176) | Same | OK |
| `N_H` | Human player set (L174) | Same | OK |
| `N_A` | AI agent set (L175) | Same | OK |
| `\pi_i(s)` | Material payoff (L217) | Same | OK |
| `\psi_i` | Psychological payoff (L218) | Same | OK |
| `\tilde{h}_i^{(2,j)}` | Attributed second-order belief (L254) | Same | OK |
| `\lambda_i^{IND}` | Indignation attenuation (L397) | Same (simplified to `\lambda^{IND}`) | OK |
| `\lambda_i^{GUILT}` | Guilt attenuation (L416) | Same (simplified to `\lambda^{GUILT}`) | OK |
| `\omega_i` | Anthropomorphism tendency (L99, L260) | Used as `\omega` | OK (minor) |
| `\gamma_i` | Guilt sensitivity for humans (L208-209) | N/A | OK |
| `\beta_i` | Indignation sensitivity (L208-209) | N/A | OK |

### B2. Potential Notation Issues

#### Issue 1: `\gamma_A` vs `\gamma_j` Conflict

- **Welfare section**: Uses `\gamma_A` for AI prosociality (L28-29)
- **Foundations**: Uses `\gamma_j` for AI prosociality (L447-448)
- **Conflict**: Different subscript conventions for same concept
- **Recommendation**: Standardize on `\gamma_j` (consistent with individual indexing)

#### Issue 2: Subscript Simplification in Welfare

- **Welfare section**: Often drops subscript `i` (writes `\omega` instead of `\omega_i`, `\lambda` instead of `\lambda_i`)
- **Foundations**: Consistently uses subscripted versions
- **Impact**: Minor stylistic difference; welfare section treats parameters as population-level rather than individual-level
- **Recommendation**: Either (a) clarify that welfare analysis uses representative agent, or (b) restore subscripts for consistency

#### Issue 3: `x_A^*` vs `x_j` for AI Signals

- **Welfare section**: Uses `x_A^*` for optimal anthropomorphic design (L63)
- **Foundations**: Uses `x_j \in X$ for observable signals (L259)
- **Issue**: Same concept, different notation
- **Recommendation**: Use `x_j^*` for optimal design of AI $j$

### B3. Missing Definitions (Used in Welfare but Not in Foundations)

| Symbol | Welfare Usage | Status |
|--------|---------------|--------|
| `W(s)` | Social welfare function | **MISSING in foundations** |
| `W^{ext}` | Extended welfare function | **MISSING in foundations** |
| `\tilde{h}_i^{(2,j),RAT}` | Rational attribution benchmark | **MISSING in foundations** |
| `x_A^*` | Optimal anthropomorphic design | **MISSING in foundations** |
| `m` | Public goods multiplier | Context-specific, acceptable |

### B4. Defined in Foundations but Not Used in Welfare

| Symbol | Foundations Definition | Welfare Relevance |
|--------|----------------------|-------------------|
| `\alpha` | Human population share $n_H/n$ | Not used; could be relevant |
| `\phi_i` | Attribution function | Implicitly used via $\tilde{h}$ |
| `U_i^H$, `U_j^A` | Utility functions | Implicit in optimization |
| `h_i^{(n)}` | Higher-order genuine beliefs | Not needed for welfare |

### B5. Same Symbol, Different Meanings (Potential Conflicts)

| Symbol | Meaning 1 | Meaning 2 | Conflict? |
|--------|-----------|-----------|-----------|
| `\gamma` | Guilt sensitivity (humans) | Prosociality (AI) | **YES** - both $\gamma_i$ and $\gamma_j$ used |

**Critical Issue**: In foundations L447, AI prosociality uses $\gamma_j$, but this collides with the human guilt sensitivity notation $\gamma_i$ from L208-209. The welfare section uses $\gamma_A$ to distinguish, which is actually clearer.

**Recommendation**:
- Keep `\gamma_i` for human guilt sensitivity
- Use different symbol for AI prosociality (e.g., `\rho_j` for prosociality ratio)

---

## Part C: Summary of Issues

### Critical Issues (Must Fix)

1. **Missing welfare definitions in foundations**: Add $W(s)$ and $W^{ext}$ to foundations.tex
2. **Symbol collision**: $\gamma$ used for both human guilt sensitivity and AI prosociality

### Minor Issues (Consider Fixing)

1. **Subscript consistency**: Welfare drops subscripts ($\omega$, $\lambda$) that foundations has ($\omega_i$, $\lambda_i$)
2. **AI design notation**: `x_A^*` vs `x_j` inconsistency
3. **Missing RAT benchmark**: `\tilde{h}_i^{(2,j),RAT}` not defined in foundations

### Recommendations

1. Add a welfare section to foundations.tex defining $W(s)$ and $W^{ext}$
2. Rename AI prosociality from $\gamma_j$ to $\rho_j$ to avoid collision
3. Define $\tilde{h}_i^{(2,j),RAT}$ formally in foundations.tex
4. Clarify in welfare section whether dropping subscripts implies representative agent assumption
