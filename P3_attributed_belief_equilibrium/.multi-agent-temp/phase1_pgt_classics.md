# Foundational Psychological Game Theory Literature

## Overview

This document summarizes the foundational literature in Psychological Game Theory (PGT), focusing on the seminal contributions of Geanakoplos, Pearce & Stacchetti (1989) and Battigalli & Dufwenberg (2009). These papers establish the theoretical foundations for belief-dependent preferences and their integration into game-theoretic analysis.

---

## 1. Geanakoplos, Pearce & Stacchetti (1989): "Psychological Games and Sequential Rationality"

### Publication Details
- **Journal**: Games and Economic Behavior, Vol. 1, pp. 60-79
- **Citation**: GPS 1989
- **Significance**: Foundational paper introducing psychological game theory

### Core Innovation

GPS (1989) identified a fundamental limitation in traditional game theory: the inability to model **belief-dependent preferences**. Traditional games assume utility depends only on actions, but real decision-makers' utilities often depend on beliefs about others' intentions, expectations, and their own reputation.

### Key Theoretical Contributions

#### 1.1 Formal Framework for Psychological Games

A psychological game is defined by:
- **Action sets**: $A_1, A_2, ..., A_n$ for each player $i$
- **Payoff functions**: $u_i: A \times \Delta(A_{-i}) \rightarrow \mathbb{R}$ where $u_i$ depends on both actions and beliefs about others' actions
- **Belief structure**: Higher-order beliefs about what others believe

#### 1.2 Belief-Dependent Utilities

The key innovation is that utility functions incorporate beliefs:
$$U_i(a_i, a_{-i}, \mu_i) = \pi_i(a_i, a_{-i}) + f_i(\mu_i, a_i, a_{-i})$$

Where:
- $\pi_i(a_i, a_{-i})$: Material payoff component
- $f_i(\cdot)$: Psychological payoff component depending on beliefs $\mu_i$
- $\mu_i \in \Delta(A_{-i})$: Player i's beliefs about others' actions

#### 1.3 Second-Order Beliefs

GPS introduced the concept of **second-order beliefs** - beliefs about what others believe:
- $E_i^{(2)} \in \Delta(A_{-i})$: Player i's beliefs about others' expected actions
- These beliefs enter the utility function directly

#### 1.4 Sequential Rationality in Psychological Games

**Sequential Rationality**: At each information set, players choose actions that maximize expected utility given their beliefs and the continuation game.

**Key Equilibrium Concept**: Psychological Sequential Equilibrium (PSE)
- Actions are sequentially rational given beliefs
- Beliefs are consistent with actions through Bayes' rule where possible

### Mathematical Formalization

#### Utility Function Structure
For a two-player psychological game:
$$U_1(a_1, a_2, \mu_1) = \pi_1(a_1, a_2) + g_1(\mu_1(a_2|a_1), a_1, a_2)$$
$$U_2(a_1, a_2, \mu_2) = \pi_2(a_1, a_2) + g_2(\mu_2(a_1|a_2), a_2, a_1)$$

Where:
- $\mu_i(a_{-i}|a_i)$: Player i's belief about others' actions conditional on their own action
- $g_i(\cdot)$: Psychological component capturing emotional responses

#### Belief Consistency
Beliefs must satisfy consistency conditions:
$$\mu_i(a_{-i}) = \sum_{a_i} P(a_i) \cdot \mu_i(a_{-i}|a_i)$$

### Key Limitations of GPS (1989)

1. **Static Belief Structure**: Beliefs are fixed and don't update based on observations
2. **Limited Psychological Effects**: Only second-order beliefs enter utility
3. **No Dynamic Learning**: No mechanism for belief updating over time
4. **Simplified Emotional Responses**: Limited types of psychological payoffs

---

## 2. Battigalli & Dufwenberg (2009): "Dynamic Psychological Games"

### Publication Details
- **Journal**: Journal of Economic Theory, Vol. 144, Issue April, pp. 1-35
- **DOI**: http://dx.doi.org/10.1016/j.jet.2008.01.004
- **Significance**: Major extension enabling dynamic psychological games

