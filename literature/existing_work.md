# Literature Review: PGT and Human-AI Interaction

> Foundational papers from Zotero library
> Compiled: 2026-01-11

---

## 1. Psychological Game Theory Foundations

### 1.1 Core Theory

#### Geanakoplos, Pearce & Stacchetti (1989) - The Origin
**Title:** Psychological game and sequential rationality
**Journal:** Games and Economic Behavior, 1(1), 60-79
**Zotero Key:** EU4NZZ98

**Core Contribution:**
- Introduced psychological games where payoffs depend on beliefs about beliefs
- Defined psychological equilibrium: beliefs correspond to reality
- Showed backward induction fails, but subgame perfect and sequential equilibria exist
- Enabled modeling belief-dependent emotions (anger, surprise)

**Key Quote:** "In psychological games the payoff to each player depends not only on what every player does but also on what he thinks every player believes, and on what he thinks they believe others believe."

**Relevance to Project:** Foundation for belief hierarchy structure. Need to extend to asymmetric case where AI lacks genuine beliefs.

---

#### Battigalli & Dufwenberg (2009) - Dynamic Extension
**Title:** Dynamic psychological games
**Journal:** Journal of Economic Theory, 144, 1-35
**Zotero Key:** 33W8M5G4

**Core Contribution:**
- Extended GPS (1989) to dynamic settings
- Updated higher-order beliefs, plans of action influence motivation
- Captured sequential reciprocity, psychological forward induction, regret
- More general framework than original PGT

**Key Innovations:**
- Dynamic interactive epistemology foundation
- Beliefs of others can influence motivation
- Sequential psychological effects modeled

**Relevance to Project:** Provides tools for dynamic analysis. Multi-period human-AI interaction requires these extensions.

---

#### Battigalli & Dufwenberg (2022) - Survey/JEL
**Title:** Belief-Dependent Motivations and Psychological Game Theory
**Journal:** Journal of Economic Literature (forthcoming)
**Zotero Key:** NJZF8JVK

**Core Contribution:**
- Comprehensive survey of PGT field
- Synthesizes theory and applications
- Reviews guilt aversion, reciprocity, self-image

**Relevance to Project:** Essential reference for current state of PGT. Check what's missing for human-AI extension.

---

### 1.2 Empirical Applications

#### Charness & Dufwenberg (2006) - Promises and Partnership
**Title:** Promises and Partnership
**Journal:** Econometrica, 74(6), 1579-1601
**Zotero Key:** STQN53T4

**Core Contribution:**
- Experimental test of guilt aversion
- Communication influences beliefs → behavior
- Promises enhance trustworthy behavior
- Direct evidence for belief-dependent motivation

**Key Finding:** People strive to live up to others' expectations to avoid guilt.

**Relevance to Project:** Experimental paradigm for testing indignation/guilt. Can we replicate with AI partners?

---

#### Dufwenberg, Gächter & Hennig-Schmidt (2011) - Framing Effects
**Title:** The framing of games and the psychology of play
**Journal:** Games and Economic Behavior, 73(2), 459-478
**Zotero Key:** A94LIUXR

**Core Contribution:**
- Frames affect first- and second-order beliefs
- Beliefs affect contributions in public goods games
- Guilt aversion and reciprocity both supported

**Relevance to Project:** Framing of AI partner may affect attributed beliefs. Design implication for how to present AI.

---

#### Dufwenberg & Dufwenberg (2018) - Lies in Disguise
**Title:** Lies in disguise – a theoretical analysis of cheating
**Journal:** Journal of Economic Theory
**Zotero Key:** F93HXU9N

**Relevance to Project:** Can AI be perceived as "lying"? Attribution of deception to AI.

---

## 2. Stochastic Stability Theory

### 2.1 Core Theory

#### Li (2026) - Indignation and Cooperation Norms ⭐
**Title:** Indignation and the evolution of cooperation norms
**Journal:** Games and Economic Behavior, 155, 228-249
**Zotero Key:** V3Q34FSC

**Core Contribution:**
- First application of stochastic stability to psychological games
- Indignation sustains cooperation in long run
- Works for both global and local interaction structures
- Mobility fosters stable norms via sorting into cooperative communities

**Key Results:**
1. Indignation can sustain cooperation stochastically stably
2. Mobility allows sorting → cooperative communities grow and persist
3. Extends Young's (1993) framework to belief-dependent preferences

**Direct Foundation:** This is the paper to extend. Add AI agents to the population.

---

#### Sandholm (2010) - Orders of Limits
**Title:** Orders of limits for stationary distributions, stochastic dominance, and stochastic stability
**Journal:** Theoretical Economics, 5(1), 1-26
**Zotero Key:** RFD27Q87

**Core Contribution:**
- Characterized asymptotics when noise → 0 and population → ∞
- **Order of limits doesn't matter** (under regularity conditions)
- Introduced stochastic dominance refinement of risk dominance
- Different noisy best response rules can generate different stochastically stable states

**Key Technical Result:** Limits commute under mild conditions.

**Relevance to Project:** Critical for multi-speed analysis. When human and AI have different mutation rates, order of limits may matter again. Need to verify.

---

#### Young (2015) - Evolution of Social Norms
**Title:** The evolution of social norms
**Journal:** Annual Review of Economics, 7(1), 359-387
**Zotero Key:** LQQ4TLT6

