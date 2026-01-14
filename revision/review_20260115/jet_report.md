# Referee Report: "Thinking for Machines: Attributed Belief Equilibrium"

**Journal of Economic Theory**

---

## Summary

This paper introduces Attributed Belief Equilibrium (ABE) to analyze strategic interaction between humans and artificial agents. The central innovation addresses a dual asymmetry: humans have belief-dependent preferences (guilt, reciprocity, indignation) while AI agents have design-dependent objectives without genuine mental states. Standard psychological game theory cannot accommodate this heterogeneity because it assumes symmetric belief-dependent preferences. ABE resolves this through an "attribution function" that formalizes how humans project mental states onto AI agents. The paper establishes existence under regularity conditions, shows that ABE nests standard frameworks (PNE, Nash, Bayes-Nash) as special cases, demonstrates that different attribution patterns sustain different equilibria, and derives welfare implications distinguishing prosocial from materialist AI design.

## Overall Assessment

This is a theoretically ambitious paper that addresses an important and timely question: how should game theory accommodate the growing presence of AI agents in strategic interactions? The core insight---that humans attribute mental states to AI through anthropomorphism, and these attributed beliefs trigger psychological payoffs---is both empirically grounded and theoretically novel. The paper makes a genuine contribution to psychological game theory by introducing asymmetric player types with distinct consistency requirements for beliefs.

The paper is well-executed technically. The existence proof is clean, the nesting results establish ABE as a proper generalization rather than an ad hoc construction, and the welfare analysis yields sharp, policy-relevant implications. The distinction between material and extended welfare, and the conditions under which they diverge, is particularly well-developed.

My main concerns are: (1) the empirical content of the attribution function remains underspecified despite the extensive discussion of testability, (2) the welfare analysis depends heavily on functional form assumptions that are not well-motivated beyond tractability, and (3) the paper would benefit from more direct engagement with the mechanism design literature on implementation.

## Major Comments

### 1. The Attribution Function Requires Sharper Identification

The attribution function $\phi_i(\theta_j, x_j, \omega_i)$ is the key primitive distinguishing ABE from standard theory. Yet its empirical content remains unclear. The paper presents three approaches (behavioral, signal-based, dispositional) but does not commit to one or derive conditions under which they can be distinguished empirically.

The linear specification in Example 1 is adopted for tractability, but the claim that "mind perception research finds monotonic relationships between anthropomorphism and attributed mental states---linearity captures this without untested curvature" (p. 16) understates the issue. Linearity is a strong functional form assumption; monotonicity is consistent with many non-linear specifications including the logistic and threshold models mentioned later.

**Suggestion**: The paper should either (a) provide conditions under which different attribution specifications generate observationally distinct predictions, or (b) explicitly characterize the class of attribution functions for which the main results hold. The current treatment switches between general $\phi_i$ and the linear specification without clear guidance on which results depend on which.

### 2. Welfare Measure Selection and the Extended Welfare Concept

The paper introduces two welfare measures: material welfare $W$ and extended welfare $W^{ext}$ that incorporates psychological payoffs. The distinction is conceptually important, but the paper's treatment raises two concerns.

First, the normative justification in Section 2.7 is incomplete. The "intrinsic vs. instrumental" framing suggests these are alternative philosophical positions, but the paper does not acknowledge that extended welfare including guilt toward AI raises novel welfare-theoretic questions. If AI lacks genuine mental states, should guilt from failing to meet phantom expectations count in social welfare? This is not merely a prior normative position but a question the paper's framework makes salient.

Second, the divergence between $W$ and $W^{ext}$ (Corollary 3) depends on phantom expectations exceeding feasible returns. This is an extreme case. The paper would benefit from characterizing when the two measures agree more systematically, beyond the sufficient conditions in Corollary 2.

**Suggestion**: Add discussion of the welfare-theoretic status of guilt toward non-conscious agents, and provide tighter characterization of when welfare measures agree versus diverge.

### 3. The "Phantom Expectations" Mechanism Needs Stronger Empirical Grounding

