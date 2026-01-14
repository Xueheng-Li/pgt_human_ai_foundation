# Referee Report: "Thinking about Machines: Attributed Belief Equilibrium"

**Journal**: Games and Economic Behavior
**Manuscript Type**: Theory
**Date**: January 14, 2026

---

## Summary

This paper extends psychological game theory to analyze strategic interaction between humans and AI agents. The central innovation is the "Attributed Belief Equilibrium" (ABE), which addresses a fundamental asymmetry: humans have belief-dependent preferences (guilt, reciprocity, indignation) while AI agents have design-dependent objectives without genuine mental states. The key modeling device is the "attribution function," which captures how humans project mental states onto AI---forming beliefs about what AI "expects"---even when such expectations do not exist. The paper establishes existence under regularity conditions, proves that ABE nests standard equilibrium concepts as special cases, applies the framework to trust games, public goods, and coordination, and derives welfare implications for AI design. A notable finding is that elevated anthropomorphism improves welfare with prosocial AI but may reduce welfare with materialist AI through "phantom expectations."

## Overall Assessment

This is a serious theoretical contribution addressing an important and timely question: how do humans strategically interact with AI agents that lack genuine mental states? The paper identifies a genuine gap in the literature---standard psychological game theory cannot accommodate agents with belief-dependent preferences interacting with agents that lack beliefs entirely. The attribution function is a clever modeling device that captures documented psychological phenomena (anthropomorphism, mind perception) in a tractable way.

The paper is well-written, carefully structured, and exhibits strong technical competence. The existence proof is sound, the nesting results clarify the relationship to existing theory, and the applications generate testable predictions. The welfare analysis---particularly the asymmetry between prosocial and materialist AI---delivers economic insight with policy relevance.

That said, the paper faces a tension between theoretical novelty and empirical content. The attribution function is the key primitive distinguishing ABE from standard game theory, yet its specification remains largely parametric. The paper acknowledges this limitation and proposes an identification strategy, but the framework's ultimate value depends on whether the attribution function can be disciplined empirically.

For Games and Economic Behavior, the paper makes a solid contribution to psychological game theory with clear applications. It is suitable for publication after addressing the issues below.

---

## Major Comments

### 1. The Attribution Function Requires Sharper Discipline

The attribution function $\phi_i(\theta_j, x_j, \omega_i)$ is the paper's central innovation, but also its primary source of degrees of freedom. The paper offers three approaches (behavioral, signal-based, dispositional) and a linear specification (Example 1), but does not establish which applies when or how parameters would be recovered in practice.

**Concern**: Without restrictions on $\phi$, the framework can accommodate almost any pattern of behavior by choosing an appropriate attribution function ex post. This threatens the framework's falsifiability.

**Suggestion**: Either (a) impose axiomatic restrictions on $\phi$ derived from psychological theory (e.g., monotonicity in signals, boundedness, specific functional forms justified by SEEK theory), or (b) commit to a canonical specification for the applications and clearly state which parameters are free versus which are pinned by theory. The paper moves in direction (b) with the linear specification but does not make this the default throughout the applications.

### 2. Clarify the Relationship Between Existence and Behavioral Attribution

The existence proof (Theorem 1) relies critically on attributed beliefs being determined by an exogenous function of $(\theta_j, x_j, \omega_i)$. The paper notes that "behavioral attribution"---where $\phi$ depends on observed AI behavior---complicates the fixed-point structure. The current treatment defers this to an Online Appendix.

**Concern**: If attributed beliefs depend on AI strategy (as seems natural when humans observe AI behavior), the best-response correspondence becomes more complex, and existence may require additional conditions. The paper should either prove existence for this case in the main text or clearly scope the contribution to exogenous attribution.

**Suggestion**: Add a brief discussion in Section 3.2 explaining why behavioral attribution is deferred and what additional structure is needed. Alternatively, prove existence for behavioral attribution in the appendix and summarize the result in the main text.

### 3. Strengthen the Multiplicity Result

Proposition 5 establishes that different attribution functions sustain different equilibria. However, the proof is a straightforward consequence of the model structure: if attributed beliefs affect payoffs and different $\phi$ yield different beliefs, equilibria differ. The result would be more compelling if it demonstrated multiplicity under empirically plausible parameter configurations.

**Suggestion**: Provide a concrete numerical example in the main text (not just the appendix) showing that small changes in anthropomorphism levels or interface signals shift equilibrium outcomes substantially. The trust game example in Section 3.5 moves in this direction but could be more explicit about the magnitude of effects and whether parameter values are empirically reasonable.

---

