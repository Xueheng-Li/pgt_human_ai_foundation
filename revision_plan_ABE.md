# Comprehensive Revision Plan: Attributed Belief Equilibrium Paper

**Document Version**: 1.0
**Date**: 2026-01-14
**Paper Title**: Thinking for Machines: Attributed Belief Equilibrium
**Authors**: Xueheng Li
**Target Journals**: Econometrica (primary), Journal of Economic Theory, Games and Economic Behavior

---

## 1. Executive Summary

### 1.1 Paper Overview

This paper extends psychological game theory (PGT) to human-AI strategic interaction. The core innovation is the **Attributed Belief Equilibrium (ABE)**, which accommodates the fundamental asymmetry between humans (who have genuine beliefs and belief-dependent preferences) and AI agents (who have design-dependent objectives but lack mental states). The key insight is that humans **attribute** beliefs to AI—projecting expectations onto agents that cannot actually hold them—and these attributed beliefs trigger real psychological responses (guilt, indignation) that shape strategic behavior.

### 1.2 Overall Recommendation from Reviewers

**Recommendation**: Major Revision (all three simulated reviewers)

**Assessment Summary**:
- **Econometrica**: High novelty, adequate technical quality, needs improvement in foundations and exposition
- **JET**: Well-executed theoretical contribution to timely problem; framework carefully constructed
- **GEB**: Genuine theoretical contribution; elegant formalization; sound technical execution

### 1.3 Key Themes Requiring Revision

Five universal concerns emerged across all three reviewers:

