# Detailed Proof Strategy for Theorem 1 (Existence of ABE)

> Date: 2026-01-12
> Target: Publication-quality proof for Econometrica/JET

---

## Executive Summary

This document provides a rigorous proof strategy for the existence of Attributed Belief Equilibrium (ABE). The main insight is that ABE existence is **structurally simpler** than standard psychological game equilibrium existence because attributed beliefs are exogenously determined by the attribution function---they do not need to satisfy equilibrium consistency conditions.

**Key Result**: Under Assumptions A1-A3, an ABE exists. The proof applies Kakutani's fixed-point theorem to a correspondence on the finite-dimensional strategy space $\Sigma$.

---

## Part A: Assumption Verification

### A.1 Assumption A1 (Regularity)

**Current Statement (from sec_framework.tex)**:
> (A1) Strategy spaces $S_i$ are non-empty and finite. Type spaces $T_i$ and $\Theta_j$ are non-empty, convex, and compact. Payoff functions are continuous.

**Analysis**:

1. **Sufficiency for intended purpose**:
   - Finite strategy spaces ensure $\Delta(S_i)$ is a compact, convex simplex in $\mathbb{R}^{|S_i|-1}$
   - Compactness of type spaces supports integration over types if needed
   - Continuity of payoffs is essential for Berge's Maximum Theorem

2. **Necessity assessment**:
   - Finiteness of $S_i$ can be relaxed to compactness if payoffs are continuous, but finite is standard and simplifies exposition
   - Convexity of type spaces is **not needed** for the basic existence theorem (only for parametric analysis)
   - Compactness of type spaces is **not directly used** in the existence proof but matters for extensions

3. **Implicit assumptions**:
   - **ISSUE**: The current statement says "payoff functions are continuous" but doesn't specify the domain
   - Material payoff $\pi_i$ should be continuous on $S$ (trivially satisfied for finite $S$)
   - The statement doesn't explicitly address continuity of $\psi_i$ in beliefs

4. **Recommended modifications**:

**MODIFIED A1 (Regularity)**:
> (A1a) Strategy spaces $S_i$ are non-empty and finite for all $i \in N$.
>
> (A1b) Material payoffs $\pi_i: S \to \mathbb{R}$ are well-defined.
>
> (A1c) Psychological payoffs $\psi_i: S \times \mathcal{B}_i^{(2)} \times \tilde{\mathcal{B}}_i^{(2)} \to \mathbb{R}$ are continuous in second-order beliefs, where $\mathcal{B}_i^{(2)} = \prod_{k \in N_H \setminus \{i\}} \Delta(S_i)$ and $\tilde{\mathcal{B}}_i^{(2)} = \prod_{j \in N_A} \Delta(S_i)$.

**Justification**: Splitting into sub-assumptions clarifies exactly what is needed. A1c makes explicit that psychological payoffs must be continuous in beliefs---this is the key condition for upper hemicontinuity of best-response.

---

### A.2 Assumption A2 (Attribution Continuity)

**Current Statement**:
> (A2) The attribution function $\phi_i: \Theta_j \times X \times \Omega_i \to \Delta(S_i)$ is continuous in $(\theta_j, x_j)$ for fixed $\omega_i$.

**Analysis**:

1. **Sufficiency**:
   - For the existence proof with **fixed** parameters $(\theta_j, x_j, \omega_i)$, continuity is not directly needed---the attributed belief is just a constant
   - Continuity matters for comparative statics and robustness

2. **Necessity**:
   - For existence alone, we only need that $\phi_i$ is well-defined and yields a valid probability distribution
   - Continuity is a convenience, not a necessity for existence

3. **Implicit assumptions**:
   - The codomain $\Delta(S_i)$ is correct: attributed belief is about what AI expected *human i* to do
   - **ISSUE**: Does $\phi_i$ depend on AI's observed behavior $\sigma_j$? Current specification excludes this

4. **Recommended modification**: Keep A2 as stated, but add clarifying remark:

**CLARIFICATION**: For the existence theorem, A2 can be weakened to:
> (A2') The attribution function $\phi_i$ is well-defined: for each $(\theta_j, x_j, \omega_i)$, $\phi_i(\theta_j, x_j, \omega_i) \in \Delta(S_i)$.

Continuity is restored for comparative statics applications.

---

### A.3 Assumption A3 (Bounded Psychological Payoffs)

**Current Statement**:
> (A3) There exists $M < \infty$ such that $|\psi_i(s, h_i^{(2)}, \tilde{h}_i^{(2)})| \leq M$ for all $i \in N_H$, all $s \in S$, and all beliefs.

**Analysis**:

1. **Sufficiency**:
   - Boundedness ensures $U_i^H = \pi_i + \psi_i$ is well-defined and bounded
   - Combined with continuity of $\psi_i$, ensures best-response is well-behaved

2. **Necessity**:
   - **A3 is automatically satisfied** if $\psi_i$ is continuous and belief spaces are compact
   - For finite $S$ and compact $\Delta(S_i)$, any continuous $\psi_i$ is bounded by Weierstrass
   - So A3 is **redundant** given A1c (continuity of $\psi_i$) and finiteness of $S$

3. **Implicit assumptions**: None

4. **Recommended modification**:

**Option 1**: Remove A3 entirely (it follows from A1).

**Option 2**: Keep A3 for clarity and ease of verification in applications.

**Recommendation**: Keep A3 but add remark that it is implied by A1 when $\psi_i$ is continuous.

---

### A.4 Missing Assumptions

The following assumptions are **implicit** in the proof sketch but not stated:

**A4 (Genuine Belief Consistency)**: In equilibrium, first-order beliefs equal actual strategies:
$$h_i^{*(1,k)} = \sigma_k^* \quad \text{for all } i, k \in N_H$$

This is part of the equilibrium definition, not a separate assumption.

**A5 (Well-Defined Game)**: The game $\Gamma$ is well-defined with all primitives specified.

This is implicit and need not be stated separately.

---

## Part B: Theorem Statement Review

### B.1 Current Statement

**Theorem 1 (Existence of ABE)**: Under Assumptions A1-A3, an Attributed Belief Equilibrium exists.

### B.2 Precision Assessment

**Issue 1: Mixed vs. Pure Strategies**

The ABE definition in sec_equilibrium.tex uses pure strategies $s_i^*$, but existence requires mixed strategies. The theorem should clarify:

> An ABE exists in **mixed strategies**: there exist $\sigma^* \in \Sigma$, $h^*$, and $\tilde{h}^*$ satisfying the ABE conditions with mixed strategy optimality.

**Issue 2: Belief Domain**

The current definition is ambiguous about what beliefs are over. Clarify:
- First-order beliefs $h_i^{(1)}$: probability distributions over opponents' mixed strategies, or over pure strategy profiles?
- Standard convention: in mixed strategy equilibrium, beliefs are point masses on the equilibrium mixed strategy profile

**Issue 3: Second-Order Belief Specification**

The second-order belief $h_i^{(2,k)}$ is defined as "what $k$ expects from others." For the indignation/guilt applications, we need beliefs about what $k$ expected from $i$ specifically. Notation should be:

$$h_i^{(2,k)}(s_i) = \text{probability } i \text{ assigns to: } k \text{ expected } i \text{ to play } s_i$$

This is consistent with the current notation but should be stated explicitly.

### B.3 Edge Cases

**Case 1: $N_A = \emptyset$ (No AI)**

When there are no AI agents:
- Attributed belief system $\tilde{h}$ is empty
- ABE reduces to standard psychological game equilibrium
- Should be stated as a corollary (Proposition 3.2 in manuscript)

**Case 2: $N_H = \emptyset$ (No Humans)**

Not meaningful---ABE requires at least one human. Add: $n_H \geq 1$.

**Case 3: $\psi_i \equiv 0$ (No Psychological Payoffs)**

- ABE reduces to Nash equilibrium
- Proposition 3.3 in manuscript captures this

**Case 4: Single-Action Games**

If $|S_i| = 1$ for some $i$, player $i$ has no choice. This is a degenerate case but doesn't affect existence.

### B.4 Recommended Modifications

**REVISED THEOREM STATEMENT**:

**Theorem 1 (Existence of ABE)**: Let $\Gamma = (N_H, N_A, \{S_i\}, \{U_i^H\}, \{U_j^A\}, \phi)$ be an asymmetric psychological game with $n_H \geq 1$ satisfying:
- (A1) Strategy spaces $S_i$ are finite and non-empty
- (A1c) Psychological payoffs $\psi_i$ are continuous in beliefs
- (A2') Attribution functions $\phi_i$ are well-defined

Then an Attributed Belief Equilibrium exists in mixed strategies.

**Justification**:
- Explicitly requires $n_H \geq 1$
- Clarifies existence is for mixed strategies
- Removes redundant bounded payoff assumption
- Weakens A2 to what's actually needed

---

## Part C: Detailed Proof Steps

### Step 1: Space Construction

**Claim 1.1**: The domain for the fixed-point argument is the mixed strategy simplex $\Sigma = \prod_{i \in N} \Delta(S_i)$.

**Why this works**:
- $\Sigma$ is finite-dimensional: $\dim(\Sigma) = \sum_{i \in N}(|S_i| - 1)$
- Each $\Delta(S_i)$ is compact (closed, bounded subset of $\mathbb{R}^{|S_i|}$)
- Each $\Delta(S_i)$ is convex
- By Tychonoff, $\Sigma$ is compact
- Product of convex sets is convex

**CRITICAL OBSERVATION**: We work on $\Sigma$ alone, NOT on $\Sigma \times \mathcal{H}$ (strategy-belief product space).

**Why?** Both genuine and attributed beliefs are **determined by** the strategy profile:
- Attributed beliefs: $\tilde{h}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$ (constant, independent of $\sigma$)
- Genuine beliefs: determined by consistency $h_i^{*(1,k)} = \sigma_k^*$

So beliefs are functions of strategies, not independent variables. This is the key simplification.

**Assumptions used**: A1 (finiteness of $S_i$)

---

### Step 2: Belief Computation Mapping

**Claim 2.1**: Define the belief computation mapping $\kappa: \Sigma \to \mathcal{B} \times \tilde{\mathcal{B}}$ by:

For attributed beliefs (constant in $\sigma$):
$$\kappa^{attr}(\sigma)_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i) \in \Delta(S_i)$$

For genuine first-order beliefs:
$$\kappa^{gen}(\sigma)_i^{(1,k)} = \sigma_k \in \Delta(S_k)$$

For genuine second-order beliefs (in equilibrium):
$$\kappa^{gen}(\sigma)_i^{(2,k)} = \kappa^{gen}(\sigma)_k^{(1,i)} = \sigma_i$$

**Key observation**: $\kappa^{attr}$ is constant in $\sigma$; $\kappa^{gen}$ is continuous (identity on components).

**Claim 2.2**: $\kappa$ is continuous.

**Proof**:
- $\kappa^{attr}$ is constant, hence continuous
- $\kappa^{gen}(\sigma)_i^{(1,k)} = \sigma_k$ is a projection, hence continuous
- $\kappa^{gen}(\sigma)_i^{(2,k)} = \sigma_i$ is a projection, hence continuous
- Product of continuous functions is continuous

**Assumptions used**: A2' (well-definedness of $\phi_i$)

---

### Step 3: Best-Response Correspondence Properties

**Claim 3.1**: For each human $i \in N_H$, the best-response correspondence
$$BR_i^H: \Sigma \rightrightarrows \Delta(S_i)$$
defined by
$$BR_i^H(\sigma) = \arg\max_{\sigma_i' \in \Delta(S_i)} \mathbb{E}_{\sigma_{-i}}[U_i^H(\sigma_i', \sigma_{-i}, \kappa^{gen}(\sigma)_i, \kappa^{attr}(\sigma)_i)]$$
is:
1. Non-empty valued
2. Convex valued
3. Upper hemicontinuous