## Minor Comments

### Presentation

1. **Definition 1 (Attributed Beliefs)**: The notation $\tilde{h}_i^{(2,j)}$ is introduced but not immediately explained. Consider adding a sentence clarifying that this represents "human $i$'s attributed second-order belief about what AI $j$ expects $i$ to do" before the formal definition.

2. **Table 1 (Assumption Summary)**: This is helpful but appears late in Section 2. Consider moving it earlier or at least referencing it when assumptions are first introduced. Some readers may not notice it.

3. **Welfare Measures Section (2.7)**: The discussion of material versus extended welfare is philosophically interesting but somewhat tangential to the main contribution. Consider condensing this section and moving the detailed justification to an appendix.

4. **Proposition 4 (RAE Existence)**: The conditions for existence are somewhat technical. A brief intuitive explanation of when rational attribution equilibria fail to exist would help readers.

### Technical Issues

5. **Assumption A2 (Attribution Continuity)**: The assumption states continuity in $(\theta_j, x_j)$ for fixed $\omega_i$, but applications sometimes vary $\omega_i$. Should continuity in $\omega_i$ also be assumed?

6. **Guilt Definition (Definition 5)**: The guilt payoff includes $\max\{0, h_i^{(2,k)} - \pi_k(s)\}$, but $h_i^{(2,k)}$ is a probability distribution while $\pi_k(s)$ is a scalar. This notation is inconsistent with the earlier definition. I assume the intended interpretation is the expected return or a scalar summary of the belief, but this should be clarified.

7. **Proposition 6 (Trust Game ABE)**: The result states $y^* = \min\{\tilde{h}_H^{(2,A)}, 3x\}$, but this holds only when guilt dominance is strict ($G > 1$). When $G < 1$, the human may return less than attributed expectations. The proposition statement should clarify this boundary case.

### Literature

8. **Rabin (1993)**: The paper cites Dufwenberg and Kirchsteiger (2004) for reciprocity but does not cite Rabin's (1993) foundational paper on fairness and reciprocity in normal-form games. This is a significant omission for a GEB audience.

9. **Battigalli, Dufwenberg, and Smith**: Recent work by these authors on guilt aversion in dynamic games should be cited, as it directly relates to the psychological mechanisms modeled here.

10. **AI Economics Literature**: The paper cites Acemoglu and Restrepo on AI and labor but does not engage with the growing literature on AI decision-making in games (e.g., Calvano et al. on algorithmic collusion). A brief mention of how ABE relates to this literature would strengthen positioning.

### Empirical Content

11. **Section 2.6 (Empirical Implementation)**: The identification strategy is well-described, but no power analysis or sample size estimates are provided. For the interaction effect $\beta_3$ to be detectable, how large must it be? What sample sizes are required?

12. **Cross-Cultural Predictions**: The paper repeatedly cites Karpus et al. (2025) on cross-cultural variation in attenuation. This is valuable, but the paper should acknowledge that cultural differences in anthropomorphism ($\omega_i$) may confound predictions about attenuation ($\lambda$).

### Welfare Analysis

13. **Phantom Expectations Example (Example 5)**: The numerical example effectively illustrates the concept, but the parameter $\phi_H(0, x, \omega_H) = 5\omega_H x$ appears arbitrary. What justifies the coefficient 5? Is this empirically calibrated?

14. **Optimal Design Comparative Statics**: Proposition 11 provides comparative statics $\partial x^*/\partial m$ with opposite signs for prosocial and mixed AI. The intuition for this reversal is explained but could be made more prominent, as it is a key design insight.

---

## Confidential Comments to Editor

**Recommendation**: Minor Revision

This paper makes a genuine contribution to psychological game theory by addressing human-AI strategic interaction---a topic of growing importance that existing theory cannot handle well. The attribution function is a sensible modeling device grounded in established psychology, and the welfare results generate actionable insights for AI design.

The main concern is disciplining the attribution function. The current framework is flexible enough to accommodate many behavioral patterns, which is both a strength (generality) and a weakness (potential lack of falsifiability). The suggested revision---either axiomatic restrictions or commitment to a canonical specification---would sharpen the contribution without requiring fundamental changes.

The technical execution is solid. The existence proof is correct, the nesting results are useful for positioning, and the applications are well-chosen. The writing is clear and professional.

For GEB, this paper fits well as a theory contribution with behavioral foundations. It extends a core methodology (psychological games) to an empirically relevant domain (human-AI interaction) while maintaining technical rigor. After minor revisions addressing the attribution function specification and the technical/presentational issues above, the paper should be acceptable.
