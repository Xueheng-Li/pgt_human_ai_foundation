# Referee Report: "Thinking about Machines: Attributed Belief Equilibrium"

**Manuscript submitted to Econometrica**

---

## Summary

This paper introduces Attributed Belief Equilibrium (ABE) to analyze strategic interaction between humans and AI agents. The central innovation is the "attribution function," which captures how humans project mental states onto AI agents that lack genuine beliefs. The framework accommodates asymmetric player types: humans with belief-dependent preferences (guilt, indignation, reciprocity) and AI with design-dependent objectives. The paper establishes existence under regularity conditions, proves that ABE nests standard equilibrium concepts as special cases, and demonstrates that different attribution patterns sustain different equilibria in the same material game. Applications to trust games, public goods, and coordination generate testable predictions. The welfare analysis reveals an asymmetry: elevated anthropomorphism improves welfare with prosocial AI but reduces welfare with materialist AI through "phantom expectations"---attributed beliefs about expectations AI never held.

## Overall Assessment

This is a well-executed theoretical paper addressing a genuinely important question: how should game theory accommodate the fundamental asymmetry between human belief-dependent preferences and AI design-dependent objectives? The contribution is timely and potentially significant. As AI agents become increasingly prevalent in economic and social interactions, standard psychological game theory cannot accommodate the heterogeneity between agents with genuine mental states and those without.

The paper's main strength is its clean conceptual architecture. The attribution function is a natural primitive that captures an empirically established phenomenon (anthropomorphism) and generates economically meaningful predictions. The nesting results (Propositions 1-3) establish ABE as a genuine generalization rather than a separate theory. The welfare analysis identifying "phantom expectations" as a distinct mechanism is conceptually sharp and policy-relevant.

The paper's main weakness is the gap between theoretical generality and empirical traction. While the framework is flexible, the applications rely on specific functional forms (linear attribution, binary strategies) whose empirical validity remains untested. The distinction between "exogenous" and "behavioral" attribution is theoretically clean but the paper does not provide guidance on which specification is appropriate in which contexts.

## Major Comments

### 1. The attribution function requires stronger empirical grounding

The attribution function is the central primitive distinguishing ABE from standard game theory, yet its empirical content remains largely assumed. Section 2.5.1 describes an identification strategy using incentivized belief elicitation, but this is a proposal, not evidence. The paper would be strengthened by:

(a) Citing existing experimental evidence that directly supports the functional form assumptions. The current citations (Blut et al. 2021, Waytz et al. 2014) establish that anthropomorphism affects trust but do not validate the specific linear specification.

(b) Discussing what experimental patterns would falsify the model. For instance, if attributed beliefs do not respond to interface manipulation as predicted (beta_3 = 0 in equation 7), what would this imply?

(c) Clarifying whether the attribution function is identified separately from the psychological payoff parameters. The regression in equation (7) assumes knowledge of guilt sensitivity; joint identification may require additional instruments.

### 2. The relationship between exogenous and behavioral attribution needs clarification

The paper distinguishes exogenous attribution (signal-based or dispositional) from behavioral attribution (depending on observed AI behavior). Theorem 1 establishes existence under both specifications, and Remark 5 states that applications use exogenous attribution. However:

(a) The conceptual distinction is unclear. If AI behavior is observable, why would humans form expectations based only on interface features (exogenous) rather than actual behavior (behavioral)? The paper should provide economic reasoning for when each specification applies.

(b) Under behavioral attribution, the existence proof (Online Appendix OA.1.3) requires "own-strategy independence"---that attributed beliefs depend only on AI strategy, not on the human's own strategy. This seems restrictive: a human might attribute different expectations to an AI depending on what the human has done. The paper should discuss whether this restriction is empirically plausible.

### 3. The welfare analysis conflates descriptive and normative claims

The paper defines "zero-anthropomorphism benchmark" as a descriptive concept (attributed beliefs when omega_i = 0) but then uses it normatively in the welfare analysis. Several issues arise:

(a) Why is omega_i = 0 the appropriate benchmark? The paper states this is "descriptive, not normative" (Definition 3), but the welfare propositions treat deviations from this benchmark as welfare-relevant. If anthropomorphism is a stable psychological trait, forcing omega_i = 0 may not be a feasible policy option.

(b) The extended welfare measure includes psychological payoffs as intrinsically valuable, but phantom guilt arises precisely because humans misattribute expectations. Should welfare count psychological costs based on incorrect beliefs? The paper acknowledges this tension (Section 2.6.2) but does not resolve it.

(c) The policy recommendations (minimal anthropomorphic signaling for materialist AI) assume designers can control attributed beliefs through interface choice. But if attribution is primarily dispositional (driven by omega_i), signal manipulation may have limited effect. The paper should discuss heterogeneity in attribution sources and its policy implications.

### 4. The proof of Proposition 5 (multiplicity) is too abbreviated

Proposition 5 is central to the paper's claim that ABE generates new predictions. The proof sketch (three steps, each one sentence) does not establish the result rigorously. Specifically:

(a) Condition (iii) "best-response separation" is assumed, not derived. The proposition should provide sufficient conditions under which payoff changes from different attributed beliefs actually shift equilibrium strategies.

(b) The numerical examples following the proposition are helpful but do not constitute proof. The Online Appendix (OA.2.4) restates the conditions but does not verify them for a general class of games.