### Abstract Summary
> "The motivation of decision makers who care for various emotions, intentions-based reciprocity, or the opinions of others may depend directly on beliefs (about choices, beliefs, or information). Geanakoplos, Pearce and Stacchetti (1989) point out that traditional game theory is ill-equipped to address such matters, and they pioneer a new framework which does. However, their toolbox – psychological game theory – incorporates several restrictions that rule out plausible forms of belief-dependent motivation. Building on recent work on dynamic interactive epistemology, we propose a more general framework."

### Core Innovation

BD (2009) extend psychological games to **dynamic settings** where:
1. Beliefs update based on observed actions
2. Higher-order beliefs (beliefs about beliefs) can influence utilities
3. Plans of action may depend on beliefs
4. Dynamic psychological effects are captured

### Key Theoretical Contributions

#### 2.1 Dynamic Belief-Dependent Utilities

Extended utility structure allowing for:
- **Updated beliefs**: $U_i(s_i, \mu_i^t)$ where $\mu_i^t$ are time-t beliefs
- **Higher-order beliefs**: $U_i$ depends on beliefs about others' beliefs
- **Plan-dependent motivation**: Utilities depend on planned actions

#### 2.2 Higher-Order Belief Notation

Standard notation for beliefs:
- $P_i^k$: Player i's k-th order beliefs
- $P_i^1$: First-order beliefs (beliefs about actions)
- $P_i^2$: Second-order beliefs (beliefs about beliefs)
- $P_i^3$: Third-order beliefs (beliefs about beliefs about beliefs)

#### 2.3 Dynamic Sequential Rationality

**Dynamic Sequential Rationality**: At each history, players choose actions/continuation plans that maximize expected utility given their current beliefs and the structure of the continuation game.

### Mathematical Formalization

#### Extended Utility Function
$$U_i(h^t, \mu_i^t, \sigma_i^{t+1}) = \pi_i(\sigma_i^{t+1}, \sigma_{-i}^{t+1}) + f_i(P_i^{1,t}, P_i^{2,t}, ..., P_i^{k,t}, \sigma_i^{t+1}, \sigma_{-i}^{t+1})$$

Where:
- $h^t$: History up to time t
- $\mu_i^t$: Player i's beliefs at time t
- $\sigma_i^{t+1}$: Player i's continuation plan
- $P_i^{k,t}$: k-th order beliefs at time t

