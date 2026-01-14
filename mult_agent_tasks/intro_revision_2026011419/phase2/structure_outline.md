# Introduction Structure Outline

## Target: ~2,500 words (current ~2,800)

---

## SECTION 1: Opening (Motivation and Problem)

**Target: 350 words | 2 paragraphs**

### Paragraph 1: The Challenge (~175 words)

**Key points to include:**
- AI transforms economic life (cite Kaplan, Maslej, Acemoglu)
- Humans interact with AI as collaborators, counterparties, competitors
- The core problem: dual psychological asymmetry
  - Humans experience belief-dependent preferences (guilt, reciprocity, indignation)
  - AI have design-dependent objectives, no mental states
- Existing psychological game theory cannot accommodate this heterogeneity

**Phrasing suggestion:**
> "Artificial intelligence transforms economic and social life. Humans increasingly interact with AI agents---as collaborators, counterparties, and competitors---creating a dual psychological asymmetry. Humans experience belief-dependent emotions: guilt from disappointing expectations, reciprocity from perceived intentions, indignation from violated trust. AI optimize programmed objectives without mental states. Existing psychological game theory assumes symmetric belief-dependent agents and cannot accommodate this heterogeneity."

**What to remove from current intro:**
- Keep this paragraph largely intact; it is well-written

**Emphatic ending:** "cannot accommodate this heterogeneity"

---

### Paragraph 2: Empirical Regularities (~175 words)

**Key points to include:**
- Anthropomorphism: humans attribute mental states to non-human agents
  - SEEK framework: agent knowledge, effectance, sociality (Epley 2007)
  - Meta-analysis: 97 effect sizes show increased trust/cooperation (Blut 2021)
- Attenuation: moral emotions weaker toward AI than humans
  - Less guilt exploiting machines (De Melo 2017)
  - Less outrage at algorithmic discrimination (Bigman 2023)
  - Cross-cultural variation: Japan vs. West (Karpus 2025)
  - Design-dependent: emotional expressions restore guilt

**Phrasing suggestion:**
> "Two empirical regularities complicate matters. First, anthropomorphism: humans attribute beliefs, intentions, and expectations to non-human agents. A meta-analysis of 97 effect sizes shows anthropomorphism increases trust and cooperation in human-AI contexts. Second, attenuation: moral emotions are weaker toward AI than toward humans. Humans feel less guilt exploiting machines and less outrage when algorithms discriminate. Attenuation varies culturally---Japanese participants exhibit guilt toward robots comparable to guilt toward humans, while Western participants show strong attenuation---and is design-dependent: AI expressing distress partially restores guilt."

**What to remove from current intro:**
- Remove the SEEK framework details (elicited agent knowledge, effectance motivation, sociality needs)---defer to literature section
- Keep cross-cultural specifics (good empirical grounding)

**Emphatic ending:** "partially restores guilt"

---

## SECTION 2: Core Innovation (ABE Concept)

**Target: 400 words | 2-3 paragraphs**

### Paragraph 3: ABE Introduction (~150 words)

**Key points to include:**
- Introduce Attributed Belief Equilibrium (ABE)
- Extends psychological game theory to human-AI games
- Central insight: humans *attribute* mental states to AI
- Attributed beliefs trigger psychological responses (guilt, indignation)
- These responses operate as in purely human interaction

**Phrasing suggestion:**
> "We introduce Attributed Belief Equilibrium (ABE) to address this dual asymmetry. ABE extends psychological game theory to games where humans experience psychological payoffs from beliefs about beliefs, while AI optimize programmed objectives. The central insight is that humans attribute mental states to AI: they form beliefs about what AI 'expect' or 'believe,' and these attributed beliefs trigger psychological responses---guilt from disappointing attributed expectations, indignation from perceived violations---that parallel purely human interaction."

**What to remove from current intro:**
- Keep this paragraph structure
- Remove footnote with Epley/Waytz citations (move to literature section)

**Emphatic ending:** "parallel purely human interaction"

---