The phantom expectations result (Proposition 9, Part 2) is central to the policy implications. Yet the mechanism requires a specific configuration: (i) materialist AI ($\rho_A = 0$), (ii) elevated anthropomorphism such that attributed expectations exceed feasibility, and (iii) positive guilt sensitivity.

The empirical evidence cited (De Melo et al. 2017, Karpus et al. 2025) establishes that guilt toward AI is attenuated, which works against the phantom expectations mechanism. The paper acknowledges this tension ("attenuation cuts both ways") but does not quantify when phantom expectations are likely to arise empirically.

**Suggestion**: Provide conditions on the magnitude of anthropomorphism $\omega$ and attenuation $\lambda^{GUILT}$ under which phantom expectations have material welfare consequences. The current existence result is too weak for policy guidance.

## Minor Comments

### 4. Notation for Transfer vs. Signal

In the trust game, $x$ denotes both the monetary transfer and (implicitly in the attribution function) the signal. While Remark 4 acknowledges this, using the same letter creates confusion when reading the proofs. Consider using $\tau$ or $t$ for the transfer to distinguish from the signal $x_j$.

### 5. RAE Existence Conditions

Proposition 5 provides two sufficient conditions for Rational Attribution Equilibrium existence: unique Nash benchmark, or equilibrium-projecting attribution. The second condition is nearly tautological (attribution projects equilibrium if the attribution function is defined to do so). More substantive existence conditions would strengthen the result.

### 6. Cross-Cultural Variation

The paper repeatedly invokes Karpus et al. (2025) on Japanese vs. Western attenuation. This is a single study with limited sample composition information. The policy implications (culture-dependent optimal design, international regulatory coordination) may be premature given the thin empirical base.

### 7. Connection to Mechanism Design

The paper briefly mentions that "optimal presentation can be viewed as a mechanism design problem" (p. 53) but does not develop this. The connection is natural: the AI designer chooses signals $x_j$ to implement desired outcomes subject to incentive constraints from attributed beliefs. Engaging more directly with the implementation literature would strengthen the design results.

### 8. Behavioral Attribution Extension

Remark A.1 conjectures that existence extends to behavioral attribution under assumption (A2'). Since behavioral attribution creates equilibrium feedback (attributed beliefs depend on AI strategies), this extension is non-trivial. The paper should either prove this or clarify that the current results apply only to exogenous attribution.

### 9. Proof of Proposition 4 (Multiplicity)

The proposition states three generic conditions but the proof in the appendix consists mainly of numerical examples. While the examples are illustrative, a formal proof that conditions (i)-(iii) generically hold would strengthen the claim that "attribution-dependent multiplicity is the typical outcome."

### 10. Minor Typos and Presentation

- p. 7: "behavioural cues" uses British spelling inconsistently with American English elsewhere
- Table 1: The distinction between (G) and (G') could be clarified earlier in the text
- The paper is long (55+ pages with appendix); some proofs could be shortened without loss

---

## Confidential Comments to Editor

**Recommendation: Minor Revision**

This paper makes a genuine theoretical contribution to an important topic. The ABE framework is novel, technically sound, and addresses a real gap in the literature: standard psychological game theory assumes symmetric belief-dependent preferences and cannot accommodate human-AI interactions where only humans have psychological payoffs.

The existence theorem is correctly proved, the nesting results are valuable for positioning ABE within the literature, and the welfare analysis yields non-obvious implications. The distinction between prosocial and materialist AI---and the asymmetric welfare effects of anthropomorphism---is the paper's most policy-relevant contribution.

My concerns are about exposition and empirical grounding rather than technical correctness. The attribution function is the key primitive but remains underspecified. The welfare analysis is sensitive to functional form assumptions. The policy implications about optimal AI design depend on magnitudes (how much anthropomorphism, how much attenuation) that the paper does not pin down.

I recommend minor revision with attention to:
1. Sharper characterization of when results depend on specific functional forms vs. general properties
2. Acknowledgment of the welfare-theoretic novelty of counting guilt toward non-conscious agents
3. Tighter empirical grounding for the phantom expectations mechanism

The paper would be strengthened by these revisions but is already a substantial contribution suitable for JET.
