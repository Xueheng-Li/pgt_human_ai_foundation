# Literature Review: Existence Proofs for Psychological Game Equilibria

> Research for proving Theorem 1 (Existence of ABE)
> Date: 2026-01-12

---

## Executive Summary

This review synthesizes approaches to proving existence of equilibria in psychological games, focusing on techniques applicable to Attributed Belief Equilibrium (ABE). The key insight: **ABE is structurally simpler than standard psychological equilibrium** because attributed beliefs toward AI are pinned down by the attribution function, not determined endogenously by equilibrium conditions.

---

## 1. Standard Approaches in Psychological Games

### 1.1 GPS (1989) - The Foundation

**Source:** Geanakoplos, Pearce & Stacchetti (1989), *Games and Economic Behavior* 1(1): 60-79

**Key Results:**
- Defined psychological equilibrium where beliefs correspond to reality
- Showed backward induction fails in psychological games
- **Existence theorem:** Subgame perfect and sequential psychological equilibria always exist

**Proof Approach:**
- Payoffs depend on beliefs, which themselves become strategic variables
- The space of consistent belief hierarchies forms a compact convex set
- Best-response correspondences are defined over strategy-belief pairs
- Fixed-point argument applied to joint correspondence

**Critical Quote from Abstract:** "Although backward induction cannot be applied, and 'perfect' psychological equilibria may not exist, subgame perfect and sequential equilibria always do exist."

### 1.2 BD (2009) - Dynamic Extension

**Source:** Battigalli & Dufwenberg (2009), *Journal of Economic Theory* 144: 1-35

**Key Innovations:**
1. Extended GPS to dynamic multi-stage settings
2. Incorporated updated higher-order beliefs
3. Handled belief-dependent motivation more generally

**Existence Approach:**
- Work in the product space of strategies and belief hierarchies
- Belief hierarchies satisfy coherence conditions (consistency)
- Continuity of payoffs in beliefs ensures upper hemicontinuity of best-response
- Fixed-point via Kakutani's theorem on compact convex domain

**Conditions for Existence (extracted from BD 2009):**
1. Finite strategy spaces (or compact with continuous payoffs)
2. Belief hierarchies form a compact space with appropriate topology
3. Utility continuous in actions and beliefs
4. Best-response correspondences non-empty, convex-valued, upper hemicontinuous

---

## 2. Kakutani Fixed-Point Theorem Applications

### 2.1 Standard Approach for Nash Equilibrium

**The Template (from search results):**

> "The best-response correspondence that maps a strategy of one player into the nonempty, compact set of best-response strategies of the other player is upper hemicontinuous. By Kakutani's fixed point theorem, there exists a fixed point of the joint best-response correspondence."
> -- Arxiv paper on Trust-Building Game (2024)

**Kakutani's Fixed-Point Theorem Requirements:**
1. **Non-empty, compact, convex domain** $X$
2. **Correspondence** $F: X \rightrightarrows X$
3. $F(x)$ is **non-empty and convex** for all $x$
4. $F$ is **upper hemicontinuous**

### 2.2 Conditions for Upper Hemicontinuity

From the literature, upper hemicontinuity of best-response correspondences requires:

1. **Continuity of payoffs:** If $u_i(s_i, s_{-i}, h_i)$ is continuous in all arguments, then argmax varies continuously (upper hemicontinuously)

2. **Compactness of strategy space:** Finite strategies trivially satisfy this; for continuous strategies, need compact action spaces

3. **For psychological games specifically:** Continuity of psychological payoff $\psi_i$ in beliefs $h_i$ is the key condition

### 2.3 The Maximum Theorem (Berge)

The Maximum Theorem guarantees:
- If $f(x, a)$ is continuous and the constraint correspondence $A(x)$ is continuous, then:
  - The value function $V(x) = \max_{a \in A(x)} f(x, a)$ is continuous
  - The argmax correspondence $a^*(x)$ is upper hemicontinuous

This directly implies upper hemicontinuity of best-response when payoffs are continuous.

---

## 3. Belief Hierarchy Treatment in Fixed-Point Construction

### 3.1 The Standard Problem

In psychological games, beliefs are:
- **Endogenous:** Determined in equilibrium
- **Higher-order:** Must be mutually consistent across players
- **Infinite-dimensional:** Hierarchies of beliefs about beliefs about beliefs...

### 3.2 How GPS/BD Handle This

**Step 1: Universal Type Space**
- Construct the space of all consistent belief hierarchies
- This is compact under the appropriate topology (Mertens-Zamir construction)

**Step 2: Strategy-Belief Pair**
- Work in the product space $\Sigma \times \mathcal{H}$ where:
  - $\Sigma = \prod_i \Delta(S_i)$ is the space of mixed strategy profiles
  - $\mathcal{H} = \prod_i \mathcal{H}_i$ is the space of belief hierarchies

