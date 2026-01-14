# Referee Report: "Thinking about Machines: Attributed Belief Equilibrium"

**Journal:** Games and Economic Behavior

---

## Summary

This paper introduces Attributed Belief Equilibrium (ABE) to analyze strategic interactions between humans and artificial agents. The central innovation is the attribution function, which formalizes how humans project mental states (beliefs, expectations) onto AI agents that lack genuine mental states. The framework accommodates two empirically documented asymmetries: humans attribute beliefs to AI (anthropomorphism) while experiencing attenuated psychological responses toward AI (attenuation). The paper establishes existence under regularity conditions, proves that ABE nests standard equilibrium concepts as special cases (PNE, Nash, Bayes-Nash), and demonstrates that different attribution patterns sustain different equilibria in the same material game. Applications to trust games, public goods, and coordination illustrate how anthropomorphism affects equilibrium behavior. Welfare analysis reveals that anthropomorphism improves welfare with prosocial AI but may harm welfare with materialist AI through "phantom expectations"---attributed beliefs about expectations AI never held.

---

## Overall Assessment

This paper makes a genuine contribution to psychological game theory by extending the framework to asymmetric interactions where some players (AI) lack the mental states that drive psychological payoffs for others (humans). The attribution function is a conceptually clean solution to this asymmetry, and the paper demonstrates that it generates novel predictions beyond standard frameworks. The nesting results (Propositions 1-4) are technically sound and establish ABE as a proper generalization rather than an ad hoc modification. The multiplicity result (Proposition 5) and its implications for interface design are economically meaningful.

The paper is well-written with clear exposition of both the formal framework and its economic interpretation. The technical execution is careful, with assumptions clearly stated and proofs delegated appropriately to appendices. The connection to empirical evidence on anthropomorphism and mind perception strengthens the motivation.

My main concern is whether the contribution is sufficiently novel relative to existing psychological game theory. The existence proof follows standard fixed-point arguments, and many of the application results are qualitative extensions of known mechanisms (guilt aversion, indignation). The paper would benefit from sharper characterization of when ABE predictions diverge from standard approaches and from more concrete empirical predictions that could distinguish ABE from alternative models.

---

## Major Comments

### 1. Novelty Relative to Standard PGT

The paper establishes that ABE reduces to standard PGT when all players are human (Proposition 1) and to Nash when psychological payoffs vanish (Proposition 2). These nesting results are valuable but also raise a question: what is the marginal contribution beyond recognizing that AI players have different utility functions?

One could argue that standard PGT already accommodates heterogeneous players---simply model AI as having zero psychological sensitivity parameters. The attribution function adds structure, but it is not clear how much work it does beyond scaling psychological terms. The authors should clarify more precisely what ABE predicts that standard PGT with heterogeneous parameters cannot.

**Suggested revision:** Add a discussion (perhaps after the nesting results) that explicitly identifies a prediction or phenomenon that arises in ABE but not in PGT with heterogeneous players. The phantom expectations concept is promising here, but it needs sharper formalization of why this cannot be captured by standard guilt aversion with different belief specifications.

### 2. Attribution Function Specification

The attribution function is the key primitive, but the paper offers multiple specifications (behavioral, signal-based, dispositional) without resolving which applies where. The linear specification in Example 1 is tractable, but its empirical validity is assumed rather than established.

More importantly, the paper does not address how the attribution function would be identified in practice. Section 2.5.1 sketches an experimental design, but the regression equation (8) appears underidentified: $\beta_3$ captures the interaction between $\omega_i$ and $x_{At}$, but the structural parameters ($\eta$, $\rho_A$) are not separately identified without additional restrictions.

**Suggested revision:** Either provide a complete identification argument for the attribution function parameters, or acknowledge this as a limitation and discuss what experimental designs could achieve identification.

### 3. Welfare Claims and Phantom Expectations