#### Belief Updating
Standard Bayesian updating:
$$P_i^{k,t+1}(a | h^t, a_i^t) = \frac{P_i^{k,t}(a) \cdot P(a_i^t | a, h^t)}{\sum_{a'} P_i^{k,t}(a') \cdot P(a_i^t | a', h^t)}$$

### Key Innovations Beyond GPS (1989)

#### 3.1 Sequential Reciprocity
- Beliefs update based on observed actions
- Utilities depend on updated beliefs about intentions
- Captures dynamic reciprocity (not just static)

#### 3.2 Psychological Forward Induction
- Players anticipate how their actions will affect others' beliefs
- Strategic considerations include psychological effects
- Forward-looking psychological reasoning

#### 3.3 Regret and Counterfactual Emotions
- Utilities can depend on beliefs about what would have happened under different actions
- Captures regret, disappointment, elation
- Counterfactual thinking about outcomes

### Equilibrium Concepts

#### 1. Psychological Sequential Equilibrium (PSE)
- Actions are sequentially rational given beliefs
- Beliefs consistent with actions via Bayes' rule
- Applies to both static and dynamic games

#### 2. Dynamic Psychological Equilibrium (DPE)
- Continuation plans are optimal given beliefs
- Beliefs update consistently
- Forward-looking psychological reasoning

### Applications and Examples

#### Trust Game with Dynamic Beliefs
- **Setup**: Player 1 (trustor) sends money to Player 2 (trustee)
- **Psychological Component**: Trustee's guilt depends on updated beliefs about trustor's expectations
- **Dynamic Effect**: Trustor's beliefs about trustee's guilt affect initial trust decision

#### Public Goods with Reciprocity
- **Setup**: Multiple players contribute to public good
- **Psychological Component**: Contributions affected by beliefs about others' contributions
- **Dynamic Effect**: Beliefs update based on observed contributions over time

---

## 3. Comparative Analysis: GPS (1989) vs. BD (2009)

### Similarities
1. **Core Premise**: Both papers address belief-dependent preferences
2. **Mathematical Framework**: Both use extended utility functions incorporating beliefs
3. **Sequential Rationality**: Both require sequential rationality given beliefs
4. **Belief Consistency**: Both require belief consistency (Bayesian where possible)

### Key Differences

| Aspect | GPS (1989) | BD (2009) |
|--------|------------|-----------|
| **Time Structure** | Static games only | Dynamic games with updating |
| **Belief Order** | Up to second-order | Arbitrary high-order beliefs |
| **Belief Updating** | Fixed beliefs | Dynamic Bayesian updating |
| **Psychological Effects** | Limited to guilt/indignation | Full range including regret, reciprocity |
| **Equilibrium Concept** | Psychological Sequential Equilibrium | Both PSE and Dynamic Psychological Equilibrium |
| **Applications** | Simple trust/reciprocity games | Complex dynamic games with learning |

### Evolution of Notation

#### GPS (1989) Notation
- $\mu_i$: Simple beliefs about actions
- $U_i(a_i, a_{-i}, \mu_i)$: Utility depending on beliefs
- $E_i^{(2)}$: Second-order beliefs (expectations)

#### BD (2009) Notation
- $P_i^k$: k-th order beliefs
- $\mu_i^t$: Time-t beliefs
- $\sigma_i^{t+1}$: Continuation plans
- $U_i(h^t, \mu_i^t, \sigma_i^{t+1})$: Dynamic utility function

---

## 4. Standard Notation for Belief-Dependent Utilities

### Core Components

#### 4.1 Basic Elements
- **Players**: $N = \{1, 2, ..., n\}$
- **Actions**: $A_i$ for player i, $A = \times_{i \in N} A_i$
- **Types**: $T_i$ for player i (if incomplete information)

#### 4.2 Belief Structure
- **First-order beliefs**: $P_i^1 \in \Delta(A_{-i})$ about others' actions
- **Second-order beliefs**: $P_i^2 \in \Delta(A_{-i} \times \Delta(A_{-i}))$ about others' beliefs
- **Higher-order beliefs**: $P_i^k$ for $k > 2$

#### 4.3 Utility Functions
**Material Component**: $\pi_i(a_i, a_{-i})$ - traditional material payoff
**Psychological Component**: $f_i(P_i^1, P_i^2, ..., P_i^k, a_i, a_{-i})$ - belief-dependent part

**Total Utility**:
$$U_i(a_i, a_{-i}, P_i^1, P_i^2, ..., P_i^k) = \pi_i(a_i, a_{-i}) + f_i(P_i^1, P_i^2, ..., P_i^k, a_i, a_{-i})$$

### Common Psychological Payoff Functions

#### 4.4 Guilt-Aversion (typical form)
$$f_i(P_i^2, a_i, a_{-i}) = -\beta_i \cdot \max\{0, E_i^{(2)}(a_{-i}^C) - a_i\}$$
Where:
- $\beta_i > 0$: Guilt sensitivity parameter
- $E_i^{(2)}(a_{-i}^C)$: Belief about others' expectations for cooperative action

#### 4.5 Indignation (typical form)
$$f_i(P_i^2, a_i, a_{-i}) = -\gamma_i \cdot \mathbf{1}_{\{a_i = D\}} \cdot P_i^1(a_{-i}^C)$$
Where:
- $\gamma_i > 0$: Indignation sensitivity parameter
- $\mathbf{1}_{\{a_i = D\}}$: Indicator for defection
- $P_i^1(a_{-i}^C)$: Belief that others will cooperate

---

## 5. Equilibrium Concepts in Psychological Games

### 5.1 Psychological Sequential Equilibrium (PSE)

**Definition**: A psychological game equilibrium where:
1. **Sequential Rationality**: At each information set, players choose actions maximizing expected utility given beliefs
2. **Belief Consistency**: Beliefs are consistent with actions through Bayes' rule where possible
3. **Self-Confirming**: On the equilibrium path, beliefs about others' actions are correct

**Mathematical Condition**:
For player i at information set I:
$$\sigma_i(I) \in \arg\max_{\sigma_i' \in \Sigma_i(I)} \sum_{a \in A} U_i(a, \sigma_{-i}(I), \mu_i(I)) \cdot \sigma_i'(a)$$

### 5.2 Dynamic Psychological Equilibrium (DPE)

**Definition**: Extends PSE to dynamic settings with:
1. **Dynamic Consistency**: Continuation plans optimal at each history
2. **Forward-Looking**: Players anticipate how actions affect future beliefs
3. **Adaptive Beliefs**: Beliefs update based on observations

**Mathematical Condition**:
At history $h^t$:
$$\sigma_i^{t+1}(h^t) \in \arg\max_{\sigma_i' \in \Sigma_i^{t+1}(h^t)} \mathbb{E}_{\sigma^{t+1}(h^t)}[U_i(h^t, \mu_i^t, \sigma')]$$

---

## 6. Implications for Human-AI Psychological Games

### 6.1 Key Insights from PGT Literature

1. **Belief Dependence**: Human utilities can depend on beliefs about AI intentions
2. **Higher-Order Beliefs**: Humans may form beliefs about AI's beliefs (even if AI has no actual beliefs)
3. **Dynamic Effects**: Beliefs about AI behavior may update over time
4. **Attribution Problem**: Humans may attribute beliefs/intentions to AI even when AI lacks them

### 6.2 Extension to Human-AI Settings

When extending PGT to human-AI games, key modifications needed:

#### Belief Attribution
- Humans may form beliefs $\tilde{P}_i^2$ about AI's "expected" actions
- These beliefs enter human utility functions
- Attribution function $\phi_i$ maps AI design parameters to human's attributed beliefs

#### Asymmetric Belief Structures
- Humans: Full belief-dependent preferences with higher-order beliefs
- AI: Design-dependent objectives (may or may not incorporate beliefs)

#### Modified Utility Structure
**Human Utility**:
$$U_i^H(a_i, a_{-i}, P_i^2, \tilde{P}_i^2) = \pi_i(a_i, a_{-i}) + f_i(P_i^2, \tilde{P}_i^2, a_i, a_{-i})$$

**AI Utility**:
$$U_j^A(a_j, a_{-j}; \theta_j) = \pi_j(a_j, a_{-j}) + g_j(\theta_j, a_j, a_{-j})$$

Where $\theta_j$ represents AI's design parameters.

---

## 7. Key Mathematical Definitions

### 7.1 Belief Spaces
- **First-order beliefs**: $P_i^1 \in \Delta(A_{-i})$
- **Second-order beliefs**: $P_i^2 \in \Delta(A_{-i} \times \Delta(A_{-i}))$
- **Higher-order beliefs**: Inductive limit of belief spaces

### 7.2 Psychological Game Definition
**Definition**: A psychological game is a tuple $(N, A, U, P)$ where:
- $N$: Set of players
- $A = \times_{i \in N} A_i$: Action profiles
- $U = \{U_i\}_{i \in N}$: Belief-dependent utility functions
- $P = \{P_i^1, P_i^2, ..., P_i^k\}_{i \in N}$: Belief structure

### 7.3 Sequential Rationality
**Definition**: Player i is sequentially rational at information set I if:
$$\sigma_i(I) \succeq_{i,I} \sigma_i' \quad \forall \sigma_i' \in \Sigma_i(I)$$

Where $\succeq_{i,I}$ is the preference relation over actions at I given beliefs.

---

## 8. Conclusion

The foundational PGT literature establishes:

1. **GPS (1989)** introduced the core concept of belief-dependent utilities with second-order beliefs
2. **BD (2009)** extended this to dynamic settings with arbitrary higher-order beliefs and updating
3. **Standard notation** includes belief spaces, psychological utility components, and equilibrium concepts
4. **Key innovation**: Utilities depend directly on beliefs, not just actions
5. **Sequential rationality** requires optimal actions given beliefs, with belief consistency

These foundations provide the framework for extending psychological games to human-AI populations, where belief attribution and asymmetric belief structures become central concerns.

---

## References

1. **Battigalli, Pierpaolo, and Martin Dufwenberg.** 2009. "Dynamic psychological games." *Journal of Economic Theory* 144 (1): 1-35. DOI: http://dx.doi.org/10.1016/j.jet.2008.01.004

2. **Geanakoplos, John, David Pearce, and Ennio Stacchetti.** 1989. "Psychological games and sequential rationality." *Games and Economic Behavior* 1 (1): 60-79.

3. **Cui, Zhi, Xueheng Li, and Chengjiang Zhang.** 2025. "Spite in imitation: Theory and experimental evidence." *Journal of Mathematical Economics* (forthcoming).

4. **Li, Xueheng.** 2026. "Indignation and the evolution of cooperation norms." *Games and Economic Behavior* (conditionally accepted).
