# Gap Analysis: Introduction vs. Main Body

## Summary

The introduction contains substantial mathematical notation that should be replaced with verbal descriptions. Several proposition numbers and content summaries need updating to match the revised main body. Key concepts now developed in the framework section (RAE, welfare measures, mind perception theory) are absent or underrepresented in the introduction.

---

## 1. Notation to Remove

### High-Priority Removals

Economics paper introductions rarely include heavy notation. The following should be replaced with verbal descriptions:

| Location | Current Notation | Suggested Verbal Replacement |
|----------|------------------|------------------------------|
| Line 14 | `$\tilde{h}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$` | "The attribution function captures how humans form beliefs about AI expectations based on AI design parameters, observable signals, and individual anthropomorphism tendency." |
| Line 15 | `$\theta_j$` denotes AI design parameters `($\rho_A$)` | "AI design parameters such as its prosociality level" |
| Line 15 | `$x_j$` denotes observable signals | "observable signals including interface and behavioral cues" |
| Line 15 | `$\omega_i$` captures anthropomorphism tendency | "the human's anthropomorphism tendency" |
| Line 15 | `$\lambda^{\text{GUILT}}, \lambda^{\text{IND}} \in [0,1]$` | "attenuation parameters that scale emotional intensity toward AI, ranging from no attenuation (emotions equal to human-directed) to full attenuation (no emotion toward AI)" |
| Line 23 | `$\tilde{h}_i^{(2,j),\text{ZA}} = \phi_i(\theta_j, x_j, 0)$` | "the zero-anthropomorphism benchmark---what humans would attribute absent anthropomorphic bias" |
| Line 27 | `$y^* = \min\{\tilde{h}_H^{(2,A)}, 3x\}$` | "equilibrium returns equal either the attributed expectation or the maximum feasible return, whichever is lower" |
| Line 31 | `$\tilde{h}_i^{(2,j)} > \tilde{h}_i^{(2,j),\text{ZA}}$` | "elevated anthropomorphism---attributed beliefs exceeding the zero-anthropomorphism benchmark" |
| Line 33 | All notation in the welfare/design paragraph: `$x^* = x_{\text{crit}}$`, `$\partial x^*/\partial m < 0$`, `$x^* = 0$`, `$x^* \in (0, \bar{x})$`, comparative statics | Describe verbally: "optimal signaling just crosses the cooperation threshold," "higher efficiency reduces required signaling," "zero signaling is optimal," "intermediate signaling balances cooperation benefits against guilt costs" |

### Moderate-Priority Removals

| Location | Current Notation | Notes |
|----------|------------------|-------|
| Line 5 | Greek letters in passing (guilt, reciprocity, indignation citations) | These are acceptable in context but could be simplified |
| Line 9 | Footnote reference style | Acceptable |

### Notation That May Be Acceptable

- `$N_A = \emptyset$` (Line 23) - Brief, conceptually clear
- Proposition/Theorem numbers - Standard practice

---

## 2. Results Needing Update

### Proposition Number Verification

| Introduction Claim | Main Body Reality | Status |
|-------------------|-------------------|--------|
| Theorem 1: Existence | Theorem 1 in sec_equilibrium.tex | **CORRECT** |
| Proposition 1: Nesting (N_A = empty -> PNE) | Proposition 1 (prop:nesting) | **CORRECT** |
| Proposition 2: Nesting (psi = 0 -> Nash) | Proposition 2 (prop:nash) | **CORRECT** |
| Proposition 3: Rational attribution -> BNE | Proposition 3 (prop:rational-attribution) | **CORRECT** |
| Proposition 4: Multiplicity | Proposition 4 (prop:multiplicity) | **CORRECT** |
| Propositions 5-7: Applications | Not shown in files read | **VERIFY in sec_applications.tex** |
| Proposition 8: Welfare effects | Proposition 8 (prop:welfare-anthro) in sec_welfare.tex | **CORRECT** |
| Proposition 9: Elevated anthropomorphism | Proposition 9 (prop:over-anthro) | **CORRECT** |
| Proposition 10: Optimal design | Proposition 10 (prop:optimal-design) | **CORRECT** |

### Content Accuracy Issues

1. **Introduction Line 21-23**: Describes "zero-anthropomorphism benchmark" but does not mention RAE (Rational Attribution Equilibrium), which is now a formal definition (Definition 4 in sec_equilibrium.tex). The introduction conflates/confuses the two concepts.

2. **Introduction Line 31-32**: Describes Proposition 9 as covering both prosocial and materialist AI effects. The main body now has:
   - Proposition 8: Welfare effects of anthropomorphism (general, with prosocial/materialist parts)
   - Proposition 9: Welfare effects of *elevated* anthropomorphism specifically
   - This distinction is not clear in the introduction.

3. **Introduction Line 33**: Describes Proposition 10 but the main body now also has:
   - Proposition 10: Optimal AI Design (under material welfare W)
   - Proposition 10': Extended Welfare Optimal Design (under extended welfare W^ext)
   - Corollaries 2-3: Agreement and divergence of welfare measures
   - These are missing from the introduction.

4. **Welfare measures terminology**: The introduction uses "extended welfare" casually (Line 33) but the framework section now has formal definitions:
   - Definition 3: Material Welfare
   - Definition 4: Extended Welfare
   - Section 2.6: Normative justification (decision utility vs. experienced utility)
   - This formal structure should be previewed.

---

## 3. Missing Content

### Critical Additions Needed

