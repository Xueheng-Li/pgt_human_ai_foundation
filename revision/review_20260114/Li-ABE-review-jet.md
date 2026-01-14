# Referee Report: "Thinking for Machines: Attributed Belief Equilibrium"

**Journal**: Journal of Economic Theory
**Manuscript**: "Thinking for Machines: Attributed Belief Equilibrium" by Xueheng Li

---

## Summary

This paper introduces Attributed Belief Equilibrium (ABE), a new equilibrium concept for strategic interactions between humans and artificial agents. The key innovation addresses a fundamental asymmetry: humans have belief-dependent preferences (guilt, reciprocity, indignation) while AI have design-dependent objectives without genuine mental states. The paper formalizes how humans attribute mental states to AI through an "attribution function" that captures anthropomorphism, and incorporates "attenuation parameters" that scale emotional intensity toward AI. The author establishes existence of ABE under regularity conditions, proves that ABE nests standard frameworks (psychological Nash equilibrium, Nash equilibrium, Bayes-Nash equilibrium) as special cases, and derives welfare implications showing that over-anthropomorphism improves welfare with prosocial AI but reduces welfare with materialist AI through "phantom expectations."

## Overall Assessment

This is a well-executed theoretical contribution to an important and timely problem. The paper addresses a genuine gap in the literature: standard psychological game theory assumes symmetric belief-dependent preferences across all players, which fails when one player class (AI) lacks mental states entirely. The core insight---that humans *attribute* beliefs to AI even when those beliefs do not exist, and that these attributed beliefs trigger real psychological responses---is both theoretically novel and empirically grounded.

The formal framework is carefully constructed. The existence proof extends fixed-point arguments to dual belief structures in a natural way. The nesting results (Propositions 1-3) establish ABE as a proper generalization of existing theory, which strengthens the contribution. The welfare analysis identifying the prosocial/materialist asymmetry is the most interesting substantive result.

However, several issues require attention before publication.

---

## Major Comments

### 1. The Attribution Function Requires More Structure

The attribution function $\phi_i(\theta_j, x_j, \omega_i)$ is the paper's central primitive, yet it remains largely unspecified. The paper offers three approaches (behavioral, signal-based, dispositional) and one parametric example (linear attribution), but does not discipline which approach applies when or how the function should be empirically estimated.

This matters for two reasons:
- **Testability**: Without restrictions on $\phi$, the framework can rationalize almost any observed behavior by choosing an appropriate attribution function. The paper acknowledges this flexibility as a feature ("different attribution functions sustain different equilibria"), but it cuts both ways---predictions require specifying $\phi$ ex ante.
- **Comparative statics**: Propositions 5-7 and 8-10 condition on properties of $\phi$ (monotonicity, non-degeneracy) without establishing when these properties hold empirically.

**Request**: Either (a) provide axiomatic foundations for the attribution function that discipline its form, or (b) be more explicit that the framework's current contribution is conceptual rather than predictive, and that empirical applications require separate work to calibrate $\phi$.

### 2. The Existence Proof Needs Clarification

Theorem 1's proof sketch is informative but incomplete. Two issues:

(i) The proof claims attributed beliefs are "independent of $\sigma$---constants determined by AI design parameters" (Appendix A.1, Step 2). But for behavioral attribution $\phi^{beh}_i(\theta_j, x_j, \omega_i) = g(s^{obs}_j, \omega_i)$, attributed beliefs depend on observed AI behavior, which depends on equilibrium strategies. The proof appears to assume signal-based or dispositional attribution.

(ii) The claim that "A3 (bounded psychological payoffs) is implied by A1 given compactness of $\Sigma$" (Remark 11) is not obvious. Compactness of the strategy space does not immediately imply boundedness of psychological payoffs, which may depend on beliefs in unbounded ways.

**Request**: Clarify whether the existence result holds for all three attribution approaches or only some. If behavioral attribution creates a feedback loop, this should be addressed explicitly.

### 3. Rational Attribution Deserves Fuller Treatment

