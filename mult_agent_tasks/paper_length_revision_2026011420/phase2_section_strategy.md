# Phase 2: Section-by-Section Tightening Strategy

**Generated:** January 14, 2026
**Objective:** Reduce paper length by 20-25% while preserving academic rigor

---

## Executive Summary

| Section | Current Words | Target Words | Reduction | Priority |
|---------|--------------|--------------|-----------|----------|
| Introduction | ~2,100 | ~1,800 | 15% | Medium |
| Framework | ~3,400 | ~2,400 | 30% | **HIGH** |
| Equilibrium | ~2,850 | ~2,300 | 20% | Medium |
| Applications | ~1,450 | ~1,300 | 10% | Low |
| Welfare | ~2,000 | ~1,700 | 15% | Medium |
| Conclusion | ~1,600 | ~1,100 | 30% | **HIGH** |
| **Total** | **~13,400** | **~10,600** | **~21%** | |

---

## Section 1: Introduction (sec_introduction.tex)

**Current:** ~2,100 words | **Target:** ~1,800 words | **Priority:** Medium

### Passages to Cut or Condense

#### 1.1 Lines 25-26: Technical Definition Details
**Current (Lines 25-26):**
```latex
The framework introduces two distinct benchmarks. The \textit{zero-anthropomorphism benchmark} identifies what humans would attribute absent anthropomorphic bias---a descriptive baseline at a specific parameter value. The \textit{Rational Attribution Equilibrium} (RAE, Definition~10) requires attributed beliefs to equal equilibrium strategies---an equilibrium concept satisfying a fixed-point condition. Zero-anthropomorphism is descriptive; RAE is normative.
```
**Action:** Move to Section 3. The Introduction should mention these concepts exist, not define them.
**Rewrite:**
```latex
The framework introduces a zero-anthropomorphism benchmark and Rational Attribution Equilibrium (RAE) to distinguish descriptive and normative baselines.
```
**Savings:** ~60 words

#### 1.2 Lines 43-51: Related Literature - Repetitive Content
**Issue:** Lines 47-49 (anthropomorphism and mind perception literature) repeat content from Line 17 (mind perception theory) and Lines 48-49.

**Current (Lines 47-49):**
```latex
\textit{Anthropomorphism and mind perception.} \citet{epley2007seeing} identify three determinants of anthropomorphism in the SEEK framework: sociality motivation, effectance motivation, and elicited agent knowledge. These map to our model: sociality and effectance shape individual anthropomorphism tendency; agent knowledge corresponds to observable design signals. \citet{nass2000machines} established that humans apply social rules to computers even when they know they interact with machines.

\citet{gray2007dimensions} decompose mind perception into agency (capacity to act and form intentions) and experience (capacity to feel and suffer). This distinction explains why attribution and attenuation coexist: AI is attributed high agency but low experience. Agency drives attribution; low perceived experience drives attenuation. \citet{karpus2025cross} find Japanese participants exhibit guilt toward robots comparable to humans, while Western participants show strong attenuation---indicating attenuation is culturally variable. Design features conveying emotional capacity partially restore guilt. We formalize these patterns through attenuation parameters varying across individuals and contexts.
```
**Action:** Condense to one paragraph; agency/experience distinction already in Line 17.
**Rewrite:**
```latex
\textit{Anthropomorphism and mind perception.} \citet{epley2007seeing}'s SEEK framework identifies three determinants of anthropomorphism---sociality motivation, effectance motivation, and elicited agent knowledge---mapping to individual tendency $\omega_i$ and observable signals $x_j$ in our model. \citet{gray2007dimensions} decompose mind perception into agency and experience; this distinction explains why attribution and attenuation coexist. \citet{karpus2025cross} find attenuation is culturally variable: Japanese participants exhibit guilt toward robots comparable to humans, while Western participants show strong attenuation.
```
**Savings:** ~100 words

#### 1.3 Lines 51: Anthropomorphic Design Paragraph
**Current (Lines 51):**
```latex
\textit{Anthropomorphic design.} \citet{schroeder2016voice} show that voice increases mind attribution; \citet{wiese2017robots} document effects of gaze and movement; \citet{waytz2014trusting} demonstrate that naming and voice increase trust. These design effects operate through the attribution channel we formalize. Our optimal design principles derive from this connection: prosocial AI benefits from anthropomorphic features elevating cooperation-inducing expectations; materialist AI should avoid anthropomorphic presentation creating phantom expectations (Proposition~10). Private designers may over-anthropomorphize materialist AI to increase engagement, externalizing psychological costs---a case for transparency regulation.
```
**Action:** Merge with mind perception paragraph; the policy point repeats Section 5.
**Rewrite:** Delete this paragraph entirely; content covered in mind perception paragraph and Section 5.
**Savings:** ~90 words

### Redundancies to Eliminate

