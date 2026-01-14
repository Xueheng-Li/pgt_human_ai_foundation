# Referee Report: "Thinking about Machines: Attributed Belief Equilibrium"

**Journal**: Econometrica
**Recommendation**: Major Revision

---

## Summary

This paper introduces Attributed Belief Equilibrium (ABE) to analyze strategic interaction between humans and AI agents. The central innovation is the *attribution function*, which captures how humans project mental states onto AI agents that lack genuine beliefs. Humans experience psychological payoffs (guilt, indignation) from violating attributed expectations, even when those expectations exist only in human perception. The paper establishes existence under standard regularity conditions, proves that ABE nests psychological Nash equilibrium and standard Nash equilibrium as special cases, and derives welfare implications: anthropomorphism improves welfare with prosocial AI but creates "phantom expectations" with materialist AI, imposing pure psychological costs.

---

## Overall Assessment

This paper addresses a genuinely important question at the frontier of economic theory: how should we model strategic interaction when one party (humans) has belief-dependent preferences while the other (AI) has programmed objectives? The psychological game theory literature has no tools for this asymmetry, and the paper's contribution---formalizing attributed beliefs as a distinct primitive---fills this gap cleanly.

The paper's main strength is conceptual clarity. The attribution function $\phi_i(\theta_j, x_j, \omega_i)$ elegantly captures the key behavioral regularity (anthropomorphism) while remaining tractable. The nesting results (Propositions 1-3) establish ABE as a proper generalization, and the welfare analysis identifies a substantive design failure: anthropomorphic presentation of materialist AI creates deadweight loss.

Three concerns require attention. First, the existence proof relies on exogenous attribution (signal-based or dispositional), but behavioral attribution---where attributed beliefs depend on observed AI behavior---creates a simultaneity problem that the current proof does not address. Second, the "phantom expectations" concept, while intuitive, needs clearer distinction from standard psychological game theory's belief-dependent payoffs. Third, the empirical strategy section, though detailed, identifies testable predictions that are not yet tested; the paper would benefit from acknowledging more explicitly what experimental evidence would falsify the model.

---

## Major Comments

### 1. Existence with Behavioral Attribution (Section 3.2)

The existence proof (Theorem 1) works cleanly for signal-based and dispositional attribution, where $\tilde{h}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$ is constant in the strategy profile $\sigma$. But Section 2.5 introduces behavioral attribution: $\phi_i^{beh}(\theta_j, x_j, \omega_i) = g(s_j^{obs}, \omega_i)$, where attributed beliefs depend on observed AI behavior. This creates a simultaneity: AI strategies affect attributed beliefs, which affect human best responses, which affect AI best responses.

The proof sketch notes that "under exogenous attribution... attributed beliefs do not create additional equilibrium conditions." But behavioral attribution is not exogenous. The paper should either:
- Provide an extended existence proof for behavioral attribution (likely requiring continuity of $g$ in $s_j^{obs}$ and an expanded fixed-point argument), or
- Clearly restrict the scope of Theorem 1 to exogenous attribution cases and discuss when behavioral attribution is likely to admit equilibria.

