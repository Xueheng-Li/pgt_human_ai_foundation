# Phase 1: Proof Analysis for Supplementary Appendix

**Date**: 2026-01-14
**Task**: Identify technical material to relocate from main appendix to supplementary appendix
**Reviewer Guidance**: "Topology details in Theorem 1 could be relegated to technical appendix" and "proofs could be shortened"

---

## Executive Summary

| Proof File | Current Words | Suggested Main | Suggested Supp. | Savings |
|------------|---------------|----------------|-----------------|---------|
| 01_thm_existence.tex | ~1,975 | ~900 | ~1,075 | 54% |
| 02_prop_reduction_pgt.tex | ~675 | ~400 | ~275 | 41% |
| 03_prop_reduction_nash.tex | ~600 | ~350 | ~250 | 42% |
| 04_prop_rational_attribution.tex | ~750 | ~500 | ~250 | 33% |
| 05_prop_multiplicity.tex | ~375 | ~300 | ~75 | 20% |
| 06_prop_trust_game.tex | ~750 | ~500 | ~250 | 33% |
| 07_prop_public_goods.tex | ~1,250 | ~600 | ~650 | 52% |
| 08_prop_coordination.tex | ~1,000 | ~550 | ~450 | 45% |
| 09_prop_welfare_anthro.tex | ~1,050 | ~550 | ~500 | 48% |
| 10_prop_welfare_over_anthro.tex | ~2,810 | ~1,200 | ~1,610 | 57% |
| 11_prop_optimal_design.tex | ~4,377 | ~1,800 | ~2,577 | 59% |
| **TOTAL** | **~15,612** | **~7,650** | **~7,962** | **51%** |

**Priority Ranking for Cuts**:
1. **11_prop_optimal_design.tex** (HIGHEST PRIORITY) - 4,377 words, extensive routine calculations
2. **10_prop_welfare_over_anthro.tex** (HIGH PRIORITY) - 2,810 words, verbose numerical examples
3. **01_thm_existence.tex** (HIGH PRIORITY - REVIEWER CITED) - 1,975 words, topology details specifically mentioned
4. 07_prop_public_goods.tex - extensive remarks can move
5. 09_prop_welfare_anthro.tex - similar structure to 10
6. 08_prop_coordination.tex - numerical example verbose

---

## Detailed Analysis by Proof

### 1. 01_thm_existence.tex (Theorem 1 - Existence) - KEY TARGET

**Current Word Count**: ~1,975 words

**REVIEWER SPECIFICALLY CITED**: "topology details in Theorem 1 could be relegated to technical appendix"

#### Core Argument (MUST STAY - ~900 words):
- **Lines 56-57**: Main theorem statement and proof sketch (key insight about beliefs as functions of strategies)
- **Lines 60-66**: Step 1 strategy space construction (essential for understanding the argument)
- **Lines 93-113**: Step 3 best-response correspondence (core verification of Kakutani conditions)
- **Lines 116-121**: Step 4 fixed-point application (the actual existence argument)
- **Lines 124-145**: Step 5 equilibrium verification (ABE conditions verified)

#### Technical Details to MOVE TO SUPPLEMENT (~1,075 words):
1. **Lemma A.1 (Boundedness) - Lines 10-47** (~350 words)
   - Full proof of boundedness lemma
   - Weierstrass theorem applications
   - Type: Routine measure-theoretic argument
   - Keep in main: Just state the lemma and note "proof in supplement"

2. **Topology Details in Step 1 - Lines 61-66** (~100 words)
   - "We equip each $\Delta(S_i)$ with the Euclidean (relative) topology..."
   - "By Tychonoff's theorem..."
   - Replace with: "Each $\Delta(S_i)$ is compact and convex; so is $\Sigma$."

3. **Belief Computation Details - Lines 68-91** (~250 words)
   - Three attribution approaches (i), (ii), (iii)
   - Attribution validity discussion
   - Keep in main: Just "Under exogenous attribution, $\tilde{h}_i^{(2,j)}$ is constant in $\sigma$."

4. **All Remarks - Lines 151-184** (~375 words)
   - Remark on Behavioral Attribution (lines 151-162)
   - Remark on Role of Assumptions (lines 164-174)
   - Remark on Comparison with Standard PGT (lines 176-179)
   - **Remark on Topology (lines 181-184)** - ESPECIALLY THIS ONE per reviewer

#### Suggested Main Appendix Version:
Keep streamlined proof (~900 words) with:
- Strategy space is compact/convex (one sentence)
- Beliefs computed as functions of $\sigma$ (brief)
- Best-response correspondence satisfies Kakutani (keep verification)
- Fixed-point gives ABE (keep)
- Note: "Technical details including boundedness lemma, topology considerations, and extensions in Online Appendix OA.1"

---

### 2. 02_prop_reduction_pgt.tex (Reduction to PGT)

**Current Word Count**: ~675 words

#### Core Argument (MUST STAY - ~400 words):
- PNE Definition (lines 7-20)
- Steps 1-2: Vacuous conditions and empty attributed beliefs (lines 26-41)
- Step 7: Conclusion summary (lines 103-116)