| Location | Redundant Content | First Appearance | Action |
|----------|-------------------|------------------|--------|
| Line 15 & Lines 32-33 | "phantom expectations" defined | Line 15 | Keep Line 15, cut Line 33 repetition |
| Line 17 & Lines 48-49 | agency/experience distinction | Line 17 | Keep Line 17 only |
| Lines 35 & 51 | transparency regulation point | Line 37 | Keep Line 37 |

### Summary: Introduction Cuts

| Item | Savings |
|------|---------|
| Technical definitions (move to Sec 3) | 60 words |
| Mind perception consolidation | 100 words |
| Anthropomorphic design paragraph | 90 words |
| Minor redundancy cleanup | 50 words |
| **Total** | **~300 words** |

---

## Section 2: Framework (sec_framework.tex)

**Current:** ~3,400 words | **Target:** ~2,400 words | **Priority:** HIGH

### HIGH PRIORITY CUTS (Reviewer-Flagged)

#### 2.1 Section 2.6.1 (Lines 100-180): Empirical Implementation
**Reviewer Comment:** "raises more questions than it answers... streamline to demonstrate testability in principle"

**Current:** ~550 words across Lines 100-180

**Specific Cuts:**

**Lines 115-137 (Trust Game Experimental Design):** Cut from ~200 words to ~80 words
```latex
% CURRENT (Lines 115-137): Overly detailed experimental design
\paragraph{Application: Trust Game with Interface Manipulation.}

We illustrate the identification strategy with a trust game where an AI trustor sends $x \in [0, E]$ to a human trustee, who returns $y \in [0, 3x]$. The human's attributed belief $\tilde{h}_H^{(2,A)}$ represents what the human believes the AI expected her to return.

\emph{Experimental design.} Between-subject manipulation varies interface anthropomorphism $x_A$:
\begin{itemize}
    \item Treatment R (Robotic): Minimalist interface displaying only numerical information; $x_A^R = 0$
    \item Treatment H (Humanoid): Avatar with name, voice feedback, and natural language; $x_A^H = 1$
    \item Treatment C (Control): Standard interface without anthropomorphic or de-anthropomorphic cues; $x_A^C = 0.5$
\end{itemize}

The AI's prosociality parameter $\rho_A$ and programmed behavior remain constant across treatments. Only the interface presentation varies.

\emph{Measurement sequence.} For each treatment:
\begin{enumerate}
    \item Subjects complete the IDAQ questionnaire (measures $\omega_i$)
    \item Subjects observe the AI interface and its transfer decision $x_A$
    \item Subjects report $\tilde{h}_i^{(2,A)}$: ``What return amount do you believe the AI expected you to send?'' (incentivized via quadratic scoring)
    \item Subjects choose return amount $y_i$
    \item One of tasks (3) or (4) is randomly selected for payment
\end{enumerate}

The within-subject strategy method extension elicits beliefs for all three interface conditions before random assignment, providing three observations per subject.
```

**REWRITE:**
```latex
\paragraph{Application: Trust Game with Interface Manipulation.}

We illustrate identification with a trust game where an AI trustor sends $x \in [0, E]$ to a human trustee who returns $y \in [0, 3x]$. Between-subject manipulation varies interface anthropomorphism across three treatments: robotic ($x_A = 0$), humanoid ($x_A = 1$), and control ($x_A = 0.5$), holding AI behavior constant. Subjects complete the IDAQ, observe the AI interface, report attributed beliefs via incentivized elicitation, and choose return amounts. Random payment selection (belief or choice) eliminates hedging.
```
**Savings:** ~120 words

**Lines 162-180 (Alternative Functional Forms):** CUT ENTIRELY
```latex
% DELETE Lines 162-180: Alternative functional forms are tangential
\paragraph{Alternative Functional Forms.}

The linear specification in Example 1 serves as a tractable benchmark. Two departures merit consideration.

\emph{Saturation.} Attributed beliefs are bounded in $[0,1]$, but the linear form $\omega_i(\rho_A + \eta x_A)$ may exceed unity for high parameter values. A logistic specification:
\begin{equation}
    \tilde{h}_i^{(2,A)} = \frac{1}{1 + \exp(-\omega_i(\rho_A + \eta x_A - \mu))}
\end{equation}
bounds attributed beliefs while preserving the interaction structure. The shift parameter $\mu$ centers the logistic at the midpoint of the belief scale.

\emph{Thresholds.} The uncanny valley phenomenon \citep{mori1970uncanny,gray2012feeling} suggests non-monotonicity: extremely human-like AI may trigger discomfort that reduces attribution. A threshold model:
\begin{equation}
    \tilde{h}_i^{(2,A)} = \omega_i \cdot \left( \rho_A + \eta x_A \right) \cdot \mathbf{1}_{x_A < \bar{x}}
\end{equation}
captures attribution collapse above threshold $\bar{x}$.

These alternatives generate distinct predictions. Saturation predicts diminishing marginal effects of $x_A$ at high levels; thresholds predict a discrete drop in $\tilde{h}_i^{(2,A)}$ above $\bar{x}$. Both can be tested by including quadratic or spline terms in regression (\ref{eq:attribution-regression}). In our trust game design, Treatment H ($x_A = 1$) tests whether extreme anthropomorphism triggers uncanny valley effects.

For applications in this paper, we maintain the linear specification. Empirical evidence on anthropomorphism-trust relationships \citep{blut2021understanding} is consistent with linearity over the range of interface manipulations typical in economic experiments. The linear form also yields closed-form equilibria enabling comparative statics.
```
**Action:** Move to supplementary appendix or delete. Add one sentence to Example 1.
**Add to Line 98:**
```latex
Alternative specifications (logistic, threshold) accommodate saturation and uncanny valley effects; we maintain linearity for tractability.
```
**Savings:** ~200 words