### Paragraph 4: Attribution and Attenuation Mechanisms (~150 words)

**Key points to include:**
- Attribution function: how humans form beliefs about AI expectations
  - Depends on AI design parameters (prosociality level)
  - Depends on observable signals (interface, behavioral cues)
  - Depends on human's anthropomorphism tendency
- Attenuation parameters: scale emotional intensity toward AI
  - Range from full attenuation (no emotion toward AI) to no attenuation (equal to human-directed)
- Consistency conditions differ from genuine beliefs
  - Need not correspond to actual AI mental states
  - Only to what humans project given AI characteristics

**Phrasing suggestion:**
> "The attribution function captures how humans form beliefs about AI expectations based on three inputs: AI design parameters such as prosociality level, observable signals including interface and behavioral cues, and the human's anthropomorphism tendency. Attenuation parameters scale emotional intensity toward AI, ranging from no attenuation (emotions equal to human-directed) to full attenuation (no emotion toward AI). These attributed beliefs satisfy different consistency conditions than genuine beliefs: they need not correspond to any actual AI mental state, only to what the human projects given AI characteristics."

**What to remove from current intro:**
- REMOVE: The equation $\tilde{h}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$
- REMOVE: Notation $\theta_j$, $x_j$, $\omega_i$, $\lambda^{\text{GUILT}}$, $\lambda^{\text{IND}} \in [0,1]$
- REMOVE: Technical details about mind perception (voice, gaze, movement)---move to literature

**Emphatic ending:** "what the human projects given AI characteristics"

---

### Paragraph 5: Psychological Foundations Connection (~100 words)

**Key points to include:**
- Connect to mind perception theory (Gray 2007)
- Agency vs. Experience dimensions
  - Agency triggers attribution (capacity to act)
  - Experience triggers attenuation (capacity to feel)
- AI: high agency, low experience
  - Explains why attribution forms but emotions attenuate

**Phrasing suggestion:**
> "This structure reflects mind perception theory. Humans perceive AI as having agency---capacity to act and form intentions---but lacking experience---capacity to feel and suffer. Agency drives attribution: humans form beliefs about AI expectations. Low perceived experience drives attenuation: moral emotions weaken when the target lacks capacity to suffer. The asymmetry between agency and experience explains why attribution and attenuation coexist."

**What to remove from current intro:**
- This is NEW content from the gap analysis
- Draws on main body Section 2.5.2 (Psychological Foundations)

**Emphatic ending:** "why attribution and attenuation coexist"

---

## SECTION 3: Results Preview

**Target: 650 words | 5 clusters, ~130 words each**

### Results Cluster 1: Existence (~100 words)

**Proposition coverage:** Theorem 1

**Key points:**
- ABE exists under regularity conditions
- Proof extends fixed-point arguments to dual belief structures
  - Genuine beliefs about humans
  - Attributed beliefs about AI

**Phrasing suggestion:**
> "First, existence: under regularity conditions on strategy spaces, utilities, and attribution functions, ABE exists (Theorem 1). The proof extends fixed-point arguments to dual belief structures---genuine beliefs about humans, attributed beliefs about AI."

**What to remove:** None needed

---

### Results Cluster 2: Nesting (~150 words)

**Proposition coverage:** Propositions 1-3, Definition of RAE

**Key points:**
- ABE reduces to standard frameworks as special cases
- All human players: ABE = Psychological Nash Equilibrium (Prop 1)
- No psychological payoffs: ABE = Nash equilibrium (Prop 2)
- Rational attribution: ABE = Bayes-Nash equilibrium (Prop 3)
- Zero-anthropomorphism benchmark: baseline absent bias
- Rational Attribution Equilibrium (RAE): attribution correctly projects equilibrium play
- RAE is distinct from zero-anthropomorphism benchmark

