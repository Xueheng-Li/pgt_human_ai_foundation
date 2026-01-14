# Pilot Experiment: Human-AI Cooperation and Punishment

> Empirical test of theoretical predictions
> Collaborators to seek: Valeria Burdea, Lucas Molleman

---

## Objectives

Test three core predictions from theoretical framework:

1. **H1 (Indignation Asymmetry)**: Humans punish AI differently than humans
2. **H2 (Norm Contagion)**: AI cooperation level affects human norm internalization
3. **H3 (Threshold Effect)**: Population composition has non-linear effects

---

## Experimental Design

### Paradigm

Repeated Public Goods Game with Costly Punishment

**Standard setup**:
- 4-person groups
- Endowment: 20 tokens per round
- Contribution to public good
- MPCR = 0.4 (each token contributed returns 0.4 to each member)
- Punishment: 1 token spent reduces target by 3 tokens
- 10 rounds

### Treatment Structure (Between-subjects)

| Treatment | Composition | AI Cooperation | N groups |
|-----------|-------------|----------------|----------|
| T1: Baseline | 4 humans | N/A | 40 |
| T2: Low AI | 3H + 1A | 50% | 40 |
| T3: High AI | 3H + 1A | 90% | 40 |
| T4: Half AI | 2H + 2A | 70% | 40 |
| T5: Majority AI | 1H + 3A | 70% | 40 |

**Total**: 200 groups, 800 participants

### AI Behavior Programming

**Contribution**:
- Low AI (T2): Contribute 50% of endowment (10 tokens)
- High AI (T3): Contribute 90% of endowment (18 tokens)
- Mixed (T4, T5): Contribute 70% of endowment (14 tokens)

**Punishment**:
- AI does not punish (to isolate human punishment behavior)
- Or: AI punishes proportionally to deviation from contribution norm

### Key Manipulations

**AI disclosure**: Participants know which group members are AI

**AI appearance**: Text-based interaction (no avatar manipulation)

---

## Measures

### Primary Outcomes

#### 1. Punishment toward AI vs Humans

- **Punishment intensity**: Tokens spent punishing
- **Punishment targeting**: Conditional on defection level
- **Emotional response**: Self-reported anger/indignation (Likert scale)
- **Reaction time**: Faster = more automatic/emotional

#### 2. Norm Internalization

- **Contribution in final rounds**: After learning
- **Surprise all-human rounds**: Rounds 8-10 secretly switch to all-human
- **Post-experiment norm survey**: "How much should one contribute?"

#### 3. Threshold Effects

- Compare T2, T4, T5 for non-linear AI share effects
- Test for discontinuous jumps in cooperation

### Secondary Outcomes

- **Belief elicitation**: What do you expect others to contribute?
- **Anthropomorphism scale**: Individual difference measure
- **AI experience**: Prior interaction with AI systems

---

## Hypotheses and Predictions

### H1: Indignation Asymmetry

**Prediction**: Humans punish defecting AI *less* than defecting humans.

**Mechanism**: Lower attributed expectations toward AI → less indignation → less punishment.

**Moderator**: Anthropomorphism tendency. High anthropomorphizers should show smaller H-A gap.

**Test**:
$$\text{Punishment}_{i \to j} = \beta_0 + \beta_1 \cdot \text{AI}_j + \beta_2 \cdot \text{Defection}_j + \beta_3 \cdot \text{AI}_j \times \text{Defection}_j + \epsilon$$

Expect $\beta_3 < 0$ (interaction: less punishment for AI defection).

### H2: Norm Contagion

**Prediction**: Exposure to high-cooperation AI (T3) increases human cooperation in surprise all-human rounds, compared to low-cooperation AI (T2).

**Mechanism**: AI behavior anchors normative expectations.

**Test**:
$$\text{Contribution}_{i,\text{surprise}} = \beta_0 + \beta_1 \cdot \text{T3} + \beta_2 \cdot \text{T2} + \text{controls} + \epsilon$$

Expect $\beta_1 > \beta_2$ (higher cooperation after high-AI exposure).

### H3: Threshold Effect

**Prediction**: Discontinuous drop in human cooperation between T4 (50% AI) and T5 (75% AI).

**Mechanism**: Critical mass of AI triggers strategic exploitation mode.

**Test**:
$$\text{Contribution}_i = f(\text{AI share}) + \epsilon$$

Test for non-linearity/threshold via spline regression or structural break test.

---

## Procedure

### Timeline per Session

1. **Instructions** (10 min): Game explanation, AI disclosure
2. **Comprehension quiz** (5 min): Ensure understanding
3. **Practice rounds** (5 min): 2 rounds without punishment
4. **Main game** (25 min): 10 rounds with punishment
5. **Surprise rounds** (10 min): 3 rounds all-human (undisclosed)
6. **Belief elicitation** (5 min): Expectations about others
7. **Survey** (10 min): Anthropomorphism, AI experience, demographics
8. **Payment** (5 min): Show earnings, collect payment info

**Total**: ~75 minutes

### Platform

Online experiment via oTree or similar

**Requirements**:
- Synchronous play (real-time matching)
- AI agents implemented as bots
- Clear AI/human labeling

---

## Power Analysis

### Effect Size Assumptions

Based on prior punishment experiments:
- Punishment H-H defector: ~3 tokens
- Expected H-A gap: ~1 token (d ≈ 0.5)

### Sample Size Calculation

For between-subjects comparison (α = 0.05, power = 0.80):
- Effect size d = 0.5
- Required n per group: ~64 per cell

With 40 groups × 4 subjects = 160 per treatment (adequate for group-level analysis).

### Clustering

Account for within-group correlation in analysis (random effects).

---

## Analysis Plan

### Pre-registration

Register on AsPredicted before data collection:
- Hypotheses H1-H3
- Primary analysis specifications
- Exclusion criteria

### Primary Analysis

1. **H1**: Mixed-effects regression of punishment on target type × defection
2. **H2**: Comparison of surprise-round contributions across T2 vs T3
3. **H3**: Spline regression / threshold detection for AI share

### Secondary Analysis

1. **Structural estimation**: Estimate indignation parameter $\beta$ from punishment data
2. **Heterogeneity**: Anthropomorphism as moderator
3. **Dynamics**: Learning over rounds

### Exploratory

- Mediation via beliefs
- AI experience effects
- Gender differences

---

## Budget Estimate

| Item | Cost |
|------|------|
| Participant payment (800 × $15) | $12,000 |
| Platform fees | $500 |
| Research assistant | $2,000 |
| Contingency (10%) | $1,450 |
| **Total** | **$15,950** |

---

## Potential Collaborators

### Valeria Burdea (Exeter)
- Expertise: Experimental economics, social preferences
- Prior work: Trust games, belief elicitation

### Lucas Molleman (Amsterdam)
- Expertise: Social learning, cooperation experiments
- Prior collaboration: Li, Molleman & van Dolder (2021)

### Contact Plan
1. Send project summary with theoretical framework
2. Propose co-authorship on empirical paper
3. Discuss design refinements
4. Apply for joint funding if needed

---

## Timeline

| Month | Milestone |
|-------|-----------|
| 1 | Finalize design, contact collaborators |
| 2 | Program experiment, IRB submission |
| 3 | Pilot study (n=40), refine |
| 4-5 | Main data collection |
| 6 | Analysis and write-up |

---

## Open Questions

- [ ] Should AI punish or not?
- [ ] How to handle deception concerns (AI disclosure)?
- [ ] Online vs lab: Trade-offs?
- [ ] Incentive compatibility of belief elicitation?

---

*Draft: 2026-01-11*