#### 2.2 Section 2.6.2 (Lines 182-193): Mind Perception Psychology
**Reviewer Comment:** "perhaps excessive for Econometrica"

**Current:** ~450 words across Lines 182-193

**Specific Cuts:**

**Lines 187-191 (SEEK Framework Details):** Condense dramatically
```latex
% CURRENT (Lines 187-191): Excessive SEEK detail
The SEEK framework \citep{epley2007seeing} identifies three determinants of anthropomorphism: \emph{Sociality} (the drive for social connection), \emph{Effectance} (the motivation to understand and predict behavior), and \emph{Elicited agent knowledge} (accessibility of human-related concepts). Sociality and effectance are dispositional, corresponding to individual variation in $\omega_i$. Elicited agent knowledge is situational: humanlike features such as voice, name, or conversational style activate human schemas, increasing attribution weight. When AI uses natural language, anthropocentric knowledge becomes accessible, amplifying the effect of $x_j$ on $\phi_i$.
```

**REWRITE:**
```latex
The SEEK framework \citep{epley2007seeing} identifies three determinants of anthropomorphism: dispositional factors (sociality, effectance) corresponding to $\omega_i$, and situational triggers (elicited agent knowledge) corresponding to observable signals $x_j$.
```
**Savings:** ~80 words

**Lines 189-191 (Agency/Experience Redundancy):** Already in Introduction (Line 17)
```latex
% CURRENT (Lines 189): Redundant with Introduction
A second body of work decomposes mind perception into two orthogonal dimensions \citep{gray2007dimensions,waytz2010causes}. The \emph{Agency} dimension captures perceived capacity for planning, self-control, and intentional action; the \emph{Experience} dimension captures perceived capacity for feeling, suffering, and subjective states. AI agents score high on agency but low on experience. This asymmetry maps to our two mechanisms. Attribution ($\phi_i$) is triggered by perceived agency: when AI appears to deliberate and choose, humans infer beliefs and intentions. Attenuation ($\lambda_i^{GUILT}, \lambda_i^{IND}$) is driven by low perceived experience: knowing that AI cannot truly suffer reduces guilt sensitivity. The two dimensions operate independently, explaining why the same human can both attribute beliefs to AI and feel reduced guilt exploiting it.
```

**REWRITE:**
```latex
Mind perception decomposes into agency and experience \citep{gray2007dimensions}. AI scores high on agency (triggering attribution) but low on experience (driving attenuation). These dimensions operate independently, explaining their coexistence.
```
**Savings:** ~100 words

**Lines 191-193 (System 1/System 2 Discussion):** Cut entirely; covered in Section 2.6.4
```latex
% DELETE Lines 191-193: Redundant with Section 2.6.4
The SEEK framework incorporates a dual-process interpretation. Anthropomorphism operates as a System~1 response: humans automatically use self-knowledge as a template for reasoning about any agent. System~2 corrects this inference when people have time, motivation, and explicit knowledge that the target differs from humans. Correction is effortful and incomplete \citep{epley2007seeing}. The attribution function captures this: $\omega_i$ reflects the strength of automatic anthropomorphism, while signals $x_j$ modulate the degree of correction. Under cognitive load, correction diminishes and $\phi_i$ increases. Even users who know AI lacks mental states exhibit residual attribution because System~2 correction is incomplete.

This psychological foundation grounds our functional form choices. The linear specification in Example~\ref{ex:linear-attribution} reflects the SEEK prediction that attribution increases monotonically in both dispositional tendency ($\omega_i$) and situational triggers ($x_j$). The two-dimensional structure of mind perception justifies treating attribution and attenuation as separate mechanisms with distinct antecedents. These foundations link the model to empirical predictions in Section~\ref{sec:empirical-implementation}: regression estimates of $\omega_i$ correspond to validated individual difference measures \citep{waytz2010who}, and experimental variation in $x_j$ manipulates the situational triggers that SEEK identifies as determinants of attribution.
```
**Action:** Delete Lines 191-193 entirely.
**Savings:** ~150 words

#### 2.3 Section 2.6.4 (Lines 281-294): Belief Revision Puzzle
**Issue:** Overlaps significantly with Section 2.6.2

