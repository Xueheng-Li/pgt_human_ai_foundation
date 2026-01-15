# Referee Report: Attributed Belief Equilibrium: Psychological Games between Humans and AI

**Journal**: Econometrica
**Manuscript**: "Attributed Belief Equilibrium: Psychological Games between Humans and AI"
**Date**: January 15, 2026

---

## Summary

This paper extends psychological game theory (PGT) to mixed human-AI strategic interactions. The central innovation is the *attribution function*, which captures how humans project mental states onto AI agents that lack genuine beliefs. Humans form "attributed beliefs" about AI expectations, and these beliefs trigger guilt, indignation, and reciprocity through standard psychological mechanisms. The paper establishes existence of Attributed Belief Equilibrium (ABE) under regularity conditions, proves that ABE nests standard PGT and Nash equilibrium as special cases, and demonstrates attribution-dependent equilibrium multiplicity. Applications to trust games, public goods, and coordination illustrate how AI interface design serves as an equilibrium selection device. A welfare analysis shows that anthropomorphism improves outcomes with prosocial AI but creates "phantom expectations"---and associated guilt---with materialist AI, generating design principles for AI presentation.

---

## Overall Assessment

This paper makes a substantive contribution to economic theory by providing equilibrium foundations for human-AI strategic interaction. The core insight---that humans attribute beliefs to AI agents, and these attributed beliefs enter utility through established psychological mechanisms---is both conceptually elegant and empirically grounded. The attribution function is a well-motivated primitive that bridges mind perception psychology and game theory.

The paper's main strengths are: (1) the conceptual clarity of separating genuine beliefs (about humans) from attributed beliefs (about AI), (2) the nesting results that position ABE as a proper generalization of existing frameworks, (3) the feed-forward multiplicity mechanism that differs structurally from standard PGT multiplicity, and (4) the policy-relevant welfare analysis distinguishing prosocial from materialist AI.

The main concern is that the paper's value depends heavily on the empirical content of the attribution function. While Section 2.5.1 provides a thoughtful identification strategy, the attribution function remains a theoretical primitive whose properties are assumed rather than derived. The paper would benefit from more explicit acknowledgment of which predictions are robust to alternative specifications and which depend on specific functional forms.

A secondary concern is scope: the paper attempts to cover existence, nesting, multiplicity, three applications, welfare analysis, and design principles. Each component is competently executed, but some sections feel compressed. The proofs are appropriately concise (with details relegated to an Online Appendix), but the applications could benefit from deeper development.

Overall, this is a well-crafted theory paper that opens a new research direction. The contribution is genuine: existing PGT cannot handle the asymmetric player types that characterize human-AI interaction, and the proposed solution is both tractable and insightful.

---

## Major Comments

### 1. The Attribution Function Requires Sharper Economic Foundations

