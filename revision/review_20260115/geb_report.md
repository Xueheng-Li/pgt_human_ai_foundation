# Referee Report: Games and Economic Behavior

**Manuscript:** "Thinking for Machines: Attributed Belief Equilibrium"

**Date:** January 14, 2026

---

## Summary

This paper introduces Attributed Belief Equilibrium (ABE), an extension of psychological game theory to strategic interactions between humans and AI agents. The central innovation addresses a fundamental asymmetry: humans have belief-dependent preferences (guilt, reciprocity, indignation), while AI have design-dependent objectives with no genuine mental states. The paper formalizes how humans "attribute" beliefs to AI through an attribution function that depends on AI design parameters, observable signals, and individual anthropomorphism tendencies. The main results establish: (1) existence of ABE under regularity conditions; (2) nesting of standard equilibrium concepts as special cases; (3) attribution-dependent equilibrium multiplicity; (4) applications to trust, public goods, and coordination games; and (5) welfare implications showing that anthropomorphism benefits welfare with prosocial AI but may harm welfare with materialist AI through "phantom expectations."

## Overall Assessment

This is a well-executed theoretical contribution that addresses a genuinely novel problem: how to extend psychological game theory when one class of players lacks the mental states that standard theory assumes. The motivation is timely---human-AI interaction is economically significant and growing. The technical execution is sound, and the framework generates interesting predictions that distinguish it from standard game theory.

The paper's main strength is its conceptual clarity. The distinction between genuine beliefs (about humans) and attributed beliefs (about AI) is well-motivated and carefully formalized. The attribution function is a natural primitive that captures the empirically documented phenomenon of anthropomorphism without requiring that AI actually possess mental states. The welfare analysis reveals a non-obvious asymmetry: anthropomorphism that improves cooperation with prosocial AI creates pure welfare losses with materialist AI.

My main concern is about the paper's contribution relative to existing psychological game theory. While the framework is novel, the departure from standard PGT is localized to a single function (the attribution function), and the equilibrium concept inherits its structure from Battigalli and Dufwenberg (2009). The paper would benefit from sharper articulation of when ABE generates predictions that differ qualitatively from either standard PGT or standard game theory.

## Major Comments (Essential for Publication)

### 1. Clarify the Empirical Content of the Attribution Function

The attribution function $\phi_i(\theta_j, x_j, \omega_i)$ is the key primitive that distinguishes ABE from standard theory, yet its empirical content remains somewhat vague. Section 2.6 provides an experimental design, but the paper should address:

- What restrictions does the theory place on $\phi_i$? The current assumptions (continuity, monotonicity) are mathematically convenient but not obviously derived from psychological theory.
- How does the linear specification in Example 1 compare to alternatives? The paper acknowledges saturation and threshold effects but does not explain why linearity is preferred beyond tractability.

The paper should either (a) derive functional form restrictions from the psychological literature on mind perception, or (b) more explicitly acknowledge that $\phi_i$ is a reduced-form that must be identified empirically.

### 2. Strengthen the Comparison with Standard Approaches

The nesting results (Propositions 1-3) are valuable, but the paper should more precisely characterize when ABE yields different predictions. Specifically:

- Proposition 3 shows that under "rational attribution," ABE reduces to Bayes-Nash equilibrium. When is rational attribution the appropriate benchmark? The paper treats departures from rational attribution as the interesting case but does not explain under what conditions we should expect such departures.
- The attribution-dependent multiplicity result (Proposition 4) shows that different $\phi_i$ functions sustain different equilibria. But standard PGT also exhibits belief-dependent multiplicity. What is the empirical signature that distinguishes ABE multiplicity from PGT multiplicity?

A sharper comparison would help readers understand the paper's contribution to the broader literature.

### 3. Phantom Expectations: Behavioral Foundations

The "phantom expectations" mechanism (Proposition 9) is central to the welfare analysis, but its behavioral foundation needs strengthening. The paper claims that humans experience guilt from failing to meet expectations that AI never held. However:

- Why doesn't learning eliminate phantom expectations? Section 2.7 discusses belief revision but concludes that System 1/System 2 asymmetries prevent full correction. This is plausible but not obviously true for repeated interactions with transparent AI.
- Are phantom expectations empirically documented? The paper cites anthropomorphism literature extensively but does not cite direct evidence of guilt from disappointing AI that lacks genuine expectations.

The paper should either provide more direct empirical support for phantom expectations or acknowledge this as a theoretical prediction requiring future testing.

## Minor Comments (Suggestions)

### Presentation

1. The paper is long (approximately 50 pages with appendix). Consider moving some technical material (e.g., detailed proof of Theorem 1, the attribution function specification discussion) to a supplementary appendix to improve readability.

2. The notation for belief hierarchies ($h_i^{(2,k)}$, $\tilde{h}_i^{(2,j)}$) is clear but cumbersome. A notation table at the beginning of Section 2 would help readers track the many subscripts and superscripts.

3. The distinction between "elevated anthropomorphism" and "over-anthropomorphism" (Section 3.5) is subtle. Consider a clearer explanation of why the paper adopts descriptive rather than normative terminology.

### Technical

4. The existence proof (Theorem 1) covers signal-based and dispositional attribution but explicitly excludes behavioral attribution (Remark 1 in appendix). Since behavioral attribution---where attributed beliefs depend on observed AI behavior---seems empirically relevant, the paper should discuss when this extension might hold.

5. Proposition 10 (optimal AI design) derives comparative statics for prosocial, materialist, and mixed AI separately. The transition from prosocial to mixed to materialist design appears discontinuous (threshold-finding vs. marginal-balancing objectives). Is this discontinuity an artifact of the model or economically meaningful?

6. The cross-cultural implications (Section 5.7) are interesting but underdeveloped. The Karpus et al. (2025) finding that Japanese participants exhibit less attenuation toward robots suggests that optimal AI design varies across cultures. This has practical implications that could be expanded.

### Literature

7. The paper could engage more with the AI alignment literature. The phantom expectations problem---humans optimizing on attributed rather than actual AI objectives---parallels specification problems in AI safety. This connection is mentioned briefly but could be developed.

8. The discussion of behavioral game theory (Section 1) mentions quantal response equilibrium but does not compare ABE to other bounded rationality approaches. How does ABE relate to level-k thinking or cognitive hierarchy models in human-AI contexts?

### Applications

9. The trust game application positions AI as trustor rather than trustee, which is the more natural test of human trust in AI. While the design choice is justified (isolating attribution effects), the paper should discuss whether results extend to the reverse configuration.

10. The public goods application assumes binary contributions. Does the characterization extend to continuous contribution games? This seems relevant for many real-world public goods problems.

---

## Confidential Comments to Editor

**Recommendation:** Minor Revision

This paper makes a genuine contribution to game theory by extending psychological games to human-AI interaction. The framework is well-constructed, the technical execution is sound, and the welfare implications are novel and policy-relevant.

My main reservation is whether the contribution is sufficiently sharp. The paper introduces one new primitive (the attribution function) and otherwise inherits the structure of Battigalli-Dufwenberg psychological games. The three major comments above ask the author to better distinguish ABE from existing approaches and to strengthen the empirical foundations of the key mechanism (phantom expectations).

The paper is appropriate for Games and Economic Behavior. It combines theoretical rigor with timely application (human-AI interaction) and generates testable predictions. With revisions addressing the major comments, I would recommend acceptance.

**Strengths:**
- Novel and timely research question
- Clean theoretical framework with existence result
- Interesting welfare implications (phantom expectations)
- Well-grounded in empirical psychology literature

**Weaknesses:**
- Contribution relative to standard PGT could be sharper
- Phantom expectations mechanism needs more empirical grounding
- Paper length could be reduced

The author should be commended for a careful, well-written paper on an important topic. The revisions requested are substantial but feasible.