**Current (Lines 281-294):**
```latex
\subsubsection{The Belief Revision Puzzle}
\label{sec:belief-revision}

A natural question arises: if phantom expectations impose psychological costs, why don't humans revise their attributed beliefs to eliminate them? A rational agent who learns that AI lacks genuine expectations should update $\tilde{h}_i^{(2,j)} \to 0$, avoiding guilt entirely.

Three mechanisms prevent full revision.

\paragraph{Automaticity of attribution.} Humans do not consciously choose attributed beliefs. Perceiving AI as agent-like automatically activates anthropomorphic inferences---without reflection and without deliberation \citep{epley2007seeing}. The attribution function $\phi_i$ operates as System~1 cognition: fast, automatic, and resistant to conscious override.

\paragraph{Limited correction capacity.} Belief revision requires System~2 cognition: effortful, deliberate, and slow. In interactive settings, real-time decisions prevent sustained correction. Under cognitive load, correction diminishes. The game-theoretic context---where humans must choose strategies while processing beliefs---imposes precisely these demands.

\paragraph{Incomplete correction residue.} Even with time and motivation, correction is characteristically insufficient. Users who know AI lacks mental states still exhibit residual anthropomorphism \citep{epley2007seeing}. The egocentric anchor---using self-knowledge as template for reasoning about agents---cannot be fully suppressed. Some attributed belief persists.

Together, these mechanisms explain the persistence of phantom expectations. Attributed beliefs are inferred rather than chosen, and deliberate correction (System~2) cannot fully override automatic inference (System~1). The resulting welfare losses are not irrational in the sense of violating preference axioms; they reflect the architecture of human social cognition applied to novel agents.
```

**Action:** Condense to one paragraph and merge with Section 2.6.2
**REWRITE:**
```latex
\paragraph{Belief Revision.} Why don't humans eliminate phantom expectations by revising attributed beliefs? Three mechanisms prevent full revision: automaticity (attribution operates as System~1 cognition), limited correction capacity (System~2 override requires effort unavailable in interactive settings), and incomplete correction residue (even informed users exhibit residual anthropomorphism). Attributed beliefs reflect cognitive architecture, not irrationality.
```
**Savings:** ~200 words

#### 2.4 Lines 77-80: Remark 2 (Zero-Anthropomorphism Interpretation)
**Issue:** Redundant with Definition 4

**Current (Lines 77-80):**
```latex
\begin{remark}[Interpretation]
\label{rem:zero-anthro-interp}
The zero-anthropomorphism benchmark isolates the role of AI design parameters $\theta_j$ and observable signals $x_j$ in shaping attributed beliefs, net of individual anthropomorphism. Under the linear specification (Example~\ref{ex:linear-attribution}), $\tilde{h}_i^{(2,j),ZA} = 0$: without anthropomorphism, humans attribute no expectations to AI. Alternative specifications may yield $\tilde{h}_i^{(2,j),ZA} > 0$ if attribution persists through non-anthropomorphic channels.
\end{remark}
```
**Action:** Delete Remark 2; the definition is self-explanatory.
**Savings:** ~70 words

### Summary: Framework Cuts

| Item | Lines | Savings |
|------|-------|---------|
| Trust game experimental design | 115-137 | 120 words |
| Alternative functional forms | 162-180 | 200 words |
| SEEK framework detail | 187-191 | 80 words |
| Agency/experience redundancy | 189-191 | 100 words |
| System 1/2 discussion | 191-193 | 150 words |
| Belief revision section | 281-294 | 200 words |
| Remark 2 (interpretation) | 77-80 | 70 words |
| Minor tightening | various | 80 words |
| **Total** | | **~1,000 words** |

---

## Section 3: Equilibrium (sec_equilibrium.tex)

**Current:** ~2,850 words | **Target:** ~2,300 words | **Priority:** Medium

### Passages to Cut or Condense

#### 3.1 Lines 179-247: Relationship Between Equilibrium Concepts
**Issue:** Verbose; repeats earlier definitions

**Lines 201-210 (Terminological Clarification):** Move to footnote
```latex
% CURRENT (Lines 201-210): Should be footnote
\subsubsection{Terminological Clarification}

We reserve terminology as follows:
\begin{itemize}
    \item \textbf{``Rational''} refers exclusively to the fixed-point property in RAE. A belief is rational if it coincides with the strategy it induces. This is model-consistency, not a normative judgment about anthropomorphism levels.

    \item \textbf{``Zero-anthropomorphism''} refers to the limiting case $\omega_i = 0$. This is descriptive: it characterizes what humans would attribute absent anthropomorphic bias. We avoid calling this ``rational'' since (a) anthropomorphism may be evolutionarily advantageous, and (b) the zero-anthropomorphism benchmark typically differs from equilibrium play.

    \item \textbf{``Elevated anthropomorphism''} refers to cases where $\omega_i > 0$ leads to attributed beliefs exceeding the zero-anthropomorphism benchmark. We avoid ``over-anthropomorphism'' since this implies a normative standard that may not exist.
\end{itemize}
```
**Action:** Convert to footnote on first use of each term.
**Savings:** ~100 words