The attribution function $\phi_i$ is the key primitive distinguishing ABE from standard game theory. The paper grounds it in mind perception psychology (SEEK framework, gray's agency/experience dimensions), which is appropriate. However, the economic foundations could be strengthened.

Currently, the paper presents three specifications (behavioral, signal-based, dispositional) as "complementary modeling choices" without providing criteria for when each applies beyond the experimental design context. From an economic perspective, we need to understand:

- What determines $\phi_i$ in non-experimental settings?
- Is attribution subject to equilibrium forces (learning, selection)?
- Can designers manipulate $\phi_i$ directly, or only through signals $x_j$?

The paper acknowledges in the conclusion that "the attribution function is the key primitive...yet its empirical content remains to be established." This is appropriate humility, but the paper should be more explicit about which results are robust to alternative specifications. For example, Proposition 5 (multiplicity) holds generically---this is a strength. But the welfare results depend on monotonicity assumptions (A2') that may or may not hold empirically.

**Suggestion**: Add a subsection explicitly characterizing the testable restrictions of ABE. What patterns of behavior are consistent with ABE but not with alternative theories? The interaction effect $\beta_3 > 0$ is a good start, but additional sharp predictions would strengthen the paper's empirical content.

### 2. The Rational Attribution Equilibrium Concept Needs Clarification

The paper introduces RAE (Definition 5) as a refinement where attributed beliefs equal equilibrium strategies. This is a useful benchmark, but its role in the paper is unclear.

RAE is motivated by analogy to rational expectations, but the analogy is imperfect. In macroeconomics, rational expectations hold in equilibrium because agents have correct beliefs about the model. In ABE, attributed beliefs are about AI mental states that *do not exist*. How should we interpret "correct" beliefs about non-existent objects?

The paper notes that RAE need not exist (Remark 8) and that it reduces to Bayes-Nash equilibrium (Proposition 3). This raises the question: what is the value-added of RAE over simply noting that ABE reduces to BNE when attribution happens to project equilibrium play?

**Suggestion**: Either develop RAE more fully (when does it arise? through what mechanism?) or downplay it as a technical condition rather than a separate equilibrium concept.

### 3. The Welfare Analysis Should Address Heterogeneity More Directly

The welfare results (Propositions 9-12) assume a representative agent with common $\omega$ and $\lambda$ parameters. This simplification enables clear comparative statics but obscures an important issue: welfare effects depend on the joint distribution of anthropomorphism and AI exposure.

Consider a population with heterogeneous $\omega_i$ interacting with a mix of prosocial and materialist AI. The paper's analysis suggests that high-$\omega$ individuals benefit from prosocial AI but are harmed by materialist AI. But if high-$\omega$ individuals also self-select into more frequent AI interaction, the welfare calculation becomes more complex.

The cross-cultural discussion (Section 5.6) gestures at this issue but does not analyze it formally. Since the policy implications (transparency regulation, anthropomorphism limits) depend on population-level welfare effects, this gap is consequential.

**Suggestion**: Extend Propositions 10-12 to allow for heterogeneous $\omega_i$, at least in a simple two-type model. Characterize when aggregate welfare increases with anthropomorphism and when it decreases.

---

## Minor Comments

### Clarity and Exposition

1. **Notation consistency**: The paper uses both $h_i^{(2,k)}$ and $\tilde{h}_i^{(2,j)}$ for second-order beliefs, distinguished by genuine vs. attributed. This is logical but creates visual clutter. Consider using distinct base letters (e.g., $b$ for genuine beliefs, $a$ for attributed) to reduce reader burden.

2. **Definition 1 (Attributed Beliefs)**: The definition introduces $x_j$ as "observable interface signals" but the examples in Section 2.4 (voice, gaze, movement) suggest these are features, not signals in the game-theoretic sense. Remark 2 clarifies this, but the clarification comes late. Consider noting immediately that $x_j$ are design features, not strategic choices.

3. **Example 1 (Linear Attribution)**: The multiplicative structure---$\omega_i$ multiplying $(\rho_j + \eta x_j)$---is well-motivated but the economic interpretation could be clearer. Does this mean that individuals with $\omega_i = 0$ attribute zero expectations regardless of AI design? This seems extreme. Perhaps discuss whether a floor effect ($\phi_i \geq \underline{h}$ for all $\omega_i$) would change the results.

4. **Table 1 (Attribution Specification Selection Guide)**: Useful but somewhat disconnected from the formal analysis. The applications all use exogenous attribution (Remark 3), so the behavioral specification receives limited development. Either drop behavioral attribution from Table 1 or add an application that uses it.

5. **Proposition 5 (Multiplicity)**: The proposition states conditions under which different attribution functions yield different equilibria. The examples are helpful, but the general conditions (i)-(iii) are somewhat tautological: "if attributed beliefs differ and this changes utilities and best responses, then equilibria differ." A sharper statement would characterize when multiplicity is *strict* (not just weak).

### Technical Issues

6. **Theorem 1 (Existence)**: The proof sketch is clear. However, the extension to behavioral attribution (A2-beh) deserves more discussion. The own-strategy independence condition---$\phi_i^{beh}$ depends only on $\sigma_j$, not $\sigma_i$---rules out cases where humans attribute beliefs based on joint outcomes. Is this restrictive? When might it fail?

7. **Proposition 3 (Rational Attribution)**: The construction of the equivalent Bayesian game $\Gamma^B$ is relegated to the Appendix. Given the importance of this nesting result for positioning ABE relative to standard theory, a brief sketch in the main text would be helpful.

8. **Proposition 7 (Public Goods)**: The binary contribution assumption ($c_i \in \{0, E\}$) simplifies the analysis but may not be innocuous. With continuous contributions, interior equilibria could arise, and the comparative statics (Part iii on AI population share) might differ. A remark on robustness would be appropriate.

9. **Welfare Measure Choice**: The paper carefully distinguishes material welfare $W$ from extended welfare $W^{ext}$ but ultimately uses both without recommending one. For policy purposes, this ambiguity is problematic. Consider taking a stance, or at least noting which conclusions hold under both measures and which depend on the choice.

10. **Phantom Expectations (Example 3)**: The concept is vivid and important. However, the example assumes that phantom expectations can exceed feasible returns indefinitely. In practice, would humans revise attributed beliefs after repeated disappointment? The paper acknowledges this ("Belief Revision" paragraph in Section 2.6.2) but the argument for persistent phantom expectations (System 1/System 2 dual process) is asserted rather than derived.

### Literature

11. The paper cites Battigalli et al. (2019) for incorporating belief-dependent motivation but does not engage with the specific technical apparatus (belief hierarchies, coherent plans). A brief discussion of how ABE relates to the Battigalli-Dufwenberg framework would strengthen the literature positioning.

12. The connection to behavioral mechanism design (e.g., Koszegi and Rabin on expectations-based reference dependence) is not explored. Attributed expectations could serve as reference points, generating an alternative channel for belief-dependent payoffs.

### Minor Typos and Formatting

13. Page 1, abstract: "analyse" appears twice (British spelling) but the paper otherwise uses American spelling. Standardize.

14. Section 2.5.1, Equation 7: The regression specification includes $\beta_0, \beta_1, \beta_2, \beta_3$ which could be confused with the indignation sensitivity parameter $\beta_i$ introduced earlier. Consider renaming the regression coefficients.

15. Proposition 11, Part (i): The condition (T) "temptation dominance" is stated but not defined in the table of assumptions until after it is used. Reorder or add forward reference.

---

## Confidential Comments to Editor

**Recommendation**: Major Revision

This paper addresses an important and timely question---how to model strategic interaction between humans and AI---with a well-crafted theoretical framework. The attribution function is a novel and well-motivated primitive, and the nesting results establish that ABE is a proper generalization of existing theory.

The paper's main weakness is that its empirical content rests on a primitive (the attribution function) whose properties are assumed rather than derived. This is not unusual for theory papers, but it limits the paper's ability to generate sharp predictions. The welfare analysis, while conceptually interesting, depends on monotonicity assumptions that may or may not hold.

A major revision should address:
1. The empirical foundations of the attribution function (Major Comment 1)
2. The role of RAE in the paper (Major Comment 2)
3. Heterogeneity in the welfare analysis (Major Comment 3)

The paper is well-written and the contribution is genuine. With these revisions, it would be a strong candidate for publication in a top general-interest journal.
