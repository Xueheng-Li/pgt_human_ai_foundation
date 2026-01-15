# Referee Report: "Attributed Belief Equilibrium: Psychological Games between Humans and AI"

**Journal:** Games and Economic Behavior
**Date:** January 15, 2026

---

## Summary

This paper extends psychological game theory to human-AI interactions by introducing Attributed Belief Equilibrium (ABE). The central innovation is the attribution function, which captures how humans project mental states onto AI agents that lack genuine beliefs. The framework accommodates two documented psychological phenomena: humans attribute expectations to AI through anthropomorphism, yet experience attenuated emotional responses toward machines compared to humans. The paper establishes existence under standard regularity conditions, proves that ABE nests psychological Nash equilibrium, Nash equilibrium, and Bayes-Nash equilibrium as special cases, and demonstrates attribution-dependent multiplicity---different attribution patterns sustain different equilibria in the same material game. Applications to trust games, public goods, and coordination illustrate how interface design affects equilibrium selection through the psychological channel. The welfare analysis identifies an asymmetry: elevated anthropomorphism improves outcomes with prosocial AI but creates "phantom expectations" and welfare losses with materialist AI.

## Overall Assessment

This paper makes a genuine contribution to the literature on psychological games and human-AI interaction. The research question---how to model strategic interaction when one player type has belief-dependent preferences while the other does not---is both timely and theoretically interesting. The core insight that humans attribute beliefs to AI through anthropomorphism, and that these attributed beliefs enter utility through standard psychological mechanisms, is well-motivated by established psychology literature.

The main strengths are: (1) a clean conceptual framework that naturally extends existing psychological game theory; (2) rigorous technical execution, particularly the existence theorem and nesting results; (3) clear economic implications for AI design; and (4) strong grounding in empirical psychology research on anthropomorphism and mind perception.

My main concerns are: (1) the linear specification of the attribution function, while tractable, may be overly restrictive for some applications; (2) the welfare analysis could more carefully address the normative status of phantom guilt; and (3) some conditions in the application propositions could be weakened.

The paper is well-suited for Games and Economic Behavior. The equilibrium analysis is technically sound, the applications are illustrative without being contrived, and the welfare implications are economically meaningful. I recommend acceptance after minor revisions addressing the points below.

---

## Major Comments

### 1. Clarify the Welfare Treatment of Phantom Guilt

The paper introduces "phantom expectations" and argues that guilt from disappointing these non-existent expectations is "pure welfare loss." This claim deserves more careful treatment.

The instrumental vs. intrinsic distinction (Section 2.6) is helpful but incomplete. Under the intrinsic view, phantom guilt is genuine disutility experienced by humans---it reduces their well-being regardless of whether it corresponds to any AI mental state. Why should the planner discount this experience simply because its object is "phantom"? One could argue that experienced guilt is experienced guilt, whether the disappointing-someone exists or not.

The paper implicitly adopts a position that phantom guilt is somehow less legitimate than guilt toward humans. This may reflect a form of moral realism about belief-dependent preferences that warrants explicit defense. Alternative framings are possible: phantom guilt could be viewed as a cognitive tax on anthropomorphism, analogous to other preference errors that welfare economics handles without dismissing the experienced disutility.

**Suggestion:** Add a paragraph explicitly addressing why phantom guilt should be treated asymmetrically from guilt toward humans in welfare calculations. The current framing suggests it is wasteful because "it benefits no one," but this conflates the transfer interpretation of guilt (where disappointing someone benefits them) with the experience interpretation (where guilt is simply disutility).

### 2. The Linear Attribution Specification

The linear specification $\tilde{h}_i^{(2,j)}(C) = \omega_i \cdot (\rho_j + \eta \cdot x_j)$ is defended on grounds of tractability and first-order approximation. This is reasonable for theoretical development, but the paper should acknowledge limitations more directly.

The multiplicative structure---where $\omega_i = 0$ implies no attribution regardless of AI characteristics---is a strong assumption. Some individuals with low general anthropomorphism tendency may still attribute beliefs to highly human-like AI. The specification rules this out.