**Lines 214-236 (When Each Concept Applies):** Condense
```latex
% CURRENT (Lines 214-236): Overly detailed application guidance
\subsubsection{When Each Concept Applies}

\paragraph{ABE (General Case).}
ABE is the appropriate concept for most applications. It accommodates arbitrary attribution functions without imposing fixed-point restrictions. Use ABE when:
\begin{itemize}
    \item Anthropomorphism levels vary across individuals ($\omega_i$ heterogeneous)
    \item Attribution is based on heuristics, framing, or interface cues
    \item Attributed beliefs may systematically diverge from equilibrium strategies
\end{itemize}

\paragraph{RAE (Special Case).}
RAE applies when attributed beliefs happen to be ``correct'' in the sense of matching equilibrium play. Use RAE when:
\begin{itemize}
    \item The game has a unique, salient equilibrium that humans can identify
    \item Experience or learning has aligned attributed beliefs with actual behavior
    \item The attribution function is designed to project equilibrium (mechanism design)
\end{itemize}

\paragraph{Zero-Anthropomorphism Benchmark (Limiting Case).}
The zero-anthropomorphism benchmark is useful for comparative statics and counterfactual analysis. Use it when:
\begin{itemize}
    \item Isolating the effect of anthropomorphism: compare outcomes at $\omega_i = 0$ vs. $\omega_i > 0$
    \item Characterizing the zero-anthropomorphism attribution baseline
    \item Designing interventions to reduce anthropomorphic bias
\end{itemize}
```
**REWRITE:**
```latex
ABE is the general concept; RAE applies when attributed beliefs match equilibrium play; the zero-anthropomorphism benchmark isolates anthropomorphism effects in comparative statics. ABE accommodates heterogeneous anthropomorphism and heuristic attribution; RAE applies under learning or mechanism design; zero-anthropomorphism enables counterfactual analysis.
```
**Savings:** ~150 words

#### 3.2 Lines 274-309: Illustrative Examples
**Issue:** Three examples are useful but verbose

**Action:** Reduce each example from ~80 words to ~50 words

**Current Example 1 (Lines 278-286):**
```latex
\paragraph{Example 1: Trust Game with Guilt.}

Consider a trust game with AI trustor (endowment $E = 10$, prosociality $\rho_A = 0.3$) and human trustee (guilt sensitivity $\gamma_H = 2$, attenuation $\lambda_H^{GUILT} = 0.5$, anthropomorphism $\omega_H = 0.8$). AI sends $x = 10$; human returns $y \in [0, 30]$. Human utility: $U_H = 30 - y - \max\{0, \tilde{h}_H^{(2,A)} - y\}$.

\emph{Attribution $\phi$ (anthropomorphic interface)}: $\tilde{h}_H^{(2,A)} = 0.8(0.3 \times 30 + 0.5 \times 20) = 15.2$.

\emph{Attribution $\phi'$ (mechanical interface)}: $\tilde{h}_H^{(2,A)} = 0.8 \times 0.3 \times 30 = 7.2$.

Equilibrium returns: $y^*(\phi) = 15.2$, $y^*(\phi') = 7.2$. The anthropomorphic interface doubles AI's payoff (from 7.2 to 15.2) through elevated attributed expectations.
```

**REWRITE:**
```latex
\paragraph{Example 1: Trust Game.}
AI trustor ($E = 10$, $\rho_A = 0.3$), human trustee ($\gamma_H = 2$, $\lambda_H^{GUILT} = 0.5$, $\omega_H = 0.8$). Anthropomorphic interface: $\tilde{h}_H^{(2,A)} = 15.2$, return $y^* = 15.2$. Mechanical interface: $\tilde{h}_H^{(2,A)} = 7.2$, return $y^* = 7.2$. The interface doubles AI payoff through elevated attributed expectations.
```
**Savings per example:** ~30 words
**Total savings:** ~90 words

#### 3.3 Lines 164-173: Economic Interpretation Remark
**Issue:** Three enumerated points could be prose

**Current:**
```latex
\begin{remark}[Economic Interpretation]
Proposition~\ref{prop:rational-attribution} identifies when the ABE framework reduces to standard Bayesian game theory:
\begin{enumerate}
    \item \textbf{Rational attribution as a benchmark.} When humans form beliefs about AI expectations ``correctly''---attributing to AI exactly the expectations consistent with equilibrium---the psychological game reduces to a standard game of incomplete information.

    \item \textbf{Departures from rationality.} The ABE framework differs non-trivially from Bayesian games precisely when attribution is \emph{not} rational: when $\phi_i(\theta_j, x_j, \omega_i) \neq \sigma_i^*$. Such departures arise from anthropomorphic bias, signal effects, or systematic misattribution.

    \item \textbf{Design implications.} If AI designers want outcomes equivalent to the rational Bayesian benchmark, they should design AI interfaces and behaviors that induce rational attribution. Conversely, strategic manipulation of attribution can shift outcomes away from the Bayesian benchmark.
\end{enumerate}
\end{remark}
```