**Proof**:

**(1) Non-empty**:
- $\Delta(S_i)$ is compact
- The expected utility function $\sigma_i' \mapsto \mathbb{E}_{\sigma_{-i}}[U_i^H(\sigma_i', \sigma_{-i}, h_i, \tilde{h}_i)]$ is continuous in $\sigma_i'$ (linear in the simplex)
- By Weierstrass, a maximum exists

**(2) Convex**:
- Expected utility is linear in $\sigma_i'$ (since utility is averaged over the simplex)
- The argmax of a linear function over a convex set is a convex set (could be a face of the simplex)
- **Note**: If the maximizer is unique, $BR_i^H(\sigma)$ is a singleton; if multiple maximizers exist, any convex combination is also a maximizer

**(3) Upper hemicontinuous**:
- Follows from Berge's Maximum Theorem
- **Conditions to verify**:
  - Objective function $f(\sigma_i', \sigma) = \mathbb{E}[U_i^H(\sigma_i', \sigma_{-i}, \kappa(\sigma))]$ is continuous in $(\sigma_i', \sigma)$
  - Constraint correspondence $\sigma \mapsto \Delta(S_i)$ is continuous (trivially, it's constant)

**Continuity of objective function**:
- $\pi_i(s)$ is fixed (finite game)
- $\psi_i(s, h_i^{(2)}, \tilde{h}_i^{(2)})$ is continuous in beliefs by A1c
- $\kappa^{gen}(\sigma)$ is continuous in $\sigma$
- $\kappa^{attr}(\sigma)$ is constant
- Composition of continuous functions is continuous
- Expected value (weighted sum) preserves continuity

**Assumptions used**: A1 (compactness), A1c (continuity of $\psi_i$)

---

**Claim 3.2**: For each AI $j \in N_A$, the best-response correspondence
$$BR_j^A: \Sigma \rightrightarrows \Delta(S_j)$$
defined by
$$BR_j^A(\sigma) = \arg\max_{\sigma_j' \in \Delta(S_j)} \mathbb{E}_{\sigma_{-j}}[U_j^A(\sigma_j', \sigma_{-j}; \theta_j)]$$
satisfies the same properties (non-empty, convex, UHC).

**Proof**: Standard argument for Nash equilibrium existence. AI has no belief-dependent payoffs, so this is the classical case.

**Assumptions used**: A1 (compactness)

---

### Step 4: Product Correspondence

**Claim 4.1**: The product best-response correspondence
$$BR: \Sigma \rightrightarrows \Sigma$$
defined by
$$BR(\sigma) = \prod_{i \in N_H} BR_i^H(\sigma) \times \prod_{j \in N_A} BR_j^A(\sigma)$$
is non-empty valued, convex valued, and upper hemicontinuous.

**Proof**:
- Product of non-empty sets is non-empty
- Product of convex sets is convex
- Product of UHC correspondences is UHC (standard result)

---

### Step 5: Kakutani Application

**Claim 5.1**: The correspondence $BR: \Sigma \rightrightarrows \Sigma$ has a fixed point.

**Proof**: Apply Kakutani's Fixed-Point Theorem.

**Kakutani conditions**:
1. $\Sigma$ is non-empty: $\checkmark$ (each $S_i$ is non-empty by A1)
2. $\Sigma$ is compact: $\checkmark$ (product of compact simplices)
3. $\Sigma$ is convex: $\checkmark$ (product of convex sets)
4. $BR(\sigma)$ is non-empty for all $\sigma$: $\checkmark$ (Claim 3.1, 3.2)
5. $BR(\sigma)$ is convex for all $\sigma$: $\checkmark$ (Claim 3.1, 3.2)
6. $BR$ is upper hemicontinuous: $\checkmark$ (Claim 4.1)

Therefore, there exists $\sigma^* \in \Sigma$ such that $\sigma^* \in BR(\sigma^*)$.

---

### Step 6: Equilibrium Verification

**Claim 6.1**: A fixed point $\sigma^*$ of $BR$, together with the induced beliefs $h^* = \kappa^{gen}(\sigma^*)$ and $\tilde{h}^* = \kappa^{attr}(\sigma^*)$, constitutes an ABE.

**Proof**: Verify the four ABE conditions.

**(ABE1) Human Optimality**: For all $i \in N_H$,
$$\sigma_i^* \in BR_i^H(\sigma^*) = \arg\max_{\sigma_i'} \mathbb{E}[U_i^H(\sigma_i', \sigma_{-i}^*, h_i^*, \tilde{h}_i^*)]$$
This is exactly the definition of $BR_i^H$.