#### To MOVE TO SUPPLEMENT (~275 words):
- Steps 3-6: Detailed derivations (lines 43-100)
  - Simplification of psychological payoffs
  - Reduction of human utility
  - These follow mechanically from definitions
- Remark on Converse Direction (lines 118-120)

---

### 3. 03_prop_reduction_nash.tex (Reduction to Nash)

**Current Word Count**: ~600 words

#### Core Argument (MUST STAY - ~350 words):
- Part 1 conclusion: ABE implies Nash (key steps only)
- Part 2 conclusion: Nash implies ABE (construction)
- Part 3: Uniqueness statement

#### To MOVE TO SUPPLEMENT (~250 words):
- Step-by-step algebra in Part 1 (lines 14-47)
- Verification details in Part 2 (lines 69-91)
- Both remarks (lines 98-104)

---

### 4. 04_prop_rational_attribution.tex (Rational Attribution = BNE)

**Current Word Count**: ~750 words

#### Core Argument (MUST STAY - ~500 words):
- Bayesian game construction $\Gamma^B$ (essential)
- Part (a) main argument
- Part (b) main argument

#### To MOVE TO SUPPLEMENT (~250 words):
- Remark on equilibrium-dependence (lines 35-37)
- Detailed step-by-step belief characterization (lines 47-62)
- Can condense Part (b) verification

---

### 5. 05_prop_multiplicity.tex (Attribution-Dependent Multiplicity)

**Current Word Count**: ~375 words

**Already concise** - minimal cuts needed

#### To MOVE TO SUPPLEMENT (~75 words):
- Sufficient Conditions block (lines 9-14) - can be stated more briefly in main

---

### 6. 06_prop_trust_game.tex (Trust Game ABE)

**Current Word Count**: ~750 words

#### Core Argument (MUST STAY - ~500 words):
- Part (i): Anthropomorphism increases attributed expectations (key)
- Part (ii): Optimal return derivation (key result $y^* = \min\{\tilde{h}, 3x\}$)
- Part (iii): Example setup and conclusion

#### To MOVE TO SUPPLEMENT (~250 words):
- All four remarks (lines 111-127):
  - Knife-edge case $G=1$
  - Low guilt case $G<1$
  - Connection to multiplicity
  - Empirical support
- Detailed numerical calculations in example table

---

### 7. 07_prop_public_goods.tex (Public Goods ABE)

**Current Word Count**: ~1,250 words

#### Core Argument (MUST STAY - ~600 words):
- Setup and utility function
- Part (i) Steps 1-7: Cooperation threshold derivation
- Part (ii) defection equilibrium (brief)
- Part (iii) population share effects (key insight)

#### To MOVE TO SUPPLEMENT (~650 words):
- **All seven remarks** (lines 164-203) - Very verbose
  - Connection to standard PGT
  - Role of attenuation
  - Boundary cases
  - Role of A2'
  - Empirical implications
  - Threshold interpretation
- Detailed derivations in Part (iii) (lines 123-161)

---

### 8. 08_prop_coordination.tex (Coordination ABE)

**Current Word Count**: ~1,000 words

#### Core Argument (MUST STAY - ~550 words):
- Game setup
- Part (i): AI signaling makes attributed beliefs favor A
- Part (ii): Psychological pull formula
- Part (iii): Uniqueness of $(A,A)$ equilibrium

#### To MOVE TO SUPPLEMENT (~450 words):
- Numerical example remark (lines 146-158)
- Knife-edge case remark (lines 161-163)
- Contrast with Schelling remark (lines 165-167)
- Connection to multiplicity remark (lines 169-171)
- Detailed AI utility calculations (lines 51-61)

---

### 9. 09_prop_welfare_anthropomorphism.tex (Welfare Effects of Anthropomorphism)

**Current Word Count**: ~1,050 words

#### Core Argument (MUST STAY - ~550 words):
- Part 1: Prosocial AI + higher $\omega$ increases material welfare
- Part 2: Materialist AI + higher $\omega$ may reduce extended welfare
- Key mechanism: phantom expectations

#### To MOVE TO SUPPLEMENT (~500 words):
- All remarks (lines 144-172):
  - Weak vs strict inequality
  - Why "may reduce"
  - Asymmetry between parts
  - Connection to application propositions
  - Policy implications
- Detailed numerical example in Part 2 (lines 108-131)

---

### 10. 10_prop_welfare_over_anthro.tex (Elevated Anthropomorphism Welfare) - KEY TARGET

**Current Word Count**: ~2,810 words

**Second largest proof - significant cuts possible**

#### Core Argument (MUST STAY - ~1,200 words):
- Zero-anthropomorphism benchmark definition (essential)
- Elevated anthropomorphism definition
- Part 1: Direct corollary of Prop 8 (can be brief)
- Part 2: Phantom expectations mechanism (novel contribution - keep core)

