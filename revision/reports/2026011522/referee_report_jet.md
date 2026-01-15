# Referee Report: "Attributed Belief Equilibrium: Psychological Games between Humans and AI"

**Journal:** Journal of Economic Theory
**Manuscript ID:** [To be assigned]
**Date:** January 15, 2026

---

## Summary

This paper introduces Attributed Belief Equilibrium (ABE) to analyze strategic interaction between humans and AI agents. The core insight is that humans attribute mental states to AI agents that lack genuine beliefs or expectations, triggering psychological mechanisms (guilt, indignation, reciprocity) through these attributed rather than actual beliefs. The framework models this through an "attribution function" that maps AI design parameters, interface signals, and individual anthropomorphism tendency to attributed second-order beliefs. The paper establishes existence under regularity conditions, demonstrates that ABE nests standard psychological game theory and Nash equilibrium as special cases, and shows that different attribution patterns sustain different equilibria in the same material game. Applications to trust games, public goods, and coordination illustrate the framework's predictions. The welfare analysis reveals an asymmetry: anthropomorphism improves welfare with prosocial AI but reduces extended welfare with materialist AI through "phantom expectations."

## Overall Assessment

This is an ambitious and timely paper that addresses a genuine gap in game-theoretic foundations for human-AI interaction. The central observation---that humans attribute beliefs to AI agents lacking mental states, and that this attribution affects strategic behavior through psychological mechanisms---is both theoretically novel and empirically grounded. The paper demonstrates solid technical competence: the existence proof correctly extends Kakutani's fixed-point argument to accommodate dual belief structures, and the nesting results (Propositions 1-3) elegantly connect ABE to established frameworks.

The paper's main contribution lies in identifying attribution-dependent multiplicity as a distinct source of equilibrium selection in human-AI games. Unlike standard PGT multiplicity (which arises from belief-strategy feedback), ABE multiplicity operates through a feed-forward chain where design choices directly determine equilibrium outcomes. This has clear implications for AI interface design and regulation.

However, the paper faces a significant tension between its theoretical ambition and empirical grounding. The attribution function---the paper's key primitive---remains underspecified in important ways. While Section 2.5 provides a detailed identification strategy, the functional form (linear attribution) is assumed rather than derived from microfoundations. The paper acknowledges this limitation but perhaps underestimates how much the specific predictions depend on this choice.

---

## Major Comments (Essential for Publication)

### 1. Identification of Attribution Function Parameters

The identification strategy in Section 2.5 proposes a two-stage approach: estimate psychological parameters from human-human interactions, then identify the attribution function from human-AI interactions. This is sensible in principle but faces a serious econometric challenge that requires additional discussion.

**The problem:** The two-stage approach assumes guilt sensitivity ($\gamma_i$) and indignation sensitivity ($\beta_i$) are stable across human and AI counterparts. But attenuation factors ($\lambda^{GUILT}$, $\lambda^{IND}$) explicitly allow these psychological responses to differ toward AI. How does the researcher distinguish between (a) a human with high $\gamma_i$ but high attenuation $\lambda^{GUILT} \approx 0$ toward AI, versus (b) a human with low $\gamma_i$ but no attenuation $\lambda^{GUILT} \approx 1$? Both generate similar observed behavior toward AI despite different underlying mechanisms.

**Required revision:** The paper should either (i) provide formal identification conditions under which $(\gamma_i, \lambda_i^{GUILT})$ can be separately identified, or (ii) acknowledge that the framework identifies only the compound parameter $G = \gamma_i \lambda_i^{GUILT}$ from human-AI data, which suffices for behavioral predictions but limits welfare analysis requiring separate attenuation estimates.

### 2. Testability of Attribution Monotonicity (A2')