**Step 3: Consistency Mapping**
- Define a mapping $\Phi: \Sigma \to \mathcal{H}$ that generates consistent beliefs from strategies
- In equilibrium: if players use $\sigma$, then beliefs must equal $\Phi(\sigma)$

**Step 4: Best-Response Mapping**
- Define $BR: \Sigma \times \mathcal{H} \to \Sigma$ as the best-response correspondence
- A fixed point $(σ^*, h^*)$ satisfies:
  - $\sigma^* \in BR(\sigma^*, h^*)$ (optimality)
  - $h^* = \Phi(\sigma^*)$ (consistency)

### 3.3 Key Simplification for ABE

**Critical observation:** In ABE, attributed beliefs about AI are NOT endogenous equilibrium objects. They are determined by:

$$\tilde{h}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$$

This is a **function**, not an equilibrium condition. The attribution function $\phi_i$ is:
- Given exogenously (part of the model primitives)
- Continuous by Assumption A2
- Independent of the equilibrium strategy profile

**Implication:** The fixed-point problem in ABE is **simpler** than in standard PGT because:
1. Fewer degrees of freedom in the belief system
2. Attributed beliefs don't need to satisfy complex consistency conditions
3. Only genuine beliefs (H-H) require equilibrium consistency

---

## 4. Space Construction for ABE Existence Proof

### 4.1 Proposed Domain

Define the domain $\mathcal{D} = \Sigma_H \times \Sigma_A \times \mathcal{H}^{genuine}$ where:

- $\Sigma_H = \prod_{i \in N_H} \Delta(S_i)$: Human mixed strategies
- $\Sigma_A = \prod_{j \in N_A} \Delta(S_j)$: AI mixed strategies
- $\mathcal{H}^{genuine}$: Genuine belief hierarchies (H-H only)

**Note:** Attributed beliefs $\tilde{h}$ are NOT part of the domain. They are computed from $(\theta, x, \omega)$ via $\phi$.

### 4.2 Why This Works

**Compactness:**
- $\Sigma_H$, $\Sigma_A$ are simplices (compact, convex)
- $\mathcal{H}^{genuine}$ is compact under product topology (finite players, finite strategies)

**Convexity:**
- All component spaces are convex
- Product of convex sets is convex

### 4.3 The Correspondence

Define $F: \mathcal{D} \rightrightarrows \mathcal{D}$ by:

1. **Human best-response:** Given $(\sigma_{-i}, h_i^{genuine})$, compute attributed beliefs via $\phi_i$, then:
   $$BR_i^H = \arg\max_{s_i} U_i^H(s_i, \sigma_{-i}, h_i^{genuine}, \tilde{h}_i)$$

2. **AI best-response:** Standard (no beliefs):
   $$BR_j^A = \arg\max_{s_j} U_j^A(s_j, \sigma_{-j}; \theta_j)$$

3. **Belief update:** Generate consistent beliefs from the strategy profile
   $$\Phi(\sigma) = \text{consistent beliefs given } \sigma$$

---

## 5. Conditions on Payoffs for Upper Hemicontinuity

### 5.1 Required Conditions

From the literature review, the following conditions ensure upper hemicontinuity of best-response:

**A1 (Strategy Spaces):** $S_i$ finite for all $i \in N$ (trivially compact, convex when extended to mixed strategies)

**A1' (Payoff Continuity):**
- Material payoff $\pi_i(s)$ continuous in mixed strategies
- Psychological payoff $\psi_i(s, h^{(2)}, \tilde{h}^{(2)})$ continuous in all arguments

**A2 (Attribution Continuity):** $\phi_i(\theta_j, x_j, \omega_i)$ continuous in $(\theta_j, x_j)$

**A3 (Boundedness):** $|\psi_i| \leq M$ for some $M < \infty$

### 5.2 Why These Suffice

**For human players:**
- $U_i^H = \pi_i + \psi_i$ is continuous because both components are continuous
- $\tilde{h}_i = \phi_i(...)$ is continuous by A2
- By Berge's Maximum Theorem: $BR_i^H$ is upper hemicontinuous

**For AI players:**
- $U_j^A(s; \theta_j)$ is continuous (no beliefs involved)
- Standard Nash existence argument applies

**For belief consistency:**
- The mapping $\Phi: \sigma \mapsto h^{consistent}$ is continuous
- First-order beliefs are point masses on equilibrium strategies
- Higher-order beliefs inherit continuity from lower orders

---

## 6. Key Simplifications in ABE vs. Standard PGT