**(ABE2) AI Optimality**: For all $j \in N_A$,
$$\sigma_j^* \in BR_j^A(\sigma^*) = \arg\max_{\sigma_j'} \mathbb{E}[U_j^A(\sigma_j', \sigma_{-j}^*; \theta_j)]$$
This is exactly the definition of $BR_j^A$.

**(ABE3) Genuine Belief Consistency**: For all $i, k \in N_H$,
$$h_i^{*(1,k)} = \kappa^{gen}(\sigma^*)_i^{(1,k)} = \sigma_k^*$$
$$h_i^{*(2,k)} = \kappa^{gen}(\sigma^*)_i^{(2,k)} = \sigma_i^* = h_k^{*(1,i)}$$
Both hold by construction of $\kappa^{gen}$.

**(ABE4) Attribution Consistency**: For all $i \in N_H$, $j \in N_A$,
$$\tilde{h}_i^{*(2,j)} = \kappa^{attr}(\sigma^*)_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$$
Holds by definition of $\kappa^{attr}$.

**Q.E.D.**

---

## Part D: Technical Issues

### D.1 Psychological Payoff Continuity

**Issue**: Is the continuity specification in A1c correct?

**Analysis**: The psychological payoff $\psi_i$ depends on:
1. Strategy profile $s \in S$
2. Genuine second-order beliefs $h_i^{(2)} = \{h_i^{(2,k)}\}_{k \in N_H \setminus \{i\}}$
3. Attributed second-order beliefs $\tilde{h}_i^{(2)} = \{\tilde{h}_i^{(2,j)}\}_{j \in N_A}$