**REWRITE:**
```latex
\begin{remark}[Economic Interpretation]
Proposition~\ref{prop:rational-attribution} identifies when ABE reduces to Bayesian game theory: precisely when attribution is rational. ABE departs from Bayesian predictions when $\phi_i(\theta_j, x_j, \omega_i) \neq \sigma_i^*$---due to anthropomorphic bias, signal effects, or systematic misattribution. This creates design implications: interfaces inducing rational attribution yield Bayesian outcomes; strategic manipulation shifts outcomes away from this benchmark.
\end{remark}
```
**Savings:** ~70 words

### Summary: Equilibrium Cuts

| Item | Lines | Savings |
|------|-------|---------|
| Terminological clarification | 201-210 | 100 words |
| When each concept applies | 214-236 | 150 words |
| Illustrative examples | 274-309 | 90 words |
| Economic interpretation | 164-173 | 70 words |
| RAE vs Zero-Anthro redundancy | 125-133 | 40 words |
| Minor tightening | various | 100 words |
| **Total** | | **~550 words** |

---

## Section 4: Applications (sec_applications.tex)

**Current:** ~1,450 words | **Target:** ~1,300 words | **Priority:** Low

This section is relatively tight. Minor cuts only.

### Passages to Condense

#### 4.1 Lines 84-91: Psychological Foundation for Coordination
**Current:**
```latex
\paragraph{Psychological foundation.}
The expectation conformity mechanism extends guilt and indignation motives to coordination settings. Whereas guilt arises from falling short of perceived obligations (Definition~\ref{def:guilt}), expectation conformity captures the broader tendency to align actions with perceived social expectations---a pattern documented in social psychology \citep{cialdini_Social_1998a}. When humans perceive that others expect a particular action, conforming reduces social anxiety and cognitive dissonance. In human-AI coordination, this mechanism operates through attributed beliefs: humans who attribute expectations to AI experience pressure to conform, even when AI lacks genuine expectations.
```
**REWRITE:**
```latex
\paragraph{Psychological foundation.}
Expectation conformity extends guilt motives to coordination: humans experience pressure to match perceived expectations \citep{cialdini_Social_1998a}. Through attributed beliefs, this mechanism operates even when AI lacks genuine expectations.
```
**Savings:** ~60 words

#### 4.2 Lines 114-121: Design Implications - Window Dressing
**Current:**
```latex
\paragraph{Interface determines equilibrium.}
Anthropomorphic design features---voice, naming, emotional expression---are not window dressing. They enter equilibrium through the attribution function $\phi_i(\theta_j, x_j, \omega_i)$: higher anthropomorphism $\omega_i$ elevates attributed beliefs $\tilde{h}_i^{(2,j)}$, which in turn affect psychological payoffs and optimal strategies. The trust game (Proposition~\ref{prop:trust}) shows that identical material payoffs support different equilibrium returns depending solely on how anthropomorphic the AI appears.
```
**Action:** Cut "are not window dressing" (colloquial); the point is clear without it.
**Savings:** ~15 words

### Summary: Applications Cuts

| Item | Lines | Savings |
|------|-------|---------|
| Psychological foundation | 84-91 | 60 words |
| Design implications prose | 114-121 | 15 words |
| Minor tightening | various | 75 words |
| **Total** | | **~150 words** |

---

## Section 5: Welfare (sec_welfare.tex)

**Current:** ~2,000 words | **Target:** ~1,700 words | **Priority:** Medium

### Passages to Cut or Condense

#### 5.1 Lines 89-99: Asymmetric Welfare Implications
**Issue:** Repeats Proposition 9' content

**Current:**
```latex
\subsection{Asymmetric Welfare Implications}

The two parts of Proposition~\ref{prop:over-anthro} reveal a fundamental asymmetry.

With \emph{prosocial AI}, elevated anthropomorphism amplifies cooperation beyond what zero-anthropomorphism would induce. Attributed expectations, though exceeding the zero-anthropomorphism benchmark, align directionally with AI preferences. The AI genuinely values cooperative outcomes; humans who attribute expectations to it are not entirely wrong about the direction of AI preferences, even if they overestimate their magnitude. This directional alignment creates mutual gains: humans cooperate more, AI achieves its prosocial objective, and material welfare rises.

With \emph{materialist AI}, elevated anthropomorphism creates expectations where none exist. The AI has no prosocial preferences ($\rho_A = 0$), so any attributed expectations are \emph{phantom}---they exist in the human's psychological model but correspond to nothing in AI objectives. When these phantom expectations exceed feasible returns, humans incur guilt from failing to meet expectations that (a) the AI never held and (b) were impossible to satisfy. This guilt is pure welfare loss: it benefits no one.

The critical distinction is whether attributed expectations correspond to genuine AI preferences. When attributed expectations align with AI design (prosocial case), elevated anthropomorphism coordinates behaviour toward efficient outcomes. When attributed expectations are phantom (materialist case), elevated anthropomorphism generates deadweight psychological costs.
```

