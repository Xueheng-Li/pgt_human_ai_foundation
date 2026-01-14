# Proof Analysis: Required Modifications for Behavioral Attribution

## 1. Current Proof Summary

The existence proof uses Kakutani's fixed-point theorem on Σ = ∏ᵢ Δ(Sᵢ). Five steps:
1. Strategy space construction (compact, convex)
2. Belief computation (genuine + attributed)
3. Best-response correspondence (non-empty, convex, uhc)
4. Fixed-point application (Kakutani)
5. Equilibrium verification (ABE1-4)

## 2. Where Exogeneity Is Assumed

**Step 2 (line 38)**: "Under exogenous attribution... attributed beliefs do not create additional equilibrium conditions."

**Step 3(iii)**: Continuity argument relies on "constants for attributed beliefs"

**Step 5**: ABE4 is "definitional, not an equilibrium condition"

## 3. Required Modifications

Under behavioral attribution: $\tilde{h}_i^{(2,j)} = \phi_i^{beh}(\theta_j, x_j, \sigma_j, \omega_i)$

**Complications**:
- Continuity in σ requires φ^beh continuous in σ_j
- Convexity preserved if φ^beh depends only on σ_j (not σ_i)
- ABE4 evaluates at equilibrium σ_j*

## 4. Proposed Assumption (A2-beh)

**Behavioral Attribution Regularity:**
1. **(Continuity)** φ^beh continuous in σ_j ∈ Δ(S_j)
2. **(Own-Strategy Independence)** φ^beh depends only on σ_j, not σ_i
3. **(Validity)** φ^beh maps to valid probability distributions

## 5. Extended Argument Sketch

**Step 3 (Modified)**:
- (i) Non-empty: unchanged (compact domain, continuous objective)
- (ii) Convex: preserved because φ^beh depends on σ_j, not σ_i'
- (iii) UHC: continuity follows from (A2-beh.1) + Berge's theorem

**Key insight**: Extension is straightforward under (A2-beh). Only Step 3(iii) continuity requires the new assumption.

## 6. Summary Table

| Aspect | Exogenous | Behavioral |
|--------|-----------|------------|
| Dependence on σ | None (constant) | Depends on σ_j |
| Continuity | Trivial | Requires (A2-beh.1) |
| Convexity | Automatic | Requires (A2-beh.2) |
| ABE4 | Definitional | Evaluates at σ_j* |
