# Phase 2: Utility and Payoff Notation Consistency Check

## Summary

This analysis reviews utility and payoff notation across all four sections: framework, equilibrium, applications, and welfare. The check identified **8 issues** (2 Critical, 3 Major, 3 Minor).

---

## 1. Material Payoff Notation ($\pi_i$)

### Finding: CONSISTENT with minor variation

| File | Notation | Argument Style |
|------|----------|----------------|
| sec_framework.tex L17 | $\pi_i(s)$ | Strategy profile $s$ |
| sec_framework.tex L104 | $\pi_k(s)$, $\pi_j(s)$ | Strategy profile $s$ |
| sec_applications.tex L11 | $\pi_A$, $\pi_H$ | No explicit argument (implicit) |
| sec_applications.tex L39 | $\pi_i$ | No argument in formula |
| sec_welfare.tex L11 | $\pi_i(s)$ | Strategy profile $s$ |

**Issue 1 - Minor**: Applications section sometimes omits the $(s)$ argument on $\pi$.

- **File**: sec_applications.tex
- **Location**: Lines 11, 39
- **Issue**: $\pi_A$, $\pi_H$, $\pi_i$ written without $(s)$ argument
- **Severity**: Minor
- **Suggested Fix**: Add $(s)$ for consistency: $\pi_A(s) = E - x + y$

**Note**: No $u_i$ vs $\pi_i$ confusion found. All sections consistently use $\pi_i$ for material payoffs.

---

## 2. Human Utility Notation ($U_i^H$)

### Framework Definition (L18-19):
```latex
U_i^H(s, h_i, \tilde{h}_i) = \pi_i(s) + \psi_i(s, h_i^{(2)}, \tilde{h}_i^{(2)})
```

### Cross-Section Analysis:

| File | Notation | Arguments |
|------|----------|-----------|
| sec_framework.tex L19 | $U_i^H(s, h_i, \tilde{h}_i)$ | Full 3-argument form |
| sec_equilibrium.tex L15 | $U_i^H(s_i, s_{-i}^*, h_i^*, \tilde{h}_i^*)$ | **4-argument form** (separated $s_i, s_{-i}$) |
| sec_equilibrium.tex L59 | $U_i^H(\sigma_i, \sigma_{-i}, h_i, \tilde{h}_i)$ | 4-argument form with mixed strategies |
| sec_applications.tex L19 | $U_H(y; \tilde{h}_H)$ | **2-argument form** (semicolon!) |

**Issue 2 - Major**: Inconsistent argument structure for $U_i^H$.

- **File**: sec_equilibrium.tex vs sec_framework.tex
- **Location**: sec_equilibrium.tex L15, L59
- **Issue**: Equilibrium uses 4-argument form $U_i^H(s_i, s_{-i}^*, h_i^*, \tilde{h}_i^*)$ while framework uses 3-argument form $U_i^H(s, h_i, \tilde{h}_i)$
- **Severity**: Major
- **Suggested Fix**: Choose one convention. Recommend 3-argument form in framework/welfare, 4-argument when optimizing over $s_i$.

**Issue 3 - Major**: Applications uses abbreviated notation with semicolon.

- **File**: sec_applications.tex
- **Location**: Line 19
- **Issue**: $U_H(y; \tilde{h}_H)$ uses semicolon and drops superscript $H$, also drops material payoff from argument list
- **Severity**: Major
- **Suggested Fix**: Use $U_H^H(s; h_H, \tilde{h}_H)$ or clarify this is a simplified game-specific form

---

## 3. AI Utility Notation ($U_j^A$)

### Framework Definition (L22-23):
```latex
U_j^A(s; \theta_j) = f_j(s; \theta_j)
```

### Cross-Section Analysis:

| File | Notation | Separator |
|------|----------|-----------|
| sec_framework.tex L23 | $U_j^A(s; \theta_j)$ | Semicolon |
| sec_framework.tex L26 | $U_j^A = \pi_j(s)$ | No argument list |
| sec_equilibrium.tex L20 | $U_j^A(s_j, s_{-j}^*; \theta_j)$ | Semicolon (expanded strategy) |
| sec_applications.tex L12-13 | $U_A(x, y; \gamma_A)$ | Semicolon |

**Finding**: CONSISTENT - Semicolon used consistently to separate parameters from strategies.

