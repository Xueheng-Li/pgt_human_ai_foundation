# Referee Report: "Thinking for Machines: Attributed Belief Equilibrium"

**Journal:** Econometrica
**Manuscript:** Thinking for Machines: Attributed Belief Equilibrium
**Author:** Xueheng Li
**Referee:** Anonymous
**Date:** January 2026

---

## Summary

This paper introduces Attributed Belief Equilibrium (ABE), a new solution concept for strategic interactions between humans and artificial agents. The key innovation addresses a fundamental asymmetry: humans have belief-dependent preferences (guilt, reciprocity, indignation) while AI have design-dependent objectives without genuine mental states. Standard psychological game theory (Geanakoplos et al., 1989; Battigalli and Dufwenberg, 2009) cannot accommodate this heterogeneity because it assumes symmetric belief-dependent preferences.

The paper's core contribution is formalizing how humans attribute mental states to AI through an "attribution function" that captures anthropomorphism. Attributed beliefs enter human utility through standard psychological mechanisms but satisfy different consistency conditions than genuine beliefs. The framework distinguishes between genuine beliefs (about other humans, satisfying Bayesian consistency) and attributed beliefs (about AI, determined by the attribution function given AI design parameters, observable signals, and the human's anthropomorphism tendency).

The main results include: (1) existence of ABE under regularity conditions; (2) nesting theorems showing ABE reduces to psychological Nash equilibrium, Nash equilibrium, and Bayes-Nash equilibrium as special cases; (3) attribution-dependent multiplicity where different attribution functions sustain different equilibria; (4) applications to trust games, public goods, and coordination; (5) welfare analysis showing over-anthropomorphism improves welfare with prosocial AI but reduces welfare with materialist AI through "phantom expectations"; and (6) optimal AI design principles.

---

## Overall Assessment

This is an ambitious and intellectually stimulating paper that tackles a genuinely important problem. As AI agents become ubiquitous economic actors, we need theoretical foundations for analyzing human-AI strategic interaction. The paper identifies a real gap in existing theory: psychological game theory assumes all players have genuine mental states, but AI agents do not. The attribution function is a clever modeling device that addresses this gap.

The paper's main strength is its conceptual innovation. The distinction between genuine and attributed beliefs, and the idea that anthropomorphism creates "phantom expectations" toward materialist AI, is insightful and generates testable predictions. The welfare analysis is particularly interesting: the asymmetry between prosocial and materialist AI provides clear design implications.

However, several issues must be addressed before the paper meets Econometrica standards. The most significant concerns are: (1) the attribution function is essentially assumed rather than derived from primitives; (2) several key conditions lack clear economic interpretation or empirical grounding; (3) the welfare analysis conflates material and psychological welfare in ways that require justification; and (4) the proofs, while correct, sometimes obscure the economic intuition.

---

## Major Comments (Issues Affecting Publishability)

### 1. The Attribution Function Requires Deeper Foundation

The attribution function is the central primitive of the paper, yet it appears somewhat ad hoc. The paper presents three approaches (behavioral, signal-based, dispositional) but does not explain which is appropriate when, or how they relate to each other. For Econometrica, readers will want to know:

- **Microfoundations:** Can the attribution function be derived from more primitive assumptions about human cognition? The psychology literature on anthropomorphism (Epley et al., 2007) provides rich qualitative insights, but the paper does not explain how their model relates to established theories of mind perception.

- **Identification:** Given data on human behavior in human-AI games, how would one estimate the attribution function? The paper should discuss what experimental designs would identify the parameters of interest.

- **Functional form:** The linear specification in Example 1 is convenient but arbitrary. What restrictions does economic theory place on admissible attribution functions? For instance, should attribution satisfy some form of coherence or consistency across games?

**Recommendation:** Add a subsection discussing microfoundations of the attribution function, relating it more precisely to the psychological literature. Discuss identification strategies and provide at least one worked example showing how experimental data would pin down the attribution function.

### 2. The Dual Consistency Requirement Needs Stronger Motivation

