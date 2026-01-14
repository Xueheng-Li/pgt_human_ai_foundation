# Style Review: Integrated ABE Existence Proof

**File reviewed:** `phase2_integrated_proof.tex`
**Reference files:** `sec_equilibrium.tex`, `sec_framework.tex`
**Date:** 2026-01-12

---

## Summary Assessment

The integrated proof is logically sound and well-structured. The six-step organization provides clear navigation. However, several notation inconsistencies with the main manuscript need correction, and the writing can be tightened in places. The proof is appropriate for Econometrica/JET in rigor but slightly verbose for those venues.

**Overall grade:** B+. Ready after notation fixes and targeted cuts.

---

## Notation Issues

### 1. Pure vs. Mixed Strategy Notation

**Problem:** The proof uses $\sigma$ throughout for mixed strategies, but `sec_equilibrium.tex` Definition 3.1 uses $s^*$ for equilibrium strategies with a separate remark about mixed strategy extension.

**Recommendation:** Either:
- (a) State explicitly at the proof's start that we work in mixed strategies and use $\sigma$ consistently, or
- (b) Match `sec_equilibrium.tex` by using $s$ for pure strategies and adding a brief note about the mixed extension.

Option (a) is cleaner for the proof; ensure the main text accommodates this.

### 2. Theorem Numbering

**Problem:** The proof labels the theorem as `Theorem 1` (via `\label{thm:existence}`), but `sec_equilibrium.tex` places this as Theorem 3.1 (Section 3). The numbering will not match when integrated.

**Recommendation:** Use `\label{thm:ABE-existence}` or similar to distinguish from the theorem counter in the main document. When integrating into the appendix, ensure the counter resets appropriately or use lettered theorem numbers (e.g., Theorem A.1).

### 3. Utility Function Arguments

**Problem:** The proof writes:
```
U_i^H(s_i, s_{-i}, h_i(\sigma), \tilde{h}_i)
```
But `sec_framework.tex` defines:
```
U_i^H(s, h_i, \tilde{h}_i)
```
The proof inconsistently uses $h_i(\sigma)$ (functional notation) and $\tilde{h}_i$ (object notation).

**Recommendation:** Use consistent notation. Either:
- Write $U_i^H(s, h_i, \tilde{h}_i)$ with beliefs understood as determined by $\sigma$, or
- Write $U_i^H(s, h_i(\sigma), \tilde{h}_i(\sigma))$ to make functional dependence explicit throughout.

### 4. Belief Mapping Notation

**Problem:** The proof introduces $\kappa_i^{attr,j}$ and $\kappa_i^{(1,k)}$ for belief mappings, but these do not appear in the main manuscript.

**Recommendation:** These are fine as internal proof notation, but add a sentence: "For notational convenience in this proof, we define belief computation mappings..."

### 5. ABE Condition Labels

**Problem:** The proof uses (ABE1)--(ABE4) in Proposition 6, but `sec_equilibrium.tex` uses numbered list items (1)--(4) without labels.

**Recommendation:** Add consistent labels in `sec_equilibrium.tex` for cross-referencing, or remove labels in the proof and say "the four conditions of Definition 3.1."

### 6. Player Index Conventions

**Problem:** The proof uses $i \in N_H$ for humans and $j \in N_A$ for AI consistently, which matches the framework. Good.

**Verified:** No issues here.

---

## Style Improvements Needed

### 1. Wordy Phrases to Cut

| Location | Current | Suggested |
|----------|---------|-----------|
| Abstract | "self-contained proof that" | "proof that" |
| Abstract | "proceeds in six steps" | cut (the structure shows this) |
| Remark 1 | "A key simplification relative to standard psychological game equilibrium" | "Unlike standard PGT" |
| Remark 1 | "This is possible because" | "because" |
| Step 3 intro | "We establish that the best-response correspondences satisfy the conditions for Kakutani's theorem." | "The best-response correspondences satisfy Kakutani's conditions." |
| Lemma 4 proof | "The same reasoning as Lemma 3 applies." | "Same reasoning as Lemma 3." |

### 2. Passive Voice Instances

| Location | Current | Suggested |
|----------|---------|-----------|
| Line 43 | "an ABE exists in mixed strategies" | "a mixed-strategy ABE exists" |
| Line 53 | "This allows the fixed-point argument to operate" | "This confines the fixed-point argument to" |
| Line 163 | "the maximum is attained" | "the maximum exists" |

### 3. Redundant Statements

**Line 70-82 (Lemma 1 proof):** The non-emptiness argument is overstated. "By A1, each $S_i$ is non-empty. Hence each simplex $\Delta(S_i)$ is non-empty" can be: "Each $\Delta(S_i)$ is non-empty since $S_i$ is non-empty by A1."

**Line 206:** "The Cartesian product of non-empty (resp. convex) sets is non-empty (resp. convex)." This is a standard fact; either cut or inline into the proof without separate statement.

### 4. Remarks Assessment

| Remark | Assessment | Recommendation |
|--------|------------|----------------|
| Remark 1 (Why $\Sigma$ Alone Suffices) | Essential. This is the key insight. | Keep, but tighten. |
| Remark 5 (Role of Attributed Beliefs) | Redundant with Remark 1. | Cut. The point was made. |
| Remark 7 (Comparison with Standard PGT) | Repeats Remark 1 content. | Cut or merge with Remark 1. |
| Remark 8 (Role of Each Assumption) | Useful for exposition. | Keep. |
| Remark 9 (Uniqueness) | Standard but useful. | Keep, possibly shorten. |
| Remark 10 (Extensions) | Forward-looking; may belong in main text. | Move to main text or cut from proof appendix. |