This matters for applications: the trust game plausibly involves behavioral attribution (the AI's sending decision $x$ affects attributed expectations about returns).

### 2. Distinguishing Phantom Expectations from Standard Guilt (Section 5)

The paper's welfare analysis relies heavily on "phantom expectations"---attributed beliefs that correspond to no genuine AI mental state. The concept is intuitive: guilt from disappointing an entity that never expected anything. But the formal treatment blurs the distinction from standard guilt aversion.

In Charness-Dufwenberg guilt aversion, guilt arises from falling short of second-order beliefs that other humans genuinely hold. The psychological cost has a counterpart: the disappointed party experiences loss. In ABE, guilt arises from falling short of attributed beliefs that AI cannot hold. The psychological cost has no counterpart.

The paper should make this distinction more formally precise. Consider adding:
- A definition that clearly separates *matched expectations* (attributed beliefs reflecting genuine AI objectives, as with prosocial AI) from *unmatched expectations* (attributed beliefs with no basis in AI design, as with materialist AI).
- A welfare decomposition showing that with prosocial AI, guilt costs are offset by cooperation gains (net positive), while with materialist AI, guilt costs are pure loss (no offset).

Currently, the reader must infer this from the numerical example (Example 5.1). The conceptual point deserves formal statement.

### 3. Rational Attribution Equilibrium: Existence Conditions

Proposition 4 (RAE existence) states conditions under which attributed beliefs equal equilibrium strategies. But the proposition's conditions are restrictive: either the material game has a unique Nash equilibrium, or the attribution function is defined to project equilibrium play. The second condition is nearly tautological.

The paper should address:
- When is RAE a reasonable prediction, beyond games with unique equilibria?
- Does RAE exist generically, or only in special cases?
- What is the measure of games (in an appropriate sense) for which RAE fails?

The current treatment makes RAE seem like a normative benchmark that is rarely descriptively accurate. If that is the intended interpretation, say so explicitly. If RAE is meant to capture "sophisticated" agents who learn the equilibrium, the paper should discuss the learning dynamics that would produce convergence.

---

## Minor Comments

### 1. Assumption Labeling

The assumption table (Table 1) is helpful, but some conditions appear only in later sections (e.g., (G), (I), (T)) without forward reference. Consider noting in Section 2.8 that additional context-specific conditions will be introduced as needed.

### 2. Notation: Transfer vs. Signal in Trust Game

Remark 4.2 clarifies that $x$ denotes the monetary transfer in the trust game, distinct from the signal $x_j$ in the attribution function. But the trust game analysis (Proposition 6) uses the linear attribution $\tilde{h}_H^{(2,A)} = \omega_H \cdot (\rho_A + \eta \cdot x_A)$ where $x_A$ appears to be the signal. The relationship between the transfer and the signal should be clarified: is the signal exogenous (interface design) or endogenous (correlated with transfer)?

### 3. Cross-Cultural Variation

The paper cites Karpus et al. (2025) on cross-cultural variation in attenuation. This is promising for empirical work, but the paper does not develop testable predictions that distinguish ABE from alternative explanations (e.g., cultural differences in trust, risk preferences, or fairness norms). Consider adding a brief discussion of what patterns would uniquely support the attribution mechanism.

### 4. Coordination Game Application

Proposition 8 shows that AI can serve as a focal point, resolving coordination game multiplicity. But the result relies on expectation conformity (humans experience disutility from deviating from attributed expectations), which is related to but distinct from guilt and indignation. The psychological foundation (one paragraph citing Cialdini 1998) is thin compared to the guilt and indignation foundations. Consider either:
- Strengthening the psychological justification for expectation conformity, or
- Noting that this application extends the framework beyond the core guilt/indignation mechanisms.

### 5. Dynamic Extensions

The conclusion notes that "humans likely update $\omega$ and $\lambda$ based on experience with AI" but does not pursue this. For a theory paper, this is acceptable, but the static treatment limits policy relevance. Disclosure requirements, for instance, might shift $\omega$ over time as humans learn AI objectives. A brief discussion of how dynamic considerations might modify the optimal design results would strengthen the policy analysis.

### 6. Proofs: Condensation

The main text includes proof sketches with references to an Online Appendix for details. This is appropriate, but ensure that the Online Appendix is available to referees. Several proofs (e.g., Proposition 5) are quite terse---three steps covering "attribution determines beliefs, beliefs affect payoffs, payoffs shift equilibria"---and readers may want more detail.

### 7. Title

"Thinking about Machines" is evocative but may be too informal for Econometrica. Consider a title that signals the theoretical contribution more directly, e.g., "Attributed Belief Equilibrium: Psychological Games with Human and Artificial Agents."

---

## Confidential Comments to Editor

**Recommendation**: Major Revision

This paper makes a genuine contribution to game theory by extending psychological games to accommodate asymmetric player types. The question is timely and the framework is well-constructed. However, three issues require substantive revision:

1. **Existence with behavioral attribution**: The proof works for exogenous attribution but the paper introduces behavioral attribution without establishing existence for that case. This is not fatal---the paper can restrict scope or extend the proof---but it needs resolution.

2. **Conceptual clarity on phantom expectations**: The key welfare insight depends on distinguishing guilt toward prosocial AI (which has offsetting benefits) from guilt toward materialist AI (which is pure loss). This distinction needs formal statement, not just illustrative examples.

3. **RAE interpretation**: The Rational Attribution Equilibrium concept is underdeveloped. The paper should clarify whether RAE is normatively interesting, descriptively plausible, or primarily a technical benchmark.

If these issues are addressed, the paper would make a strong contribution to the literature on psychological games and human-AI interaction. The applications are well-chosen, the welfare analysis is substantive, and the framework has clear policy implications.

The paper is technically sound, clearly written, and addresses an important gap in the literature. I recommend major revision rather than rejection because the core contribution is solid; the issues are about completeness and precision rather than fundamental flaws.

---

*Report prepared for Econometrica editorial review.*
