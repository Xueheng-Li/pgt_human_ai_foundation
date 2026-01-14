# Referee Report: "Thinking for Machines: Attributed Belief Equilibrium"

**Journal:** Econometrica
**Manuscript:** Thinking for Machines: Attributed Belief Equilibrium
**Date:** January 14, 2026

---

## Summary

This paper introduces Attributed Belief Equilibrium (ABE), a new equilibrium concept for games involving both human and artificial agents. The key innovation addresses a fundamental asymmetry: humans have belief-dependent preferences (guilt, reciprocity, indignation) while AI agents have design-dependent objectives with no genuine mental states. Standard psychological game theory cannot accommodate this heterogeneity because it assumes symmetric belief-dependent preferences across all players. The paper formalizes how humans project mental states onto AI through an "attribution function," establishes existence of equilibrium under regularity conditions, demonstrates that ABE nests standard frameworks (psychological Nash equilibrium, Nash equilibrium, Bayesian games) as special cases, and derives welfare implications for AI design. The main welfare result shows that anthropomorphism improves welfare when AI is prosocially designed but may reduce welfare through "phantom expectations" when AI is materialistically designed.

---

## Overall Assessment

This is a serious, technically competent theory paper that addresses a genuinely novel question: how should game theory model strategic interaction when one class of players has psychological preferences triggered by beliefs about beliefs, while another class (AI) lacks genuine mental states but is nonetheless anthropomorphized by human players? The question is timely given the growing presence of AI agents in economic and social settings.

The paper's main contribution is conceptual: the attribution function that maps AI characteristics and human anthropomorphism tendencies to attributed beliefs. This formalization captures an empirically documented phenomenon (anthropomorphism) and integrates it into a rigorous equilibrium framework. The existence theorem is technically sound, and the nesting results are helpful for positioning ABE within the existing literature.

However, I have concerns about the paper's structure and whether the current applications and welfare analysis justify Econometrica-level contribution. The framework is elegant, but the payoff in terms of new economic insights is modest relative to the extensive conceptual apparatus. The applications (trust game, public goods, coordination) yield predictions that, while internally consistent, are relatively straightforward given the framework's assumptions. The welfare analysis, while carefully done, relies heavily on stark contrasts between prosocial and materialist AI.

---

## Major Comments (Must Address)

### 1. The Attribution Function Remains a Black Box

The attribution function phi_i is the paper's key primitive, but its specification is underexplored. The paper offers three approaches (behavioral, signal-based, dispositional) without resolving which is empirically appropriate. The linear specification in Example 1 is convenient but potentially restrictive. The paper acknowledges this limitation (Section 6.3) but defers resolution to future work.

For a theory paper introducing a new equilibrium concept, this leaves the reader uncertain about what the framework actually predicts. Different attribution functions can sustain different equilibria (Proposition 4), so the selection among attribution functions is crucial for applied work. The paper should either:
- Provide stronger theoretical restrictions on phi_i derived from first principles, or
- Demonstrate that key qualitative results hold for a broader class of attribution functions.

### 2. Behavioral Attribution Is Deferred But May Be Central

The existence theorem (Theorem 1) explicitly restricts to signal-based and dispositional attribution, deferring behavioral attribution to Remark A.1. Yet behavioral attribution---where attributed beliefs depend on observed AI behavior---seems the most natural specification for many applications. When humans observe that an AI cooperates, they may attribute cooperative expectations; this feedback loop is exactly what behavioral attribution captures.

The paper should either extend the existence result to behavioral attribution or explain why the signal-based/dispositional restriction is economically appropriate. The current treatment risks excluding the most empirically relevant case.

### 3. Welfare Results Depend on a Stark Dichotomy

The welfare analysis hinges on a sharp distinction between prosocial AI (rho_A > 0) and materialist AI (rho_A = 0). With prosocial AI, anthropomorphism helps; with materialist AI, it may harm through phantom expectations. This dichotomy is clean but potentially misleading:

- Most real AI systems have objectives that are neither purely prosocial nor purely materialist. The "mixed AI" analysis (Proposition 10, Part iii) is brief compared to the polar cases.
- The phantom expectations result (Proposition 8, Part ii) requires not just rho_A = 0 but also that phantom expectations exceed feasible returns. This is a joint restriction on the attribution function and the game's payoff structure that may be knife-edge.

