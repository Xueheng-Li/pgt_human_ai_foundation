# Referee Report: "Thinking for Machines: Attributed Belief Equilibrium"

**Journal**: Games and Economic Behavior
**Manuscript**: Thinking for Machines: Attributed Belief Equilibrium
**Author**: Xueheng Li

---

## Summary

This paper introduces Attributed Belief Equilibrium (ABE), an extension of psychological game theory to strategic interactions between humans and artificial agents. The key innovation addresses a fundamental asymmetry: humans experience belief-dependent preferences (guilt, reciprocity, indignation) while AI have design-dependent objectives with no genuine mental states. The author formalizes how humans attribute beliefs to AI through an "attribution function" that captures anthropomorphism. The paper establishes existence under regularity conditions, proves that ABE nests standard frameworks (psychological Nash equilibrium, Nash equilibrium, Bayes-Nash equilibrium) as special cases, and derives welfare implications showing that over-anthropomorphism improves welfare with prosocial AI but reduces welfare with materialistic AI through "phantom expectations."

## Overall Assessment

This paper makes a genuine theoretical contribution to an increasingly important domain. The core insight---that humans project mental states onto AI agents and these projections have strategic consequences---is both economically meaningful and well-grounded in empirical psychology. The formalization through the attribution function is elegant, and the dual consistency requirement (Bayesian consistency for human-human beliefs, attribution consistency for human-AI beliefs) is the right conceptual move. The welfare analysis identifying "phantom expectations" as a source of welfare loss is novel and policy-relevant.

The paper is technically competent and well-written. The proofs are complete and the logic is clear. The nesting results provide confidence that ABE is a proper generalization rather than an ad hoc construction. The applications to trust games, public goods, and coordination are well-chosen to illustrate the framework's scope.

My main concern is whether the contribution justifies publication in a top field journal. The framework, while sound, is essentially an application of existing psychological game theory machinery with a new interpretation. The attributed belief is formally just a probability distribution like any other belief; what is new is the consistency condition it must satisfy. The substantive content comes from the attribution function, but this is treated as a primitive rather than derived from deeper principles. The welfare results, while interesting, follow fairly directly from the setup once phantom expectations are defined.

That said, the paper addresses a genuinely important question---how to model human-AI strategic interaction---and provides a tractable framework with clear predictions. The timing is excellent given the rapid deployment of AI systems in economic contexts. I recommend major revision with attention to the issues below.

---

## Major Comments (must address)

### 1. The attribution function needs sharper empirical grounding

The attribution function is the key primitive that distinguishes ABE from standard psychological game theory, yet Section 2.5 presents three approaches (behavioral, signal-based, dispositional) without guidance on which applies when. The linear example (Equation 8) is useful but appears chosen for tractability rather than empirical validity.

**Required**: Either (a) provide evidence that linear attribution is empirically reasonable, citing specific studies that measure how attributed beliefs respond to prosociality parameters and anthropomorphic signals; or (b) weaken the claims to acknowledge this is a modeling choice whose empirical content remains to be established. The current presentation suggests more precision than the empirical literature supports.

### 2. Clarify the relationship between anthropomorphism and attenuation

The paper treats anthropomorphism (omega) and attenuation (lambda) as separate parameters, but the psychology literature suggests they may be related. Gray et al. (2007) decompose mind perception into agency and experience dimensions; agency drives attribution while experience drives moral concern. The paper acknowledges this (lines 183-188) but does not incorporate it formally.

**Required**: Either (a) model the omega-lambda relationship explicitly, perhaps as lambda = f(omega) for some function derived from the two-dimensional mind perception framework; or (b) provide a clear justification for treating them as independent parameters, including discussion of what patterns this independence allows that a constrained specification would rule out.

### 3. The existence theorem needs more precise statement

Theorem 1 states existence "under Assumptions A1-A3" but the proof sketch in Section 3.2 is informal. The full proof in Appendix A.1 is more complete but still leaves gaps. Specifically:

- The claim that "attributed beliefs are pinned down by the attribution function" is true, but the proof should explicitly verify that phi_i(theta_j, x_j, omega_i) lies in Delta(S_i) for all inputs (this requires A2 but is not stated).
- The continuity argument in Step 3 of the proof relies on A1 for continuity of psi_i in beliefs, but A1 only states "payoff functions are continuous" without specifying the topology on belief spaces.

