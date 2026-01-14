# Referee Report: "Thinking about Machines: Attributed Belief Equilibrium"

**Journal**: Journal of Economic Theory
**Manuscript**: Attributed Belief Equilibrium in Human-AI Games
**Date**: January 14, 2026

---

## Summary

This paper introduces Attributed Belief Equilibrium (ABE) to analyze strategic interactions between humans and artificial agents. The central innovation is the attribution function, which captures how humans project mental states---beliefs, intentions, expectations---onto AI agents that lack genuine mental states. Humans experience guilt from disappointing these attributed expectations and indignation from perceived violations, even when the AI holds no actual expectations. The paper establishes existence under regularity conditions, proves that ABE nests standard psychological game theory and Nash equilibrium as special cases, and demonstrates that different attribution patterns sustain different equilibria. Applications to trust games, public goods, and coordination games generate testable predictions. The welfare analysis reveals an asymmetry: anthropomorphism improves welfare with prosocial AI by inducing cooperation but reduces welfare with materialist AI through "phantom expectations"---attributed beliefs that impose guilt costs without corresponding AI preferences.

## Overall Assessment

This paper makes a genuine contribution to economic theory by extending psychological game theory to human-AI interaction. The core insight---that humans attribute mental states to AI through anthropomorphism, and these attributed beliefs enter utility through standard psychological mechanisms---is economically substantive and empirically grounded in psychology literature. The framework is technically sound, the exposition is clear, and the welfare implications for AI design are policy-relevant.

The main strength is conceptual: the paper identifies a real economic phenomenon (humans treating AI as if it had beliefs) and provides rigorous tools to analyze it. The attribution function is a well-motivated primitive that connects psychological research on mind perception to game-theoretic analysis. The nesting results (Propositions 1-3) establish that ABE is a proper generalization rather than a separate theory, which strengthens its claim to theoretical importance.

The main limitation is empirical: the attribution function is the key novel primitive, but its empirical content remains largely unspecified. The paper acknowledges this (Section 2.5.1 provides an identification strategy; the conclusion notes that "experimental work measuring how attributed beliefs respond to AI design features would enable calibration"), but without empirical grounding, the framework's predictive power depends on functional form assumptions (e.g., linearity) that are convenient rather than tested.

## Major Comments

1. **Tighten the existence proof's reliance on exogenous attribution.** The existence theorem (Theorem 1) relies crucially on attributed beliefs being "exogenous" in the sense that they do not depend on equilibrium strategies (Step 2 of the proof: "attributed beliefs do not create additional equilibrium conditions"). This is appropriate for signal-based or dispositional attribution but breaks down for behavioral attribution, where $\phi_i$ depends on observed AI behavior. The paper mentions this issue in the Online Appendix (referenced in the proof) but should clarify in the main text which class of attribution functions the existence result covers. If behavioral attribution requires a different argument, state this explicitly.

2. **Clarify the welfare comparison across measures.** Propositions 9-10 and 11-12 switch between material welfare $W$ and extended welfare $W^{ext}$ across different parts. The paper discusses when these measures agree (Corollary 2) and diverge (Corollary 3), but the normative status of each remains ambiguous. The intrinsic/instrumental distinction (Section 2.6.1) is helpful, but the paper should take a clearer position on which measure is appropriate for policy analysis. The current treatment risks leaving readers uncertain about the paper's normative claims.

3. **Strengthen the connection to testable predictions.** Section 2.5.1 outlines an experimental design and derives testable restrictions ($\beta_2 = 0$, $\beta_3 > 0$ in regression equation 11). This is valuable, but the predictions are quite specific to the linear attribution specification. The paper should discuss robustness: which predictions survive under alternative functional forms (logistic, threshold)? If different specifications yield different predictions, what distinguishes them empirically?

## Minor Comments

1. **Notation for transfer vs. signal.** Remark 4.2 clarifies that $x$ denotes monetary transfer in the trust game while $x_j$ denotes anthropomorphic signals in the attribution function. This creates potential confusion since both appear in Section 4. Consider using distinct notation (e.g., $t$ for transfer) throughout the applications.

2. **Rational Attribution Equilibrium existence conditions.** Proposition 4 states that RAE exists under two alternative conditions, but Remark 3.4 notes that RAE need not exist in general. The paper could more clearly characterize when RAE fails---beyond the example of pure-strategy attribution with mixed equilibria---to help readers understand the scope of this refinement.

3. **Cross-cultural variation.** The paper repeatedly cites Karpus et al. (2025) for cross-cultural differences in attenuation. This is appropriate, but the paper relies heavily on a single empirical source. If other evidence supports cross-cultural variation in anthropomorphism or attenuation, citing it would strengthen the empirical foundation.

4. **Assumption table.** Table 1 provides a helpful summary of assumptions, but some labels are used inconsistently. For example, (G) and (G') appear in different propositions with different thresholds ($G > 1$ vs. $G > 0$). A brief explanation in the table of why different thresholds apply in different contexts would aid readers.

5. **Phantom expectations terminology.** The term "phantom expectations" is evocative and appears throughout the welfare analysis. Consider defining it formally (as in Example 2.2) earlier in the paper, perhaps in Section 2.4 where attributed beliefs are introduced, to establish the concept before its welfare implications are analyzed.

6. **Public goods application.** Proposition 7 uses binary contributions ($c_i \in \{0, E\}$), which simplifies the analysis but limits applicability. The remark preceding Proposition 9 notes that results extend to continuous strategies. Consider adding a brief discussion of whether the qualitative predictions (dual channels, attenuation-dependent net effect) survive with interior contributions.

7. **Typo in Section 3.4.** The heading "Illustrative Examples" appears after Proposition 5 but is not numbered as a subsection. Either number it or integrate the examples into the proposition's discussion.

---

## Confidential Comments to Editor

**Recommendation**: Minor Revision

This paper makes a solid contribution to economic theory by extending psychological game theory to human-AI interaction. The core conceptual innovation---the attribution function capturing how humans project beliefs onto AI---is well-motivated by psychology literature and generates economically interesting predictions. The existence theorem is correctly proved, the nesting results establish theoretical coherence, and the welfare analysis yields clear design implications.

The paper is suitable for JET. The topic is timely given the proliferation of AI in economic contexts, and the framework provides tools that other researchers can apply. The main concerns (exogeneity assumption in existence proof, normative status of welfare measures, robustness of empirical predictions) are addressable through clarification rather than fundamental revision.

The writing is clear and the paper is well-organized. The mathematical exposition is rigorous without being unnecessarily technical. I recommend acceptance conditional on addressing the major comments, which should require modest revision.