For the indignation payoff:
$$\psi_i^{IND}(s, h_i^{(2)}, \tilde{h}_i^{(2)}) = -\beta_i \cdot \mathbf{1}_{s_i = D} \cdot \left[ \sum_{k \in N_H} h_i^{(2,k)}(C) + \lambda_i \sum_{j \in N_A} \tilde{h}_i^{(2,j)}(C) \right]$$

This is:
- Discrete in $s_i$ (indicator function)
- **Linear** in $h_i^{(2,k)}(C)$ and $\tilde{h}_i^{(2,j)}(C)$
- Hence continuous in beliefs for fixed $s$

For the guilt payoff:
$$\psi_i^{GUILT} = -\gamma_i \cdot \left[ \sum_k \max\{0, h_i^{(2,k)} - \pi_k(s)\} + \lambda_i \sum_j \max\{0, \tilde{h}_i^{(2,j)} - \pi_j(s)\} \right]$$

This is:
- Continuous in beliefs (max is continuous, composition preserves continuity)

**Conclusion**: The standard psychological payoff specifications (indignation, guilt) satisfy A1c. The assumption is correctly specified.

---

### D.2 Second-Order Belief Space

**Issue**: Is the second-order belief space properly handled?

**Analysis**: In standard PGT (GPS/BD), second-order beliefs are infinite-dimensional:
$$h_i^{(2,k)} \in \Delta(\Delta(S_{-k}))$$

However, for the specific applications in ABE:
- Indignation/guilt only use the **marginal** belief about own action: $h_i^{(2,k)}(s_i)$
- This is finite-dimensional: $h_i^{(2,k)} \in \Delta(S_i)$

**Simplification**: For ABE with indignation/guilt, we can work with:
$$h_i^{(2,k)} \in \Delta(S_i) \quad \text{(belief about what } k \text{ expected } i \text{ to do)}$$

This is the interpretation used in the manuscript and is sufficient for the applications.

**Resolution**: The manuscript correctly uses finite-dimensional belief spaces. The proof is valid.

---

### D.3 Mixed Strategy Incorporation

**Issue**: Are mixed strategies correctly incorporated?

**Analysis**: The proof works with mixed strategies $\sigma_i \in \Delta(S_i)$ throughout:
- Best-response is over $\Delta(S_i)$, not $S_i$
- Expected utility is computed by averaging over mixed strategy profiles
- Beliefs in equilibrium are about mixed strategies (point masses on $\sigma_k^*$)

**Potential issue**: In genuine second-order beliefs, we have
$$h_i^{(2,k)} = h_k^{(1,i)} = \sigma_i^*$$

This means $h_i^{(2,k)}$ is itself a probability distribution over $S_i$ (the equilibrium mixed strategy). When computing psychological payoffs, we use $h_i^{(2,k)}(C)$, which is the probability assigned to cooperation.

**This is correct**: In mixed strategy equilibrium, the belief about what $k$ expected $i$ to do is exactly $\sigma_i^*$---the equilibrium mixed strategy.

---

### D.4 Product Structure

**Issue**: Is the product structure correct?

**Analysis**: The correspondence $BR: \Sigma \rightrightarrows \Sigma$ is defined as a product:
$$BR(\sigma) = \prod_{i \in N} BR_i(\sigma)$$