(c) A comparison with multiplicity in standard PGT would clarify the paper's contribution. In standard PGT, multiplicity arises from feedback between strategies and beliefs. In ABE, multiplicity arises from exogenous variation in the attribution function. The paper should characterize when ABE multiplicity is "larger" or "different" from standard PGT multiplicity.

## Minor Comments

### Presentation and Exposition

1. The notation switches between indexed subscripts (i, j, k) and named subscripts (H, A) without consistent convention. The remark in Section 4 helps but a clearer convention throughout would improve readability.

2. The phrase "phantom expectations" is evocative but potentially misleading. These are real expectations (held by humans) about phantom mental states (not held by AI). Consider "ungrounded expectations" or "misattributed expectations" to avoid suggesting the expectations themselves are illusory.

3. Table 1 (assumption summary) is helpful but appears late in Section 2. Consider moving it earlier or providing a roadmap at the section's start.

4. The paper uses both "elevated anthropomorphism" and "over-anthropomorphism" (in proof file names). Standardize terminology.

### Technical Points

5. Definition 1 (Attributed Beliefs): The notation tilde{h}_i^{(2,j)} is introduced as "what human i believes AI j expected human i to do." This is a second-order attributed belief. The paper should clarify why higher-order attributed beliefs (what human i believes AI j believes human k expects...) are not considered. The conclusion acknowledges this limitation but does not explain why the restriction is without loss for the applications.

6. Assumption A3 (Bounded Psychological Payoffs): Lemma A.1 in the Online Appendix shows this is implied by A1-A2, making it redundant. The main text should note this to avoid the impression that three independent conditions are required.

7. Proposition 4 (RAE Existence): Condition (ii) "equilibrium-projecting attribution" essentially assumes the conclusion. The proposition would be more informative if it provided primitive conditions on the game structure under which equilibrium-projecting attribution exists.

8. Proposition 6 (Trust Game): The condition G > 1 ("guilt dominance") is strong. Remark OA.5.1.2 in the Online Appendix discusses the knife-edge case G = 1 and the regime G < 1. These boundary cases should be mentioned in the main text since they affect the generality of the result.

9. Proposition 7 (Public Goods): The binary contribution specification (c_i in {0, E}) is restrictive. The paper should discuss whether the results extend to continuous contributions and, if so, under what conditions.

10. The coordination game application (Proposition 8) introduces "expectation conformity" as a third psychological mechanism beyond guilt and indignation. This mechanism is not formally defined in Section 2. Consider adding a definition parallel to Definitions 4-5, or explain how expectation conformity maps to existing definitions.

### Literature and Framing

11. The related literature section could better position the paper relative to Charness and Dufwenberg (2006) on guilt aversion and Battigalli et al. (2022) on belief-dependent motivations. The current framing emphasizes what ABE adds (attributed beliefs about AI) but underemphasizes what it inherits (the psychological payoff structure).

12. The paper claims ABE "nests" standard PGT, but Proposition 1 shows equivalence only for static games. The extension to dynamic games (following Battigalli and Dufwenberg 2009) would strengthen the nesting claim. If this extension is straightforward, it should be stated; if not, the limitation should be acknowledged.

13. The connection to "theory of mind" literature in cognitive science could be strengthened. The attribution function formalizes how humans model AI mental states; the theory of mind literature provides rich evidence on how humans (mis)model other humans' mental states. This connection would help ground the attribution function in established psychology.

### Specific Corrections

14. Equation (3) in Section 2.3: The notation h_i^{(2,k)} in Delta(Delta(S_{-k})) suggests second-order beliefs are distributions over distributions. But the subsequent text treats h_i^{(2,k)}(C) as a probability. Clarify whether h_i^{(2,k)} is a point belief or a distribution over beliefs.

15. Section 4.1 (Trust Game): The remark on "transfer vs. signal" notation helps but comes late. Consider distinguishing variables x (transfer) and x_A (signal) from first introduction.

16. The bibliography mixes citation styles. Some entries use APA format; others use journal-specific conventions. Standardize for Econometrica submission.

---

## Confidential Comments to Editor

**Recommendation: Major Revision**

This paper makes a genuine contribution to game theory by providing a framework for analyzing human-AI interaction that accommodates the fundamental asymmetry between human psychology and AI design. The research question is important and timely, the theoretical framework is coherent, and the welfare implications are policy-relevant.

However, the paper is not yet ready for publication in Econometrica. The major issues are:

1. **Empirical grounding**: The attribution function is the paper's key innovation, but its empirical content is largely assumed. Econometrica readers will expect either direct empirical evidence or a clearer path to falsification.

2. **Incomplete proofs**: Proposition 5 on multiplicity is central to the paper's contribution but inadequately proved. The Online Appendix provides additional detail but still relies on assumed conditions rather than derived results.

3. **Normative ambiguity**: The welfare analysis conflates descriptive benchmarks with normative judgments in ways that require clarification.

These issues are addressable through revision. The paper's conceptual architecture is sound, and the applications demonstrate the framework's potential. With stronger empirical grounding and more complete proofs, this paper could make a significant contribution.

The paper would benefit from the authors addressing whether any experimental evidence (existing or planned) can validate the attribution function's properties, and from providing a more rigorous treatment of the multiplicity result. The welfare analysis should more carefully distinguish between feasible policy interventions (changing AI presentation) and infeasible ones (changing human anthropomorphism tendencies).
