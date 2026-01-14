# Phase 3: Aggregated Issues Report

**Generated**: 2026-01-12
**Source Files**: 5 Phase 2 analysis reports
**Scope**: All manuscript sections (framework, equilibrium, applications, welfare) + proof files

---

## 1. Critical Issues (Must Fix Before Submission)

### C1: Gamma Symbol Collision - Human Guilt vs AI Prosociality

- **Description**: The symbol $\gamma$ is used for two semantically different concepts:
  - $\gamma_i$ = human guilt sensitivity (psychological trait)
  - $\gamma_j$/$\gamma_A$ = AI prosociality parameter (design choice)
- **Source Files**:
  - sec_framework.tex (L13, L26)
  - sec_applications.tex (L11, L15, L19)
  - sec_welfare.tex (L28-29)
- **Impact**: Reader confusion; potential for misinterpretation in proofs and applications
- **Cross-Reference**: Appears in 4 Phase 2 reports (Players, Utility, Logic, Proofs)
- **Recommended Fix**: Rename AI prosociality to $\rho_j$ throughout; keep $\gamma_i$ for human guilt sensitivity

### C2: Missing Definition - Marginal First-Order Belief $h_i^{(1,k)}$

- **Description**: Equilibrium section uses $h_i^{(1,k)}$ (belief about specific player $k$) but framework only defines $h_i^{(1)} \in \Delta(S_{-i})$ (belief about entire profile)
- **Source Files**:
  - sec_framework.tex L33: $h_i^{(1)} \in \Delta(S_{-i})$
  - sec_equilibrium.tex L25-26: $h_i^{*(1,k)} = s_k^*$
- **Impact**: Logical gap in ABE definition; notation not formally grounded
- **Cross-Reference**: Appears in Beliefs report
- **Recommended Fix**: Add to framework: "We write $h_i^{(1,k)}$ for the marginal of $h_i^{(1)}$ on player $k$'s strategy"

---

## 2. Major Issues (Should Fix)

### M1: Missing Definition - Rational Attribution Benchmark $\tilde{h}_i^{(2,j),RAT}$

- **Description**: Welfare section uses $\tilde{h}_i^{(2,j),RAT}$ for rational benchmark without defining it
- **Source Files**: sec_welfare.tex L43-45
- **Impact**: Proposition 9 (over-anthropomorphism) lacks formal foundation
- **Cross-Reference**: Appears in Players, Logic, Proofs reports
- **Recommended Fix**: Add formal definition to framework section

### M2: Argument Structure Inconsistency - $U_i^H$ Function

- **Description**: Human utility function has inconsistent argument counts:
  - Framework: $U_i^H(s, h_i, \tilde{h}_i)$ (3 arguments)
  - Equilibrium: $U_i^H(s_i, s_{-i}^*, h_i^*, \tilde{h}_i^*)$ (4 arguments)
  - Applications: $U_H(y; \tilde{h}_H)$ (2 arguments, semicolon notation)
- **Source Files**: sec_framework.tex L19, sec_equilibrium.tex L15, sec_applications.tex L19
- **Impact**: Notation inconsistency affects readability
- **Cross-Reference**: Appears in Utility report
- **Recommended Fix**: Clarify that 4-argument form is used when optimizing; add note about applications abbreviation

### M3: Attenuation Factor Missing Subscript in Welfare

- **Description**: Welfare section uses $\lambda^{IND}$, $\lambda^{GUILT}$, $\lambda$ without subscript $i$
- **Source Files**: sec_welfare.tex L75, L78
- **Impact**: Inconsistent with individual-level definition $\lambda_i^{IND}$
- **Cross-Reference**: Appears in Players, Utility reports
- **Recommended Fix**: Either add subscripts or explicitly state representative-agent assumption

### M4: A1c Subscript Reference Without Definition

- **Description**: Existence proof uses "A1c (continuity)" but Assumption A1 has no sub-labels
- **Source Files**: sec_equilibrium.tex L65; sec_framework.tex L126-129
- **Impact**: Proof references undefined assumption sub-label
- **Cross-Reference**: Appears in Logic, Proofs reports
- **Recommended Fix**: Change to "A1 (continuity)" or add explicit A1a, A1b, A1c labels

### M5: Generic $\lambda_i$ Without Emotion Superscript in Coordination

- **Description**: Coordination game uses $\lambda_i$ without specifying IND or GUILT
- **Source Files**: sec_applications.tex L69, L74
- **Impact**: Unclear which psychological mechanism is being attenuated
- **Cross-Reference**: Appears in Players report
- **Recommended Fix**: Either define expectation-matching as third mechanism or specify which existing mechanism applies

### M6: Psychological Payoff Missing Second-Order Superscript in Welfare

- **Description**: Welfare uses $\psi_i(s, h_i, \tilde{h}_i)$ but framework defines $\psi_i(s, h_i^{(2)}, \tilde{h}_i^{(2)})$
- **Source Files**: sec_welfare.tex L17; sec_framework.tex L19
- **Impact**: Argument inconsistency with canonical definition
- **Cross-Reference**: Appears in Utility report
- **Recommended Fix**: Add $(2)$ superscripts or clarify that $h_i$ abbreviates $h_i^{(2)}$