Similarly, the additive structure inside the bracket assumes AI prosociality and interface signals operate through independent channels. Interactions between these (e.g., prosocial AI with mechanical interface vs. materialist AI with anthropomorphic interface) may exhibit non-additive effects.

**Suggestion:** Acknowledge these limitations in the discussion of Example 1. The current text notes that "nonlinear specifications (logistic saturation, uncanny valley discontinuities) may better fit extreme ranges" but does not address the multiplicative and additive structural assumptions.

---

## Minor Comments

### 3. Condition (G) vs. (G') Notation

The paper uses (G) for $G > 1$ (guilt dominance) and (G') for $G > 0$ (positive guilt sensitivity). The footnote in Proposition 11 explains the distinction, but it would be clearer to use distinct symbols rather than primed notation, which typically suggests a strengthening rather than weakening of a condition.

### 4. Trust Game Design Choice

The remark explaining why AI is positioned as trustor rather than trustee is helpful. However, the claim that this design "isolates the attribution mechanism" could be strengthened. With AI as trustee, the human's trust decision would confound attribution effects with risk preferences toward AI. Stating this explicitly would clarify the identification advantage.

### 5. Public Goods: Binary vs. Continuous Contributions

The public goods application restricts contributions to binary choices ($c_i \in \{0, E\}$). This yields clean equilibrium characterizations but may miss interior solutions where partial contributions respond to attributed expectations. A brief remark on whether the qualitative results extend to continuous contribution spaces would be valuable.

### 6. Proposition 5 Conditions

Condition (iii) in Proposition 5 ("best-response separation: the change in attributed beliefs shifts equilibrium strategies") is somewhat tautological---it assumes what the proposition aims to establish. The proposition would be stronger if it characterized when best-response separation holds in terms of primitives (e.g., sufficient curvature of the psychological payoff function).

### 7. Rational Attribution Equilibrium

The RAE concept is interesting but its practical relevance is unclear. The paper notes that RAE "need not exist in general" and identifies restrictive sufficient conditions. A reader might wonder when RAE is the appropriate solution concept rather than the more general ABE. Adding a brief discussion of economic settings where rational attribution is plausible would help.

### 8. Cross-Cultural Implications

The discussion of cross-cultural variation (Section 5.8) is thought-provoking but speculative. The cited evidence from Karpus et al. (2025) concerns attenuation, not anthropomorphism tendency per se. The paper sometimes conflates these: "high-$\omega$ cultures" appears to mean cultures with low attenuation, but $\omega$ and $\lambda$ are distinct parameters. Clarifying terminology would strengthen this section.

### 9. Minor Typographical Issues

- Page 7: "human $i$'s anthropomorphism tendency" appears twice in Definition 3---consider consolidating.
- The notation $h_i^{(2,k)}(a)$ for point beliefs could be introduced earlier; it first appears in Section 2.3 but is used heavily in applications.
- Table 1 (Assumption Summary) is helpful but could note which assumptions are standard vs. novel to this framework.

---

## Confidential Comments to Editor

**Recommendation:** Minor Revision

This paper extends psychological game theory to an economically important domain---human-AI interaction---in a technically sound and conceptually clear way. The attribution function is the key innovation, and the paper does a good job grounding it in established psychology while developing its game-theoretic implications.

The major comments concern interpretation rather than correctness. The phantom guilt welfare treatment is the most substantive issue: the paper's position that phantom guilt is "wasteful" reflects an implicit normative stance that warrants explicit defense. This does not undermine the technical contribution but affects how readers should interpret the welfare results.

The linear attribution specification is a reasonable modeling choice, but the paper could be more forthcoming about its limitations. These are minor revisions that would strengthen an already strong paper.

The paper fits well within GEB's scope: it contributes to the theory of psychological games, develops new equilibrium concepts, and derives economically meaningful implications for AI design. The technical execution meets the journal's standards. I recommend acceptance conditional on addressing the major comments and selected minor comments.