#### To MOVE TO SUPPLEMENT (~1,610 words):
1. **Equivalence under (A2') and (A2'')** - Lines 52-62 (~150 words)
   - Technical verification

2. **Part 1 detailed steps** - Lines 72-135 (~450 words)
   - "This part is a direct corollary of Proposition 8" - just reference it
   - Keep only the threshold formula and regime switch insight

3. **Numerical example in Part 2** - Lines 234-263 (~300 words)
   - Full three-column comparison table
   - Detailed calculations
   - Keep: Just state "At $\omega_H=0.75$, extended welfare falls to 7.5 vs 30 benchmark"

4. **All eight remarks** - Lines 283-330 (~710 words)
   - Contribution relative to Prop 8
   - Terminology
   - Weak vs strict
   - Why "may reduce"
   - Asymmetric welfare
   - Policy implications
   - Cultural variation

---

### 11. 11_prop_optimal_design.tex (Optimal AI Design) - HIGHEST PRIORITY TARGET

**Current Word Count**: ~4,377 words

**Largest proof by far - most cuts possible**

#### Core Argument (MUST STAY - ~1,800 words):
- Preamble: Key assumptions stated briefly
- Part (i): Prosocial AI - minimal threshold-crossing signal
- Part (ii): Materialist AI - $x^* = 0$
- Part (iii): Mixed AI - interior solution with comparative statics

#### To MOVE TO SUPPLEMENT (~2,577 words):

1. **Preamble Assumptions Block** - Lines 29-44 (~250 words)
   - Can reference "Under Assumptions A1-A3, A2', A2''', E, T, I, G'"
   - Move detailed statements to supplement

2. **Part (i) Detailed Threshold Analysis** - Lines 118-136 (~200 words)
   - Proof of claim that $\bar{\omega}(x) \in (0,1)$
   - Keep just the statement

3. **Part (ii) Complete Case Analysis** - Lines 239-288 (~350 words)
   - Cases A, B, C exhaustively verified
   - Main text: Just state $W^{ext}(x) \leq W^{ext}(0)$

4. **Part (iii) SOC Verification** - Lines 366-386 (~250 words)
   - Second-order condition details
   - Standard envelope argument

5. **Part (iii) Full IFT Derivations** - Lines 389-462 (~500 words)
   - Implicit function theorem applications
   - Keep just the results: $\partial x^*/\partial m > 0$, $\partial x^*/\partial G < 0$, $\partial x^*/\partial \omega < 0$

6. **All eleven remarks** - Lines 480-570 (~1,027 words)
   - Unified interpretation
   - Welfare criterion consistency
   - Reconciliation of $m$ comparative statics
   - Nesting of cases
   - Role of each assumption
   - Decision-maker and designer incentives
   - Boundary cases
   - Policy implications
   - Connection to Props 8 and 9

---

## Implementation Recommendations

### Priority Order for Revision:

1. **Theorem 1 (01_thm_existence.tex)** - Reviewer explicitly cited topology details
2. **Prop 11 (optimal design)** - Largest file, most routine calculations
3. **Prop 10 (elevated anthropomorphism)** - Second largest, verbose examples
4. **Prop 7 (public goods)** - Seven remarks excessive
5. **Prop 9 (welfare anthropomorphism)** - Similar structure to 10, can parallel cut

### Structural Suggestion:

**Main Appendix** (~7,650 words):
- Concise proofs with key arguments
- References to supplement for "routine verifications"
- Key formulas and results preserved

**Online/Supplementary Appendix** (~7,962 words):
- Lemma A.1 proof (boundedness)
- Topology and measure theory details
- Complete case analyses
- Numerical examples with full calculations
- All remarks and extensions
- IFT and SOC verification details

### Key Phrases for Main Text:

- "The full proof appears in Online Appendix OA.X; here we sketch the key steps."
- "Technical verification of the SOC appears in the Supplement."
- "Routine calculations confirm that... (see OA.X for details)."
- "Numerical examples illustrating this mechanism appear in the Supplement."

---

## Summary Table: Line Ranges for Technical Material

| Proof | Lines to Move | Content Type |
|-------|---------------|--------------|
| 01 | 10-47, 61-66, 73-91, 151-184 | Lemma, topology, attribution cases, remarks |
| 02 | 43-100, 118-120 | Step-by-step reductions, remarks |
| 03 | 14-47, 69-91, 98-104 | Algebra, verification, remarks |
| 04 | 35-37, 47-62 | Remarks, belief characterization |
| 05 | 9-14 | Sufficient conditions block |
| 06 | 111-127 | All four remarks |
| 07 | 123-161, 164-203 | Part (iii) details, all seven remarks |
| 08 | 51-61, 146-171 | AI utility calc, all four remarks |
| 09 | 108-131, 144-172 | Numerical example, all remarks |
| 10 | 52-62, 72-135, 234-263, 283-330 | Equivalence, Part 1 details, example, remarks |
| 11 | 29-44, 118-136, 239-288, 366-386, 389-462, 480-570 | Assumptions, threshold proof, cases, SOC, IFT, remarks |
