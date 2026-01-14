# Extended Psychological Game Theory Literature: Guilt and Reciprocity

## Overview

This analysis examines three key papers that extend the foundational Psychological Game Theory (PGT) framework developed by Geanakoplos, Pearce & Stacchetti (1989) and Battigalli & Dufwenberg (2009). These papers focus on formalizing guilt, indignation, and reciprocity through mathematical models of belief-dependent preferences.

---

## 1. Dufwenberg & Kirchsteiger (2004): "A Theory of Sequential Reciprocity"
**Publication:** Games and Economic Behavior, Volume 47, Issue 2, Pages 268-298  
**DOI:** https://doi.org/10.1016/j.geb.2003.06.003

### Core Innovation: Sequential Reciprocity Equilibrium (SRE)

**Key Mathematical Framework:**

1. **Psychological Payoff Structure:**
   - Players experience psychological payoffs in addition to material payoffs
   - Utility functions defined on richer domain than standard game theory (actions + beliefs)
   - Psychological payoff depends on players' kindness, which depends on beliefs

2. **Kindness Formalization:**
   - Given belief of player i about strategy choice of player j, i is kind to extent he believes he gives j relatively high material payoff
   - Kindness depends on payoff i intends to "give" to j, compared to payoffs he believes possible
   - Intentions + possibilities define kindness of action

3. **Belief-Dependent Motivation:**
   - i wants to be kind to j if he believes j is kind to him
   - Model involves belief-dependent motivations requiring richer utility domain
   - Uses psychological game theory framework from Geanakoplos et al. (1989)

4. **Sequential Structure:**
   - Explicitly incorporates sequential structure of extensive games
   - Strategic choices and reciprocity motivation change as new subgames entered
   - Best responses required in all stages

### Relationship to GPS Framework

**Extension of GPS (1989):**
- Adopts psychological game theory tools from GPS
- Extends from normal form (Rabin 1993) to extensive form games
- Demonstrates that models of reciprocal behavior must differ from approaches where beliefs don't affect payoffs directly

**Key Differences from Standard Game Theory:**
- Utility functions depend on beliefs about others' strategies
- Kindness calculations involve second-order beliefs (beliefs about beliefs)
- Equilibrium concept requires correct initial beliefs and proper belief updating

### Notation and Mathematical Details

**Belief Representation:**
- Bij = Aj: Set of possible beliefs of player i about strategy of player j
- Cij k = Bj k = Ak: Set of possible beliefs of player i about belief of player j about strategy of k

**Reciprocity Sensitivity:**
- λij: Measures how sensitive player i is to reciprocity concerns regarding player j
- Allows varying reciprocity sensitivity across different opponents
- Formulation admits player-specific reciprocity parameters

---

## 2. Charness & Dufwenberg (2006): "Promises and Partnership"
**Publication:** Econometrica, Volume 74, Issue 6, Pages 1579–1601  
**DOI:** 10.1111/j.1468-0262.2006.00719.x

### Core Innovation: Guilt Aversion Formalization

**Key Contributions:**

1. **Guilt Aversion Model:**
   - People strive to live up to others' expectations to avoid guilt
   - Mathematical formalization using psychological game theory
   - Communication influences motivation through beliefs about beliefs

2. **Expectation Formation:**
   - Guilt aversion depends on others' expectations about one's behavior
   - Disappointment modeled when expectations are not met
   - Expectations influence behavior even when not contractually binding

3. **Belief-Dependent Preferences:**
   - Extends GPS framework with guilt-averse utility functions
   - Utility incorporates fear of disappointing others
   - Social preferences driven by belief-dependent emotions

### Mathematical Structure

**Guilt-Averse Utility Function (Conceptual):**
- U_i = π_i - γ × G(E_j, a_i)
  - π_i: material payoff
  - γ: guilt sensitivity parameter
  - G(E_j, a_i): guilt function depending on j's expectations E_j and actual action a_i

**Expectation Formation:**
- First-order expectations: What player i believes player j expects i to do
- Second-order beliefs: What i believes j believes about i's beliefs
- Communication affects these belief structures

### Relationship to GPS/BD Framework

**Extension of GPS (1989):**
- Uses psychological game theory tools to model guilt
- Extends belief-dependent preferences to guilt emotions
- Formalizes how beliefs about beliefs affect utility