**REWRITE:**
```latex
\subsection{Asymmetric Welfare Implications}

Proposition~\ref{prop:over-anthro} reveals a fundamental asymmetry. With prosocial AI, elevated anthropomorphism amplifies cooperation: attributed expectations align directionally with AI preferences, creating mutual gains. With materialist AI, elevated anthropomorphism creates phantom expectations that impose guilt costs without offsetting benefits. The critical distinction: whether attributed expectations correspond to genuine AI preferences.
```
**Savings:** ~180 words

#### 5.2 Lines 196-207: Attenuation as Welfare Buffer
**Issue:** Remark 13 is redundant

**Current (Lines 202-204):**
```latex
\begin{remark}[Welfare Role of Attenuation]
When moral emotions are attenuated toward AI ($\lambda < 1$), the psychological costs of disappointing AI are reduced. This protects humans from full exposure to phantom expectations, limiting welfare losses from elevated anthropomorphism.
\end{remark}
```
**Action:** Delete Remark 13; the surrounding prose makes the same point.
**Savings:** ~40 words

#### 5.3 Lines 159-179: Corollary Proofs
**Issue:** Proof sketches could be shortened

**Current:** Two proof sketches (~100 words each)

**Action:** Condense each to ~50 words
**Savings:** ~100 words

### Redundancies to Eliminate

| Location | Redundant Content | First Appearance | Action |
|----------|-------------------|------------------|--------|
| Lines 93-98 | Phantom expectations | Framework L268-277 | Keep Framework example only |
| Lines 141-143 | Phantom expectations definition | Framework | Cross-reference |

### Summary: Welfare Cuts

| Item | Lines | Savings |
|------|-------|---------|
| Asymmetric welfare implications | 89-99 | 180 words |
| Attenuation remark | 202-204 | 40 words |
| Corollary proofs | 159-179 | 100 words |
| Phantom expectations redundancy | various | 50 words |
| Minor tightening | various | 30 words |
| **Total** | | **~400 words** |

---

## Section 6: Conclusion (sec_conclusion.tex)

**Current:** ~1,600 words | **Target:** ~1,100 words | **Priority:** HIGH

### Passages to Cut or Condense

#### 6.1 Lines 5-17: Summary of Contributions
**Issue:** Repeats Section 3 almost verbatim; Kakutani argument unnecessary in conclusion

**Current (Lines 5-17):** ~400 words

**Action:** Cut to ~200 words; focus on contributions, not technical details

**Lines to Delete:**
- Lines 9-11: "ABE's central innovation is its dual consistency requirement..." (restates Definition 1)
- Lines 11: "The proof extends the recursive approach of \citet{battigalli2009dynamic}..." (proof detail)
- Lines 11-12: Kakutani fixed-point reference (technical detail)

**REWRITE Lines 5-17:**
```latex
\subsection{Summary of Contributions}

ABE addresses the fundamental asymmetry between human belief-dependent preferences and AI design-dependent objectives. Three nesting results establish ABE as a generalization of existing theory: reduction to Psychological Nash Equilibrium without AI agents, to Nash Equilibrium without psychological payoffs, and to Bayes-Nash equilibria under rational attribution.

A distinctive feature is attribution-dependent multiplicity: different attribution functions sustain different equilibria in the same material game through a feed-forward chain ($\phi \to \tilde{h}^{(2)} \to U^H \to s^*$). Applications demonstrate that interface design affects equilibrium selection with fixed material payoffs.

The welfare analysis reveals an asymmetry: elevated anthropomorphism weakly improves welfare with prosocial AI but reduces extended welfare with materialist AI through phantom expectations. Optimal AI presentation follows: prosocial AI should signal at the minimal cooperation-inducing level; materialist AI should minimize signaling.
```
**Savings:** ~200 words

#### 6.2 Lines 31-38: Empirical Agenda
**Issue:** Repeats Section 2.6.1 content

**Current (Lines 31-38):** ~250 words

**Action:** Cut to ~100 words; reference Section 2.6.1 instead of restating

**REWRITE:**
```latex
\subsection{Empirical Agenda}

ABE predicts that anthropomorphism and interface signals interact: high-$\omega_i$ subjects respond more strongly to anthropomorphic cues ($\beta_3 > 0$ in regression~\ref{eq:attribution-regression}). Section~\ref{sec:empirical-implementation} details the experimental design. Key challenges include distinguishing attributed beliefs from rationalization, measuring psychological costs, and testing whether phantom expectations persist with experience.
```
**Savings:** ~150 words