This is correct because:
- Each player optimizes independently given others' strategies
- No coordination constraint couples different players' best responses
- The product of UHC correspondences is UHC

**Potential issue**: Interdependence through beliefs.

Human $i$'s payoff depends on $h_i^{(2,k)} = \sigma_i^*$ (belief about what $k$ expected). This creates interdependence: $i$'s payoff depends on their own equilibrium strategy through the second-order belief.

**Resolution**: This is handled correctly. In the fixed-point, we have:
- $\sigma_i^*$ enters $i$'s payoff through the second-order belief
- But $\sigma_i^*$ is the **output** of the best-response, not an input
- The belief $h_i^{(2,k)}$ equals $\sigma_i$ (the candidate strategy profile)
- At the fixed point: $\sigma_i^* = BR_i(\sigma^*)$, and beliefs are consistent

The circularity is resolved by the fixed-point structure.

---

## Part E: Recommended Modifications

### E.1 Assumption A1 (Regularity)

**Original**:
> (A1) Strategy spaces $S_i$ are non-empty and finite. Type spaces $T_i$ and $\Theta_j$ are non-empty, convex, and compact. Payoff functions are continuous.

**Modified**:
> **Assumption A1 (Regularity)**
>
> (A1a) For all $i \in N$, strategy spaces $S_i$ are non-empty and finite.
>
> (A1b) For all $i \in N_H$, psychological payoffs $\psi_i(s, h_i^{(2)}, \tilde{h}_i^{(2)})$ are continuous in $(h_i^{(2)}, \tilde{h}_i^{(2)})$ for each $s \in S$.

**Justification**:
- A1a directly supports compactness of $\Sigma$
- A1b makes explicit the continuity needed for UHC of best-response
- Type space regularity moved to separate assumption for extensions
- Payoff continuity specified for the relevant argument (beliefs)

**Impact**: No change to other results. Clarifies proof structure.

---

### E.2 Assumption A3 (Bounded Psychological Payoffs)

**Original**:
> (A3) There exists $M < \infty$ such that $|\psi_i(s, h_i^{(2)}, \tilde{h}_i^{(2)})| \leq M$ for all beliefs.

**Recommendation**: Keep as stated, but add remark.

**New Remark**:
> Assumption A3 is implied by A1 when $\psi_i$ is continuous: the domain $S \times \prod_k \Delta(S_i) \times \prod_j \Delta(S_i)$ is compact, so any continuous $\psi_i$ attains a maximum. We state A3 explicitly for clarity in applications.

---

### E.3 Theorem Statement

**Original**:
> **Theorem 1 (Existence of ABE)**: Under Assumptions A1-A3, an Attributed Belief Equilibrium exists.

**Modified**:
> **Theorem 1 (Existence of ABE)**: Let $\Gamma$ be an asymmetric psychological game satisfying Assumptions A1 and A2. Then an Attributed Belief Equilibrium exists in mixed strategies.

**Justification**:
- Explicitly notes mixed strategies
- A3 is redundant (follows from A1)
- Cleaner statement

---

### E.4 Second-Order Belief Clarification

**Add to Definition 2.1 (Attributed Beliefs)**:
> The attributed belief $\tilde{h}_i^{(2,j)} \in \Delta(S_i)$ represents the distribution over human $i$'s actions that $i$ believes AI $j$ expected. Formally, $\tilde{h}_i^{(2,j)}(s_i)$ is the probability that $i$ attributes to: "AI $j$ expected $i$ to play $s_i$."

**Add to Definition 3.1 (ABE), Condition 3**:
> For genuine second-order beliefs in mixed strategy equilibrium: $h_i^{*(2,k)}(s_i) = \sigma_i^*(s_i)$ for all $s_i \in S_i$. That is, $i$ believes $k$ expected $i$ to play according to the equilibrium mixed strategy.

---

## Summary: Proof Roadmap

1. **Domain**: $\Sigma = \prod_{i \in N} \Delta(S_i)$ (compact, convex, non-empty)

2. **Belief computation**:
   - Attributed: $\tilde{h}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$ (constant)
   - Genuine: $h_i^{(1,k)} = \sigma_k$, $h_i^{(2,k)} = \sigma_i$ (continuous in $\sigma$)

