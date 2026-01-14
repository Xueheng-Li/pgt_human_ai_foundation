# Phase 2: Proof Reorganization Strategy

**Date**: 2026-01-14
**Objective**: Create a two-tier appendix structure to reduce paper length while preserving key arguments
**Target**: 51% word reduction in proofs (from ~15,600 to ~7,650 words in main appendix)

---

## Executive Summary

| Proof File | Current Words | Main Appendix | Supplement | Reduction |
|------------|---------------|---------------|------------|-----------|
| 01_thm_existence.tex | ~1,975 | ~850 | ~1,125 | 57% |
| 02_prop_reduction_pgt.tex | ~675 | ~375 | ~300 | 44% |
| 03_prop_reduction_nash.tex | ~600 | ~325 | ~275 | 46% |
| 04_prop_rational_attribution.tex | ~750 | ~475 | ~275 | 37% |
| 05_prop_multiplicity.tex | ~375 | ~325 | ~50 | 13% |
| 06_prop_trust_game.tex | ~750 | ~475 | ~275 | 37% |
| 07_prop_public_goods.tex | ~1,250 | ~575 | ~675 | 54% |
| 08_prop_coordination.tex | ~1,000 | ~525 | ~475 | 47% |
| 09_prop_welfare_anthropomorphism.tex | ~1,050 | ~525 | ~525 | 50% |
| 10_prop_welfare_over_anthro.tex | ~2,810 | ~1,100 | ~1,710 | 61% |
| 11_prop_optimal_design.tex | ~4,377 | ~1,700 | ~2,677 | 61% |
| **TOTAL** | **~15,612** | **~7,250** | **~8,362** | **54%** |

---

## Supplement Structure Template

Create file: `supplementary_appendix.tex` with this structure:

```latex
\documentclass[12pt]{article}
\title{Online Appendix: Thinking about Machines}
\date{\today}

\begin{document}
\maketitle

\section*{Overview}
This supplementary appendix contains technical details, routine calculations,
and extended discussions supporting the main text proofs.

%% SECTION OA.1: Existence Theorem Details
\section{Theorem 1: Existence of ABE}\label{oa:existence}
\subsection{Lemma A.1: Boundedness Proof}
[Content from lines 10-47 of 01_thm_existence.tex]

\subsection{Topology and Measure Theory Details}
[Content from lines 61-66, 73-91 of 01_thm_existence.tex]

\subsection{Remarks on Extensions}
[Content from lines 151-184 of 01_thm_existence.tex]

%% SECTION OA.2-OA.4: Reduction Propositions
\section{Propositions 2-4: Reduction Results}\label{oa:reductions}
\subsection{Detailed Steps for Reduction to PGT}
[Content from 02_prop_reduction_pgt.tex]

\subsection{Algebra for Reduction to Nash}
[Content from 03_prop_reduction_nash.tex]

\subsection{Belief Characterization for Rational Attribution}
[Content from 04_prop_rational_attribution.tex]

%% SECTION OA.5-OA.7: Application Proofs
\section{Application Proofs: Technical Details}\label{oa:applications}
\subsection{Trust Game: Numerical Examples and Remarks}
\subsection{Public Goods: Detailed Derivations and Remarks}
\subsection{Coordination: AI Utility Calculations and Remarks}

%% SECTION OA.8-OA.9: Welfare Results
\section{Welfare Propositions: Extended Analysis}\label{oa:welfare}
\subsection{Proposition 8: Numerical Examples and Remarks}
\subsection{Proposition 9: Part 1 Details and Remarks}

%% SECTION OA.10: Optimal Design
\section{Proposition 10: Optimal AI Design}\label{oa:optimal-design}
\subsection{Preamble Assumptions (Full Statement)}
\subsection{Part (i): Threshold Analysis Details}
\subsection{Part (ii): Complete Case Analysis}
\subsection{Part (iii): SOC and IFT Derivations}
\subsection{Remarks and Extensions}

\end{document}
```

---

## Detailed File-by-File Instructions

### 1. 01_thm_existence.tex (REVIEWER PRIORITY: Topology Details)