### M7: $x_A^*$ Design Variable Conflicts with Signal Notation

- **Description**: $x_A^*$ used for "optimal anthropomorphic design" may conflict with $x_j$ for "observable signals"
- **Source Files**: sec_welfare.tex L63; Definition 2 (framework)
- **Impact**: Notation ambiguity between design choice and signal
- **Cross-Reference**: Appears in Proofs report
- **Recommended Fix**: Clarify that $x_A$ is the signal choice, or use different notation for design (e.g., $\xi_A$)

### M8: Proposition 3 Precision Issue - "Consistent with AI's Objective"

- **Description**: Rational attribution claim is imprecise - "consistent with AI's actual objective function" is vague
- **Source Files**: sec_equilibrium.tex (Prop 3)
- **Impact**: Logical incompleteness in reduction theorem
- **Cross-Reference**: Appears in Logic report
- **Recommended Fix**: Define precisely: $\phi_i(\theta_j, x_j, \omega_i) = \hat{h}^{RAT}(\theta_j)$ where $\hat{h}^{RAT}$ is the rational inference operator

---

## 3. Minor Issues (Nice to Fix)

### m1: AI Indexed as $A$ Instead of $j$ in Applications

- **Description**: Trust game uses $\gamma_A$, $U_A$, $\pi_A$ instead of indexed $\gamma_j$
- **Source Files**: sec_applications.tex L11, L17
- **Recommended Fix**: Add clarifying note for single-AI cases

### m2: Human Indexed as $H$ Instead of $i$ in Applications

- **Description**: Trust game uses $\pi_H$, $U_H$, $\omega_H$ instead of indexed $\pi_i$
- **Source Files**: sec_applications.tex L17-21
- **Recommended Fix**: Add clarifying note for single-human cases

### m3: $\omega$ vs $\omega_i$ Subscripting Inconsistent

- **Description**: Sometimes $\omega_i$ (individual), sometimes $\omega$ (population/representative)
- **Source Files**: sec_applications.tex L27, L52; sec_welfare.tex L28, L29, L52
- **Recommended Fix**: Use $\omega_i$ consistently or explain representative agent

### m4: $\pi$ Without $(s)$ Argument in Applications

- **Description**: Material payoff written without explicit argument: $\pi_A$, $\pi_H$ instead of $\pi_A(s)$
- **Source Files**: sec_applications.tex L11, L39
- **Recommended Fix**: Add $(s)$ for consistency

### m5: Functional Notation for Beliefs Needs Clarification

- **Description**: Uses $h_i^{(2,k)}(c^*)$, $h_i^{(2,k)}(s^{exp})$ with argument notation not formally defined
- **Source Files**: sec_applications.tex L44, L47, L67, L74
- **Recommended Fix**: Clarify in framework that $h_i^{(2,k)}(a)$ denotes probability belief about action $a$

### m6: Collection Notation $h_i^{(2)}$ Not Explicitly Defined

- **Description**: Uses $h_i^{(2)}$ for collection $\{h_i^{(2,k)}\}_{k \in N_H}$ without explicit definition
- **Source Files**: sec_framework.tex L19, L138
- **Recommended Fix**: Add: "We write $h_i^{(2)} = \{h_i^{(2,k)}\}_{k \in N_H \setminus \{i\}}$"

### m7: Terms Used Before Definition

- **Description**: $\tilde{h}_i^{(2,j)}$ (L19) and $\psi_i$ (L19) used in utility equation before formal definitions
- **Source Files**: sec_framework.tex L19 (before Defs 1, 3-4)
- **Recommended Fix**: Add forward references

### m8: SPE Not Formally Defined

- **Description**: Sequential Psychological Equilibrium cited but not defined in manuscript
- **Source Files**: sec_equilibrium.tex (Prop 1)
- **Recommended Fix**: Add brief definition or explicit citation note

### m9: $\Sigma$ Mixed Strategy Space Not Formally Defined

- **Description**: Proof uses $\Sigma = \prod_{i \in N} \Delta(S_i)$ without framework definition
- **Source Files**: sec_equilibrium.tex L55
- **Recommended Fix**: Add to framework notation section

### m10: $\lambda_H^{GUILT}$ Subscript Inconsistency

- **Description**: Uses subscript "H" but framework defines $\lambda_i^{GUILT}$ with index $i$
- **Source Files**: sec_applications.tex L19, L24
- **Recommended Fix**: Standardize to $\lambda_i^{GUILT}$

### m11: Indicator Function Notation Mismatch

- **Description**: Public goods uses $\mathbf{1}_{c_i < c^*}$ but indignation definition uses $\mathbf{1}_{s_i = D}$
- **Source Files**: sec_applications.tex; sec_framework.tex (Def 3)
- **Recommended Fix**: Generalize Definition 3 or explain adaptation