3. **Best-response**:
   - Humans: $BR_i^H(\sigma) = \arg\max_{\sigma_i'} \mathbb{E}[U_i^H(\sigma_i', \sigma_{-i}, h(\sigma), \tilde{h})]$
   - AI: $BR_j^A(\sigma) = \arg\max_{\sigma_j'} \mathbb{E}[U_j^A(\sigma_j', \sigma_{-j})]$

4. **Properties**: Both correspondences are non-empty, convex-valued, UHC

5. **Fixed point**: Kakutani's theorem guarantees existence

6. **Verification**: Fixed point satisfies all four ABE conditions by construction

**Key simplification vs. standard PGT**: Attributed beliefs are constants, not equilibrium variables. The fixed-point problem is on $\Sigma$ alone, not on $\Sigma \times \mathcal{H}$.

---

## Appendix: Full Proof Write-Up (Publication Format)

**Theorem 1 (Existence)**. *Under Assumptions A1 and A2, an Attributed Belief Equilibrium exists.*

*Proof.* The proof applies Kakutani's fixed-point theorem to the best-response correspondence on the strategy space.

**Step 1 (Domain).** Let $\Sigma = \prod_{i \in N} \Delta(S_i)$ be the space of mixed strategy profiles. Since each $S_i$ is finite and non-empty (A1a), each $\Delta(S_i)$ is a non-empty, compact, convex simplex. By Tychonoff's theorem, $\Sigma$ is non-empty, compact, and convex.

**Step 2 (Belief Computation).** For each strategy profile $\sigma \in \Sigma$, define beliefs as follows:
- Attributed beliefs: $\tilde{h}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$, which is well-defined by A2.
- Genuine first-order beliefs: $h_i^{(1,k)} = \sigma_k$.
- Genuine second-order beliefs: $h_i^{(2,k)} = \sigma_i$.

Note that attributed beliefs are independent of $\sigma$, while genuine beliefs are continuous functions of $\sigma$.

**Step 3 (Best-Response Correspondence).** For human $i \in N_H$, define:
$$BR_i^H(\sigma) = \arg\max_{\sigma_i' \in \Delta(S_i)} \sum_{s \in S} \left(\prod_{k \neq i} \sigma_k(s_k)\right) \sigma_i'(s_i) \cdot U_i^H(s, h_i(\sigma), \tilde{h}_i)$$

For AI $j \in N_A$, define:
$$BR_j^A(\sigma) = \arg\max_{\sigma_j' \in \Delta(S_j)} \sum_{s \in S} \left(\prod_{k \neq j} \sigma_k(s_k)\right) \sigma_j'(s_j) \cdot U_j^A(s; \theta_j)$$

Each correspondence is:
- *Non-empty*: The objective is continuous and $\Delta(S_i)$ is compact.
- *Convex-valued*: The objective is linear in $\sigma_i'$.
- *Upper hemicontinuous*: By Berge's Maximum Theorem, using continuity of $U_i^H$ in beliefs (A1b) and continuity of $h_i(\sigma)$ in $\sigma$.

**Step 4 (Product Correspondence).** Define $BR: \Sigma \rightrightarrows \Sigma$ by $BR(\sigma) = \prod_{i \in N_H} BR_i^H(\sigma) \times \prod_{j \in N_A} BR_j^A(\sigma)$. The product of correspondences preserves non-emptiness, convexity, and upper hemicontinuity.

**Step 5 (Fixed Point).** Since $\Sigma$ is non-empty, compact, and convex, and $BR$ is a non-empty-valued, convex-valued, upper hemicontinuous correspondence, Kakutani's fixed-point theorem guarantees the existence of $\sigma^* \in \Sigma$ with $\sigma^* \in BR(\sigma^*)$.

**Step 6 (Verification).** Define $h^* = h(\sigma^*)$ and $\tilde{h}^* = \phi(\theta, x, \omega)$. Then:
- Human optimality: $\sigma_i^* \in BR_i^H(\sigma^*)$ by construction.
- AI optimality: $\sigma_j^* \in BR_j^A(\sigma^*)$ by construction.
- Genuine belief consistency: $h_i^{*(1,k)} = \sigma_k^*$ and $h_i^{*(2,k)} = \sigma_i^* = h_k^{*(1,i)}$ by construction.
- Attribution consistency: $\tilde{h}_i^{*(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$ by definition.

Hence $(\sigma^*, h^*, \tilde{h}^*)$ is an ABE. $\square$

---

*Last updated: 2026-01-12*
