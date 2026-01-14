# Multi-Agent Execution Plan: Logic and Notation Consistency Review

**Task**: Review and double-check the logic and notation consistency of the model setup, basic concepts, and notations in the drafts directory.

**Date**: 2026-01-12

**Target**: `/Users/xueheng/SynologyDrive/Research/pgt_human_ai_foundation/drafts/`

---

## Document Structure Overview

| File | Content |
|------|---------|
| `main.tex` | Master document, includes all sections |
| `sec_framework.tex` | Player types, payoffs, belief hierarchies, attribution function |
| `sec_equilibrium.tex` | ABE definition, existence theorem, special cases |
| `sec_applications.tex` | Trust game, public goods, coordination |
| `sec_welfare.tex` | Welfare analysis |
| `sec_introduction.tex` | Introduction |
| `sec_conclusion.tex` | Conclusion |
| `proofs/*.tex` | 12 proof files |

---

## Execution Architecture

### Phase 1: Information Collection & Analysis (规划阶段)
**Objective**: Systematically extract all definitions, notations, and logical dependencies.

| Agent ID | Task | Input | Output File |
|----------|------|-------|-------------|
| 1A | Extract all notation definitions from framework | `sec_framework.tex` | `phase1_notation_framework.md` |
| 1B | Extract all notation definitions from equilibrium | `sec_equilibrium.tex` | `phase1_notation_equilibrium.md` |
| 1C | Extract all notation definitions from applications | `sec_applications.tex` | `phase1_notation_applications.md` |
| 1D | Extract notation from welfare and cross-reference with `theory/foundations.tex` | `sec_welfare.tex`, `theory/foundations.tex` | `phase1_notation_welfare.md` |

**Parallelization**: Agents 1A, 1B, 1C, 1D run in parallel.

---

### Phase 2: Implementation & Integration (实施阶段)
**Objective**: Perform detailed consistency checks across all extracted notations.

| Agent ID | Task | Input | Output File |
|----------|------|-------|-------------|
| 2A | Check notation consistency: Player sets, types, parameters | Phase 1 outputs | `phase2_check_players.md` |
| 2B | Check notation consistency: Belief hierarchies (h vs β) | Phase 1 outputs | `phase2_check_beliefs.md` |
| 2C | Check notation consistency: Utility functions, psychological payoffs | Phase 1 outputs | `phase2_check_utility.md` |
| 2D | Check logical consistency: Definition dependencies and theorem assumptions | Phase 1 outputs + all sec_*.tex | `phase2_check_logic.md` |
| 2E | Check proof consistency: Notation used in proofs vs main text | `proofs/*.tex` + sec_*.tex | `phase2_check_proofs.md` |

**Parallelization**: Agents 2A, 2B, 2C run in parallel after Phase 1 completes. Agent 2D and 2E run in parallel with 2A-2C.

---

### Phase 3: Review & Feedback (审阅与反馈)
**Objective**: Synthesize findings and generate comprehensive review report.

| Agent ID | Task | Input | Output File |
|----------|------|-------|-------------|
| 3A | Aggregate all Phase 2 findings, categorize by severity (critical/major/minor) | All phase2_*.md files | `phase3_aggregated_issues.md` |
| 3B | Generate specific recommendations for each issue | `phase3_aggregated_issues.md` | `phase3_recommendations.md` |

**Parallelization**: Agent 3A runs first, then 3B uses its output.

---

### Phase 4: Revision & Final Report (修订与定稿)
**Objective**: Create actionable revision checklist and final consistency report.

| Agent ID | Task | Input | Output File |
|----------|------|-------|-------------|
| 4A | Create detailed revision checklist with line-by-line fixes | Phase 3 outputs | `phase4_revision_checklist.md` |
| 4B | Generate final consistency report summary | All phase outputs | `phase4_final_report.md` |

**Parallelization**: Agents 4A and 4B run in parallel.

---

## Key Notation Elements to Check

