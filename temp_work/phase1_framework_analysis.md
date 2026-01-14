# Phase 1.2: Mathematical Analysis of ABE Framework

## 1. SPACE IDENTIFICATION

### 1.1 Strategy Spaces

**Pure Strategy Space:**
- For each player $i \in N = N_H \cup N_A$: $S_i$ is finite (non-empty)
- Finite cardinalities: $|S_i| = m_i$ for humans, $m_j$ for AI
- Strategy profile space: $S = \prod_{i \in N} S_i$ is finite

**Mixed Strategy Space:**
- For each player: $\sigma_i \in \Delta(S_i)$ (simplex)
- Dimension of $\Delta(S_i)$: $m_i - 1$ (continuous Euclidean)
- Mixed strategy profile space: $\Sigma = \prod_{i \in N} \Delta(S_i)$
- Dimension of $\Sigma$: $\sum_{i \in N} (m_i - 1)$
- **Topological properties**: Compact, convex, metrizable

### 1.2 Belief Spaces (Genuine Beliefs)

**First-Order Belief Space for Human $i$:**
- $\mathcal{B}_i^{(1)} = \Delta(S_{-i})$ where $S_{-i} = \prod_{k \neq i} S_k$
- Dimension: $(|S_{-i}| - 1)$
- Topological properties: Compact, convex simplex

**Second-Order Belief Space for Human $i$ about Human $k$:**
- $\mathcal{B}_i^{(2,k)} = \Delta(\Delta(S_{-k}))$
- **ISSUE**: Infinite-dimensional in general

**KEY OBSERVATION**: Second-order beliefs about humans are infinite-dimensional objects, but handled via the compact metric space of probability measures with weak topology.

### 1.3 Attributed Belief Spaces (Novel Component)

**Second-Order Attributed Belief Space:**
$$\tilde{\mathcal{B}}_i^{(2,j)} = \Delta(S_i) \quad \text{for } i \in N_H, j \in N_A$$

**CRITICAL**: Codomain is $\Delta(S_i)$ not $\Delta(S_j)$
- Represents: "What does human $i$ believe AI $j$ expected human $i$ to do?"
- Dimension: $|S_i| - 1$ (finite-dimensional simplex)
- **Exogenously determined** by attribution function: $\tilde{h}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$
- NOT a variable to be solved for in equilibrium

---

## 2. CORRESPONDENCE STRUCTURE

### 2.1 Best-Response Correspondence for Humans

**Given Beliefs $(h_i, \tilde{h}_i)$:**
$$BR_i^H(h_i, \tilde{h}_i) = \arg\max_{\sigma_i \in \Delta(S_i)} \mathbb{E}[U_i^H(\sigma_i, \sigma_{-i}^*, h_i, \tilde{h}_i)]$$

**Properties:**
1. **Non-empty**: $\Delta(S_i)$ compact, $U_i^H$ continuous → Weierstrass theorem
2. **Convex-valued**: By concavity in $\sigma_i$ of expected utility
3. **Upper hemicontinuous**: By Berge's theorem

### 2.2 Best-Response Correspondence for AI

$$BR_j^A(\sigma_{-j}) = \arg\max_{\sigma_j \in \Delta(S_j)} \mathbb{E}[U_j^A(\sigma_j, \sigma_{-j}; \theta_j)]$$

**Domain:** $\Sigma_{-j} = \prod_{k \neq j} \Delta(S_k)$ (finite-dimensional)
**Codomain:** $\Delta(S_j)$
**Properties:** Same as for humans (non-empty, convex-valued, UHC)

### 2.3 Critical Asymmetry

- Human best-response depends on **both** genuine and attributed beliefs
- AI best-response depends **only** on other players' strategies (no beliefs)

---

## 3. KEY SIMPLIFICATION: EXOGENOUS ATTRIBUTION

### 3.1 The Crucial Observation

