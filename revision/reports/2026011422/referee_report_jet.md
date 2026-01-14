# Referee Report: "Thinking about Machines: Attributed Belief Equilibrium"

**Journal:** Journal of Economic Theory
**Date:** January 14, 2026

---

## Summary

This paper introduces Attributed Belief Equilibrium (ABE) to analyze strategic interaction between humans and artificial agents. The central innovation is the attribution function, which captures how humans project mental states onto AI agents that lack genuine beliefs. Humans experience belief-dependent preferences (guilt, indignation, reciprocity) while AI optimize design-dependent objectives. The paper establishes existence under regularity conditions, proves that ABE nests standard equilibrium concepts (Psychological Nash Equilibrium, Nash Equilibrium, Bayes-Nash Equilibrium) as special cases, demonstrates attribution-dependent multiplicity, and derives welfare implications for AI design. The main insight is that elevated anthropomorphism improves welfare with prosocial AI but reduces welfare with materialist AI through "phantom expectations."

## Overall Assessment

This is a well-crafted theoretical contribution that addresses a timely and important question: how should we model strategic interaction when one party attributes mental states to another party that lacks them? The paper makes a genuine contribution by extending psychological game theory to accommodate the fundamental asymmetry between humans and AI. The framework is technically sound, the nesting results are valuable for positioning the contribution, and the welfare analysis yields actionable design principles.

The main strengths are: (1) the conceptual clarity of the attribution function as the novel primitive, (2) the clean nesting results that show precisely when ABE departs from standard theory, and (3) the phantom expectations concept, which captures a distinctive welfare cost of human-AI interaction. The writing is direct and the economic content is clearly communicated.

However, several issues warrant attention before publication. The most significant concern is the empirical grounding of the attribution function---the paper's central primitive remains largely theoretically specified without guidance on how to calibrate it empirically. Additionally, some propositions make claims that require stronger conditions than stated, and the welfare analysis could be tightened.

## Major Comments (must address)

### 1. Empirical Identification of the Attribution Function

The attribution function $\phi_i$ is the paper's central innovation, yet its empirical content remains underspecified. Section 2.5.1 outlines an identification strategy, but several gaps remain:

- The linear specification $\tilde{h}_i^{(2,j)}(C) = \omega_i(\rho_j + \eta x_j)$ assumes AI prosociality $\rho_j$ is known to the econometrician. In practice, $\rho_j$ is a design choice that may be proprietary. How does one identify $\phi_i$ when AI objectives are opaque?

- The testable prediction $\beta_3 > 0$ (interaction between $\omega_i$ and $x_j$) is informative, but distinguishing attributed beliefs from rationalization requires careful design. Subjects may report beliefs that justify their actions post hoc. The paper should discuss how incentive-compatible elicitation addresses this concern.

- The paper should provide more guidance on which attribution specification (behavioral, signal-based, dispositional) applies in different contexts. The current treatment leaves this entirely to future empirical work.

**Required action:** Strengthen the discussion of empirical identification. Acknowledge limitations of the strategy method when subjects may rationalize. Discuss conditions under which each attribution specification is appropriate.

### 2. Proposition 5 Conditions Need Strengthening

Proposition 5 (Attribution-Dependent Multiplicity) states three conditions: (i) belief-dependent payoffs, (ii) distinct attributions, and (iii) best-response separation. However, condition (iii) is not a primitive assumption---it is an equilibrium property that depends on the payoff structure. The proposition effectively states: "If best responses differ, then equilibria differ." This is tautological unless condition (iii) is replaced with primitive conditions on payoffs.

**Required action:** Either (a) replace condition (iii) with verifiable conditions on payoffs and attribution functions that guarantee best-response separation, or (b) reframe the proposition as providing necessary and sufficient conditions for multiplicity (making the structure transparent).

### 3. Welfare Measure Selection Needs Justification

The paper uses material welfare $W$ in some propositions and extended welfare $W^{ext}$ in others. While Section 2.6 discusses the normative foundations, the actual choice in Propositions 9-12 appears ad hoc:

- Proposition 9 Part (i) uses material welfare; Parts (ii)-(iii) implicitly use extended welfare (since phantom guilt is the mechanism).
- Proposition 11 Part (i) uses material welfare; Parts (ii)-(iii) use extended welfare.