### 1. Player and Type Notation
- [ ] $N_H, N_A, N$ - player sets
- [ ] $n_H, n_A, n$ - population sizes
- [ ] $\alpha$ - human population share
- [ ] $t_i, T_i$ - human types
- [ ] $\theta_j, \Theta_j$ - AI design parameters
- [ ] $\beta_i, \gamma_i, \omega_i$ - psychological parameters

### 2. Strategy and Payoff Notation
- [ ] $S_i, s_i, \sigma_i$ - strategies
- [ ] $\pi_i(s)$ - material payoffs
- [ ] $U_i^H, U_j^A$ - total utilities
- [ ] $\psi_i$ - psychological payoffs

### 3. Belief Hierarchy Notation
- [ ] $h_i^{(0)}, h_i^{(1)}, h_i^{(2)}$ - belief orders
- [ ] $h_i^{(2,k)}$ vs $h_i^{*(1,k)}$ - consistency
- [ ] $\tilde{h}_i^{(2,j)}$ - attributed beliefs (tilde notation)

### 4. Attribution Function Notation
- [ ] $\phi_i$ - attribution function
- [ ] $\phi_i^{beh}, \phi_i^{sig}, \phi_i^{disp}$ - variants
- [ ] $x_j, X$ - signals
- [ ] $\omega_i, \Omega_i$ - anthropomorphism

### 5. Psychological Payoff Notation
- [ ] $\psi_i^{IND}$ - indignation
- [ ] $\psi_i^{GUILT}$ - guilt
- [ ] $\lambda_i^{IND}, \lambda_i^{GUILT}$ - attenuation factors

### 6. Equilibrium Notation
- [ ] $s^*, h^*, \tilde{h}^*$ - equilibrium objects
- [ ] $BR_i^H, BR_j^A$ - best response correspondences
- [ ] $\Phi$ - fixed-point mapping

---

## Critical Logic Dependencies to Verify

1. **Definition → Theorem chain**:
   - Def 1 (Attributed Beliefs) → Def 5 (Game) → Def 6 (ABE) → Thm 1 (Existence)

2. **Assumption coverage**:
   - A1 (Regularity) used in existence proof Step 2
   - A2 (Attribution Continuity) used in Step 1
   - A3 (Boundedness) used in Step 2 for upper hemicontinuity

3. **Special case logic**:
   - Prop 1: $N_A = \emptyset$ → reduces to SPE
   - Prop 2: $\psi_i \equiv 0$ → reduces to Nash
   - Prop 3: rational attribution → Bayesian game

---

## Output Files Summary

| Phase | Files Generated |
|-------|-----------------|
| Phase 1 | `phase1_notation_framework.md`, `phase1_notation_equilibrium.md`, `phase1_notation_applications.md`, `phase1_notation_welfare.md` |
| Phase 2 | `phase2_check_players.md`, `phase2_check_beliefs.md`, `phase2_check_utility.md`, `phase2_check_logic.md`, `phase2_check_proofs.md` |
| Phase 3 | `phase3_aggregated_issues.md`, `phase3_recommendations.md` |
| Phase 4 | `phase4_revision_checklist.md`, `phase4_final_report.md` |

---

## Execution Timeline

```
Phase 1 (Parallel): [1A] [1B] [1C] [1D]
                         ↓
Phase 2 (Parallel): [2A] [2B] [2C] [2D] [2E]
                         ↓
Phase 3 (Sequential): [3A] → [3B]
                         ↓
Phase 4 (Parallel): [4A] [4B]
                         ↓
                   Final Report
```

**Total Agents**: 11 subagents across 4 phases

---

## Success Criteria

1. All notation symbols used consistently throughout all files
2. All definitions properly numbered and cross-referenced
3. All theorems/propositions cite correct assumptions
4. Belief hierarchy notation ($h$ vs original $\beta$) consistent
5. Attributed vs genuine belief distinction maintained
6. Proofs use notation consistent with main text