**ABE Condition 4:**
$$\tilde{h}_i^{*(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$$

This is **NOT** an equilibrium condition. Attributed belief is **mechanically determined** by:
- AI's design parameters $\theta_j$ (fixed)
- Observable signals $x_j$ (fixed)
- Human's anthropomorphism $\omega_i$ (fixed)

**Consequence**: $\tilde{h}_i^{(2,j)}$ is a **constant** for fixed parameters.

### 3.2 No Circularity in Attribution

Unlike genuine beliefs about humans:
$$h_i^{(2,k)} = h_k^{(1,i)} \quad \text{(reciprocal beliefs)}$$

Attributed beliefs have **NO** such reciprocity:
- NO requirement that $\tilde{h}_i^{(2,j)}$ equals what AI "actually" believes
- NO consistency loop: $\tilde{h}_i^{(2,j)}$ doesn't depend on $\sigma_j^*$

**Mathematical implication**: Attribution decouples from equilibrium computation.

---

## 4. FIXED-POINT DOMAIN ANALYSIS

### 4.1 Strategy-Only Fixed Point (RECOMMENDED)

Define the fixed-point mapping on $\Sigma = \prod_{i \in N} \Delta(S_i)$ alone:
$$\Phi: \Sigma \to \Sigma$$

**Construction:**
1. Given $\sigma \in \Sigma$
2. Compute attributed beliefs (exogenously): $\tilde{h}_i^{(2,j)} := \phi_i(\theta_j, x_j, \omega_i)$
3. Compute genuine beliefs (from consistency): $h_i^{(1,k)} := \sigma_k$, $h_i^{(2,k)} := h_k^{(1,i)}$
4. Apply best responses: $\Phi(\sigma) = (BR_i^H(h_i, \tilde{h}_i), BR_j^A(\sigma_{-j}))$

**Advantage**: Finite-dimensional fixed point in $\Sigma$

---

## 5. TECHNICAL ISSUES AND RESOLUTIONS

### 5.1 Infinite-Dimensionality of Genuine Belief Spaces

**Issue**: $\mathcal{H}_i^{(n)}$ is infinite-dimensional.

**Resolution**:
- Genuine beliefs are **determined by strategies** via consistency
- Not variables to be chosen, but **functions of equilibrium strategy**
- Work only in $\Sigma$; beliefs recovered post-equilibrium

### 5.2 Compactness of $\Sigma$

$\Sigma = \prod_{i=1}^n \Delta(S_i)$ is:
- **Compact**: Product of compact simplices (Tychonoff)
- **Convex**: Product of convex sets
- **Metrizable**: Product of finitely many metrizable spaces

### 5.3 Kakutani Application

$\Phi: \Sigma \to \Sigma$ satisfies:
1. Domain: $\Sigma$ (compact, convex, non-empty)
2. Non-empty values: By Weierstrass
3. Convex values: By concavity of utility
4. Upper hemicontinuous: By Berge's theorem

**Therefore, $\Phi$ has a fixed point.**

### 5.4 Bounded Psychological Payoffs

**A3** ensures: $|\psi_i| \leq M$

**Why critical**:
- Without boundedness, psychological payoffs could dominate arbitrarily
- Could violate continuity of $U_i^H$
- Best-response could become discontinuous
- Kakutani would not apply

---

## 6. PROOF STRUCTURE SUMMARY

1. **Construct $\Sigma$**: Product of simplices (compact, convex)
2. **Define consistency mapping**: $\kappa: \Sigma \to \mathcal{H} \times \tilde{\mathcal{H}}$
3. **Define best-response**: $\Phi(\sigma) = \prod_i BR_i(h(\sigma), \tilde{h}(\sigma))$
4. **Verify Kakutani conditions**: Non-empty, convex-valued, UHC
5. **Apply Kakutani**: Fixed point $\sigma^*$ exists
6. **Recover beliefs**: $h^* = h(\sigma^*)$, $\tilde{h}^* = \tilde{h}(\sigma^*)$
7. **Verify ABE conditions**: All four hold by construction

---

## Summary Table

| Element | Space | Dimension | Properties | Role |
|---------|-------|-----------|------------|------|
| Mixed strategies | $\Sigma$ | $\sum(m_i - 1)$ | Compact, convex | Fixed-point domain |
| Genuine beliefs | $\mathcal{H}_i$ | $\infty$ | Compact metric | Derived from $\sigma$ |
| Attributed beliefs | $\Delta(S_i)$ | $m_i - 1$ | Compact, convex | Exogenously determined |