**Core Contribution:**
- Survey of stochastic stability approach to norms
- Norms as self-enforcing patterns
- Everyone conforms, expects conformity, wants to conform

**Relevance to Project:** Conceptual framework for norm erosion when AI enters.

---

#### Wallace & Young (2015) - Handbook Chapter
**Title:** Stochastic evolutionary game dynamics
**Book:** Handbook of Game Theory, Vol. 4
**Zotero Key:** GXZ9WYJR

**Core Contribution:**
- Comprehensive treatment of stochastic stability
- 2×2 games → risk-dominant equilibrium
- Bargaining → Nash bargaining solution
- Potential games → potential-maximizing equilibrium

**Key Insight:** "Evolutionary game theory dispenses with rationality, common knowledge, and common knowledge of rationality; nevertheless, main solution concepts survive."

**Relevance to Project:** Technical reference for proof techniques.

---

## 3. Human-AI Interaction

### 3.1 AI Behavioral Economics

#### Mei, Xie, Yuan & Jackson (2024) - AI Turing Test ⭐
**Title:** A Turing test of whether AI chatbots are behaviorally similar to humans
**Journal:** PNAS, 121(9), e2313925121
**Zotero Key:** PKJVPWHI

**Core Contribution:**
- GPT-4 statistically indistinguishable from random human in behavioral games
- AI modifies behavior based on experience "as if" learning
- AI behavior distinct from average human: more altruistic/cooperative
- Acts "as if" maximizing average of own and partner's payoffs

**Key Findings:**
1. Trust, fairness, risk-aversion, cooperation tested
2. Big-5 personality survey administered
3. AI responds to framing changes
4. When distinct from humans, AI is more prosocial

**Critical Relevance:** Directly tests whether AI can be treated as strategic agent. Prosociality finding supports "spite acceleration" hypothesis.

---

### 3.2 Cooperation and Punishment

#### Li, Molleman & van Dolder (2021) - Conditional Punishment
**Title:** Do descriptive social norms drive peer punishment?
**Journal:** (Zotero Key: KLMFABYD)

**Relevance:** Conditional punishment strategies. How do these change with AI partners?

---

## 4. Related Behavioral Foundations

### 4.1 Norms and Cooperation

#### Bicchieri (2006) - Grammar of Society
**Title:** The Grammar of Society: The Nature and Dynamics of Social Norms
**Zotero Key:** UNAU6XL9

**Relevance:** Foundational work on norm formation. What happens when AI enters norm-governed interactions?

---

#### Camerer (2003) - Behavioral Game Theory
**Title:** Behavioral game theory: experiments in strategic interaction
**Zotero Key:** EVUWQ9EW

**Relevance:** Comprehensive reference for experimental methods and behavioral regularities.

---

### 4.2 Additional Sources

| Paper | Key | Relevance |
|-------|-----|-----------|
| Easley & O'Hara (2023) - Financial Market Ethics | BGN6QRD5 | PGT on networks |
| Balafoutas (2011) - Public beliefs and corruption | 65JVB4L8 | Repeated psychological games |
| Çelen et al. (2017) - On blame and reciprocity | L2KUIR5K | Blame attribution |
| Azar (2019) - Influence of PGT | JHEHH933 | Impact analysis of PGT |

---

## 5. Gaps in Literature

Based on this review, the following gaps exist:

### Gap 1: Asymmetric Belief Structures
No existing work models games where some players have genuine belief-dependent preferences and others (AI) have design-dependent objectives. This is the "attributed belief equilibrium" contribution.

### Gap 2: Heterogeneous Population Dynamics
Stochastic stability theory assumes homogeneous populations. Mixed human-AI populations with different learning rules/mutation rates unexplored.

### Gap 3: Spite Acceleration
The Mei et al. (2024) finding that AI is more prosocial, combined with imitation dynamics (JME 2025), suggests AI may accelerate spite equilibrium. No formal analysis exists.

### Gap 4: Experimental Evidence
No experiments test:
- Human punishment of AI vs human defectors
- Norm contagion from AI to humans
- Threshold effects of AI population share

---

## 6. Key Papers to Acquire

Papers not yet in Zotero but needed:

1. **Horton (2023)** - Large Language Models as Simulated Economic Agents
2. **Aher et al. (2023)** - Using Large Language Models to Simulate Multiple Humans
3. **Argyle et al. (2023)** - Out of One, Many: Using Language Models to Simulate Human Samples
4. **Recent PNAS/Science papers on human-robot cooperation**
5. **Algorithm aversion literature** (Dietvorst et al.)

---

## 7. Citation Network

```
GPS (1989) ─────────────────────────────────────┐
     │                                          │
     ▼                                          │
Battigalli & Dufwenberg (2009)                  │
     │                                          │
     ├──► Charness & Dufwenberg (2006)          │
     │                                          │
     └──► Li (2026) Indignation ◄───────────────┤
              │                                 │
              │    Young (1993) ────────────────┤
              │         │                       │
              │         ▼                       │
              │    Sandholm (2010)              │
              │         │                       │
              │         ▼                       │
              └──► THIS PROJECT: ◄──────────────┘
                   PGT + AI + Stochastic Stability
```

---

*Last updated: 2026-01-11*