The paper imposes different consistency requirements for genuine beliefs (Bayesian) and attributed beliefs (determined by the attribution function). This asymmetry is the key departure from standard theory, but the justification relies heavily on the empirical observation that AI lacks genuine mental states. Yet:

- Why should attributed beliefs be determined entirely by the attribution function rather than updated based on AI behavior? In repeated interactions, surely humans learn about AI "expectations" from past play.

- The paper assumes humans know whether a counterpart is human or AI. What happens with uncertainty about counterpart type? This seems empirically relevant given that humans sometimes interact with AI unknowingly.

- The framework allows attributed beliefs that are completely disconnected from AI behavior (phantom expectations). Is this psychologically plausible? Some bounds on the divergence between attributed and revealed preferences would be more realistic.

**Recommendation:** Strengthen the motivation for the dual consistency requirement. Discuss how the framework would extend to repeated games and uncertainty about counterpart type. Consider whether some "discipline" on attributed beliefs (e.g., bounds related to revealed behavior) would improve realism without losing the key insights.

### 3. The Welfare Analysis Conflates Different Notions of Welfare

The paper uses two welfare measures: material welfare and extended welfare (including psychological payoffs). However:

- The paper switches between these measures without clear justification. Part 1 of Proposition 8 uses material welfare; Part 2 uses extended welfare. This asymmetry is explained in the proof sketch but should be highlighted and justified in the main text.

- The extended welfare measure counts guilt as welfare loss. But guilt is itself a function of attributed beliefs, which are essentially chosen by the human. Should we treat self-inflicted psychological costs the same as material losses? There is a large literature on this question in behavioral welfare economics.

- The "phantom expectations" mechanism assumes humans cannot simply revise their attributed beliefs to eliminate guilt. What constraints prevent belief revision? If beliefs are costly to hold, humans would optimally set attributed beliefs to zero toward materialist AI.

**Recommendation:** Provide a clearer welfare framework early in the paper. Discuss the normative status of psychological payoffs in welfare calculations. Address why belief revision does not eliminate phantom expectations.

### 4. Several Conditions Lack Clear Economic Interpretation