**Issue 4 - Minor**: Subscript inconsistency for AI.

- **File**: sec_applications.tex
- **Location**: Line 12
- **Issue**: Uses $U_A$ instead of $U_j^A$ and $\gamma_A$ instead of $\gamma_j$
- **Severity**: Minor (acceptable for single-AI games)
- **Suggested Fix**: Note in text that $A$ refers to the single AI agent; or use $U_1^A$ with $j=1$

---

## 4. Psychological Payoff Notation ($\psi_i$)

### Framework Definitions:
- $\psi_i^{IND}(s, h_i^{(2)}, \tilde{h}_i^{(2)})$ - Indignation (L93)
- $\psi_i^{GUILT}(s, h_i^{(2)}, \tilde{h}_i^{(2)})$ - Guilt (L104)

### Cross-Section Analysis:

| File | Symbol | Superscript | Arguments |
|------|--------|-------------|-----------|
| sec_framework.tex L19 | $\psi_i$ | None | $(s, h_i^{(2)}, \tilde{h}_i^{(2)})$ |
| sec_framework.tex L93 | $\psi_i^{IND}$ | IND (caps) | $(s, h_i^{(2)}, \tilde{h}_i^{(2)})$ |
| sec_framework.tex L104 | $\psi_i^{GUILT}$ | GUILT (caps) | $(s, h_i^{(2)}, \tilde{h}_i^{(2)})$ |
| sec_applications.tex L44 | $\psi_i^{IND}$ | IND (caps) | No explicit argument list |
| sec_applications.tex L74 | $\psi_i$ | None | No explicit argument list |
| sec_welfare.tex L17 | $\psi_i$ | None | $(s, h_i, \tilde{h}_i)$ - **different!** |

**Issue 5 - Critical**: Inconsistent argument structure for $\psi_i$ in welfare.

- **File**: sec_welfare.tex
- **Location**: Line 17
- **Issue**: Uses $\psi_i(s, h_i, \tilde{h}_i)$ but framework defines $\psi_i(s, h_i^{(2)}, \tilde{h}_i^{(2)})$ with explicit second-order superscripts
- **Severity**: Critical
- **Suggested Fix**: Change to $\psi_i(s, h_i^{(2)}, \tilde{h}_i^{(2)})$ for consistency, or clarify that $h_i$ abbreviates $h_i^{(2)}$ in welfare context

---

## 5. Attenuation Factor Notation ($\lambda$)

### Framework Definitions:
- $\lambda_i^{IND} \in [0,1]$ - Indignation attenuation (L95)
- $\lambda_i^{GUILT} \in [0,1]$ - Guilt attenuation (L106)

### Cross-Section Analysis:

| File | Symbol | Case | Subscript |
|------|--------|------|-----------|
| sec_framework.tex L93,95 | $\lambda_i^{IND}$ | CAPS | Individual $i$ |
| sec_framework.tex L104,106 | $\lambda_i^{GUILT}$ | CAPS | Individual $i$ |
| sec_applications.tex L19 | $\lambda_H^{GUILT}$ | CAPS | Player $H$ |
| sec_applications.tex L44 | $\lambda_i^{IND}$ | CAPS | Individual $i$ |
| sec_applications.tex L74 | $\lambda_i$ | None | Individual $i$ |
| sec_welfare.tex L75 | $\lambda^{IND}$, $\lambda^{GUILT}$ | CAPS | **No subscript** |
| sec_welfare.tex L78 | $\lambda$ | None | **No subscript** |

**Issue 6 - Major**: Attenuation factor subscript dropped in welfare.

- **File**: sec_welfare.tex
- **Location**: Lines 75, 78
- **Issue**: Uses $\lambda^{IND}$, $\lambda^{GUILT}$, and $\lambda$ without subscript $i$
- **Severity**: Major
- **Suggested Fix**: Either (a) add subscripts $\lambda_i^{IND}$, or (b) explicitly note representative-agent assumption in welfare section

**Note**: Superscript case (IND/GUILT in caps) is consistent across all files.

---

## 6. Decomposition ($U_i^H = \pi_i + \psi_i$)

### Framework Statement (L18-19):
```latex
U_i^H(s, h_i, \tilde{h}_i) = \pi_i(s) + \psi_i(s, h_i^{(2)}, \tilde{h}_i^{(2)})
```