1. **Rational Attribution Equilibrium (RAE)**:
   - Definition 4 in sec_equilibrium.tex
   - Now a core equilibrium concept with existence conditions
   - Remark 3 clarifies RAE vs. zero-anthropomorphism (they are distinct!)
   - Introduction should preview this refinement

2. **Welfare Measures Framework**:
   - Definitions 3-4 (Material vs. Extended Welfare)
   - Normative foundations: instrumental vs. intrinsic view of psychological payoffs
   - Decision utility vs. experienced utility distinction (citing Kahneman 1997)
   - When measures diverge (Section 2.6.2)
   - The "belief revision puzzle" (Section 2.6.3) - why don't humans correct phantom expectations?

3. **Proposition 10' (Extended Welfare Optimal Design)**:
   - Distinct from Proposition 10
   - Shows when extended-optimal differs from material-optimal
   - Corollaries on agreement/divergence

4. **Cross-Cultural Variation**:
   - Mentioned briefly (Line 7, 29, 44) but main body has dedicated subsection (Section 5.8)
   - The asymmetric implications: high-omega cultures benefit more from prosocial AI but are more vulnerable to materialist AI
   - Culture-dependent optimal design

5. **Dynamic Considerations**:
   - Section 5.9 in main body
   - Learning and long-run welfare
   - Arms race between AI presentation and human adaptation
   - Not mentioned in introduction

6. **Phantom Expectations Problem**:
   - Now has formal Example 4 (in framework section) and Example 5 (in welfare section)
   - The belief revision puzzle explains persistence
   - More substantive treatment warranted in introduction

### Moderate Additions

7. **Assumption Table**:
   - Table 1 in sec_framework.tex provides unified summary
   - Core assumptions (A1-A3) vs. optional extensions (A2', A2'', A2''') vs. context-specific conditions (G, G', I, E, C, T)
   - May be worth mentioning that assumptions are modular

8. **Empirical Implementation Section**:
   - Section 2.5.1: Identification strategy, trust game design, parameter recovery
   - Testable predictions with specific regression specifications
   - Shows theoretical claims are empirically tractable

---

## 4. Literature Gaps

### Psychology Foundations Missing

The main body (sec_framework.tex, Section 2.5.2) now includes a dedicated subsection "Psychological Foundations: Mind Perception Theory" covering:

| Topic | Main Body Coverage | Introduction Coverage | Gap |
|-------|-------------------|----------------------|-----|
| SEEK Framework (Epley 2007) | Full mapping to model parameters | Brief mention (Line 7) | **Major gap** |
| Agency vs. Experience dimensions (Gray 2007) | Explains why attribution and attenuation are separate | Only cited, not explained | **Major gap** |
| Dual-process interpretation (System 1/2) | Explains belief revision puzzle | Not mentioned | **Major gap** |
| Mind perception two dimensions | Agency triggers attribution; Experience triggers attenuation | Not connected | **Moderate gap** |

### Suggested Addition to Related Literature

The Related Literature section should add a paragraph or integrate into existing "Anthropomorphism and mind perception" paragraph:

- Connect the SEEK framework explicitly to model primitives
- Explain the agency-experience distinction and why it creates the attribution-attenuation asymmetry
- Note the dual-process interpretation explains why correction is incomplete (the belief revision puzzle)

---

## 5. Structure Issues

### Organization Problems

1. **Results subsection order**: The current order is:
   - Existence
   - Nesting
   - Multiplicity
   - Applications
   - Attenuation paragraph (Line 29)
   - Welfare and design

   **Problem**: The attenuation paragraph (Line 29) interrupts the flow between applications and welfare. It provides empirical motivation but comes late. Consider:
   - Moving attenuation discussion earlier (after introducing the model, before results)
   - Or integrating it into the applications discussion

2. **Zero-anthropomorphism vs. RAE confusion**: Line 23 introduces zero-anthropomorphism benchmark but immediately pivots to discussing when ABE reduces to BNE. The distinction between:
   - Zero-anthropomorphism (descriptive baseline, omega=0)
   - RAE (equilibrium concept, attributed beliefs = equilibrium strategies)

   is not clear. The main body (Remark 3) explicitly states these are distinct.

3. **Welfare discussion split**: Lines 31-33 cover welfare effects but mix:
   - Elevated anthropomorphism effects (Proposition 9)
   - Optimal design (Proposition 10)
   - Regulatory implications

   Consider separating into clearer paragraphs.

4. **Related literature "Evolutionary game theory" paragraph** (Line 47): References companion paper "li2026pgt" but this feels disconnected. Either integrate evolutionary considerations more substantially or move/shorten.

### Length Considerations

The introduction is substantial (about 3 pages single-spaced). For Econometrica/JET, this is acceptable but could be tightened. Removing notation alone will shorten it.

---

## 6. Action Items Summary

### Must Fix
1. Remove/verbalize all displayed equations and inline notation beyond basic definitions
2. Add RAE as distinct concept from zero-anthropomorphism benchmark
3. Preview welfare measures framework (material vs. extended, normative foundations)
4. Update welfare results to mention Proposition 10' and corollaries
5. Clarify the structure of nesting propositions

### Should Fix
6. Add SEEK framework and mind perception theory to related literature
7. Reorganize attenuation paragraph for better flow
8. Expand cross-cultural implications preview
9. Mention dynamic considerations briefly

### Could Fix
10. Tighten overall length through better verbal descriptions
11. Add mention of assumption table modularity
12. Connect phantom expectations to belief revision puzzle