Attribution monotonicity (A2')---that higher anthropomorphism $\omega_i$ increases attributed beliefs---is central to the welfare results (Propositions 9-10) and optimal design conclusions (Propositions 11-12). Yet the paper provides limited guidance on testing this assumption.

**The concern:** The IDAQ measures anthropomorphism tendency, but attributed beliefs must be elicited separately. What if subjects with high IDAQ scores do not exhibit higher attributed beliefs toward a given AI interface? This would falsify A2' and undermine the welfare analysis.

**Required revision:** Add an explicit falsification criterion for A2': state precisely what empirical pattern would reject attribution monotonicity and how this would affect the paper's conclusions. The current falsification criteria (end of Section 2.5) focus on the interaction effect $\beta_3$ but do not directly address monotonicity.

### 3. Welfare Measure Selection Needs Stronger Justification

The paper introduces two welfare measures---material ($W$) and extended ($W^{ext}$)---and shows they can diverge when phantom expectations arise. The normative discussion (Section 2.6.1) presents this as a choice between "instrumental" and "intrinsic" views of psychological payoffs. This framing is reasonable but incomplete.

**The concern:** The extended welfare measure $W^{ext}$ counts guilt from phantom expectations as a genuine cost. But phantom guilt arises from misattribution---the human believes AI expected something it did not. If we accept that phantom expectations are cognitive errors, should welfare analysis count their psychological consequences? One could argue that a paternalistic planner should not validate misattributions by counting them in social welfare.

**Required revision:** Acknowledge the philosophical tension: extended welfare may count costs arising from cognitive biases. Clarify whether the paper takes a position on this, or present both views and their implications for AI regulation. This matters because Proposition 12's recommendation to limit anthropomorphic signaling depends on accepting $W^{ext}$ as normatively relevant.

---

## Minor Comments (Suggestions)

### 4. Linear Attribution Specification

The linear specification $\tilde{h}_i^{(2,j)}(C) = \omega_i \cdot (\rho_j + \eta \cdot x_j)$ is tractable but imposes strong restrictions. The multiplicative structure implies that subjects with $\omega_i = 0$ attribute zero expectations regardless of how prosocial the AI design ($\rho_j$) or how anthropomorphic the interface ($x_j$). This seems extreme: even skeptical users might form some beliefs about AI behavior from observing its actions.

Consider whether a specification with a non-zero baseline---such as $\tilde{h} = \underline{h} + \omega_i \cdot (\rho_j + \eta x_j - \underline{h})$---better captures the psychology. This would allow zero-anthropomorphism subjects to hold non-trivial beliefs while preserving the monotonicity properties used in the analysis.

### 5. Behavioral Attribution Extension

The existence theorem elegantly handles behavioral attribution (A2-beh), where attributed beliefs depend on observed AI behavior. But the applications all use exogenous attribution. This is acknowledged (Remark 2 in Section 4) but leaves the reader wondering: when does behavioral attribution matter empirically?

Consider adding a brief discussion of contexts where behavioral attribution is likely to dominate (repeated interactions, learning settings) versus where signal-based attribution suffices (one-shot interactions with strong interface manipulation). This would help applied researchers select the appropriate specification.

### 6. Cross-Cultural Predictions

The paper makes interesting predictions about cross-cultural variation (Section 5.6), noting that Japanese participants show less attenuation than Western participants. The prediction that high-$\omega$ populations are both more vulnerable to welfare losses from materialist AI and more likely to benefit from prosocial AI is novel.

This section would benefit from more specific testable predictions. For instance: "Holding AI design constant, the difference in returns to AI trustees between high-IDAQ and low-IDAQ subjects should be larger in Japan than in Western countries." Such predictions sharpen the empirical agenda.

### 7. Connection to Mechanism Design

The paper notes (Section 6) that optimal AI presentation connects to mechanism design. This is intriguing but underdeveloped. In standard mechanism design, the principal chooses rules knowing agents will best-respond. In ABE design, the principal chooses presentation (affecting attributed beliefs) knowing humans will best-respond to those beliefs. Is there a revelation principle analog? When can the principal implement first-best outcomes through attribution manipulation?

This extension is beyond the current paper's scope but would strengthen the conclusion's discussion of future directions.

### 8. Notation Clarity

The notation switches between $h_i^{(2,k)}$ (second-order belief about human $k$) and $\tilde{h}_i^{(2,j)}$ (attributed belief about AI $j$). The tilde convention is helpful, but in some equations (e.g., Definition 4), the distinction between probability distributions and point beliefs could be clearer. Consider adding a notation table early in Section 2.

### 9. Phantom Expectations Terminology

The term "phantom expectations" is evocative but potentially misleading. These are not expectations that once existed and vanished; they are expectations that never existed but are attributed by the human. Consider "projected expectations" or "imputed expectations" as alternatives that better capture the psychological mechanism.

### 10. Missing Literature Connection

The paper does not cite the literature on "theory of mind" in AI systems. Recent work on large language models' ability to pass theory-of-mind tests (e.g., Kosinski 2023, but controversial; Ullman 2023) is relevant because it questions whether the bright line between "humans with genuine beliefs" and "AI without beliefs" will remain sharp. A brief acknowledgment that the framework assumes this distinction remains meaningful would be valuable.

---

## Confidential Comments to Editor

**Recommendation:** Minor Revision

This paper makes a genuine theoretical contribution to an important and timely topic. The core insight---that humans attribute beliefs to AI and that this attribution affects strategic behavior---is novel and well-developed. The technical execution is solid: the existence proof is correct, and the nesting results elegantly connect ABE to established frameworks.

My main concerns are about empirical grounding rather than theoretical substance. The attribution function is the paper's key primitive, and while the identification strategy is thoughtful, the separate identification of psychological parameters versus attenuation factors remains unclear. This matters because the welfare analysis depends on distinguishing genuine psychological preferences from AI-specific attenuation. The paper should either provide formal identification conditions or acknowledge the limitation and its implications.

The welfare analysis raises a subtle philosophical issue: should social welfare count psychological costs arising from cognitive biases (misattribution)? The paper treats this as a choice between welfare measures without fully engaging the philosophical tension. A brief discussion acknowledging this issue would strengthen the normative conclusions.

Despite these concerns, I recommend minor revision. The paper addresses a real gap in the literature, provides correct theoretical foundations, and generates testable predictions. The issues I raise can be addressed with additional discussion and clarification rather than fundamental changes to the analysis.

The Journal of Economic Theory is an appropriate venue. The paper's focus on equilibrium foundations, existence conditions, and welfare analysis fits JET's scope. The empirical identification sections, while important for grounding the theory, are appropriately brief for a theory journal.

---

**Summary of Required Revisions:**

1. Clarify identification conditions for separating $\gamma_i$ from $\lambda_i^{GUILT}$, or acknowledge the limitation
2. Add explicit falsification criteria for attribution monotonicity (A2')
3. Discuss the philosophical tension in counting phantom-expectation costs in extended welfare

**Summary of Suggested Revisions:**

4. Consider non-zero baseline in linear attribution specification
5. Add guidance on when behavioral vs. signal-based attribution applies
6. Sharpen cross-cultural testable predictions
7. Expand mechanism design connection in conclusion
8. Add notation summary table
9. Consider alternative terminology for "phantom expectations"
10. Acknowledge theory-of-mind literature on AI
