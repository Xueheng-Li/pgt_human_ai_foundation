# Academic Review: Introduction to "Attributed Belief Equilibrium"

**Target venue**: Econometrica / Journal of Economic Theory
**Reviewer assessment**: Referee report as for a top economics journal

---

## Summary

The paper introduces Attributed Belief Equilibrium (ABE), extending psychological game theory to human-AI interactions. The core innovation is that humans attribute mental states (beliefs, expectations) to AI agents that lack them, and these attributed beliefs trigger psychological responses (guilt, indignation) that affect strategic behavior. The framework generates predictions about trust, public goods, and coordination games, and derives optimal AI design principles based on whether AI objectives are prosocial or materialist.

## Overall Assessment

This is a well-motivated theoretical contribution addressing an important gap. The paper correctly identifies that existing psychological game theory assumes symmetric belief-dependent agents and cannot accommodate human-AI heterogeneity. The solution---allowing humans to attribute beliefs to AI and experience attenuated psychological responses---is conceptually sound and generates testable predictions.

The introduction successfully conveys the main contribution and situates it within existing literature. The economic mechanisms are clear: anthropomorphism operates through the attribution channel affecting psychological payoffs, which in turn affects equilibrium behavior. The welfare analysis connecting to AI design principles adds policy relevance.

However, the introduction could be tightened in several places, and some claims require qualification. Below I distinguish between issues that must be addressed and suggestions for improvement.

---

## Major Comments (Must Address)

### 1. Overloaded Opening Paragraph

The first paragraph attempts too much: AI transformation, dual psychological asymmetry, three different emotions (guilt, reciprocity, indignation), and a critique of existing theory. The reader encounters six citations before understanding what the paper does.

**Recommendation**: Separate the problem statement from the emotional taxonomy. Lead with the core asymmetry (humans have belief-dependent preferences; AI do not), then introduce specific emotions as examples rather than an exhaustive list.

### 2. "Dual Psychological Asymmetry" Unclear

The phrase "dual psychological asymmetry" appears without clear definition. Is this (a) asymmetry between human and AI psychology, or (b) two separate asymmetries (attribution + attenuation)? The paragraph seems to conflate these.

**Recommendation**: Define explicitly. If "dual" refers to attribution and attenuation, state this clearly: "Two asymmetries characterize human-AI interaction: humans attribute beliefs to AI (attribution), yet experience weaker emotional responses toward AI (attenuation)."

### 3. Attribution Function Lacks Economic Intuition

The attribution function is described as depending on "AI design parameters such as prosociality level, observable signals including interface and behavioral cues, and the human's anthropomorphism tendency." This is technically correct but economically opaque.

**Recommendation**: Provide a concrete example. For instance: "A chatbot designed to express concern ('I understand your frustration') generates higher attributed expectations than one providing neutral information. The attribution function formalizes how such design choices map to beliefs the human projects onto AI."

### 4. Nesting Results Need Sharper Statement

The nesting paragraph (third cluster) is confusing. It states that ABE "reduces to" PNE when all players are human, Nash when psychological payoffs vanish, and Bayes-Nash when attribution is rational. But then it introduces "zero-anthropomorphism benchmark" and "Rational Attribution Equilibrium" as distinct concepts.

**Recommendation**: The distinction between "zero-anthropomorphism benchmark" (a parameter value) and "Rational Attribution Equilibrium" (an equilibrium concept) is buried in a parenthetical. This is a key conceptual distinction deserving its own sentence. Also clarify: does RAE coincide with Bayes-Nash, or are they different?

### 5. Application Results Lack Quantitative Predictions

The applications section (fourth cluster) describes qualitative mechanisms but the testable predictions are vague. For example: "Returns increase through the guilt channel" is not testable without specifying magnitude. "Non-monotonic effects of AI population share" is testable but the prediction of direction "depending on cultural context" reduces falsifiability.

**Recommendation**: Sharpen at least one prediction. For instance: "The model predicts that in trust games, returns to AI trustees should increase with measures of anthropomorphism (e.g., Waytz et al. Mind Attribution Scale), holding AI behavior constant. The predicted elasticity is [X]."

### 6. Phantom Expectations Introduced Too Late

The concept of "phantom expectations" appears in the fifth cluster (welfare) but is central to the paper's contribution. This key term---expectations attributed to agents that hold no expectations---deserves earlier introduction and clearer motivation.

**Recommendation**: Introduce phantom expectations when first discussing attribution-attenuation asymmetry, as it directly follows from the structure: humans attribute beliefs to AI that AI does not hold, creating potential for disappointment relative to non-existent expectations.

---

## Minor Comments (Suggestions)

### 1. Empirical Magnitudes