The Remark in OA.7.2 offers a reconciliation, but this should appear in the main text. The welfare criterion should be specified upfront in each proposition statement, with the choice justified.

**Required action:** State the welfare criterion explicitly in each proposition. Move the reconciliation discussion from the Online Appendix to the main text (perhaps as a subsection in Section 5.1).

### 4. Existence of Rational Attribution Equilibrium

Proposition 4 establishes existence of RAE under two conditions, but the second condition---"equilibrium-projecting attribution"---is essentially definitional. Condition (ii) states that $\phi_i$ outputs the optimal strategy, which defines rather than guarantees RAE existence. This needs clarification.

**Required action:** Clarify that condition (ii) is a fixed-point existence result, not a set of primitive assumptions. Discuss the economic plausibility of attribution functions satisfying this property.

## Minor Comments (suggestions for improvement)

### 1. Notation for Transfers vs. Signals

Remark 4.2 clarifies that the trust game involves two variables denoted by "$x$": monetary transfer and interface signal. This notation conflict is confusing and easily remedied. Consider using $t$ for the transfer amount and reserving $x$ for signals throughout.

### 2. Cross-Cultural Variation

The paper repeatedly cites Karpus et al. (2025) on cross-cultural variation in attenuation. This is an interesting empirical foundation, but the theoretical implications could be sharpened. Specifically: does the framework predict that optimal AI design should vary by cultural context? If so, this has implications for international AI governance that deserve brief discussion.

### 3. Dynamic Extensions

The Conclusion mentions dynamic extensions where anthropomorphism $\omega$ evolves through experience. This is important because the current framework treats $\omega$ as fixed. Even a brief sketch of how learning might be incorporated would strengthen the paper's claim to provide "foundations" for human-AI interaction.

### 4. Coordination Game Psychological Foundation

The expectation conformity mechanism in Section 4.3 is introduced somewhat abruptly. While the paper cites Cialdini (1998) for social norms, the connection to guilt and indignation from Definitions 4-5 could be tightened. Is expectation conformity a third psychological mechanism, or a special case of the existing ones?

### 5. Proposition 8 and Focal Points

Proposition 8 claims AI serves as a "focal point provider." However, the mechanism differs from Schelling focal points: here, coordination follows from psychological pressure (expectation conformity), not salience. The paper acknowledges this in a remark (OA.5.3), but the main text should distinguish these mechanisms more clearly.

### 6. Attenuation Parameters

The paper introduces $\lambda^{IND}$ and $\lambda^{GUILT}$ as separate attenuation parameters but treats them symmetrically in most analysis. Are there theoretical or empirical reasons to expect these to differ? The De Melo et al. (2017) and Bigman et al. (2023) citations suggest different psychological mechanisms (experience vs. agency attribution), which might predict different attenuation patterns.

### 7. Typo in Proposition 7

The conditions reference "(I) indignation dominance" but the displayed condition in Proposition 7 involves $\bar{\omega}_i \in [0,1]$ "under (I)." The relationship between (I) and the threshold should be clarified.

### 8. Table 1 Assumptions

Table 1 is helpful but could include column indicating which assumptions are standard (carry over from Battigalli-Dufwenberg) versus novel to ABE. This would sharpen the paper's marginal contribution.

---

## Confidential Comments to Editor

**Recommendation:** Major Revision

This paper makes a genuine theoretical contribution to the intersection of psychological game theory and human-AI interaction. The attribution function is a creative solution to the fundamental asymmetry problem, and the phantom expectations concept captures something economically important. The paper is well-written and technically competent.

My concerns center on: (1) the gap between the theoretical framework and empirical implementation, (2) some propositions that need tightened conditions, and (3) the welfare analysis that switches criteria without sufficient justification in the main text.

These issues are addressable in revision. The core contribution---ABE as an extension of psychological game theory---is sound and novel. With revisions addressing the major comments, this paper would be appropriate for JET.

The paper is ambitious in scope, covering existence, nesting, multiplicity, applications, and welfare in a single manuscript. The authors have handled this well by deferring technical details to the Online Appendix. However, some material from OA (particularly the welfare criterion discussion) should migrate to the main text.

I recommend major revision with particular attention to Major Comments 1-3. If the authors can strengthen the empirical identification discussion and tighten the proposition conditions, the paper will make a valuable contribution to the literature on human-AI strategic interaction.