**Phrasing suggestion:**
> "Second, nesting: ABE reduces to standard frameworks as special cases. When all players are human, ABE coincides with psychological Nash equilibrium (Proposition 1). When psychological payoffs vanish, ABE strategies coincide with Nash equilibria (Proposition 2). When attribution is rational---humans correctly anticipate AI behavior given design parameters---ABE reduces to Bayes-Nash equilibrium with type uncertainty (Proposition 3). These reductions establish ABE as a proper generalization. The zero-anthropomorphism benchmark identifies what humans would attribute absent anthropomorphic bias. The Rational Attribution Equilibrium refines this: attributed beliefs equal equilibrium strategies. These are distinct concepts---zero-anthropomorphism is descriptive, while rational attribution is an equilibrium refinement."

**What to remove from current intro:**
- REMOVE: Notation $N_A = \emptyset$, $\psi_i \equiv 0$
- REMOVE: Notation $\tilde{h}_i^{(2,j),\text{ZA}} = \phi_i(\theta_j, x_j, 0)$
- ADD: Clearer distinction between zero-anthropomorphism and RAE (currently conflated)

---

### Results Cluster 3: Multiplicity (~130 words)

**Proposition coverage:** Proposition 4

**Key points:**
- Different attribution functions sustain different equilibria
- Same material game, different outcomes
- Trust game example: anthropomorphism above threshold elevates expectations
- Interface design as equilibrium selection device
- Consistent with absent betrayal aversion toward computers

**Phrasing suggestion:**
> "Third, multiplicity: different attribution functions sustain different equilibria in the same material game (Proposition 4). In a trust game with AI trustor and human trustee, anthropomorphism above the cooperation threshold elevates attributed expectations, increasing guilt and equilibrium returns. Below this threshold, attributed beliefs attenuate, reducing psychological pressure. Interface design and behavioral presentation serve as equilibrium selection devices through the attribution channel. This is consistent with absent betrayal aversion toward computers documented in prior work."

**What to remove:** None needed; this is well-written

---

### Results Cluster 4: Applications (~130 words)

**Proposition coverage:** Propositions 5-7

**Key points:**
- Trust games: anthropomorphism determines equilibrium returns
  - Returns equal attributed expectation or maximum feasible, whichever is lower
- Public goods: dual effects of AI population share
  - Diluted material returns reduce cooperation
  - Elevated attributed expectations increase cooperation
  - Net effect depends on indignation attenuation (cross-cultural variation)
- Coordination games: AI as focal point
  - Humans experience pressure to match attributed expectations
  - Resolves equilibrium multiplicity

**Phrasing suggestion:**
> "Fourth, applications: the framework generates testable predictions in canonical games (Propositions 5-7). In trust games, anthropomorphism determines equilibrium returns: the return equals either the attributed expectation or the maximum feasible return, whichever is lower. In public goods, increasing AI population share has dual effects: diluted material returns reduce cooperation; elevated attributed expectations increase it. The net effect depends on indignation attenuation, which varies cross-culturally. In coordination games, AI serves as focal point through expectation conformity: humans experience psychological pressure to match attributed expectations, resolving equilibrium multiplicity."

**What to remove from current intro:**
- REMOVE: Equation $y^* = \min\{\tilde{h}_H^{(2,A)}, 3x\}$
- REMOVE: Notation $\lambda_i^{\text{IND}}$

---

### Results Cluster 5: Welfare and Design (~200 words)

**Proposition coverage:** Propositions 8-10, Proposition 10', Corollaries 2-3

**Key points:**
- Anthropomorphism has asymmetric welfare effects depending on AI objectives
- Prosocial AI: higher anthropomorphism weakly increases welfare (Prop 8)
- Elevated anthropomorphism: improves welfare when inducing regime switch (Prop 9)
- Materialist AI: anthropomorphism creates phantom expectations
  - Attributed expectations to agents that neither expect nor care
  - Guilt from disappointing nonexistent expectations---pure welfare loss
- Optimal design principles (Prop 10):
  - Prosocial AI: minimal signaling to induce cooperation (threshold-finding)
  - Materialist AI: mechanical presentation (zero signaling)
  - Mixed AI: intermediate signaling (marginal-balancing)