**Current**: ~1,975 words
**Target Main**: ~850 words
**Supplement**: ~1,125 words

#### KEEP in Main Appendix (Lines to Retain)

**Lemma A.1 Statement Only** (Lines 10-17, ~75 words):
```latex
\begin{lemma}[Boundedness of Psychological Payoffs]
\label{lem:bounded-psi}
Under Assumptions A1 (Regularity) and A2 (Attribution Continuity), for each human type $t_i \in T_i$, there exists $M(t_i) < \infty$ such that $|\psi_i(...)| \leq M(t_i)$ for all strategy profiles, beliefs, and attributed beliefs. By compactness of the type space, there exists a uniform bound $M = \sup_{t_i \in T_i} M(t_i) < \infty$.
\end{lemma}
```
**Add transition**: "See Online Appendix OA.1.1 for the proof."

**Main Theorem Proof Skeleton** (Lines 56-145, condensed to ~775 words):

- **Step 1** (Lines 60-66): CONDENSE to 2 sentences:
  ```latex
  \noindent\textbf{Step 1: Strategy space.}
  The space $\Sigma = \prod_{i \in N} \Delta(S_i)$ is compact and convex.
  See Online Appendix OA.1.2 for topology details.
  ```

- **Step 2** (Lines 68-91): CONDENSE (remove attribution cases):
  ```latex
  \noindent\textbf{Step 2: Belief computation.}
  Given $\sigma \in \Sigma$, genuine beliefs are $h_i^{(1,k)}(\sigma) = \sigma_k$ and $h_i^{(2,k)}(\sigma) = \sigma_i$ (coordinate projections, continuous). Under exogenous attribution, $\tilde{h}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$ is constant in $\sigma$, the key simplification: attributed beliefs do not create additional equilibrium conditions.
  ```

- **Step 3** (Lines 93-113): KEEP IN FULL (core argument for Kakutani)

- **Step 4** (Lines 116-121): KEEP IN FULL (fixed-point application)

- **Step 5** (Lines 124-145): KEEP IN FULL (equilibrium verification)

#### MOVE to Supplement (OA.1)

| Lines | Content | Supplement Section |
|-------|---------|-------------------|
| 19-43 | Lemma A.1 proof (Weierstrass, compactness) | OA.1.1 |
| 45-47 | Remark on lemma | OA.1.1 |
| 61-66 | Tychonoff's theorem, topology details | OA.1.2 |
| 73-91 | Three attribution approaches (i)-(iii), validity | OA.1.2 |
| 151-162 | Remark: Behavioral Attribution | OA.1.3 |
| 164-174 | Remark: Role of Assumptions | OA.1.3 |
| 176-179 | Remark: Comparison with PGT | OA.1.3 |
| 181-184 | Remark: Topology (REVIEWER CITED) | OA.1.3 |

**Transition Text** (add at end of main proof):
```latex
\begin{remark}
Technical details including the boundedness lemma proof, topology considerations,
and extensions to behavioral attribution appear in Online Appendix OA.1.
\end{remark}
```

---

### 2. 02_prop_reduction_pgt.tex

**Current**: ~675 words
**Target Main**: ~375 words
**Supplement**: ~300 words

#### KEEP in Main Appendix

- **Lines 5-6**: Scope clarification (~25 words)
- **Lines 7-20**: PNE Definition (~125 words) - KEEP
- **Lines 22-31**: Steps 1-2 (vacuous conditions) - KEEP
- **Lines 103-116**: Step 7 conclusion - KEEP

#### MOVE to Supplement (OA.2.1)

| Lines | Content | Reason |
|-------|---------|--------|
| 43-53 | Step 3: Psychological payoff simplification | Routine algebra |
| 56-68 | Step 4: Human utility reduction | Follow-on |
| 71-84 | Step 5: ABE1 to PNE1 | Routine verification |
| 86-100 | Step 6: ABE3 to PNE2 | Routine verification |
| 118-120 | Remark: Converse direction | Extension |