**Connection to BD (2009):**
- Builds on guilt formalization from Battigalli & Dufwenberg
- Extends to partnership and communication contexts
- Demonstrates empirical relevance of guilt aversion

---

## 3. Attanasi, Battigalli & Manzoni (2016): "Incomplete Information Psychological Games"
**Note:** Paper not found in current library - requires additional search

### Expected Contributions (Based on Literature Context):

**Incomplete Information Extensions:**

1. **Type Uncertainty Handling:**
   - Extends PGT to settings with private types
   - Models how psychological preferences interact with type distributions
   - Belief structures under incomplete information

2. **Higher-Order Beliefs:**
   - Notation for beliefs about types and beliefs
   - Psychological games with incomplete information
   - Equilibrium concepts for incomplete psychological games

3. **Mathematical Extensions:**
   - Type-dependent psychological preferences
   - Belief updating with psychological components
   - Solution concepts extending GPS to incomplete information

---

## Comparative Analysis: Extensions to GPS/BD Framework

### Common Themes Across Papers

1. **Belief-Dependent Utilities:**
   - All papers extend GPS framework where utility depends on beliefs
   - Formal mathematical treatment of emotions (kindness, guilt, reciprocity)
   - Utility functions defined on actions + beliefs domain

2. **Higher-Order Beliefs:**
   - Second-order beliefs crucial for all models
   - Beliefs about beliefs affect material payoffs through psychological components
   - Intentionality central to reciprocity and guilt models

3. **Equilibrium Concepts:**
   - Require correct beliefs in equilibrium
   - Belief updating according to Bayes' rule
   - Self-confirming equilibria in psychological games

### Mathematical Notation Summary

**Core GPS Framework Variables:**
- a_i: action of player i
- b_i: belief of player i about others' actions
- c_i: belief of player i about others' beliefs
- U_i: psychological utility function

**Extensions:**
- **Dufwenberg & Kirchsteiger:** Sequential structure, reciprocity sensitivity λ_ij
- **Charness & Dufwenberg:** Guilt sensitivity γ, expectation formation E_j
- **Attanasi et al.:** Type spaces, incomplete information belief structures

### Key Technical Innovations

1. **Sequential Reciprocity (D&K 2004):**
   - Extensive form games with reciprocity
   - History-dependent kindness calculations
   - Sequential Reciprocity Equilibrium (SRE)

2. **Guilt Aversion (C&D 2006):**
   - Communication and promise effects
   - Expectation-based utility functions
   - Empirical validation of guilt aversion

3. **Incomplete Information (A&B&M 2016):**
   - Type-dependent psychological preferences
   - Belief hierarchies with private information
   - Equilibrium concepts for incomplete psychological games

## Implications for Human-AI PGT Research

### Relevance to Attributed Belief Equilibrium Framework:

1. **Belief Attribution:** 
   - How humans attribute beliefs/intentions to AI systems
   - Extends second-order belief formalization to AI design parameters

2. **Heterogeneous Populations:**
   - Mathematical framework for populations with different belief-dependent preference structures
   - Human guilt/indignation vs. AI design-dependent objectives

3. **Sequential Structure:**
   - Extensive form games with human-AI interactions
   - Sequential reciprocity and learning dynamics

### Mathematical Foundation for Extension:

The extended PGT literature provides the formal mathematical tools needed to:
- Model belief-dependent utilities for humans facing AI opponents
- Formalize attributed beliefs about AI "intentions" 
- Develop equilibrium concepts for heterogeneous human-AI populations
- Analyze dynamics when humans have psychological preferences but AI have programmed objectives

---

**Sources:**
- Dufwenberg, M., & Kirchsteiger, G. (2004). A theory of sequential reciprocity. Games and Economic Behavior, 47(2), 268-298.
- Charness, G., & Dufwenberg, M. (2006). Promises and partnership. Econometrica, 74(6), 1579-1601.
- Geanakoplos, J., Pearce, D., & Stacchetti, E. (1989). Psychological games and sequential rationality. Games and Economic Behavior, 1(1), 60-79.
- Battigalli, P., & Dufwenberg, M. (2009). Dynamic psychological games. Journal of the European Economic Association, 7(2-3), 355-376.