The welfare analysis (Propositions 9-12) relies on the distinction between material and extended welfare. The phantom expectations argument is intuitive: with materialist AI, humans may experience guilt from disappointing expectations that AI never held. However, the welfare implications depend critically on whether psychological costs have "intrinsic" or "instrumental" value---a normative question the paper cannot resolve.

More substantively, the claim that phantom expectations cause welfare loss assumes humans cannot correct their attribution errors. The paper acknowledges this (Section 2.6.6, "Belief Revision") but does not formalize when correction should occur. If humans interact repeatedly with AI, shouldn't they learn that materialist AI holds no expectations?

**Suggested revision:** Add a discussion of learning and belief updating. Under what conditions would phantom expectations persist in the long run? This connects to the literature on learning in games and could strengthen the case for when ABE predictions apply.

---

## Minor Comments

1. **Definition 1 (Attributed Beliefs):** The notation $\tilde{h}_i^{(2,j)}$ is clear, but it would help to state explicitly that this is a belief in $\Delta(S_i)$ (about what AI expects human $i$ to do), not a belief about AI's strategy.

2. **Theorem 1 (Existence):** The proof sketch references Kakutani's theorem, which requires closed graph rather than upper hemicontinuity. The proof in the appendix correctly verifies the closed graph property, but the main text could be more precise.

3. **Proposition 5 (Multiplicity):** The conditions (i)-(iii) are generic, but the proposition does not characterize the multiplicity structure. Are there always exactly two equilibria? A continuum? This matters for the interpretation of interface design as an equilibrium selection device.

4. **Trust Game Application (Section 4.1):** The design positions AI as trustor and human as trustee, which is unusual. The rationale (isolating the attribution mechanism) is reasonable, but the authors should acknowledge that the more policy-relevant case---humans trusting AI---is not directly addressed.

5. **Public Goods Application (Section 4.2):** The claim that AI population share has "dual effects" operating through "distinct channels" is insightful but could be formalized more precisely. A diagram showing the material and psychological channels would aid comprehension.

6. **Cross-Cultural Variation (Section 5.7):** The reference to Karpus et al. (2025) on Japanese vs. Western participants is interesting but appears only briefly. Given the welfare implications for culture-dependent AI design, this deserves more discussion.

7. **Notation Consistency:** The paper uses both $h_i^{(2,k)}$ and $\tilde{h}_i^{(2,j)}$ for second-order beliefs. The distinction (genuine vs. attributed) is clear, but using different notation conventions (superscript ordering) creates unnecessary cognitive load.

8. **Assumption Table (Table 1):** This is helpful, but some assumptions (A2', A2'', A2''') are introduced without clear motivation. A brief explanation of why these extensions are needed would improve readability.

9. **Section 3.4 (Relationship Between Equilibrium Concepts):** This section clarifies the conceptual hierarchy but is somewhat repetitive of earlier material. Consider condensing.

10. **Conclusion:** The empirical agenda is promising but vague. The claim that ABE predicts $\beta_3 > 0$ while standard theory predicts $\beta_3 = 0$ needs more justification---what is the "standard theory" comparator, and why does it predict uniform effects?

---

## Confidential Comments to Editor

**Recommendation:** Minor Revision

This paper makes a solid contribution to psychological game theory by extending the framework to human-AI interactions. The attribution function is a sensible modeling device, and the paper demonstrates that it generates economically meaningful predictions. The technical execution is sound, and the writing is clear.

My hesitation about a stronger recommendation stems from questions about the marginal contribution. The nesting results are reassuring but also suggest that much of the analysis could be conducted within standard PGT with appropriate parameter choices. The paper would benefit from a sharper statement of what ABE adds beyond this.

The phantom expectations concept is the most novel contribution, but its welfare implications depend on unresolved normative questions about the status of psychological costs. The authors should either take a clearer position or acknowledge the ambiguity more explicitly.

I believe the paper can address these concerns with modest revisions and would be a suitable contribution to GEB after revision.