Multiple conditions are introduced (A1-A3, A2', A2", A2"', E, G, G', I, T) but their economic content and interdependencies are difficult to track. Specifically:

- **Condition (G) vs (G'):** The paper uses "guilt dominance" G > 1 in some places and "positive guilt sensitivity" G > 0 in others. The relationship and when each applies is unclear.

- **Condition (T) Temptation Dominance:** This requires E(1 - m/n) > beta(nH - 1), which is essentially assuming that cooperation would fail without AI. Is this condition empirically reasonable?

- **Attribution conditions (A2'), (A2"), (A2"'):** The paper introduces monotonicity, non-degeneracy, and signal monotonicity as separate conditions. A unified treatment would improve readability.

**Recommendation:** Consolidate and clarify the assumption structure. Provide a table summarizing all conditions with their economic interpretations and which propositions require each. Discuss whether the conditions are satisfied in realistic settings.

### 5. The Rational Attribution Benchmark Requires Clarification

The paper defines "rational attribution" as the limit of the attribution function as anthropomorphism goes to zero. But:

- This definition seems to equate "rational" with "zero anthropomorphism." Yet if some anthropomorphism is adaptive (as suggested by the prosocial AI results), why call zero anthropomorphism "rational"?

- Proposition 3 defines a different notion of rational attribution as a fixed point where attributed beliefs equal equilibrium play. The relationship between these two notions is confusing.

- The term "over-anthropomorphism" is used descriptively but carries normative connotations. The paper acknowledges this but could be clearer throughout.

**Recommendation:** Use more neutral terminology for the benchmark (e.g., "zero-anthropomorphism benchmark" rather than "rational attribution benchmark"). Clearly distinguish the two notions of rational attribution in Remark 1 and Proposition 3.

---

## Minor Comments (Suggestions for Improvement)

### Exposition and Structure

1. **Introduction length:** The introduction is comprehensive but could be tightened. The "Results" subsection (pp. 3-5) largely duplicates the abstract and could be condensed.

2. **Notation:** The paper uses h for genuine beliefs and h-tilde for attributed beliefs, with superscripts for order and subscripts for players. This notation becomes unwieldy. Consider a cleaner alternative, perhaps reserving h for all beliefs and using a marker for attributed (e.g., h^A for attributed rather than h-tilde).

3. **Example placement:** The numerical examples in Section 3.4 are helpful but interrupt the flow. Consider moving to an appendix and referencing in the main text.

4. **Missing reference:** On p. 17, there is an incomplete citation: "ABE reduces to Bayesian games (?) with type uncertainty."

### Technical Issues

5. **Existence proof:** The proof sketch of Theorem 1 is adequate, but the full proof in Appendix A.1 is 3 pages. Given the straightforward extension of Kakutani arguments, the appendix proof could be condensed.

6. **Uniqueness:** The paper focuses on existence but says little about uniqueness. When is ABE unique? Attribution-dependent multiplicity is interesting but leaves open whether there is multiplicity within a fixed attribution function.

7. **Mixed strategies:** Remark 2 states the definition extends to mixed strategies but does not verify the existence argument carries through. This should be explicit.

### Applications

8. **Trust game setup:** The trust game has AI as trustor and human as trustee. This is the opposite of standard experiments (human trustor, AI trustee). The choice is fine but should be motivated.

9. **Public goods:** The binary contribution assumption (0 or E) is restrictive. Do the results extend to continuous contributions?

10. **Coordination game:** The coordination application is interesting but the "expectation conformity" psychological payoff is not standard in the literature. Is there empirical support for this specification?

### Welfare and Policy

11. **Regulatory implications:** The discussion of AI transparency regulation is intriguing but underdeveloped. What specific policies does the analysis support? Disclosure requirements? Anthropomorphism limits?

12. **Designer incentives:** The paper notes that private designers may over-anthropomorphize materialist AI but does not formally model this. A simple mechanism design extension would strengthen the policy analysis.

13. **Cultural variation:** The cross-cultural implications are interesting but speculative. The paper should be clearer about what is established empirically versus what is conjecture.

### Literature

14. **Behavioral game theory:** The paper should engage more with behavioral game theory beyond psychological games. How does ABE relate to level-k thinking or cognitive hierarchy models? These have been applied to human-AI interaction.

15. **Mechanism design with behavioral agents:** There is a growing literature on mechanism design accounting for psychological preferences (e.g., Fehr and Schmidt preferences). The optimal AI design results could be framed as a contribution to this literature.

---

## Confidential Comments to Editor

**Recommendation: Major Revision**

This paper makes a genuine contribution by formalizing human-AI strategic interaction with psychological preferences. The core idea---that humans attribute mental states to AI, creating "phantom expectations" with welfare consequences---is novel and important. The paper is technically competent, with correct proofs and appropriate application of fixed-point methods.

However, the paper is not yet ready for Econometrica publication. The attribution function, which is the key primitive, needs stronger foundations. The welfare analysis conflates material and psychological welfare without adequate justification. The assumption structure is complex and could be streamlined.

The good news is that these issues are addressable. With careful revision focusing on:
1. Microfoundations of the attribution function
2. Clear welfare framework with explicit normative assumptions
3. Consolidated assumption structure
4. Tighter exposition

...the paper could become an excellent contribution to the field. The topic is timely and the core insight is valuable. I recommend encouraging the author to revise and resubmit.

One concern worth noting: the paper is long (currently 87+ pages including appendices). For Econometrica, this would need substantial compression. Much of the proof detail could be moved to supplementary material.

---

**Summary of Recommendation:**

| Criterion | Assessment |
|-----------|------------|
| Novelty | High - new equilibrium concept for an important problem |
| Technical quality | Adequate - proofs correct but could be more elegant |
| Economic insight | Good - phantom expectations mechanism is interesting |
| Exposition | Needs improvement - could be tightened substantially |
| Policy relevance | Moderate - implications for AI design are valuable |

**Overall:** Major revision required. The paper has significant potential but needs work on foundations and exposition before meeting Econometrica standards.