The paper would benefit from analyzing when phantom expectations arise generically versus when they require special parameter configurations.

### 4. The Empirical Implementation Section Needs Tightening

Section 2.6.1 on empirical implementation is helpful but raises more questions than it answers:

- The regression specification (equation 8) tests whether anthropomorphism moderates signal effects (beta_3 > 0). But this is a test of the interaction, not a validation of the attribution function's functional form.
- The IDAQ measure of anthropomorphism (Waytz et al. 2010) captures general tendencies, not context-specific attribution. How stable is omega_i across different AI agents and game contexts?
- The quadratic scoring rule with random payment (Blanco et al. 2010) addresses hedging, but does not address whether subjects can accurately report second-order beliefs about AI "expectations."

The paper should either streamline this section (if the goal is to demonstrate testability in principle) or engage more seriously with identification challenges (if the goal is to provide a blueprint for empirical work).

---

## Minor Comments (Suggestions)

### 1. Notation Clarification

The paper uses h for beliefs in the main text but notes this differs from beta notation in Battigalli and Dufwenberg (2009). While the rationale (avoiding confusion with the indignation sensitivity parameter beta_i) is sound, readers familiar with PGT may stumble. A notation table would help.

### 2. Relationship to Behavioral Game Theory

The paper mentions quantal response equilibrium in passing (Introduction, p. 7) but does not engage substantively with behavioral game theory. ABE captures systematic belief biases, not response noise. A brief discussion of how ABE relates to other behavioral departures (level-k reasoning, cognitive hierarchy) would be useful.

### 3. The Coordination Application Is Less Developed

Propositions 5-6 (trust game, public goods) provide comparative statics and threshold conditions. Proposition 7 (coordination) is thinner, simply noting that AI serves as a focal point. The mechanism---expectation conformity pressure---is stated but not analyzed in detail. Either develop this application more fully or acknowledge that it serves primarily as an illustration.

### 4. Cross-Cultural Variation

The paper repeatedly cites Karpus et al. (2025) on cross-cultural variation in guilt attenuation (Japanese vs. Western participants). This is an interesting empirical hook, but the paper does not explore whether ABE's qualitative predictions differ across cultures or only the magnitudes. Clarifying this would sharpen the contribution.

### 5. Length and Exposition

At approximately 55 pages including appendix, the paper is long. The proofs are carefully written but some (e.g., Theorem 1) could be shortened by relegating topology details to a technical appendix. The framework section (Section 2) is thorough but could be tightened; the mind perception psychology section (2.6.2) is useful but perhaps excessive for Econometrica.

### 6. Title

"Thinking for Machines" is evocative but potentially misleading. The paper is about humans thinking *about* machines (anthropomorphism), not machines thinking. Consider a more direct title.

---

## Confidential Comments to Editor

**Recommendation:** Major Revision

This paper makes a genuine conceptual contribution by formalizing how humans attribute mental states to AI agents in strategic settings. The equilibrium concept is novel, the existence proof is sound, and the welfare analysis yields non-obvious design implications.

However, I am not yet convinced that the paper clears the Econometrica bar. The main concerns are:

1. **Contribution vs. apparatus ratio:** The framework is elaborate (attribution functions, attenuation factors, dual consistency conditions), but the applications yield relatively modest new insights. The trust game result (anthropomorphism increases returns) and welfare result (prosocial AI benefits from anthropomorphism, materialist AI harms) are intuitive given the setup.

2. **The attribution function:** This is the paper's key primitive, but it remains underspecified. Without stronger restrictions or broader robustness, the framework's predictive content is uncertain.

3. **Behavioral attribution:** Deferring this case weakens the paper, since observing AI behavior and updating attributed beliefs seems central to real-world human-AI interaction.

I recommend major revision with the following focus:
- Strengthen the treatment of the attribution function (either through theoretical restrictions or robustness)
- Extend existence to behavioral attribution
- Tighten the empirical implementation section
- Consider whether the paper's length can be reduced without losing essential content

If these issues are addressed, the paper could be a strong contribution to the literature on human-AI interaction and psychological game theory. The question being asked is important; the current execution does not yet fully realize the framework's potential.