**Net recommendation:** Cut Remarks 5 and 7. Keep Remarks 1, 8, 9. Move or cut Remark 10.

---

## Specific Suggestions

### Abstract

**Current (34 words):**
> This document provides a complete, self-contained proof that an Attributed Belief Equilibrium (ABE) exists under standard regularity conditions. The proof proceeds in six steps: (1) space construction, (2) belief computation mapping, (3) best-response correspondence properties, (4) product correspondence, (5) Kakutani fixed-point application, and (6) equilibrium verification.

**Revised (20 words):**
> We prove that an Attributed Belief Equilibrium exists under regularity conditions A1--A3. The proof applies Kakutani's fixed-point theorem.

(The six steps are visible in the structure; no need to enumerate in the abstract.)

### Theorem Statement (Lines 41-44)

**Current:**
> Consider a human-AI interaction game with $n_H \geq 1$ humans and $n_A \geq 0$ AI agents. Under Assumptions A1--A3, an Attributed Belief Equilibrium exists in mixed strategies.

**Revised:**
> Under Assumptions A1--A3, a mixed-strategy Attributed Belief Equilibrium exists.

(The player counts are premises, not part of the theorem statement proper.)

### Step 1 Opening (Lines 63-64)

**Current:**
> We establish that the domain for the fixed-point argument---the mixed strategy space $\Sigma$---has the required topological properties.

**Revised:**
> The mixed strategy space $\Sigma$ has the topological properties required for fixed-point arguments.

### Lemma 1 Proof (Compactness)

**Current (Lines 75-79):**
> Fix $i \in N$. Since $|S_i| = m_i < \infty$ by A1, the simplex [...] is a closed and bounded subset of $\mathbb{R}^{m_i}$, hence compact by Heine-Borel. The finite product $\Sigma = \prod_{i \in N} \Delta(S_i)$ is compact by Tychonoff's theorem.

**Issue:** Tychonoff is overkill for finite products of compact sets. The finite product of compact sets is compact by elementary arguments.

**Revised:**
> Each $\Delta(S_i)$ is compact (closed and bounded in $\mathbb{R}^{m_i}$ by Heine-Borel). The finite product of compact sets is compact.

### Proposition 3 (Lines 117-124)

**Current:**
> The combined belief computation mapping $\kappa: \Sigma \to \mathcal{B} \times \tilde{\mathcal{B}}$ is continuous.

**Issue:** $\mathcal{B}$ and $\tilde{\mathcal{B}}$ are not defined. The framework uses $h$ and $\tilde{h}$ notation.

**Fix:** Define these spaces or use existing notation.

### Conclusion Line (267)

**Current:**
> Combining Propositions 5 and 6, an ABE exists under A1--A3.

**Revised:**
> Propositions 5 and 6 establish ABE existence under A1--A3.

---

## Logical Presentation Order

The six-step structure is sound:

1. Space construction (domain for fixed point)
2. Belief computation (how beliefs derive from strategies)
3. Best-response properties (individual correspondences)
4. Product correspondence (joint correspondence)
5. Fixed-point application (Kakutani)
6. Equilibrium verification (fixed point is ABE)

**One possible improvement:** Merge Steps 4 and 5. The product correspondence is defined only to apply Kakutani immediately. A combined "Fixed-Point Argument" section would be tighter.

---

## Level of Detail for Econometrica/JET

**Current level:** Appropriate for a self-contained appendix proof. The step-by-step verification of Kakutani's conditions is standard.

**Potential cuts for journal submission:**
- The Kakutani theorem statement (Theorem 5) is textbook material. Either cut or relegate to a footnote.
- The proofs of Lemmas 3 and 4 are standard; consider stating "by standard arguments" with a citation to a game theory text.

**Additions needed:**
- Explicit reference to the main theorem in the body text.
- A note clarifying that this proof appears in the appendix (if that is the intended location).

---

## Checklist Summary

| Item | Status | Action |
|------|--------|--------|
| Notation: pure vs. mixed | Inconsistent | Harmonize with main text |
| Notation: theorem numbering | Will conflict | Relabel for appendix |
| Notation: utility arguments | Inconsistent | Standardize |
| Notation: belief spaces | Undefined | Define $\mathcal{B}, \tilde{\mathcal{B}}$ |
| Writing: economy | B | Cut ~15% per suggestions |
| Remarks | Too many | Cut Remarks 5, 7; move 10 |
| Logical structure | Good | Optional: merge Steps 4-5 |
| Journal appropriateness | Good | Consider cuts for final version |

---

## Final Recommendations

1. **Immediate fixes:** Resolve notation inconsistencies (Items 1-5 above).
2. **Cut 3 of 6 remarks:** Remove Remarks 5 and 7; move Remark 10 to main text.
3. **Tighten prose:** Apply line-by-line edits to reduce word count by 10-15%.
4. **Merge Steps 4-5:** Optional, but creates a cleaner "Kakutani Application" section.
5. **Add cross-references:** Ensure the proof references Definition 3.1 and Theorem 3.1 from the main text.

After these changes, the proof will be publication-ready for an Econometrica/JET appendix.
