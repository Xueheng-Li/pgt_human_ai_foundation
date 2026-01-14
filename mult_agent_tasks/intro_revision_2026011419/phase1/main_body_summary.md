# Main Body Structure Summary

## SECTION 2: FRAMEWORK

### Definitions
- **Definition 1 (Attributed Beliefs)**: $\tilde{h}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$ - human i's attributed belief about AI j
- **Definition 2 (Attribution Function)**: $\phi_i: \Theta_j \times X \times \Omega_i \to \Delta(S_i)$
- **Definition 3 (Zero-Anthropomorphism Benchmark)**: $\tilde{h}_i^{(2,j),ZA} = \phi_i(\theta_j, x_j, 0)$
- **Definition 4 (Indignation with Attenuation)**: $\psi_i^{IND}$ with attenuation factor $\lambda_i^{IND}$
- **Definition 5 (Guilt Aversion with Attenuation)**: $\psi_i^{GUILT}$ with attenuation factor $\lambda_i^{GUILT}$
- **Definition 6 (Material Welfare)**: $W(s) = \sum_{i \in N} \pi_i(s)$
- **Definition 7 (Extended Welfare)**: $W^{ext}(s, h, \tilde{h}) = W(s) + \sum_{i \in N_H} \psi_i$
- **Definition 8 (Asymmetric Human-AI Psychological Game)**: Formal tuple

### Assumptions
- (A1) Regularity: Finite strategies, compact type spaces, continuous payoffs
- (A2) Attribution Continuity
- (A3) Bounded Psychological Payoffs
- (A2') Attribution Monotonicity (optional)
- (A2'') Attribution Non-Degeneracy (optional)
- (A2''') Signal Monotonicity (optional)
- Context-specific: (G) Guilt Dominance, (G') Positive Guilt, (I) Indignation Dominance, (E) Cooperation Efficiency, (C) Signal Clarity, (T) Temptation Dominance

## SECTION 3: EQUILIBRIUM

### Definitions
- **Definition 9 (Attributed Belief Equilibrium)**: Four conditions - Human Optimality, AI Optimality, Genuine Belief Consistency, Attribution Consistency
- **Definition 10 (Rational Attribution Equilibrium)**: Fixed-point where $\tilde{h}_i^{*(2,j)} = \sigma_i^*$

### Theorems
- **Theorem 1 (Existence of ABE)**: Under A1-A3, ABE exists

### Propositions
- **Proposition 1 (Reduction to Standard PGT)**: When $N_A = \emptyset$, ABE = PNE
- **Proposition 2 (Reduction to Nash)**: When $\psi_i \equiv 0$, ABE = Nash
- **Proposition 3 (Rational Attribution)**: Under rational attribution, ABE = Bayes-Nash
- **Proposition 4 (Attribution-Dependent Multiplicity)**: Different $\phi$ sustain different equilibria

### Corollaries
- **Corollary 1 (Complete Information Reduction)**: With common knowledge types, RAE = Nash

## SECTION 4: APPLICATIONS

### Propositions
- **Proposition 5 (Trust Game ABE)**: Higher $\omega_H$ → higher attributed expectations → higher returns $y^* = \min\{\tilde{h}_H^{(2,A)}, 3x\}$
- **Proposition 6 (Public Goods ABE)**: AI contribution + anthropomorphism threshold sustains cooperation; dual material/psychological channels
- **Proposition 7 (Coordination ABE)**: AI as focal point provider, resolves multiplicity

## SECTION 5: WELFARE

### Propositions
- **Proposition 8 (Welfare Effects of Anthropomorphism)**:
  - (i) Prosocial AI: higher $\omega$ weakly increases $W$
  - (ii) Materialist AI: higher $\omega$ may reduce $W^{ext}$
  - (iii) Materialist AI: $\omega$ neutral on $W$

- **Proposition 9 (Welfare Effects of Elevated Anthropomorphism)**:
  - (i) Prosocial AI: elevated anthropomorphism weakly improves $W$
  - (ii) Materialist AI: may reduce $W^{ext}$ through phantom expectations

- **Proposition 10 (Optimal AI Design)**:
  - (i) Prosocial: $x^* = x_{crit}$, $\partial x^*/\partial m < 0$
  - (ii) Materialist: $x^* = 0$
  - (iii) Mixed: $x^* \in (0, \bar{x})$

- **Proposition 10' (Extended Welfare Optimal Design)**:
  - $x^{*,ext} \leq x^*$ when phantom expectations arise

### Corollaries
- **Corollary 2 (Welfare Measure Agreement)**: $x^* = x^{*,ext}$ when expectations don't exceed feasibility
- **Corollary 3 (Welfare Measure Divergence)**: $x^* > x^{*,ext}$ when phantom expectations exceed feasibility

## KEY CONCEPTUAL INNOVATIONS

1. **Attribution Function ($\phi$)**: Central primitive formalizing anthropomorphism
2. **Zero-Anthropomorphism Benchmark**: Descriptive baseline at $\omega_i = 0$
3. **Rational Attribution Equilibrium (RAE)**: Fixed-point where beliefs = strategies
4. **Phantom Expectations**: Attributed expectations about materialist AI that correspond to nothing
5. **Dual Welfare Measures**: Material vs. Extended welfare with normative foundations
6. **Feed-Forward Multiplicity**: $\phi \to \tilde{h}^{(2)} \to U^H \to s^*$

## ECONOMIC INSIGHTS

1. **Interface determines equilibrium**: Anthropomorphic cues enter through $\phi$
2. **Match presentation to objectives**: Prosocial AI benefits; materialist AI harms
3. **Attenuation cuts both ways**: Protects from phantom expectations but limits cooperation gains
4. **AI as coordination device**: Constructed focal point resolving multiplicity
5. **Cultural heterogeneity**: High-$\omega$ populations benefit more but more vulnerable

## TESTABLE PREDICTIONS

1. Interaction effect $\beta_3 > 0$: High-$\omega$ subjects respond more to interface manipulation
2. Trust returns increase through guilt channel, not material incentives
3. Public goods show threshold effects at $\omega_i \geq \bar{\omega}_i$
4. AI population share has non-monotonic effects
5. Cross-cultural variation: Japan (low attenuation) vs. West (high attenuation)