| Aspect | Standard PGT | ABE |
|--------|--------------|-----|
| Second-order beliefs | All endogenous | H-H: endogenous; H-A: exogenous via $\phi$ |
| Belief consistency | For all player pairs | Only for human pairs |
| Fixed-point dimension | Full belief hierarchy space | Reduced space (no AI belief variables) |
| Existence complexity | Higher (more constraints) | Lower (fewer degrees of freedom) |

### 6.1 The Key Insight

**In ABE, the attributed beliefs $\tilde{h}_i^{(2,j)}$ don't vary with the equilibrium.**

Once we fix:
- AI design parameters $\theta_j$
- Observable signals $x_j$
- Human anthropomorphism $\omega_i$

The attributed beliefs are **constants** from the perspective of the fixed-point problem. They enter the human's utility function as fixed parameters, not as equilibrium variables.

This means:
1. We don't need to find beliefs that "match" some AI mental state
2. The consistency requirement only applies to H-H beliefs
3. The fixed-point problem has fewer constraints to satisfy

---

## 7. Proof Strategy for ABE Existence

Based on this literature review, the proof should proceed as follows:

### Step 1: Define Extended Space
Let $\mathcal{D} = \Sigma \times \mathcal{H}^{genuine}$ where $\Sigma = \Sigma_H \times \Sigma_A$.

### Step 2: Compute Attributed Beliefs
For each human $i$ and AI $j$, compute:
$$\tilde{h}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$$
These are fixed throughout the analysis.

### Step 3: Define Correspondence
$F: \mathcal{D} \rightrightarrows \mathcal{D}$ where:
- Component 1: Human best-responses (using attributed beliefs)
- Component 2: AI best-responses (standard)
- Component 3: Belief consistency mapping

### Step 4: Verify Kakutani Conditions
1. $\mathcal{D}$ is non-empty, compact, convex
2. $F(d)$ is non-empty (best responses exist)
3. $F(d)$ is convex (mixed strategies)
4. $F$ is upper hemicontinuous (from payoff continuity)

### Step 5: Conclude Existence
Kakutani's theorem guarantees a fixed point $(\sigma^*, h^*)$ which constitutes an ABE.

---

## 8. Remaining Technical Issues

### 8.1 Higher-Order Beliefs
- The current framework stops at second-order beliefs
- For full generality, may need to extend to $k$-th order for arbitrary $k$
- **Resolution:** For applications (guilt, indignation), second-order suffices

### 8.2 Dependence on AI Behavior
- Current attribution function $\phi_i$ doesn't depend on AI's observed behavior
- If attribution depends on $\sigma_j$, this creates feedback:
  $$\tilde{h}_i = \phi_i(\theta_j, x_j, \sigma_j, \omega_i)$$
- **Resolution:** If $\phi_i$ is continuous in $\sigma_j$, existence still follows

### 8.3 Mixed Human Types
- Humans may have different $\omega_i$ values
- The proof needs to handle a distribution of types
- **Resolution:** Standard Bayesian game extension (expected utilities)

---

## 9. References

### Primary Sources
1. Geanakoplos, J., Pearce, D., & Stacchetti, E. (1989). Psychological games and sequential rationality. *Games and Economic Behavior*, 1(1), 60-79.

2. Battigalli, P., & Dufwenberg, M. (2009). Dynamic psychological games. *Journal of Economic Theory*, 144(1), 1-35.

### Fixed-Point Theory
3. Kakutani, S. (1941). A generalization of Brouwer's fixed point theorem. *Duke Mathematical Journal*, 8(3), 457-459.

4. Berge, C. (1963). *Topological Spaces*. (Maximum Theorem)

### Belief Hierarchy Construction
5. Mertens, J.-F., & Zamir, S. (1985). Formulation of Bayesian analysis for games with incomplete information. *International Journal of Game Theory*, 14(1), 1-29.

6. Brandenburger, A., & Dekel, E. (1993). Hierarchies of beliefs and common knowledge. *Journal of Economic Theory*, 59(1), 189-198.

---

## 10. Next Steps for ABE Proof

1. **Formalize the domain $\mathcal{D}$** with explicit topology
2. **Write out the correspondence $F$** component by component
3. **Verify non-emptiness** of $F(d)$ for all $d$ (needs: $S_i$ finite or compactness + continuity)
4. **Verify convexity** of $F(d)$ (automatic for mixed strategies)
5. **Prove upper hemicontinuity** using Maximum Theorem + payoff continuity assumptions
6. **Apply Kakutani** and interpret fixed point as ABE

**Key advantage of ABE:** The proof is simpler than standard PGT because attributed beliefs are exogenous, reducing the dimensionality and complexity of the consistency requirements.

---

*Last updated: 2026-01-12*