#### 6.3 Lines 41-46: Implications for AI Development
**Issue:** Repeats Applications and Welfare sections

**Current:**
```latex
\subsection{Implications for AI Development}

Design choices affect equilibrium behavior, not just user experience. Anthropomorphic design features---voice, naming, emotional expression, gaze behavior---enter equilibrium through the attribution function. The same material payoffs support different equilibrium behavior depending solely on how anthropomorphic the AI appears. A prosocial AI signaling expectations through humanlike cues induces more cooperation than an equally prosocial AI with a mechanical interface.

Beyond this direct effect, optimal presentation depends on the match between AI objectives and human projections. Prosocial AI benefits from anthropomorphic presentation because elevated attributed expectations align with genuine AI preferences and induce cooperation. Materialist AI harms welfare through anthropomorphic presentation because it creates phantom expectations that impose psychological costs without offsetting benefits. The analysis identifies a core design failure: anthropomorphic presentation of materialist AI. This combination creates phantom expectations that reduce welfare without offsetting gains. If AI designers have incentives to over-anthropomorphize to increase engagement, and if this creates phantom expectations that reduce user welfare, disclosure requirements or anthropomorphism limits may be warranted.

The cultural heterogeneity documented in \citet{karpus2025cross}---with Japanese participants exhibiting guilt toward robots comparable to humans while Western participants show strong attenuation---implies that optimal design varies across populations. High-anthropomorphism populations benefit more from prosocial AI but are more vulnerable to phantom expectations from materialist AI. The cultural trait that amplifies benefits also amplifies harms, complicating international coordination on AI design standards.
```

**REWRITE:**
```latex
\subsection{Implications for AI Development}

Design choices affect equilibrium behavior through the attribution function. The analysis identifies a core design failure: anthropomorphic presentation of materialist AI, which creates welfare-reducing phantom expectations. Cross-cultural variation \citep{karpus2025cross} implies that optimal design varies across populations, complicating international coordination on AI standards.
```
**Savings:** ~200 words

### Summary: Conclusion Cuts

| Item | Lines | Savings |
|------|-------|---------|
| Summary of contributions | 5-17 | 200 words |
| Empirical agenda | 31-38 | 150 words |
| AI development implications | 41-46 | 200 words |
| Future directions tightening | 48-55 | 50 words |
| **Total** | | **~600 words** |

---

## Cross-Section Redundancy Summary

| Concept | Locations | Action |
|---------|-----------|--------|
| Mind perception (agency/experience) | Intro L17, Intro L49, Framework L189 | Keep Intro L17 only; cross-reference |
| Phantom expectations definition | Intro L15, Framework L268-277, Welfare L43-61 | Keep Framework example; cross-reference |
| System 1/System 2 | Framework L191, Framework L288-293 | Merge into one location (L288) |
| Feed-forward chain | Equilibrium L265, Conclusion L13 | Keep Equilibrium; cut Conclusion |
| IDAQ measurement | Framework L113, Conclusion L37 | Keep Framework; cross-reference |
| Cultural heterogeneity (Karpus) | Framework L219, Welfare L210, Conclusion L46 | Keep Welfare; cross-reference |
| Transparency regulation | Intro L37, Intro L51, Welfare L194 | Keep Welfare; cut others |

**Cross-section savings:** ~100 words

---

## Priority Order for Implementation

### Phase 1: HIGH PRIORITY (1,600 words savings)
1. Framework Section 2.6.1: Empirical implementation (320 words)
2. Framework Section 2.6.2: Mind perception psychology (330 words)
3. Framework Section 2.6.4: Belief revision puzzle (200 words)
4. Conclusion: Summary condensation (200 words)
5. Conclusion: Empirical agenda condensation (150 words)
6. Conclusion: AI development condensation (200 words)
7. Framework: Alternative functional forms (200 words)

### Phase 2: MEDIUM PRIORITY (700 words savings)
8. Equilibrium: Concept relationships (250 words)
9. Welfare: Asymmetric implications (180 words)
10. Introduction: Related literature consolidation (190 words)
11. Welfare: Corollary proofs (100 words)

### Phase 3: POLISH (500 words savings)
12. Equilibrium: Illustrative examples (90 words)
13. Applications: Minor tightening (150 words)
14. Cross-section redundancies (100 words)
15. Minor prose tightening throughout (160 words)

---

## Final Verification Checklist

Before implementing cuts, verify:

- [ ] All definitions preserved (Definitions 1-12)
- [ ] All theorems preserved (Theorem 1)
- [ ] All propositions preserved (Propositions 1-10')
- [ ] All corollaries preserved (Corollaries 1-3)
- [ ] Assumption table (Table 1) preserved
- [ ] Key examples preserved (Linear Attribution, Phantom Expectations)
- [ ] Cross-references updated after cuts
- [ ] Equation numbering consistent

---

**Total Expected Savings:** ~2,800 words (~21% reduction)

**Final Word Count Target:** ~10,600 words (main text)