### m12: ABE Definition - Pure vs Mixed Strategies Unclear

- **Description**: ABE definition uses $s_i^*$ (pure) but existence proof uses $\sigma_i$ (mixed)
- **Source Files**: sec_equilibrium.tex (Def 6, Thm 1)
- **Recommended Fix**: Add clarifying note about mixed strategy extension

### m13: Propositions 8-9 Missing Assumption Citations

- **Description**: Welfare propositions don't cite A1-A3 assumptions
- **Source Files**: sec_welfare.tex (Props 8-9)
- **Recommended Fix**: Add "Under A1-A3" to statements

### m14: All 11 Proof Files Are Empty Placeholders

- **Description**: Files in /drafts/proofs/ contain only "[TODO: Proof to be completed]"
- **Source Files**: All 11 proof files
- **Recommended Fix**: Complete proofs or remove separate proof directory

---

## 4. Pattern Analysis

### Most Problematic Notation Symbols

| Symbol | Issue Count | Problem Type |
|--------|-------------|--------------|
| $\gamma$ | 4 (C1 counted multiple times) | Semantic collision |
| $\lambda$ | 3 (M3, M5, m10) | Subscript/superscript inconsistency |
| $h_i^{(1)}$/$h_i^{(2)}$ | 3 (C2, m5, m6) | Missing marginal/collection definitions |
| $U_i^H$ | 2 (M2, M6) | Argument structure inconsistency |
| $x_j$/$x_A$ | 2 (M7, m1) | Signal vs design ambiguity |

### Sections with Most Issues

| Section | Critical | Major | Minor | Total |
|---------|----------|-------|-------|-------|
| sec_framework.tex | 2 | 1 | 3 | 6 |
| sec_equilibrium.tex | 0 | 3 | 3 | 6 |
| sec_applications.tex | 0 | 1 | 7 | 8 |
| sec_welfare.tex | 0 | 3 | 2 | 5 |
| Proof files | 0 | 0 | 1 | 1 |

### Systematic Problems Identified

1. **Subscript Convention Breakdown**: Framework uses $i \in N_H$, $j \in N_A$ but applications often use $H$, $A$ subscripts
2. **Representative Agent Notation**: Welfare section silently drops subscripts assuming representative agent
3. **Missing Forward References**: Notation used before formal definition
4. **Superscript Overload**: $(2)$ for second-order vs $(2,k)$ for specific player vs RAT for rational

---

## 5. Issue Statistics

| Category | Count |
|----------|-------|
| **Total Critical Issues** | 2 |
| **Total Major Issues** | 8 |
| **Total Minor Issues** | 14 |
| **Grand Total** | 24 |

### Files with Most Issues

1. sec_applications.tex: 8 issues
2. sec_framework.tex: 6 issues
3. sec_equilibrium.tex: 6 issues
4. sec_welfare.tex: 5 issues

### Most Frequently Cited Problems

1. $\gamma$ collision (4 Phase 2 reports)
2. A1c subscript (2 Phase 2 reports)
3. $\tilde{h}_i^{(2,j),RAT}$ undefined (3 Phase 2 reports)
4. Index convention H/A vs i/j (2 Phase 2 reports)

---

## 6. De-duplicated Master List

The following issues appeared in multiple Phase 2 reports and have been consolidated:

| Merged Issue | Original Reports | Master ID |
|--------------|------------------|-----------|
| $\gamma$ collision | Players #3, Players #10, Utility #7, Proofs #1 | **C1** |
| $\tilde{h}^{RAT}$ undefined | Players #7, Logic #2, Proofs #3 | **M1** |
| A1c subscript | Logic #1, Proofs minor | **M4** |
| Index H/A vs i/j | Players #1-2, Proofs #2-3 | **m1, m2** |
| $\lambda$ subscript | Players #9, Utility #6 | **M3** |

### Unique Issues by Source Report

| Report | Unique Issues Added |
|--------|---------------------|
| phase2_check_players.md | 3 unique (of 10 total) |
| phase2_check_beliefs.md | 2 unique (of 4 total) |
| phase2_check_utility.md | 3 unique (of 8 total) |
| phase2_check_logic.md | 2 unique (of 8 total) |
| phase2_check_proofs.md | 2 unique (of 10 total) |

---

## 7. Priority Action Summary

### Immediate Action Required (Before Any Review)

1. **C1**: Rename AI prosociality $\gamma_j \to \rho_j$
2. **C2**: Add marginal belief definition $h_i^{(1,k)}$

### Should Complete Before Submission

3. **M1**: Define $\tilde{h}_i^{(2,j),RAT}$
4. **M2-M3**: Standardize utility/attenuation argument structure
5. **M4**: Fix A1c reference
6. **M5-M6**: Clarify psychological mechanism notation
7. **M7-M8**: Resolve design variable ambiguity and precision

### Consider for Polish

8. **m1-m14**: Address all minor notation inconsistencies

---

*Report generated by Phase 3 aggregation. Total unique issues: 24 (2 critical, 8 major, 14 minor)*
