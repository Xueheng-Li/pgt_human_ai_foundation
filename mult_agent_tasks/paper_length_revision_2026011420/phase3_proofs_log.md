# Phase 3: Proof Reorganization Log

**Date**: 2026-01-14
**Agent**: Agent-9
**Task**: Reorganize proofs into main appendix + supplementary appendix

## Summary

All 11 proof files have been reorganized. Technical details, numerical examples, and extended remarks have been moved to a new supplementary appendix (`supplementary_appendix.tex`). All proofs remain complete and rigorous---this is reorganization, not cutting.

## Line Count Comparison

| File | Before | After | Reduction |
|------|--------|-------|-----------|
| 01_thm_existence.tex | ~185 | 97 | 48% |
| 02_prop_reduction_pgt.tex | ~121 | 23 | 81% |
| 03_prop_reduction_nash.tex | ~105 | 18 | 83% |
| 04_prop_rational_attribution.tex | ~138 | 34 | 75% |
| 05_prop_multiplicity.tex | ~57 | 19 | 67% |
| 06_prop_trust_game.tex | ~128 | 68 | 47% |
| 07_prop_public_goods.tex | ~204 | 88 | 57% |
| 08_prop_coordination.tex | ~172 | 68 | 60% |
| 09_prop_welfare_anthropomorphism.tex | ~173 | 35 | 80% |
| 10_prop_welfare_over_anthropomorphism.tex | ~331 | 89 | 73% |
| 11_prop_optimal_design.tex | ~571 | 130 | 77% |
| **Total Main Appendix** | ~2,185 | 669 | **69%** |
| **Supplementary Appendix** | 0 | 991 | (new) |

## Material Moved to Supplementary Appendix

### OA.1: Existence Theorem (Theorem 1)
- OA.1.1: Full proof of Lemma A.1 (boundedness)
- OA.1.2: Topology and measure theory details (strategy space topology, attribution approaches)
- OA.1.3: 4 remarks on extensions (behavioral attribution, role of assumptions, comparison with PGT, topology generalizations)

### OA.2: Reduction Propositions (Props 2-5)
- OA.2.1: Proposition 2 detailed algebra (Steps 3-6 reduction to PGT)
- OA.2.2: Proposition 3 detailed verification (Steps 1.1-2.3 reduction to Nash)
- OA.2.3: Proposition 4 belief characterization under RAE
- OA.2.4: Proposition 5 sufficient conditions block for multiplicity

### OA.5: Application Proofs (Props 5-7)
- OA.5.1: Trust game extended analysis (knife-edge G=1, low-guilt G<1, empirical support)
- OA.5.2: Public goods detailed derivations (population share channel analysis, 7 remarks)
- OA.5.3: Coordination AI utility calculations (numerical example, 4 remarks)

### OA.6: Welfare Propositions (Props 8-9)
- OA.6.1: Proposition 8 numerical example and 5 remarks
- OA.6.2: Proposition 9 complete treatment
  - OA.6.2.1: Equivalence under (A2') and (A2'')
  - OA.6.2.2: Part 1 detailed steps
  - OA.6.2.3: Part 2 welfare calculations and numerical example
  - OA.6.2.4: 7 remarks on policy, cultural variation, asymmetry

### OA.7: Optimal Design (Prop 10)
- OA.7.1: Full preamble with assumption statements
- OA.7.2: Part (i) threshold analysis claim proof
- OA.7.3: Part (ii) complete case analysis
- OA.7.4: Part (iii) SOC verification and IFT derivations
- OA.7.5: 11 remarks on interpretation, policy, boundary cases

## Verification

All proofs remain mathematically complete:
- Core arguments preserved in main appendix
- Technical details accessible via Online Appendix references
- Transition phrases added throughout (e.g., "See Online Appendix OA.X for details")
- No logical steps removed---only reorganized

## Files Modified

1. `/drafts/proofs/01_thm_existence.tex`
2. `/drafts/proofs/02_prop_reduction_pgt.tex`
3. `/drafts/proofs/03_prop_reduction_nash.tex`
4. `/drafts/proofs/04_prop_rational_attribution.tex`
5. `/drafts/proofs/05_prop_multiplicity.tex`
6. `/drafts/proofs/06_prop_trust_game.tex`
7. `/drafts/proofs/07_prop_public_goods.tex`
8. `/drafts/proofs/08_prop_coordination.tex`
9. `/drafts/proofs/09_prop_welfare_anthropomorphism.tex`
10. `/drafts/proofs/10_prop_welfare_over_anthropomorphism.tex`
11. `/drafts/proofs/11_prop_optimal_design.tex`

## File Created

- `/drafts/supplementary_appendix.tex` (991 lines)
  - Complete LaTeX document with proper structure
  - Sections OA.1-OA.7 covering all moved material
  - Proper theorem environments and notation
  - Bibliography placeholder referencing main paper