The introduction cites several quantitative findings (e.g., "Western participants exploit robotic partners at roughly twice the rate of Japanese participants"). These are valuable. Consider adding one or two more specific numbers to anchor the theory empirically, particularly regarding the magnitude of anthropomorphism effects on cooperation.

### 2. Existing Theory Critique Could Be Gentler

The claim that psychological game theory "cannot accommodate this heterogeneity" is strong. The existing literature could potentially model human-AI interaction by treating AI as a degenerate case (zero psychological payoffs). The paper's contribution is providing a richer structure, not the first possibility of analysis.

**Suggestion**: Reframe as "existing frameworks lack tools to analyze how humans form beliefs about AI mental states, even though AI have none."

### 3. Literature Positioning: Missing Comparisons

The related literature section cites relevant work but does not clearly distinguish the paper's contribution from closest alternatives. How does ABE differ from simply modeling AI as a player type in a Bayesian game? The paper claims RAE reduces to Bayes-Nash, so what does ABE add beyond type uncertainty?

**Suggestion**: One sentence explicitly stating what ABE captures that Bayesian games cannot.

### 4. Mind Perception Paragraph Could Be Condensed

The paragraph on mind perception theory (agency vs. experience) is well-written but somewhat tangential to the game-theoretic contribution. It provides psychological foundations but interrupts the flow between model description and results.

**Suggestion**: Move to a footnote or integrate more tightly with the attribution function description.

### 5. Outline Section

The outline section is standard and functional but adds little value. Consider condensing to a single sentence or integrating with the results summary.

### 6. Terminology Consistency

The paper uses "guilt aversion," "betrayal aversion," and "expectation violation" somewhat interchangeably. While these are related concepts in the literature, explicit clarification of their relationship would help readers unfamiliar with psychological game theory.

### 7. Design Principles Paragraph Density

The welfare and design cluster (fifth) is the densest part of the introduction. It covers prosocial vs. materialist AI, threshold-finding vs. marginal-balancing objectives, material vs. extended welfare, and regulatory implications---all in one paragraph. This risks losing readers.

**Suggestion**: Either streamline to focus on one or two key insights, or break into sub-paragraphs with clearer transitions.

---

## Assessment of Quality Dimensions

| Dimension | Assessment |
|-----------|------------|
| **Contribution clarity** | Good. The main contribution (ABE as extension of psychological games to human-AI settings) is clear. The distinction between attribution and attenuation is well-motivated. |
| **Economic mechanisms** | Good. The attribution channel is clearly identified as the mechanism through which AI design affects equilibrium behavior. Guilt and indignation operate through standard psychological game channels. |
| **Literature positioning** | Adequate. Key literatures are identified and cited. The gap in existing theory is articulated. However, the paper could more sharply distinguish its contribution from Bayesian games with type uncertainty. |
| **Argumentation** | Good with minor gaps. The logical flow from problem (human-AI asymmetry) to solution (attribution function) to results is clear. Some claims could be qualified (see Major Comment 5). |
| **Accessibility** | Adequate. A general economist would understand the motivation and main results. However, some technical concepts (attribution function consistency conditions, phantom expectations) require prior familiarity with psychological games or clearer exposition. |

---

## Overall Verdict

This is a strong introduction to what appears to be a significant theoretical contribution. The paper addresses a genuine gap in the literature---the lack of game-theoretic tools for analyzing strategic interaction between belief-dependent humans and objective-optimizing AI. The solution is conceptually novel (attribution of mental states to entities lacking them) and generates testable predictions with policy relevance.

The introduction successfully conveys the main ideas but could be tightened. The major issues above concern clarity and precision rather than fundamental problems with the contribution. Addressing them would strengthen the paper's accessibility to a general economics audience.

**Recommendation**: Minor Revision

The paper merits publication after addressing the clarity issues identified above. The core contribution is sound, the mechanisms are economically meaningful, and the framework nests existing theory appropriately.

---

**Confidential Comments to Editor**

This paper makes a genuine contribution to psychological game theory by extending it to human-AI interaction. The formalization of attribution---humans projecting mental states onto AI---is novel and well-motivated. The welfare analysis connecting anthropomorphism to AI design is policy-relevant.

The introduction is dense but substantive. My main concern is accessibility: some concepts (attribution function, phantom expectations, RAE vs. zero-anthropomorphism benchmark) require more patient exposition for a general audience. The claims about testable predictions should be sharpened.

The paper would benefit from a careful revision of the introduction focusing on:
1. Clearer definition of "dual psychological asymmetry"
2. A concrete example of the attribution function in action
3. Sharper quantitative predictions
4. Earlier introduction of "phantom expectations"

These are tractable revisions. The paper should be invited to revise and resubmit.

Recommendation: **Minor Revision**
