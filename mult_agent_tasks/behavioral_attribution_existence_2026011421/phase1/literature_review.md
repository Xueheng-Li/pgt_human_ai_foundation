# Literature Review: Fixed-Point Methods for Belief-Strategy Simultaneity

## Key Findings

### 1. Standard PGT Approach (GPS 1989, BD09)
The critical insight from GPS and Battigalli-Dufwenberg is that they handle belief-strategy interdependence by making beliefs a **deterministic function** of strategies through coherence conditions. The fixed-point argument operates on strategies alone because β(σ) is uniquely determined.

### 2. Technical Conditions for Existence
Standard Kakutani conditions apply, plus:
- **Continuity of the belief mapping** β: Σ → B
- **Continuity of utility in beliefs** u(a, β)

### 3. Resolution for ABE with Behavioral Attribution
Two approaches work when attributed beliefs μ depend on σ:

**Approach 1 (Preferred)**: If the attribution function Attr: Σ → M is continuous and single-valued, substitute directly into payoffs and define ũ(a, σ) = u(a, Attr(σ)). The fixed-point operates on Σ alone.

**Approach 2**: For set-valued attribution, work on the joint space (σ, μ) and require Attr to be upper hemicontinuous with convex values.

### 4. Key Mathematical Condition
The critical requirement for extending the existence proof is:

> **Attribution continuity**: The mapping σ → μ(σ) must be continuous.

This holds naturally if attributed beliefs depend continuously on observable AI behavior (the mixed strategy σ_AI). Small changes in AI strategy produce small changes in what humans attribute.