| Priority | Issue | Description |
|----------|-------|-------------|
| 1 (Score: 9) | UC1: Attribution Function | Lacks microfoundations, no empirical identification strategy |
| 2 (Score: 9) | UC4: Existence Proof | Gaps in proof, topology unspecified, behavioral attribution feedback loop |
| 3 (Score: 8.33) | UC2: Welfare Measure | Material vs. extended welfare choice unjustified; belief revision puzzle |
| 4 (Score: 8.33) | UC3: Rational Attribution | Two inconsistent definitions; normative terminology problematic |
| 5 (Score: 8) | UC5: Assumption Structure | Multiple conditions (A1-A3, G, G', I, T) hard to track |

### 1.4 Estimated Revision Timeline

| Phase | Duration | Focus |
|-------|----------|-------|
| Phase 1 | Weeks 1-2 | Critical content (UC1-UC5) |
| Phase 2 | Week 3 | Important issues (PC1, PC2, B2) |
| Phase 3 | Week 4 | Valuable improvements (D, E, F, G series) |
| Phase 4 | Week 5 | Quick wins and extensions |
| Phase 5 | Weeks 6-7 | Response letter and polish |

**Total Estimated Effort**: 30-42 person-days (6-8 weeks full-time)

---

## 2. Cross-Reviewer Analysis

### 2.1 Summary Table: Which Reviewer Raised Which Issue

| Issue | Econometrica | JET | GEB | Priority Score |
|-------|--------------|-----|-----|----------------|
| **UC1: Attribution Function Foundation** | Major 1 | MC1 | Major 1 | 9 (all 3) |
| **UC2: Welfare Measure Justification** | Major 3 | Min6 | Major 5 | 8.33 (all 3) |
| **UC3: Rational Attribution Clarity** | Major 5 | MC3 | Minor 4 | 8.33 (all 3) |
| **UC4: Existence Proof Tightening** | Implicit | MC2 | Major 3 | 9 (all 3) |
| **UC5: Assumption Structure** | Major 4 | Implicit | Minor 2 | 8 (all 3) |
| **PC1: Dual Consistency Motivation** | Major 2 | Implicit | Not raised | 7 (2/3) |
| **PC2: Anthropomorphism-Attenuation Link** | Implicit | Not raised | Major 2 | 7 (2/3) |
| **B2: Proposition 4 Tautology** | Not raised | Not raised | Major 4 | GEB only |
| **D2: Introduction Length** | Minor 1 | Not raised | Minor 1 | 2 reviewers |
| **D3: Notation System** | Minor 2 | Not raised | Minor 2 | 2 reviewers |
| **D4: Example Placement** | Minor 3 | Not raised | Minor 1 | 2 reviewers |
| **E1: Trust Game Design** | Minor 8 | Not raised | Minor 7 | 2 reviewers |

### 2.2 Consensus Issues (All 3 Reviewers)

**UC1: Attribution Function Lacks Sufficient Foundation**
- No microfoundations derived from primitive assumptions about cognition
- No connection to established mind perception theories (Epley et al., 2007)
- No identification strategy for empirical estimation
- Linear specification (Example 1) is convenient but unmotivated

**UC2: Welfare Measure Choice Requires Justification**
- Paper switches between material welfare W and extended welfare W^ext without justification
- Normative status of psychological costs unclear
- Phantom expectations puzzle: why don't humans revise attributed beliefs?

**UC3: Rational Attribution Concept Needs Clarification**
- Two inconsistent definitions: (1) ω→0 limit, (2) fixed-point where φᵢ = σ*
- "Rational" conflates Bayesian updating with zero anthropomorphism
- "Over-anthropomorphism" carries problematic normative connotations

**UC4: Existence Proof Needs Technical Tightening**
- Behavioral attribution creates feedback loop not addressed in current proof
- Boundedness claim (A1 → bounded ψ) unclear
- Topology on belief spaces unspecified

**UC5: Assumption Structure Difficult to Track**
- 14+ distinct assumption codes (A1-A3, A2', A2'', A2''', E, G, G', I, T, etc.)
- G vs G' distinction unclear
- No comprehensive table summarizing conditions

### 2.3 Majority Issues (2 Reviewers)

**PC1: Dual Consistency Motivation** (Econometrica Major 2, JET implicit)
- Why shouldn't attributed beliefs update based on AI behavior?
- In repeated interactions, humans should learn about AI
- No bounds on divergence between attributed and revealed preferences

**PC2: Anthropomorphism-Attenuation Relationship** (GEB Major 2, Econometrica implicit)
- Treats ω and λ as independent parameters
- Gray et al. (2007) suggests they are related through two-dimensional mind perception
- Independence assumption needs justification

### 2.4 Unique Issues (1 Reviewer Only)

**Proposition 4 Tautology** (GEB Major 4 only)
- Condition (iii) "best-response separation" essentially restates conclusion
- Needs primitive conditions or reframing as possibility result

**Paper Length** (Econometrica only)
- 87+ pages excessive for Econometrica
- Needs substantial compression; proofs should move to supplement

---

## 3. Revision Plan by Priority

### 3.1 Critical Revisions (Must-Do)

#### CR1: Attribution Function Foundation (UC1)

**Issue Description**: The attribution function φᵢ(θⱼ, xⱼ, ωᵢ) is the paper's central primitive but lacks microfoundations. Three approaches (behavioral, signal-based, dispositional) are presented without explaining when each applies or how to estimate the function empirically.

**Proposed Solution**:
1. Add Subsection 2.5.4 "Empirical Implementation and Testability" (~2 pages)
   - Identification strategy using belief elicitation + signal manipulation
   - Worked example: trust game with interface manipulation
   - Parameter recovery from cross-treatment variation
   - Discussion of alternative functional forms with testable predictions

2. Add Subsection 2.5.5 "Psychological Foundations: Mind Perception Theory" (~1 page)
   - Formal mapping to Epley et al. (2007) SEEK framework
   - Sociality motivation → ωᵢ; Effectance motivation → signal sensitivity η
   - Dual process interpretation (System 1 vs System 2)
   - Connection to Gray et al. (2007) agency/experience dimensions

3. Revise Example 1 (Linear Attribution)
   - Justify linearity as tractable choice
   - Discuss alternatives and when needed
   - Link parameters to psychological primitives

4. Add Section 6.1 "Empirical Agenda" (~0.5 page)
   - Key testable predictions
   - Experimental designs to identify φ parameters

**Sections Affected**: 2.5, 6
**Effort Estimate**: 3-4 person-days
**New Material**: ~4 pages

---

#### CR2: Existence Proof Tightening (UC4)

**Issue Description**: The existence proof in Appendix A.1 has technical gaps: behavioral attribution creates a feedback loop not addressed in the proof; boundedness claim is unclear; topology on belief spaces is unspecified.

**Proposed Solution**:
1. Specify topology (weak* topology) with justification
2. Distinguish three attribution cases in proof:
   - **Case 1: Signal-based** - attributed beliefs are exogenous constants; standard Kakutani argument
   - **Case 2: Dispositional** - same as Case 1
   - **Case 3: Behavioral** - feedback loop requires joint fixed-point in (σ, h̃); additional continuity assumption on φ^beh

3. Add Lemma A.1 for boundedness: prove A1 + compactness → bounded ψ
4. Verify φᵢ produces valid probability distributions (∈ Δ(Sᵢ))
5. Revise Theorem 1 statement to clarify which attribution types are covered

**Sections Affected**: Appendix A.1, Theorem 1 statement
**Effort Estimate**: 3-4 person-days
**New Material**: ~4 pages (revised appendix)

---

#### CR3: Welfare Measure Justification (UC2)

**Issue Description**: Paper uses material welfare W in some propositions and extended welfare W^ext in others without justification. The normative status of psychological costs is unclear. The "phantom expectations" mechanism raises the puzzle of why humans don't revise attributed beliefs to eliminate guilt.

**Proposed Solution**:
1. Add NEW Section 2.7 "Welfare Measures" (~2 pages)
   - Definition 3: Material welfare W(s) = Σπᵢ(s)
   - Definition 4: Extended welfare W^ext = W + Σψᵢ
   - Normative justification: decision utility vs. experienced utility
   - When measures diverge: phantom expectations create divergence
   - Belief revision puzzle: attribution is automatic (System 1), revision is costly

2. Revise Proposition 8 to explicitly flag which measure is used
   - Part (i): Material welfare W for cooperation effects
   - Part (ii): Extended welfare W^ext for prosocial AI
   - Part (iii): Extended welfare W^ext for materialist AI (phantom expectations)

3. Add Proposition 10' for optimal design under extended welfare
4. Add Corollaries 2-3 clarifying when measures agree vs. diverge

**Sections Affected**: New Section 2.7, Section 5.2, Section 5.3
**Effort Estimate**: 4-5 person-days
**New Material**: ~5 pages

---

#### CR4: Rational Attribution Clarity (UC3)

**Issue Description**: "Rational attribution" is used in two inconsistent ways: (1) the ω→0 limit in Remark 1, and (2) the fixed-point concept in Proposition 3. The terminology carries problematic normative connotations.

**Proposed Solution**:
1. Terminological find-and-replace throughout manuscript:
   - "Rational attribution" (ω→0) → "Zero-anthropomorphism benchmark"
   - "Over-anthropomorphism" → "Elevated anthropomorphism"
   - Proposition 3 concept → "Rational Attribution Equilibrium (RAE)"

2. Add Definition 5: Zero-Anthropomorphism Benchmark
   - h̃ᵢ^(2,j),ZA = φᵢ(θⱼ, xⱼ, 0)
   - Interpretation: attributed belief when ωᵢ = 0

3. Add Definition 6: Rational Attribution Equilibrium (RAE)
   - ABE where attributed beliefs satisfy fixed-point condition
   - Formal definition: h̃ᵢ^(2,j),* = φᵢ(θⱼ, σⱼ*, ωᵢ) with fixed-point structure

4. Add Proposition 3': Existence conditions for RAE
5. Add Subsection 3.3 "Relationship Between Concepts"
   - Nested structure: ABE ⊃ RAE ⊃ {Zero-anthropomorphism}

**Sections Affected**: Throughout, especially Sections 2, 3
**Effort Estimate**: 2 person-days
**New Material**: ~2 pages

---

#### CR5: Assumption Structure Consolidation (UC5)

**Issue Description**: Multiple conditions (A1-A3, A2', A2'', A2''', E, G, G', I, T) are scattered throughout the paper. Their economic content, interdependencies, and which propositions use which conditions are difficult to track.

**Proposed Solution**:
1. Add NEW Section 2.8 "Summary of Assumptions" with comprehensive table:

| Code | Statement | Interpretation | Used In |
|------|-----------|----------------|---------|
| A1 | Finite strategy spaces, bounded payoffs | Technical regularity | Thm 1 |
| A2 | Continuous attribution function | Smooth variation | Thm 1 |
| A3 | Bounded psychological payoffs | Finite utilities | Thm 1 |
| A2' | Attribution monotonic in ω | Higher ω → higher attribution | Props 5-9 |
| G' | G ≡ γ_H λ^GUILT > 0 | Positive guilt | Prop 10(ii) |
| G | G > 1 | Guilt dominance | Props 5, 8, 9 |
| I | Indignation threshold | Strong indignation | Props 6, 8 |
| ... | ... | ... | ... |

2. Clarify G vs G' distinction with footnote at first use:
   - G' (positive guilt): G > 0
   - G (guilt dominance): G > 1
   - Hierarchy: G ⊃ G'

3. Discuss empirical reasonableness of key conditions
4. Consider consolidating A2', A2'', A2''' if proofs permit

**Sections Affected**: New Section 2.8, cross-references throughout
**Effort Estimate**: 2-3 person-days
**New Material**: ~2 pages (table + discussion)

---

### 3.2 Important Revisions (Should-Do)

#### IR1: Dual Consistency Motivation (PC1)

**Issue Description**: The asymmetric updating rules (Bayesian for genuine beliefs, attribution function for attributed beliefs) are not sufficiently motivated. In repeated interactions, humans should learn about AI; no bounds exist on phantom expectations.

**Proposed Solution**:
1. Add Subsection 3.1.3 "Why Asymmetric Updating Rules?" (~1 page)
   - Attribution is projection-based (System 1), not evidence-based
   - In one-shot games, updating cost exceeds benefit
   - Attribution function implicitly bounds divergence (maps into Δ(Sᵢ))

2. Add Subsection 6.2 "Dynamic Extensions and Learning" (~1 page)
   - Repeated games: attributed beliefs could update with experience
   - Learning dynamics: Bayesian updating of (θⱼ, ωᵢ) posterior
   - Long-run: attributed beliefs converge to rational attribution benchmark
   - Testable prediction: attribution-behavior gap narrows with experience

**Sections Affected**: Section 3.1, Section 6
**Effort Estimate**: 2 person-days
**New Material**: ~2 pages

---

#### IR2: Anthropomorphism-Attenuation Relationship (PC2)

**Issue Description**: The framework treats ω (anthropomorphism) and λ (attenuation) as independent, but Gray et al. (2007) suggests they are related through two-dimensional mind perception.

**Proposed Solution**:
Add Subsection 2.6.4 "Independence of Attribution and Attenuation" (~1.5 pages)
- Gray et al. (2007) two-dimensional framework:
  - **Agency dimension** → Attribution (ω affects φᵢ)
  - **Experience dimension** → Attenuation (λ affects emotional intensity)
- AI is typically high agency, low experience → independence plausible
- Empirical evidence for dissociation (de Melo et al., Bigman et al., Karpus et al.)
- Discussion of when independence may break down (highly anthropomorphic AI)

**Sections Affected**: Section 2.6
**Effort Estimate**: 1.5 person-days
**New Material**: ~1.5 pages

---

#### IR3: Proposition 4 Tautology Fix (B2)

**Issue Description**: GEB notes that condition (iii) "best-response separation" essentially restates the conclusion, making Proposition 4 nearly tautological.

**Proposed Solution**:
1. Reframe Proposition 4 as **possibility result**:
   - "There exist material games Γ and pairs of attribution functions (φ, φ') such that ABE(Γ, φ) sustains cooperation while ABE(Γ, φ') sustains defection"
   - Proof: constructive (exhibit specific game and attribution functions)

2. Add discussion of when multiplicity fails (~0.5 page):
   - Dominance: if material game has dominant strategy, attribution cannot override
   - Attribution power: multiplicity requires ∂BR_i/∂h̃ ≠ 0

**Sections Affected**: Section 3.4, Proposition 4
**Effort Estimate**: 1 person-day
**New Material**: ~0.5 pages (net, after reframing)

---

### 3.3 Optional Revisions (Nice-to-Have)

#### OR1: Early Illustrative Example (JET Min1)
- Add Section 2.9 with trust game preview before formal ABE definition
- Effort: 1 person-day; +1 page

#### OR2: Uniqueness Discussion (Econometrica Minor 6)
- Add Subsection 3.3.5 on when ABE is unique
- Effort: 1-2 person-days; +1 page

#### OR3: Continuous Public Goods (Econometrica Minor 9)
- Extend Section 4.2 to continuous contributions
- Effort: 1 person-day; +0.5 pages

#### OR4: Designer Incentives Formalization (Econometrica Minor 12)
- Add private vs. social optimum comparison in Section 5.3
- Effort: 1-2 person-days; +1 page

#### OR5: Experimental Design Discussion (GEB Minor 9, JET implicit)
- Add Section 4.5 "Testing Predictions"
- Effort: 1 person-day; +1 page

---

## 4. Implementation Timeline

### Phase 1: Quick Wins (Week 1)
| Day | Task | Effort |
|-----|------|--------|
| 1-2 | Fix 4 missing references (lines 171, 2748, 3078, 3806) | 0.5 days |
| 1-2 | Create assumption table (Section 2.8) - standalone addition | 1 day |
| 2-3 | Implement CR4: Rational attribution terminology | 2 days |
| 4-5 | Add G vs G' clarification footnote | 0.5 days |

**Deliverable**: Draft with terminology standardized and assumption table created

### Phase 2: Critical Content (Weeks 2-4)

**Week 2**:
| Day | Task | Effort |
|-----|------|--------|
| 1-3 | CR2: Existence proof rewrite (hardest technical work) | 3 days |
| 4-5 | CR3 Part 1: New Section 2.7 (Welfare Measures) | 2 days |

**Week 3**:
| Day | Task | Effort |
|-----|------|--------|
| 1-2 | CR3 Part 2: Revised Proposition 8, new Proposition 10' | 2 days |
| 3-5 | CR1: Attribution function subsections (2.5.4, 2.5.5) | 3 days |

**Week 4**:
| Day | Task | Effort |
|-----|------|--------|
| 1 | CR1 Part 2: Example 1 revision, Section 6.1 | 1 day |
| 2-3 | IR1: Dual consistency motivation (3.1.3, 6.2) | 2 days |
| 4 | IR2: ω-λ relationship (2.6.4) | 1 day |
| 5 | IR3: Proposition 4 reframing | 1 day |

**Deliverable**: Draft with all Tier 1-2 issues addressed

### Phase 3: Polish and Integration (Weeks 5-6)

**Week 5**:
| Day | Task | Effort |
|-----|------|--------|
| 1 | Compress Introduction Results subsection | 0.5 days |
| 1-2 | Tighten Related Literature | 1 day |
| 2-3 | Move numerical examples to Appendix B | 0.5 days |
| 3-4 | Notation clarification (h vs β footnote, x disambiguation) | 0.5 days |
| 4-5 | Trust game design motivation (E1), coordination justification (E3) | 1 day |

**Week 6**:
| Day | Task | Effort |
|-----|------|--------|
| 1-2 | Add cross-cultural evidence details (F3) | 0.5 days |
| 2-3 | Literature connections (behavioral GT, mechanism design) | 1 day |
| 3-4 | Optional: Early illustrative example (if page budget permits) | 1 day |
| 4-5 | Cross-reference verification, compile check | 1 day |

**Deliverable**: Complete revised manuscript

### Dependency Diagram

```
Week 1:
  [Terminology CR4] ──────────────────────────┐
  [Assumption Table CR5] ───────────────────┐ │
                                            │ │
Week 2-3:                                   │ │
  [Existence CR2] (independent) ────────────┼─┼───┐
  [Welfare CR3] (independent) ──────────────┼─┼───┤
                                            │ │   │
Week 3-4:                                   ▼ ▼   │
  [Attribution CR1] (requires CR4) ─────────────┐ │
                                                │ │
Week 4:                                         │ │
  [ω-λ IR2] (requires CR1) ──────────────────── │ │
  [Dual Consistency IR1] (requires CR4) ──────────┤
                                                  │
Week 5-6:                                         │
  [Compression, Polish] ◄─────────────────────────┘
```

---

## 5. Response to Reviewers Outline

The response letter should be organized by **issue category** (not by reviewer), since issues overlap heavily.

### 5.1 Theoretical Foundations

**Attribution Function (UC1)**
- *Issue*: All three reviewers noted attribution function lacks microfoundations and empirical grounding
- *How addressed*: New Subsections 2.5.4 (empirical implementation), 2.5.5 (Epley et al. connection); revised Example 1; new Section 6.1 (empirical agenda)
- *Where to find*: pp. XX-XX (Subsections 2.5.4-2.5.5), pp. XX (Example 1), pp. XX (Section 6.1)

**Rational Attribution (UC3)**
- *Issue*: Two inconsistent definitions; normative terminology
- *How addressed*: Terminological revision throughout; new Definition 5 (zero-anthropomorphism benchmark), Definition 6 (RAE); new Proposition 3' with existence conditions
- *Where to find*: Definitions on p. XX; Proposition 3' on p. XX; relationship clarification in Subsection 3.3

**Dual Consistency (PC1)**
- *Issue*: Econometrica questioned why attributed beliefs don't update based on AI behavior
- *How addressed*: New Subsection 3.1.3 explaining asymmetric updating; Section 6.2 outlining dynamic extensions
- *Where to find*: pp. XX-XX

**ω-λ Relationship (PC2)**
- *Issue*: GEB noted independence assumption needs justification
- *How addressed*: New Subsection 2.6.4 connecting to Gray et al. (2007) two-dimensional mind perception
- *Where to find*: pp. XX-XX

### 5.2 Technical Rigor

**Existence Proof (UC4)**
- *Issue*: Gaps in proof; behavioral attribution feedback loop; topology unspecified
- *How addressed*: Complete rewrite of Appendix A.1 distinguishing three attribution cases; explicit topology specification; new Lemma A.1 for boundedness
- *Where to find*: Appendix A.1 (pp. XX-XX)

**Proposition 4 (B2)**
- *Issue*: GEB noted condition (iii) nearly tautological
- *How addressed*: Reframed as possibility result; added discussion of when multiplicity fails
- *Where to find*: Proposition 4 (p. XX); discussion on p. XX

### 5.3 Normative Welfare Analysis

**Welfare Measures (UC2)**
- *Issue*: Paper switches between W and W^ext without justification; belief revision puzzle
- *How addressed*: New Section 2.7 with unified welfare framework; decision vs. experienced utility justification; revised Proposition 8 explicitly flagging measures; new Proposition 10'
- *Where to find*: Section 2.7 (pp. XX-XX); Proposition 8 (p. XX); Proposition 10' (p. XX)

### 5.4 Exposition and Presentation

**Assumption Structure (UC5)**
- *Issue*: Multiple conditions hard to track
- *How addressed*: Comprehensive assumption table in Section 2.8; G vs G' distinction clarified
- *Where to find*: Table 1 (p. XX); footnote on p. XX

**Introduction and Literature**
- *Issue*: Results subsection duplicates abstract; literature diffuse
- *How addressed*: Condensed Results (~30 lines saved); reorganized literature around three technical contributions
- *Where to find*: Section 1.1-1.2 (pp. XX-XX)

### 5.5 Applications and Extensions

**Trust Game Design (E1)**
- *Issue*: Why AI trustor, human trustee?
- *How addressed*: Added motivation paragraph and discussion of reverse case
- *Where to find*: Section 4.1 opening (p. XX)

**Experimental Design (F1)**
- *Issue*: How to test predictions?
- *How addressed*: New Section 4.5 "Testing Predictions" with belief elicitation and signal manipulation protocols
- *Where to find*: pp. XX-XX

---

## 6. Structural Changes

### 6.1 Main Text vs. Supplement Split

**Main Text (Target: 50-55 pages)**:
- Sections 1-6 with revisions
- Proof sketches only in Appendix A

**Online Supplement (Target: 45-55 pages)**:
- Appendix B: Complete proofs
- Appendix C: Detailed numerical examples (moved from Section 3.4)
- Appendix D: Technical lemmas
- Appendix E: Extensions (mixed strategies, uniqueness, continuous public goods)

### 6.2 Notation Changes

| Old | New | Context |
|-----|-----|---------|
| "Rational attribution" (ω→0) | "Zero-anthropomorphism benchmark" | Throughout |
| "Rational attribution" (fixed-point) | "Rational Attribution Equilibrium (RAE)" | Proposition 3 |
| "Over-anthropomorphism" | "Elevated anthropomorphism" | Throughout |
| β_i ambiguity | Add footnote clarifying β_i ≠ β^(n)_i | Section 2.3 |
| x (trust game amount vs. signal) | Clarify dual role in Section 4.1 | Section 4.1 |

### 6.3 Assumption Consolidation Table

**Final Structure of Assumptions**:

| Category | Codes | Purpose |
|----------|-------|---------|
| Technical Regularity | A1, A2, A3 | Existence theorem |
| Attribution Properties | A2', A2'', A2''' | Comparative statics |
| Psychological Sensitivity | G', G, I | Application-specific thresholds |
| Application-Specific | E, T, C | Game-specific conditions |

**Key Clarifications**:
- G' (positive guilt: G > 0) ⊂ G (guilt dominance: G > 1)
- A2''' (attribution validity) is implicit in A2 and verified in proof

---

## 7. Actionable Checklist

### 7.1 Critical Revisions (Must Complete)

- [ ] 1. Create unified assumption table (Section 2.8)
- [ ] 2. Add G vs G' clarification footnote
- [ ] 3. Find-and-replace "rational attribution" terminology throughout
- [ ] 4. Add Definition 5 (Zero-anthropomorphism benchmark)
- [ ] 5. Add Definition 6 (Rational Attribution Equilibrium)
- [ ] 6. Add Proposition 3' (RAE existence conditions)
- [ ] 7. Add Subsection 3.3 (Relationship between concepts)
- [ ] 8. Rewrite Appendix A.1 with three attribution cases
- [ ] 9. Add topology specification (weak* topology)
- [ ] 10. Add Lemma A.1 (boundedness from A1)
- [ ] 11. Verify φᵢ produces valid distributions
- [ ] 12. Add Section 2.7 (Welfare Measures)
- [ ] 13. Add Section 2.7.4 (Belief revision puzzle)
- [ ] 14. Revise Proposition 8 with explicit welfare measure flagging
- [ ] 15. Add Proposition 10' (Extended welfare optimal design)
- [ ] 16. Add Corollaries 2-3 (When measures agree/diverge)
- [ ] 17. Add Subsection 2.5.4 (Empirical Implementation)
- [ ] 18. Add Subsection 2.5.5 (Mind Perception Theory connection)
- [ ] 19. Revise Example 1 (Linear Attribution justification)
- [ ] 20. Add Section 6.1 (Empirical Agenda)

### 7.2 Important Revisions (Should Complete)

- [ ] 21. Add Subsection 3.1.3 (Why asymmetric updating rules)
- [ ] 22. Add Section 6.2 (Dynamic extensions)
- [ ] 23. Add Subsection 2.6.4 (ω-λ independence justification)
- [ ] 24. Reframe Proposition 4 as possibility result
- [ ] 25. Add discussion of when multiplicity fails

### 7.3 Quick Wins and Polish

- [ ] 26. Fix missing reference line 171 (Harsanyi 1967)
- [ ] 27. Fix broken references lines 2748, 3078, 3806
- [ ] 28. Compress Introduction Results subsection
- [ ] 29. Tighten Related Literature section
- [ ] 30. Move numerical examples to Appendix C (supplement)
- [ ] 31. Add h vs β clarification footnote
- [ ] 32. Clarify trust game x (action + signal) in Section 4.1
- [ ] 33. Add trust game design motivation (E1)
- [ ] 34. Add coordination psychological payoff justification (E3)
- [ ] 35. Add Proposition 10 discrete assumption remark
- [ ] 36. Add Karpus et al. cross-cultural details
- [ ] 37. Add mechanism design literature connection
- [ ] 38. Add behavioral game theory literature connection
- [ ] 39. Add machine behavior literature connection

### 7.4 Optional Extensions (If Time/Space Permits)

- [ ] 40. Add early illustrative example (Section 2.9)
- [ ] 41. Add uniqueness discussion
- [ ] 42. Extend public goods to continuous contributions
- [ ] 43. Add designer incentives formalization
- [ ] 44. Add experimental design subsection

### 7.5 Quality Control (Before Submission)

- [ ] 45. Verify all assumption citations reference Table 1
- [ ] 46. Verify G vs G' used correctly throughout
- [ ] 47. Compile full manuscript, check page count
- [ ] 48. Verify all cross-references work
- [ ] 49. Check all citations in references.bib
- [ ] 50. Create journal-specific versions (Econometrica: with supplement)

---

## 8. Risk Management

### 8.1 Potential Pitfalls

**Risk 1: Existence Proof Errors**
- *Description*: Rewriting the 5-6 page technical proof risks introducing mathematical errors
- *Probability*: Moderate
- *Impact*: High (fundamental to paper)
- *Mitigation*: Have co-author verify each case independently; test signal-based, dispositional, and behavioral attribution separately
- *Contingency*: If behavioral attribution case is problematic, restrict Theorem 1 to signal-based/dispositional with behavioral as extension

**Risk 2: Terminology Find-and-Replace Issues**
- *Description*: "Rational attribution" appears in multiple contexts; replacement may miss context or create inconsistencies
- *Probability*: Moderate
- *Impact*: Medium (readability, reviewer confusion)
- *Mitigation*: Create exhaustive list of all instances before replacing; manual review of each replacement
- *Contingency*: Add clarifying remarks if any ambiguity remains

**Risk 3: Page Budget Overrun**
- *Description*: Adding ~16-19 pages of content while compressing ~22 pages may not balance
- *Probability*: Low-Moderate
- *Impact*: Medium (journal length requirements)
- *Mitigation*: Track page count at each phase; prioritize Tier 1 additions; use online supplement aggressively
- *Contingency*: For Econometrica, move additional proofs to supplement; for JET/GEB, accept longer manuscript

**Risk 4: Welfare Framework Objections**
- *Description*: Philosophical debate about welfare measure choice may persist
- *Probability*: Low
- *Impact*: Medium
- *Mitigation*: Present results under BOTH measures; avoid taking strong normative stance
- *Contingency*: Add explicit caveats acknowledging multiple valid perspectives

**Risk 5: Attribution Function Still Seen as Ad Hoc**
- *Description*: Reviewers may want even more microfoundation than we can provide
- *Probability*: Low-Moderate
- *Impact*: High (core contribution)
- *Mitigation*: Acknowledge limitation explicitly; frame as modeling primitive requiring empirical validation (JET explicitly recommends this approach)
- *Contingency*: Emphasize "conceptual framework for emerging domain" positioning

### 8.2 Contingency Plans

**If major theoretical objection to existence proof**:
- Option A: Restrict Theorem 1 to signal-based/dispositional attribution
- Option B: Add stronger assumptions for behavioral case (A3' on continuity)
- Option C: Defer behavioral attribution to separate proposition or extension

**If attribution function objection persists**:
- Option A: Add appendix with revealed preference axioms (hard, time-consuming)
- Option B: Strengthen empirical evidence section with additional citations
- Option C: Explicitly position paper as "first formal framework" requiring empirical grounding

**If page count exceeds target**:
- For Econometrica: Move all proofs except sketches to online supplement
- For JET: Accept longer manuscript (no explicit length concern)
- For GEB: Move examples + detailed proofs to supplement

---

## Appendix A: Reviewer-Specific Concerns Matrix

| Concern | Econometrica | JET | GEB |
|---------|--------------|-----|-----|
| Attribution microfoundations | Major 1 (HARD) | MC1 (MEDIUM) | Major 1 (MEDIUM) |
| Existence proof gaps | Implicit | MC2 (detailed) | Major 3 (topology) |
| Welfare measure choice | Major 3 (detailed) | Min6 (paragraph) | Major 5 (dual presentation) |
| Rational attribution | Major 5 (terminology) | MC3 (formal separation) | Minor 4 (rename) |
| Assumption tracking | Major 4 (table) | Implicit | Minor 2 (notation) |
| Dual consistency | Major 2 (extend) | Min11 (flag) | Not raised |
| ω-λ independence | Implicit | Not raised | Major 2 (justify) |
| Proposition 4 | Not raised | Not raised | Major 4 (tautology) |
| Paper length | Critical (compress) | Not raised | Moderate (focus) |

---

## Appendix B: Page Budget Summary

**Starting Point**:
- Main text (Sections 1-6): ~40 pages
- Appendix A (Proofs): ~60 pages
- **Total**: ~100 pages

**Additions from Revisions**:
| Item | Pages | Section |
|------|-------|---------|
| Attribution function (CR1) | +4 | 2.5.4-2.5.5, 6.1 |
| Existence proof (CR2) | +2 | Appendix A.1 |
| Welfare framework (CR3) | +5 | 2.7, 5.2, 5.3 |
| Rational attribution (CR4) | +2 | Definitions, Prop 3', 3.3 |
| Assumption table (CR5) | +1.5 | 2.8 |
| Dual consistency (IR1) | +2 | 3.1.3, 6.2 |
| ω-λ relationship (IR2) | +1.5 | 2.6.4 |
| Proposition 4 fix (IR3) | +0.5 | 3.4 |
| **Total additions** | **+18.5** | |

**Subtractions from Compression**:
| Item | Pages | Section |
|------|-------|---------|
| Introduction compression | -1 | 1.1 |
| Literature tightening | -0.5 | 1.2 |
| Move examples to supplement | -1.5 | 3.4 |
| Move proofs to supplement | -50 | Appendix A → Supplement |
| **Total subtractions** | **-53** | |

**Final Structure**:
| Component | Pages | Content |
|-----------|-------|---------|
| Main text | 51-55 | Sections 1-6 + proof sketches |
| Online supplement | 50-55 | Complete proofs + examples + extensions |
| **Total** | 101-110 | Similar to current, better organized |

---

**Document Prepared By**: Agent 4.2 (Final Plan Compiler)
**Based On**: Cross-report synthesis, revision strategy, content revisions, structural revisions, and review feedback from Agents 2.1, 2.2, 3.1, 3.2, and 4.1
**Status**: Ready for Author Review and Implementation