**Condensed Main Text**:
```latex
\begin{proof}
Suppose $N_A = \emptyset$, so $N = N_H$.

\textbf{Step 1:} ABE2 and ABE4 are vacuously satisfied (quantification over empty $N_A$).

\textbf{Step 2:} The attributed belief system is empty: $\tilde{h}^* = \emptyset$.

\textbf{Step 3-6:} With empty $N_A$, psychological payoffs depend only on genuine beliefs, and the ABE conditions reduce exactly to PNE conditions. See Online Appendix OA.2.1 for detailed verification.

Therefore, $(s^*, h^*, \tilde{h}^*)$ is an ABE if and only if $(s^*, h^*)$ is a PNE.
\end{proof}
```

---

### 3. 03_prop_reduction_nash.tex

**Current**: ~600 words
**Target Main**: ~325 words
**Supplement**: ~275 words

#### KEEP in Main Appendix

- **Lines 1-9**: Setup and incomplete information note
- **Lines 11-13**: Part 1 statement
- **Lines 42-47**: Part 1 conclusion (Step 1.4)
- **Lines 50-51**: Part 2 statement
- **Lines 89-96**: Part 2 conclusion
- **Lines 94-96**: Part 3 uniqueness

#### MOVE to Supplement (OA.2.2)

| Lines | Content |
|-------|---------|
| 14-40 | Steps 1.1-1.3 detailed algebra |
| 53-88 | Steps 2.1-2.3 verification details |
| 98-104 | Both remarks |

**Condensed Main Text**:
```latex
\begin{proof}
\textbf{Part 1 (ABE $\Rightarrow$ Nash):} When $\psi_i \equiv 0$, human utility reduces to $U_i^H = \pi_i(s)$. The ABE optimality conditions become Nash best-response conditions. Hence $s^*$ is a Nash equilibrium of $\Gamma^M$. (Details in OA.2.2.)

\textbf{Part 2 (Nash $\Rightarrow$ ABE):} Given Nash equilibrium $s^*$, construct beliefs by $h_i^{*(1,k)} = s_k^*$, $h_i^{*(2,k)} = s_i^*$, and $\tilde{h}_i^{*(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$. All ABE conditions are satisfied. (Details in OA.2.2.)

\textbf{Part 3:} The belief systems are uniquely determined by the consistency conditions.
\end{proof}
```

---

### 4. 04_prop_rational_attribution.tex

**Current**: ~750 words
**Target Main**: ~475 words
**Supplement**: ~275 words

#### KEEP in Main Appendix

- **Lines 5-37**: Bayesian game construction $\Gamma^B$ (essential)
- **Lines 39-45**: Part (a) statement and setup
- **Lines 63-81**: Part (a) Steps 2-3 (optimality verification)
- **Lines 96-99**: Part (b) statement
- **Lines 114-132**: Part (b) verification sketch
- **Lines 134-137**: Conclusion

#### MOVE to Supplement (OA.2.3)

| Lines | Content |
|-------|---------|
| 35-37 | Remark on equilibrium-dependence |
| 47-62 | Step 1 detailed belief characterization |

---

### 5. 05_prop_multiplicity.tex

**Current**: ~375 words
**Target Main**: ~325 words
**Supplement**: ~50 words

**Already concise** - minimal changes needed.

#### MOVE to Supplement (OA.2.4)

| Lines | Content |
|-------|---------|
| 9-14 | Sufficient Conditions block (move to supplement, reference in main) |

**Main Text Modification**:
Add at line 8: "Under sufficient conditions stated in Online Appendix OA.2.4, attribution-dependent multiplicity occurs."

---

### 6. 06_prop_trust_game.tex

**Current**: ~750 words
**Target Main**: ~475 words
**Supplement**: ~275 words

#### KEEP in Main Appendix

- **Lines 9-27**: Part (i) proof - KEEP IN FULL
- **Lines 29-69**: Part (ii) proof - KEEP IN FULL (key derivation)
- **Lines 71-109**: Part (iii) proof and example - KEEP core, CONDENSE table

#### MOVE to Supplement (OA.5.1)

| Lines | Content |
|-------|---------|
| 111-114 | Remark: G=1 knife-edge |
| 116-119 | Remark: G<1 case |
| 121-123 | Remark: Connection to multiplicity |
| 125-127 | Remark: Empirical support |