- Extended welfare analysis (Prop 10', Corollaries 2-3):
  - Material vs. extended welfare may diverge when phantom expectations arise
  - Measures agree when expectations don't exceed feasibility
- Private over-anthropomorphization: case for transparency regulation

**Phrasing suggestion:**
> "Fifth, welfare and design: anthropomorphism has asymmetric welfare effects depending on AI objectives (Propositions 8-9). With prosocial AI, higher anthropomorphism weakly increases welfare by elevating cooperation-inducing expectations. Elevated anthropomorphism---attributed beliefs exceeding the zero-anthropomorphism benchmark---improves welfare further when it triggers a shift from defection to cooperation. With materialist AI, anthropomorphism creates phantom expectations: humans attribute expectations to agents that neither expect nor care. When phantom expectations exceed feasible returns, humans incur guilt from disappointing agents holding no such expectations---a pure welfare loss.

> These welfare effects yield design principles (Propositions 10 and 10'). Prosocial AI should use minimal anthropomorphic signaling sufficient to induce cooperation---a threshold-finding objective. Higher cooperation efficiency reduces required signaling. Materialist AI should use mechanical presentation---any positive signal creates phantom expectations reducing welfare. Mixed objectives face a tradeoff: intermediate signaling balances cooperation benefits against guilt costs. Material and extended welfare measures agree when expectations stay below feasibility but diverge when phantom expectations arise (Corollaries 2-3). Private designers may over-anthropomorphize materialist AI to increase engagement, externalizing psychological costs---a case for transparency regulation."

**What to remove from current intro:**
- REMOVE: All notation in welfare paragraph: $x^* = x_{\text{crit}}$, $\partial x^*/\partial m < 0$, etc.
- REMOVE: Notation $\tilde{h}_i^{(2,j)} > \tilde{h}_i^{(2,j),\text{ZA}}$
- ADD: Reference to Proposition 10' and Corollaries 2-3 (currently missing)
- ADD: Material vs. extended welfare distinction

---

### Attenuation Paragraph (Moved Earlier or Integrated)

**Current location:** Line 29, between applications and welfare

**Problem:** Interrupts flow between applications and welfare

**Recommendation:** Integrate attenuation specifics into Opening Section (Paragraph 2) and Welfare Section

**Key content to redistribute:**
- Cross-cultural specifics (Japan vs. West) -> Opening Paragraph 2
- "Twice the rate" exploitation statistic -> Opening Paragraph 2
- "Attenuation cuts both ways" insight -> Welfare cluster

**What to remove:** Delete standalone attenuation paragraph; content absorbed elsewhere

---

## SECTION 4: Related Literature

**Target: 550 words | 4 paragraphs (~140 words each)**

### Literature 1: Psychological Game Theory (~150 words)

**Key points:**
- GPS 1989: payoffs depend on beliefs about beliefs
- Battigalli-Dufwenberg 2009: dynamic extension
- Standard belief hierarchies (Mertens-Zamir)
- Our departure: asymmetric player types
- Attribution function replaces belief consistency for AI
- Framework nests standard theories (Props 1-3)
- Complements behavioral game theory (systematic belief biases vs. noisy responses)

**What to remove from current intro:**
- Trim detailed discussion of QRE comparison (currently too long)
- Keep nesting discussion but verbalize

---

### Literature 2: AI and Strategic Behavior (~120 words)

**Key points:**
- Mei et al.: LLMs behave like humans, more prosocial
- Rahwan: AI as social actors
- Horton: LLMs simulate human responses
- Gap: documents relevance but lacks game-theoretic foundations
- We provide equilibrium concepts with testable predictions
- Phantom expectations connect to AI alignment

**What to remove from current intro:**
- Keep mostly intact; concise and well-positioned

---

### Literature 3: Anthropomorphism and Mind Perception (~150 words)

**Key points:**
- SEEK framework (Epley 2007)---NOW INCLUDE DETAILS HERE
- Computers as social actors (Nass 2000)
- Agency vs. Experience dimensions (Gray 2007)
- Agency triggers attribution; Experience triggers attenuation
- Cross-cultural variation (Karpus 2025)
- Attenuation parameters formalize these findings
- Dual-process interpretation: explains belief revision puzzle

**What to ADD from gap analysis:**
- SEEK framework mapping to model parameters
- Dual-process interpretation (System 1/2)
- Belief revision puzzle: why humans don't correct phantom expectations

**What to remove from current intro:**
- Move SEEK details from opening to this section
- Tighten list of design features (voice, gaze, movement)

---

### Literature 4: Evolutionary Game Theory (~100 words)

**Key points:**
- Young: stochastic stability with heterogeneous learning
- Cross-cultural variation suggests culturally evolved traits
- Anthropomorphism adaptive in human-only environments
- Creates vulnerability to phantom expectations with materialist AI
- Companion paper: evolutionary extension

**What to remove from current intro:**
- Keep brief; currently appropriate length
- Could cut entirely if space needed

---

## SECTION 5: Outline

**Target: 100 words | 1 paragraph**

**Key points:**
- Section 2: Framework (asymmetric games, attribution, attenuation)
- Section 3: Equilibrium (ABE definition, existence, nesting, multiplicity)
- Section 4: Applications (trust, public goods, coordination)
- Section 5: Welfare (effects of anthropomorphism, optimal design)
- Section 6: Conclusion

**What to remove from current intro:**
- Keep as is; well-structured

---

## Summary of Changes

### Must Remove (Notation)

| Current | Action |
|---------|--------|
| $\tilde{h}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$ | Verbalize |
| $\theta_j$, $x_j$, $\omega_i$ | Replace with words |
| $\lambda^{\text{GUILT}}, \lambda^{\text{IND}} \in [0,1]$ | Verbalize |
| $\tilde{h}_i^{(2,j),\text{ZA}} = \phi_i(\theta_j, x_j, 0)$ | Verbalize |
| $N_A = \emptyset$, $\psi_i \equiv 0$ | Verbalize |
| $y^* = \min\{\tilde{h}_H^{(2,A)}, 3x\}$ | Verbalize |
| $x^* = x_{\text{crit}}$, comparative statics | Verbalize |

### Must Add (Missing Content)

| Content | Location |
|---------|----------|
| RAE as distinct concept | Results Cluster 2 |
| Proposition 10' (Extended Welfare) | Results Cluster 5 |
| Corollaries 2-3 (Welfare Agreement/Divergence) | Results Cluster 5 |
| Agency vs. Experience distinction | Core Innovation (Paragraph 5) |
| SEEK framework details | Literature Section 3 |
| Belief revision puzzle | Literature Section 3 |

### Structural Reorganization

| Change | Rationale |
|--------|-----------|
| Move attenuation paragraph content | Currently interrupts flow |
| Add psychological foundations paragraph | Connects to main body Section 2.5.2 |
| Expand welfare discussion | Propositions 8-10, 10', Corollaries now richer |
| Clarify RAE vs. zero-anthropomorphism | Currently conflated |

---

## Word Count Targets

| Section | Current (est.) | Target |
|---------|---------------|--------|
| Opening | 400 | 350 |
| Core Innovation | 350 | 400 |
| Results Preview | 750 | 650 |
| Attenuation | 200 | 0 (absorbed) |
| Related Literature | 900 | 550 |
| Outline | 100 | 100 |
| **Total** | **2,700** | **2,050** |

Note: Target allows buffer of ~450 words for flexibility. Final target: 2,500 words.

---

## Goyal-Style Checklist

- [ ] Economy: Every word earns its place
- [ ] Specificity: Numbers over adjectives ("97 effect sizes," "twice the rate")
- [ ] Directness: Active voice, findings first
- [ ] Emphatic endings: Each paragraph ends on strongest point
- [ ] Simplicity: No unexplained jargon
- [ ] Transitional: Each paragraph builds on previous

---

*Document prepared: January 14, 2026*
*Purpose: Structure outline for introduction revision*