**Required**: State precisely what topology is assumed on belief spaces, and verify explicitly that the attributed beliefs produced by phi are valid probability distributions.

### 4. Proposition 4 (multiplicity) conditions are too weak

The proposition states that different attribution functions sustain different equilibria under conditions (i)-(iii), but condition (iii)---"best-response separation"---is essentially the conclusion restated as an assumption. This makes the proposition nearly tautological.

**Required**: Either (a) provide primitive conditions on the game structure that guarantee best-response separation (e.g., conditions on the curvature of utility functions); or (b) acknowledge explicitly that the proposition is a possibility result rather than a characterization, and provide conditions under which multiplicity does NOT arise.

### 5. The welfare measure choice needs justification

Section 5.1 defines social welfare as the sum of material payoffs, treating psychological payoffs as "instrumental." This is a normative choice with significant implications. If humans value avoiding guilt intrinsically, then phantom expectations create real welfare losses even when material outcomes are unchanged. The paper acknowledges extended welfare W^ext but gives priority to material welfare W without justification.

**Required**: Provide explicit justification for the welfarist position taken. This could involve (a) arguing that psychological payoffs represent decision utility rather than experienced utility; (b) appealing to revealed preference arguments about what social planners should maximize; or (c) presenting results under both measures and discussing which assumptions favor each.

---

## Minor Comments (suggestions for improvement)

### Presentation

1. The paper is long (40+ pages plus appendix). Consider moving some material to a supplementary appendix, particularly the detailed numerical examples in Section 3.4 and some of the proofs.

2. The notation shifts between subscript conventions (i, j for generic players vs. H, A for human/AI). While Remark 8 acknowledges this, consistent notation throughout would improve readability.

3. The literature review in the introduction is comprehensive but somewhat diffuse. Consider organizing it more tightly around the specific technical contributions the paper makes.

### Technical points

4. The rational attribution benchmark (Remark 1) defines rational attribution as omega_i = 0, but this seems to conflate "rational" with "non-anthropomorphic." A Bayesian agent might rationally infer AI expectations from observed behavior even with omega > 0. Consider renaming this the "non-anthropomorphic benchmark" to avoid confusion.

5. Proposition 3 establishes equivalence with Bayesian games under rational attribution, but the construction of the equivalent game Gamma^B uses the candidate equilibrium sigma* in the payoff function (Equation 29). This equilibrium-dependence should be flagged more prominently as it limits the proposition's usefulness for predicting behavior.

6. The comparative statics in Proposition 10 (Parts i vs. iii showing opposite signs for dx*/dm) are interesting but the intuition could be sharper. The threshold-finding vs. marginal-balancing distinction is mentioned but deserves more development.

### Applications

7. The trust game application assumes the AI is the trustor and human is the trustee. The reverse case (human trustor, AI trustee) is also empirically relevant and may have different implications. Brief discussion would strengthen the section.

8. The coordination game application treats expectation conformity as the psychological mechanism. This is plausible but differs from standard treatments that emphasize risk dominance or payoff dominance. A sentence relating your approach to these standard concepts would help.

### Empirical predictions

9. The paper generates testable predictions but does not discuss experimental designs that could test them. A brief discussion of how one might measure attributed beliefs (perhaps through incentivized belief elicitation about AI "expectations") would increase the paper's empirical relevance.

---

## Confidential Comments to Editor

**Recommendation**: Major Revision

This is a competent theory paper addressing an important emerging topic. The core framework is sound and the welfare analysis offers genuine insight. However, the paper reads more as an application of existing psychological game theory machinery to a new domain than as a fundamental theoretical advance. The attribution function is doing the heavy lifting, but it is introduced as a primitive rather than derived from deeper principles.

The major comments above identify issues that must be addressed for publication. The most important are (1) grounding the attribution function empirically and (2) justifying the welfare measure. If the author can address these convincingly, the paper would be suitable for GEB. If the revisions reveal that the framework depends critically on unobservable parameters (the attribution function), the contribution may be more limited than the current draft suggests.

The paper is well-positioned relative to the literature and the timing is excellent. I would be happy to see a revised version.
