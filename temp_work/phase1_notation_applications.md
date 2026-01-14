# Phase 1: Notation Inventory - Applications Section

**Source**: `/Users/xueheng/SynologyDrive/Research/pgt_human_ai_foundation/drafts/sec_applications.tex`

---

## 1. Game-Specific Notation

### Trust Game (Lines 7-33)

| Symbol | Definition | Connection to Framework |
|--------|------------|------------------------|
| $E$ | Endowment (AI trustor's initial amount) | Game-specific parameter |
| $x$ | Amount sent by AI trustor, $x \in [0, E]$ | Action of AI agent |
| $y$ | Amount returned by human trustee, $y \in [0, 3x]$ | Action of human |
| $3x$ | Tripled amount received by trustee | Payoff multiplier |
| $\pi_A$ | AI material payoff: $E - x + y$ | Instance of $\pi_i$ |
| $\pi_H$ | Human material payoff: $3x - y$ | Instance of $\pi_i$ |
| $\gamma_A$ | AI prosociality parameter | Framework's $\gamma_j$ for AI |
| $U_A(x, y; \gamma_A)$ | AI utility function | Programmed utility |
| $E + 2x$ | Total surplus term in AI utility | Prosocial component |
| $U_H(y; \tilde{h}_H)$ | Human trustee utility | Instance of $U_i$ |
| $\gamma_H$ | Human guilt sensitivity | Framework's $\gamma_i^{k}$ |
| $\lambda_H^{GUILT}$ | Guilt attenuation factor toward AI | Framework's $\lambda_i^{k}$ |
| $\tilde{h}_H^{(2,A)}$ | Attributed second-order belief (AI's expected return) | Framework's $\tilde{h}_i^{(2,j)}$ |
| $\phi_H(\gamma_A, x_A, \omega_H)$ | Attribution function | Framework's $\phi_i$ |
| $\omega_H$ | Human anthropomorphism parameter | Framework's $\omega_i$ |
| $y^*$ | Equilibrium return amount | Equilibrium notation |

### Public Goods Game (Lines 35-60)

| Symbol | Definition | Connection to Framework |
|--------|------------|------------------------|
| $n_H$ | Number of human players | Population partition |
| $n_A$ | Number of AI agents | Population partition |
| $n$ | Total players (implicit: $n = n_H + n_A$) | Population size |
| $N$ | Set of all players | Framework's $N$ |
| $N_H$ | Set of human players | Framework's $N_H$ |
| $N_A$ | Set of AI agents | Framework's $N_A$ |
| $c_i$ | Contribution of player $i$, $c_i \in [0, E]$ | Action |
| $m$ | Public good multiplier, $m > 1$ | Game parameter |
| $\pi_i$ | Material payoff | Framework's $\pi_i$ |
| $\psi_i^{IND}$ | Indignation psychological payoff | Instance of $\psi_i^k$ |
| $\beta_i$ | Indignation intensity | Similar to $\gamma_i$ |
| $\mathbf{1}_{c_i < c^*}$ | Indicator for defection | Conditional term |
| $c^*$ | Reference contribution level | Norm/expectation |
| $h_i^{(2,k)}(c^*)$ | Second-order belief about human $k$ | Framework's $h_i^{(2,k)}$ |
| $\tilde{h}_i^{(2,j)}(c^*)$ | Attributed belief about AI $j$ | Framework's $\tilde{h}_i^{(2,j)}$ |
| $\lambda_i^{IND}$ | Indignation attenuation toward AI | Framework's $\lambda_i^k$ |
| $c_A$ | AI contribution (programmed) | AI action |
| $\omega$ | Anthropomorphism (generic) | Framework's $\omega_i$ |
| $\alpha$ | Human population share | $\alpha = n_H / n$ |
| $1 - \alpha$ | AI population share | $= n_A / n$ |

### Coordination Game (Lines 62-87)

| Symbol | Definition | Connection to Framework |
|--------|------------|------------------------|
| $A$, $B$ | Technology choices | Actions (discrete) |
| $s$ | Strategy profile | Action profile |
| $s_i$ | Player $i$'s technology choice | Action |
| $\pi_i(s)$ | Material payoff (2 if coordinate, 0 otherwise) | Framework's $\pi_i$ |
| $\psi_i$ | Psychological payoff from matching expectations | Instance of $\psi_i$ |
| $\beta_i$ | Expectation-matching intensity | Similar to $\gamma_i$ |
| $\mathbf{1}_{s_i \neq s^{exp}}$ | Indicator for mismatching expectation | Conditional |
| $s^{exp}$ | Expected technology choice | Reference point |
| $h_i^{(2,k)}(s^{exp})$ | Second-order belief about human $k$ | Framework's $h_i^{(2,k)}$ |
| $\tilde{h}_i^{(2,j)}(s^{exp})$ | Attributed belief about AI $j$ | Framework's $\tilde{h}_i^{(2,j)}$ |
| $\lambda_i$ | Generic attenuation factor | Framework's $\lambda_i^k$ |
| $x_A$ | AI signal strength (clarity of technology choice) | Framework's $x_j$ |

---

## 2. Propositions

| Proposition | Label | Content Summary |
|-------------|-------|-----------------|
| Proposition 5 | `prop:trust` | Trust Game ABE: anthropomorphism affects returns |
| Proposition 6 | `prop:public-goods` | Public Goods ABE: AI contributions and anthropomorphism affect cooperation |
| Proposition 7 | `prop:coordination` | Coordination ABE: AI as focal point provider |

---

## 3. New Parameters (Application-Specific)

| Parameter | Game | Meaning | Notes |
|-----------|------|---------|-------|
| $E$ | Trust, Public Goods | Endowment | Standard game theory |
| $m$ | Public Goods | Multiplier (MPCR) | Marginal per capita return |
| $c^*$ | Public Goods | Reference contribution | Norm/expectation level |
| $s^{exp}$ | Coordination | Expected technology | Focal point |
| $\alpha$ | Public Goods | Human population share | New ratio parameter |
| $\beta_i$ | Public Goods, Coordination | Psychological intensity | Different from $\gamma_i$? |

---

## 4. Cross-Reference Analysis

### Consistent with Framework
- $\tilde{h}_i^{(2,j)}$: Attributed beliefs notation matches framework
- $\lambda_i^k$: Attenuation factors match (though superscripts vary)
- $\omega_i$: Anthropomorphism matches
- $\phi_i$: Attribution function matches
- $N_H$, $N_A$: Population partition matches

### Potential Inconsistencies/Issues

1. **$\beta_i$ vs $\gamma_i$**: In Public Goods and Coordination games, $\beta_i$ is used for psychological intensity, while the framework uses $\gamma_i^k$. Need to verify if these are the same or different parameters.

2. **Attenuation superscripts**: Trust uses $\lambda_H^{GUILT}$, Public Goods uses $\lambda_i^{IND}$, Coordination uses plain $\lambda_i$. Framework uses $\lambda_i^k$ (emotion-indexed). Need consistency check.

3. **$h_i^{(2,k)}(c^*)$ notation**: The argument $(c^*)$ suggests belief about a specific contribution level. This differs from framework's $h_i^{(2,k)}$ without arguments. Clarify semantics.

4. **$\alpha$ vs $n_H/n$**: The ratio $\alpha$ for human population share is introduced in Public Goods but not formally defined earlier. Check if framework defines this.

5. **$\omega$ vs $\omega_i$**: Sometimes written generically as $\omega$, sometimes as $\omega_i$. Should be consistent.

6. **Proposition numbering**: Labels suggest Props 5, 6, 7, but need to verify against sec_framework.tex to confirm correct ordering.

---

## 5. Numerical Examples

- Trust game: Tripling factor (3x)
- Coordination payoffs: 2 for coordination, 0 otherwise
- Public goods: $m > 1$ (no specific value)
- No other specific numerical examples given

---

## 6. Notation Summary Statistics

- **Total unique symbols**: ~50
- **Game-specific parameters**: 6 (E, m, c*, s^{exp}, alpha, beta_i)
- **Framework notation used**: 15+ instances
- **Potential inconsistencies**: 5 items flagged
- **Propositions**: 3 (Props 5-7)