### Cross-Section Check:

| File | Statement | Consistent? |
|------|-----------|-------------|
| sec_framework.tex L17-19 | $U_i^H = \pi_i(s) + \psi_i(s, h_i^{(2)}, \tilde{h}_i^{(2)})$ | Yes (canonical) |
| sec_equilibrium.tex L99 | $U_i^H = \pi_i$ when $\psi_i \equiv 0$ | Yes (special case) |
| sec_welfare.tex L17 | $W^{ext} = \sum \pi_i(s) + \sum \psi_i(s, h_i, \tilde{h}_i)$ | Partial (see Issue 5) |

**Finding**: Decomposition consistent. No $u_i$ vs $\pi_i$ confusion.

---

## 7. $\gamma$ Symbol Collision

**Issue 7 - Critical**: Same symbol used for two different concepts.

- **File**: sec_framework.tex, sec_applications.tex
- **Location**:
  - sec_framework.tex L13: $\gamma_i$ = guilt sensitivity (human type parameter)
  - sec_framework.tex L26: $\gamma_j$ = AI prosociality parameter
  - sec_applications.tex L11, L19: $\gamma_A$ = AI prosociality, $\gamma_H$ = human guilt sensitivity
- **Issue**: $\gamma$ used for both human guilt sensitivity AND AI prosociality. In prosocial AI formula (L26), $\gamma_j$ appears to be prosociality, but in human type (L13), $\gamma_i$ is guilt sensitivity.
- **Severity**: Critical
- **Suggested Fix**: Use different symbol for AI prosociality, e.g., $\rho_j$ for prosociality ratio. Keep $\gamma_i$ for human guilt sensitivity.

---

## 8. $\beta_i$ Usage Across Sections

| File | Context | Meaning |
|------|---------|---------|
| sec_framework.tex L13 | Human type | Indignation sensitivity |
| sec_framework.tex L93 | Indignation definition | Indignation sensitivity |
| sec_applications.tex L44 | Public goods | Indignation intensity (same) |
| sec_applications.tex L74 | Coordination | Expectation-matching intensity |

**Issue 8 - Minor**: $\beta_i$ potentially overloaded in coordination game.

- **File**: sec_applications.tex
- **Location**: Line 74
- **Issue**: In coordination game, $\beta_i$ is used for "expectation-matching intensity" which may differ conceptually from indignation sensitivity
- **Severity**: Minor
- **Suggested Fix**: Clarify that $\beta_i$ measures sensitivity to disappointing expectations generally (encompassing both indignation and expectation-matching)

---

## Summary Table

| Issue | File | Severity | Description |
|-------|------|----------|-------------|
| 1 | sec_applications.tex | Minor | $\pi$ without $(s)$ argument |
| 2 | sec_equilibrium.tex | Major | 4-argument vs 3-argument $U_i^H$ |
| 3 | sec_applications.tex | Major | Abbreviated $U_H(y; \tilde{h}_H)$ notation |
| 4 | sec_applications.tex | Minor | $U_A$ vs $U_j^A$ subscript |
| 5 | sec_welfare.tex | Critical | $\psi_i(s, h_i, \tilde{h}_i)$ missing $(2)$ superscripts |
| 6 | sec_welfare.tex | Major | $\lambda$ without subscript $i$ |
| 7 | All files | Critical | $\gamma$ collision: guilt vs prosociality |
| 8 | sec_applications.tex | Minor | $\beta_i$ potentially overloaded |

---

## Recommendations

### Must Fix (Critical)
1. **Issue 5**: Add $(2)$ superscripts in sec_welfare.tex L17
2. **Issue 7**: Rename AI prosociality from $\gamma_j$ to $\rho_j$ throughout

### Should Fix (Major)
3. **Issue 2**: Document that 4-argument form is used when optimizing over $s_i$
4. **Issue 3**: Use consistent notation in applications or add clarifying note
5. **Issue 6**: Either add subscripts or note representative-agent assumption

### Consider Fixing (Minor)
6. **Issue 1**: Add $(s)$ arguments for clarity
7. **Issue 4**: Acceptable for single-AI examples
8. **Issue 8**: Add clarifying remark about $\beta_i$ generality

---

*Analysis completed: 2026-01-12*