**Transition Text**:
```latex
\begin{remark}
Extended analysis including knife-edge cases, low guilt regimes, and empirical
support appears in Online Appendix OA.5.1.
\end{remark}
```

---

### 7. 07_prop_public_goods.tex (HIGH PRIORITY: 7 Remarks)

**Current**: ~1,250 words
**Target Main**: ~575 words
**Supplement**: ~675 words

#### KEEP in Main Appendix

- **Lines 13-81**: Part (i) proof - CONDENSE Steps 1-8 to essentials
- **Lines 83-119**: Part (ii) proof - KEEP core
- **Lines 121-162**: Part (iii) proof - KEEP mechanism, MOVE detailed derivation

#### MOVE to Supplement (OA.5.2)

| Lines | Content |
|-------|---------|
| 123-148 | Part (iii) detailed channel analysis |
| 150-159 | Channel comparison table |
| 164-171 | Remark: Connection to standard PGT |
| 173-176 | Remark: Role of attenuation |
| 178-181 | Remark: Boundary cases |
| 183-186 | Remark: Role of (A2') |
| 188-198 | Remark: Empirical implications |
| 200-203 | Remark: Threshold interpretation |

**Condensed Part (iii)**:
```latex
\noindent\textbf{Proof of (iii): Population share effects.}
Higher $n_A$ affects equilibrium through two channels: (1) material---diluting MPCR,
increasing free-rider temptation; (2) psychological---more sources of attributed
expectations. The psychological channel has constant marginal effect; the material
channel weakens as $n_A$ grows. For sufficiently large $n_A$, the psychological
channel dominates. See Online Appendix OA.5.2 for detailed derivations.
```

---

### 8. 08_prop_coordination.tex

**Current**: ~1,000 words
**Target Main**: ~525 words
**Supplement**: ~475 words

#### KEEP in Main Appendix

- **Lines 9-46**: Game setup and required conditions - KEEP
- **Lines 49-74**: Part (i) proof - CONDENSE AI utility calculation
- **Lines 77-107**: Part (ii) proof - KEEP
- **Lines 109-144**: Part (iii) proof - KEEP core verification

#### MOVE to Supplement (OA.5.3)

| Lines | Content |
|-------|---------|
| 51-61 | Detailed AI utility calculation |
| 146-159 | Remark: Numerical example |
| 161-163 | Remark: Knife-edge x_A = 0.5 |
| 165-167 | Remark: Contrast with Schelling |
| 169-171 | Remark: Connection to multiplicity |

**Condensed Part (i) Step 1**:
```latex
\emph{Step 1 (AI's optimal strategy).}
Given design commitment $\theta_A > 0$, AI strictly prefers $A$ regardless of human play
when $\theta_A > 2$, or prefers $A$ when human plays $A$ for $\theta_A \leq 2$.
Under binding constraint interpretation, $s_A^* = A$ in any ABE. (Details in OA.5.3.)
```

---

### 9. 09_prop_welfare_anthropomorphism.tex

**Current**: ~1,050 words
**Target Main**: ~525 words
**Supplement**: ~525 words

#### KEEP in Main Appendix

- **Lines 11-63**: Part 1 proof - CONDENSE to key steps
- **Lines 70-106**: Part 2 mechanism - KEEP core
- **Lines 134-138**: Step 7 mechanism summary - KEEP

#### MOVE to Supplement (OA.6.1)

| Lines | Content |
|-------|---------|
| 108-131 | Step 6 numerical example (table and calculations) |
| 144-147 | Remark: Weak vs strict |
| 149-152 | Remark: Why "may reduce" |
| 154-162 | Remark: Asymmetry |
| 164-167 | Remark: Connection to propositions |
| 169-172 | Remark: Policy implications |

**Condensed Part 1**:
```latex
\noindent\textbf{Part 1:} By Proposition~\ref{prop:public-goods}(i), cooperation requires
$\omega_i \geq \bar{\omega}_i$. Higher $\omega$ lowers the threshold, expanding the
cooperation region. Since cooperation is efficient ($W^C > W^D$), $\partial W / \partial \omega \geq 0$,
with strict inequality at threshold crossings.
```

---

### 10. 10_prop_welfare_over_anthro.tex (HIGH PRIORITY)

**Current**: ~2,810 words
**Target Main**: ~1,100 words
**Supplement**: ~1,710 words

#### KEEP in Main Appendix

- **Lines 27-28**: Proof opening with conditions
- **Lines 35-50**: Zero-anthropomorphism benchmark definition - KEEP (essential)
- **Lines 52-57**: Elevated anthropomorphism definition - KEEP (key concept)
- **Lines 68-70**: Part 1 statement
- **Lines 70**: "This part is a direct corollary of Proposition 8" - KEEP
- **Lines 136**: Part 1 conclusion
- **Lines 142-147**: Part 2 statement and mechanism
- **Lines 149-174**: Part 2 phantom expectations setup (Steps 1-2)
- **Lines 176-186**: Step 3 equilibrium returns
- **Lines 266-276**: Step 7 mechanism summary
- **Lines 277**: Part 2 conclusion

#### MOVE to Supplement (OA.6.2)

| Lines | Content | Supplement Section |
|-------|---------|-------------------|
| 52-62 | Equivalence under (A2') and (A2'') verification | OA.6.2.1 |
| 73-135 | Part 1 detailed steps (Steps 1-4) | OA.6.2.2 |
| 188-231 | Part 2 Steps 4-5 welfare calculations | OA.6.2.3 |
| 234-263 | Numerical example (full table and calculations) | OA.6.2.3 |
| 283-286 | Remark: Contribution relative to Prop 8 | OA.6.2.4 |
| 288-291 | Remark: Terminology | OA.6.2.4 |
| 293-296 | Remark: Weak vs strict | OA.6.2.4 |
| 298-301 | Remark: Why "may reduce" | OA.6.2.4 |
| 303-311 | Remark: Asymmetric welfare | OA.6.2.4 |
| 313-325 | Remark: Policy implications | OA.6.2.4 |
| 327-330 | Remark: Cultural variation | OA.6.2.4 |

**Condensed Main Text Structure**:
```latex
\begin{proof}[Proof of Proposition~\ref{prop:over-anthro}]
Two parts. [Conditions as in line 28.]

\textbf{Zero-Anthropomorphism Benchmark.}
[Lines 35-50, slightly condensed]

\textbf{Elevated Anthropomorphism.}
[Lines 45-50]

\medskip
\noindent\textbf{Part 1:} This is a direct corollary of Proposition~\ref{prop:welfare-anthro}.
Higher $\omega_i$ lowers the cooperation threshold, expanding the cooperation region
when AI is prosocial. Since cooperation is efficient, material welfare weakly increases.
See Online Appendix OA.6.2.2 for detailed steps.

\medskip
\noindent\textbf{Part 2:} We construct a setting demonstrating the \emph{phantom expectations}
mechanism: elevated anthropomorphism of materialist AI creates welfare loss.

[Keep Steps 1-3 from lines 149-186]

[Condense Steps 4-5]: Extended welfare under phantom expectations that exceed feasibility
falls below the zero-anthropomorphism benchmark. At $\omega_H = 0.75$ with parameters
$E = 10$, $x = 10$, $G = 1.5$, extended welfare is 7.5 versus 30 under $\omega_H = 0$.
See Online Appendix OA.6.2.3 for complete calculations.

\textbf{Mechanism:} [Lines 266-276]

This completes Part 2. \hfill $\square$
\end{proof}

\begin{remark}
Extended analysis including detailed welfare calculations, numerical examples, and
policy implications appears in Online Appendix OA.6.2.
\end{remark}
```

---

### 11. 11_prop_optimal_design.tex (HIGHEST PRIORITY)

**Current**: ~4,377 words
**Target Main**: ~1,700 words
**Supplement**: ~2,677 words

#### KEEP in Main Appendix

**Preamble** (Lines 18-81): CONDENSE significantly
```latex
\begin{proof}[Proof of Proposition~\ref{prop:optimal-design}]
Three parts under conditions (A1)--(A3), (A2'), (A2'''), with (E), (I), (T) for Part (i)
and (G') for Parts (ii)--(iii). The planner maximizes reduced-form welfare $\mathcal{W}(x)$
over signal $x \in [0, \bar{x}]$; existence follows from Weierstrass.
See Online Appendix OA.7.1 for full assumption statements.
```

**Part (i)** (Lines 86-187): KEEP core structure
- Lines 90-105: Setup and attribution - CONDENSE
- Lines 108-116: Cooperation threshold formula - KEEP
- Lines 138-145: Threshold comparative static - KEEP
- Lines 147-156: Welfare function - KEEP
- Lines 158-176: Optimization three cases - CONDENSE
- Lines 178-186: Comparative static result - KEEP

**Part (ii)** (Lines 200-291): CONDENSE significantly
- Lines 204-237: Setup through equilibrium return - CONDENSE
- Lines 271-291: Optimality conclusion - KEEP

**Part (iii)** (Lines 304-473): KEEP key structure, MOVE derivations
- Lines 308-326: Setup and tradeoff - KEEP
- Lines 328-344: Extended welfare - CONDENSE
- Lines 356-363: FOC result - KEEP
- Lines 467-471: Summary results - KEEP

#### MOVE to Supplement (OA.7)

| Lines | Content | Supplement Section |
|-------|---------|-------------------|
| 29-44 | Full assumption statements | OA.7.1 |
| 46-74 | Decision-maker, welfare measures, linear attribution | OA.7.1 |
| 118-136 | Claim proof: threshold in (0,1) | OA.7.2 |
| 239-268 | Part (ii) complete case analysis A, B, C | OA.7.3 |
| 366-386 | Part (iii) SOC verification | OA.7.4 |
| 389-462 | Part (iii) IFT derivations | OA.7.4 |
| 480-488 | Remark: Unified interpretation | OA.7.5 |
| 490-498 | Remark: Welfare criterion consistency | OA.7.5 |
| 500-508 | Remark: Reconciliation of m | OA.7.5 |
| 510-517 | Remark: Nesting of cases | OA.7.5 |
| 519-529 | Remark: Role of assumptions | OA.7.5 |
| 531-539 | Remark: Decision-maker incentives | OA.7.5 |
| 541-549 | Remark: Boundary cases | OA.7.5 |
| 551-559 | Remark: Policy implications | OA.7.5 |
| 561-570 | Remark: Connection to Props 8-9 | OA.7.5 |

**Condensed Main Text Structure**:
```latex
\begin{proof}[Proof of Proposition~\ref{prop:optimal-design}]
Three parts. Full assumption statements in Online Appendix OA.7.1.

\medskip
\noindent\textbf{Part (i): Prosocial AI ($\rho_A = 1$).}

Cooperation requires $\omega \geq \bar{\omega}(x)$, where:
\begin{equation}
    \bar{\omega}(x) = \frac{E(1 - m/n) - \beta(n_H - 1)}{\beta \lambda^{IND} n_A (\bar{h}_H + \eta x)}.
\end{equation}
Under (T) and (I), $\bar{\omega}(x) \in (0,1)$ (proof in OA.7.2). Since
$\partial \bar{\omega}/\partial x < 0$, higher $x$ expands cooperation. The welfare-maximizing
signal is the minimal level sufficient to induce cooperation:
\begin{equation}
    x^* = \max\left\{ 0, \frac{1}{\eta}\left[ \frac{E(1-m/n) - \beta(n_H-1)}{\beta \lambda^{IND} n_A \omega} - \bar{h}_H \right] \right\}.
\end{equation}
Comparative static: $\partial x^*/\partial m < 0$ (higher efficiency reduces required signal).

\medskip
\noindent\textbf{Part (ii): Materialist AI ($\rho_A = 0$).}

With $\rho_A = 0$, all attributed expectations are phantom: $\tilde{h}_H^{(2,A)} = \omega_H \eta x$.
Equilibrium return is $y^* = \min\{\omega_H \eta x, 3x_{send}\}$. Extended welfare analysis
(complete in OA.7.3) shows $W^{ext}(x) \leq W^{ext}(0)$ for all $x$, with strict inequality
when phantom expectations exceed feasibility. Therefore $x^* = 0$: minimal anthropomorphism is optimal.

\medskip
\noindent\textbf{Part (iii): Mixed AI ($\rho_A \in (0,1)$).}

The planner faces a tradeoff: higher $x$ expands cooperation (benefit) but raises guilt
from phantom expectations (cost). At an interior optimum, the FOC balances these margins.
The SOC $\mathcal{W}''(x^*) < 0$ is verified in OA.7.4.

Comparative statics via implicit function theorem (derivations in OA.7.4):
\begin{equation}
    \frac{\partial x^*}{\partial m} > 0, \quad \frac{\partial x^*}{\partial G} < 0, \quad \frac{\partial x^*}{\partial \omega} < 0.
\end{equation}
Higher efficiency justifies more signal; higher guilt sensitivity or anthropomorphism tendency
justifies less.
\end{proof}

\begin{remark}
Technical details including threshold analysis, complete case analysis for Part (ii),
SOC/IFT derivations, and extended discussion appear in Online Appendix OA.7.
\end{remark}
```

---

## Implementation Checklist

### Phase 1: Create Supplement Structure
- [ ] Create `supplementary_appendix.tex` with section structure above
- [ ] Add preamble with shared packages/notation

### Phase 2: High-Priority Files (Reviewer-Cited)
- [ ] **01_thm_existence.tex**: Remove topology remarks, condense lemma to statement only
- [ ] **11_prop_optimal_design.tex**: Move all 11 remarks, condense assumptions preamble
- [ ] **10_prop_welfare_over_anthro.tex**: Move Part 1 details, condense numerical example

### Phase 3: Application Proofs
- [ ] **07_prop_public_goods.tex**: Move all 7 remarks
- [ ] **08_prop_coordination.tex**: Move all 4 remarks
- [ ] **06_prop_trust_game.tex**: Move all 4 remarks

### Phase 4: Reduction Propositions
- [ ] **02_prop_reduction_pgt.tex**: Condense step-by-step algebra
- [ ] **03_prop_reduction_nash.tex**: Condense verification details
- [ ] **04_prop_rational_attribution.tex**: Condense belief characterization

### Phase 5: Remaining Files
- [ ] **09_prop_welfare_anthropomorphism.tex**: Move numerical example and remarks
- [ ] **05_prop_multiplicity.tex**: Minor adjustment (sufficient conditions block)

### Phase 6: Final Verification
- [ ] Verify all cross-references work
- [ ] Check supplement section numbers match main text references
- [ ] Word count verification

---

## Standard Transition Phrases

Use these consistently throughout main appendix:

1. **For detailed proofs**: "See Online Appendix OA.X for the complete proof."
2. **For routine calculations**: "Routine calculations confirm that... (details in OA.X)."
3. **For numerical examples**: "Numerical examples appear in Online Appendix OA.X."
4. **For remarks**: "Extended discussion including [topic] appears in OA.X."
5. **For case analysis**: "The complete case analysis appears in OA.X; here we summarize the key insight."
6. **For IFT/SOC**: "Second-order conditions and implicit function theorem derivations appear in OA.X."

---

## Word Count Summary by Priority

| Priority | Files | Current | Target | Savings |
|----------|-------|---------|--------|---------|
| HIGH (Reviewer) | 01, 10, 11 | 9,162 | 3,650 | 5,512 (60%) |
| MEDIUM | 07, 08, 09 | 3,300 | 1,625 | 1,675 (51%) |
| LOWER | 02, 03, 04, 05, 06 | 3,150 | 1,975 | 1,175 (37%) |
| **TOTAL** | **11 files** | **15,612** | **7,250** | **8,362 (54%)** |

---

## Estimated Page Savings

- Main appendix reduction: ~8,350 words / 250 words per page = **~33 pages saved**
- Note: Supplement does not count toward journal page limits
- Target: Reduce main appendix from ~62 pages to ~29 pages (keeping some buffer)
