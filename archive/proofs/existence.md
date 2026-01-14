# Existence of Attributed Belief Equilibrium

## Main Theorem

**Theorem 1 (Existence)**: Under assumptions A1-A3, an Attributed Belief Equilibrium exists.

## Proof Strategy

Follow Battigalli & Dufwenberg (2009) with modifications for asymmetric structure.

### Step 1: Construct Extended Game

Define the extended game where:
- Human strategies: $\sigma_i: E_i \to \Delta(S_i)$ (belief-contingent)
- AI strategies: $\sigma_j \in \Delta(S_j)$ (standard mixed)

### Step 2: Define Best Response Correspondences

For humans:
$$BR_i^H(s_{-i}, E_i) = \arg\max_{s_i \in S_i} U_i^H(s_i, s_{-i}, E_i)$$

For AI:
$$BR_j^A(s_{-j}) = \arg\max_{s_j \in S_j} U_j^A(s_j, s_{-j}; \theta_j)$$

### Step 3: Belief Consistency Mapping

Define $\Phi: S \times \mathcal{E} \to \mathcal{E}$ that updates beliefs consistently:
- H-H beliefs: standard consistency
- H-A beliefs: via attribution function $\phi_i$

### Step 4: Fixed Point

Apply Kakutani's fixed point theorem to the composed correspondence.

**Key challenge**: Ensure attribution function maintains continuity of overall mapping.

---

*To complete: Full proof with all technical details*