Proposition 3 establishes that under "rational attribution," ABE reduces to Bayes-Nash equilibrium. This is an important result, but the treatment is somewhat confusing:

- Rational attribution is defined as a fixed-point requirement: $\phi_i(\theta_j, x_j, \omega_i) = \sigma^*_i$. But earlier (Remark 1), "rational attribution benchmark" is defined as $\lim_{\omega_i \to 0} \phi_i$.
- The paper uses "rational attribution" to mean both (a) a benchmark for comparison and (b) an equilibrium concept. These are distinct notions that should be clearly separated.
- Existence of rational attribution equilibrium "is not guaranteed for general games" (p. 17). When does it exist? Does uniqueness of Nash equilibrium in the material game suffice?

**Request**: Distinguish clearly between the rational attribution *benchmark* and rational attribution *equilibrium*. Provide conditions under which the latter exists.

---

## Minor Comments

### Exposition and Framing

1. The paper would benefit from a simple illustrative example in Section 2 (before the formal applications) showing how ABE differs from standard psychological equilibrium. The trust game example in Section 3.4 serves this purpose but arrives late.

2. The Introduction promises to address a "dual psychological asymmetry" but the second asymmetry (attenuation) receives less development than the first (attribution). Consider restructuring to make these symmetric.

3. Definition 6 (ABE) should explicitly note that conditions (ii) and (iv) apply only when $N_A \neq \emptyset$, to make the nesting (Proposition 1) more transparent.

### Technical Details

4. The notation switches between $\beta_i$ for indignation sensitivity and the standard PGT notation $\beta^{(n)}_i$ for $n$-th order beliefs (footnote, p. 10). The paper notes this but the potential for confusion remains. Consider $\kappa_i$ or $\iota_i$ for indignation.

5. Proposition 4 (multiplicity) conditions are stated as "generic" (Remark 7), but no measure-theoretic or topological sense of genericity is defined. This claim should be either formalized or softened.

6. The welfare analysis distinguishes "material welfare" $W(s)$ from "extended welfare" $W^{ext}(s,h,\tilde{h})$. The choice between these measures is consequential for the results (Proposition 8-9). The paper could briefly discuss when each measure is appropriate normatively.

7. Proposition 10's claim that prosocial AI should use "minimal anthropomorphic signaling sufficient to induce cooperation" ($x^* = x_{crit}$) assumes discrete regime switching. With continuous cooperation levels, the optimal signal might differ.

### Empirical Grounding

8. The empirical literature review is thorough, but the paper could note that most cited studies involve one-shot interactions. Whether attributed beliefs persist or decay with experience is relevant for the dynamic extensions discussed in Section 5.9.

9. The cross-cultural evidence (Karpus et al., 2025) is invoked several times but details are sparse. A sentence clarifying the magnitude of cross-cultural differences would help readers assess the practical importance.

### Literature

10. The paper could engage with the literature on "machine behavior" (Rahwan et al., 2019, which is cited) and computational social choice more directly. How does ABE relate to mechanism design when one agent class has no preferences?

11. The connection to sequential psychological equilibrium (Battigalli and Dufwenberg, 2009) is noted but not developed. Does ABE extend naturally to dynamic games? The paper's Proposition 1 only addresses static games.

---

## Confidential Comments to Editor

**Recommendation**: Major Revision

This paper makes a genuine contribution to game theory by extending psychological games to human-AI interaction. The problem is timely, the approach is novel, and the formal framework is competent. The nesting results (Propositions 1-3) are clean and establish ABE as a proper generalization. The welfare asymmetry (prosocial vs. materialist AI) is the paper's most substantive finding.

However, the attribution function---the paper's central innovation---requires more structure before the framework can generate testable predictions. Currently, the flexibility of $\phi$ makes it closer to a modeling language than a theory. This is a common issue with first papers introducing new concepts, and I do not think it should block publication, but the author should be more explicit about this limitation.

The existence proof also needs clarification, particularly regarding behavioral attribution.

The paper is appropriate for JET. With revisions addressing the major comments, it would make a solid contribution to the journal's game theory section.
