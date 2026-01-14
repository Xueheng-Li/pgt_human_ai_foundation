# Attributed Belief Equilibrium in Human-AI Games

**Target journals**: Econometrica, Journal of Economic Theory

---

## Notation and Mathematical Preliminaries

### Player Sets and Types
- $N_H = \{1, \ldots, n_H\}$: set of human players
- $N_A = \{1, \ldots, n_A\}$: set of AI agents
- $T_i$ for $i \in N_H$: human type spaces (psychological parameters)
- $T_j$ for $j \in N_A$: AI design parameter spaces

### Belief Hierarchies
- $\mathcal{H}_i^0 = T_i$: type space
- $\mathcal{H}_i^1 = \Delta(\times_{k \neq i} T_k \times S_{-i})$: first-order beliefs
- $\mathcal{H}_i^n = \Delta(\times_{k \neq i} \mathcal{H}_k^{n-1})$: $n$-th order beliefs
- $\mathcal{H}_i = \prod_{n=0}^\infty \mathcal{H}_i^n$: full belief hierarchy
- $h_i = (h_i^{(0)}, h_i^{(1)}, h_i^{(2)}, \ldots) \in \mathcal{H}_i$: belief system

### Strategies and Utilities
- $S_i$: finite strategy set for player $i$
- $\pi_i(s)$: material payoff function
- $\psi_i(s, h_i^{(2)}, \tilde{h}_i^{(2)})$: psychological payoff function
- $U_i^H(s, h_i, \tilde{h}_i) = \pi_i(s) + \psi_i(s, h_i^{(2)}, \tilde{h}_i^{(2)})$: extended human utility
- $U_j^A(s; \theta_j)$: AI utility (design-dependent)

### Attribution Functions
- $\phi_i: \Theta_j \times X \times \Omega_i \to \Delta(\Delta(S_j))$: attribution function
- $\tilde{h}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$: attributed beliefs about AI $j$
- $\theta_j \in \Theta_j$: AI design parameters
- $x_j \in X$: observable signals
- $\omega_i \in \Omega_i$: individual heterogeneity (anthropomorphism tendency)

---

## Motivation

As artificial intelligence becomes ubiquitous in economic interactions—from algorithmic trading and automated negotiations to collaborative work platforms—we confront a fundamental theoretical gap in game theory. Traditional equilibrium concepts assume symmetric belief structures among players, yet human-AI interactions are inherently asymmetric along multiple dimensions.

**The Core Asymmetry**: Human players possess genuine belief hierarchies and exhibit belief-dependent preferences (guilt, indignation, reciprocity, reciprocity). AI agents, conversely, have design-dependent objectives but lack genuine beliefs or emotions. This creates what we term *psychological asymmetry*: humans experience psychological payoffs based on their beliefs about others' beliefs, while AI experience payoffs based solely on programmed objectives and observed outcomes.

**The Attribution Phenomenon**: Despite AI lacking mental states, extensive evidence from human-computer interaction shows that humans systematically *attribute* beliefs, intentions, and expectations to AI systems. When a human interacts with an AI trading agent, they may feel guilt from "disappointing" it or indignation from violating its perceived "expectations"—even though these mental states are psychological projections rather than genuine AI experiences.

**Research Question**: What equilibrium concepts appropriately model games where some players have belief-dependent preferences while others have design-dependent objectives? How do humans' attributed beliefs about AI expectations affect outcomes, and what are the implications for AI design?

This question is not merely theoretical. As AI systems become more prevalent in collaborative, trust-dependent domains—healthcare, finance, education—we must understand how psychological mechanisms traditionally studied in purely human contexts extend to human-AI settings.

---

## Psychological Game Theory Background

### Psychological Games

Following Geanakoplos, Pearce, and Stacchetti (1989), a **psychological game** extends traditional game theory by allowing players' utilities to depend on their beliefs about others' beliefs, not just on observed actions. Formally:

\begin{definition}[Psychological Game]
A psychological game is defined by:
\begin{enumerate}
\item A Bayesian game $(N, \{T_i\}, \{S_i\}, \{u_i\}, p)$ with type space $T_i$
\item Belief hierarchies $\{h_i^{(n)}\}_{n=1}^\infty$ for each player $i$
\item Extended utility functions $U_i: S \times \prod_{n=1}^\infty \mathcal{H}_i^n \to \mathbb{R}$
\end{enumerate}
such that $U_i(s, h_i) = u_i(s, t_i) + \psi_i(s, h_i^{(2)}, h_i^{(3)}, \ldots)$, where $\psi_i$ captures belief-dependent payoffs (psychological payoffs).
\end{definition}

The decomposition into material payoffs $\pi_i(s)$ and psychological payoffs $\psi_i$ is fundamental. While material payoffs depend only on strategy profiles, psychological payoffs depend on players' belief hierarchies.

### Belief Hierarchies and Consistency

The belief hierarchy $\mathcal{H}_i$ for player $i$ is constructed recursively following the universal belief space approach of Mertens and Zamir (1985). Each player's beliefs about others' types, strategies, and beliefs must satisfy Bayesian consistency:

\begin{assumption}[Belief Consistency]
The belief hierarchy $h_i = (h_i^{(1)}, h_i^{(2)}, \ldots) \in \mathcal{H}_i$ satisfies:
\begin{enumerate}
\item $h_i^{(n)} \in \Delta(\mathcal{H}_{-i}^{n-1})$ for all $n \geq 1$ (beliefs are probability measures)
\item $h_i^{(n)} = \mu_{\mathcal{H}_{-i}^{n-1}}(h_i^{(n+1)})$ where $\mu$ denotes marginalization
\end{enumerate}
\end{assumption}

The second condition ensures that lower-order beliefs are consistent with higher-order beliefs via Bayesian updating. This recursive structure captures the infinite regress inherent in beliefs about beliefs.

### Belief-Dependent Preferences

The psychological payoff function $\psi_i$ captures how beliefs affect utilities. Battigalli and Dufwenberg (2009) identify several canonical mechanisms:

**Indignation** (GPS 1989): Players experience disutility from disappointing others' expectations:
$$\psi_i^{IND}(s_i, s_{-i}, h_i^{(2)}) = -\beta \cdot \mathbf{1}_{s_i = D} \cdot h_i^{(2)}(C)$$
where $\beta > 0$ is the indignation sensitivity parameter, and $h_i^{(2)}(C)$ is the probability that $i$ believes others expected cooperation.

**Guilt Aversion** (BD 2009): Players experience disutility from falling short of their own perceived obligations:
$$\psi_i^{GUILT}(s_i, s_{-i}, h_i^{(2)}) = -\gamma \cdot \mathbf{1}_{s_i = D} \cdot h_i^{(2)}(C)$$
where $\gamma > 0$ is the guilt sensitivity parameter.

These mechanisms create interdependencies: a player's payoff depends on others' beliefs about the player's beliefs, creating higher-order strategic considerations beyond standard game theory.

### Sequential Psychological Equilibrium

Battigalli and Dufwenberg (2009) develop **Sequential Psychological Equilibrium (SPE)** for dynamic psychological games. SPE requires:
\begin{enumerate}
\item Sequential rationality given beliefs
\item Belief consistency (Bayesian updating)
\item Psychological sequential rationality (psychological payoffs incorporated correctly)
\end{enumerate}

This equilibrium concept appropriately handles the forward-looking nature of belief-dependent preferences—players anticipate how their actions will affect others' beliefs and the resulting psychological payoffs.

---

## Asymmetric Human-AI Games

### Framework Definition

We define an asymmetric psychological game with human-AI interaction as follows:

\begin{definition}[Asymmetric Human-AI Psychological Game]
An asymmetric psychological game is a tuple
$$\Gamma = (N_H, N_A, \{T_i\}_{i \in N_H}, \{T_j\}_{j \in N_A}, \{S_i\}_{i \in N_H \cup N_A}, \{U_i\}_{i \in N_H}, \{U_j\}_{j \in N_A}, \phi, p)$$

Where:
\begin{enumerate}
\item $N_H$ and $N_A$ are finite sets of humans and AI agents
\item $T_i$ for $i \in N_H$ are human type spaces (psychological parameters: $\beta, \gamma, \omega_i$)
\item $T_j$ for $j \in N_A$ are AI design parameter spaces ($\theta_j$, prosociality level)
\item $S_i$ are finite strategy sets
\item Human utility functions decompose as:
   $$U_i^H(s, h_i, \tilde{h}_i) = \pi_i(s) + \psi_i^H(s, h_i^{(2)}, \tilde{h}_i^{(2)})$$
   where $\psi_i^H$ captures indignation and guilt toward both humans and AI
\item AI utility functions: $U_j^A(s; \theta_j) = f_j(s; \theta_j)$ (no belief dependence)
\item Attribution function $\phi: \prod_{j \in N_A} (\Theta_j \times X \times \Omega_i) \to \prod_{j \in N_A} \Delta(\Delta(S_j))$
   maps AI design parameters to humans' attributed beliefs
\item $p \in \Delta(\times_{i \in N_H} T_i \times \times_{j \in N_A} T_j)$ is the common prior
\end{enumerate}
\end{definition}

The key innovation is the attribution function $\phi$, which bridges the asymmetry between humans' genuine belief-dependent preferences and AI's design-dependent objectives.

### Attributed Beliefs

When human $i$ interacts with AI $j$, the human forms attributed second-order beliefs:

\begin{definition}[Attributed Beliefs]
For human $i \in N_H$ and AI $j \in N_A$, the attributed belief about AI $j$'s expectations is:
$$\tilde{h}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$$

where:
- $\theta_j \in \Theta_j$: AI's design parameters (prosociality, conditionality)
- $x_j \in X$: observable signals (interface design, behavioral cues, communication framing)
- $\omega_i \in \Omega_i$: individual heterogeneity (anthropomorphism tendency)
- $\tilde{h}_i^{(2,j)} \in \Delta(S_j)$: the human's belief about what the AI expected

The attribution function $\phi_i$ captures the psychological mechanism by which humans project mental states onto AI systems.
\end{definition}

\textbf{Domain and Codomain}: $\phi_i: \Theta_j \times X \times \Omega_i \to \Delta(\Delta(S_j))$. The output is a belief about a belief: the human's belief about the AI's belief about the human's action.

\textbf{Specification Options}: The attribution function can be modeled through several approaches:
\begin{enumerate}
\item \textbf{Behavioral attribution}: $\phi_i$ inferred from AI's observable actions (e.g., past cooperation patterns)
\item \textbf{Signal-based attribution}: $\phi_i$ derived from interface design and framing (anthropomorphic language, emotional expressions)
\item \textbf{Dispositional attribution}: $\phi_i$ based on the human's anthropomorphism tendency $\omega_i$
\end{enumerate}

These specifications differ in their implications for equilibrium outcomes and AI design optimization.

### Attributed Belief Equilibrium

We now define our core equilibrium concept:

\begin{definition}[Attributed Belief Equilibrium (ABE)]
A strategy profile $(s^*, \tau^*)$, belief system $h^*$, and attributed beliefs $\tilde{h}^*$ constitute an ABE if:

\begin{enumerate}
\item \textbf{Sequential Rationality (Humans)}: For all $i \in N_H$ and all $h_i \in \mathcal{H}_i$,
   $$s_i^* \in BR_i^H(h_i, \tilde{h}_i^*) = \arg\max_{s_i \in S_i} EU_i^H(s_i, s_{-i}^*, \tau^*; h_i, \tilde{h}_i^*)$$

\item \textbf{Design Optimality (AI)}: For all $j \in N_A$ and all $\theta_j \in \Theta_j$,
   $$\tau_j^*(\theta_j) \in BR_j^A(\theta_j, s^*) = \arg\max_{\tau_j} EU_j^A(\tau_j, s^*; \theta_j)$$

\item \textbf{Genuine Belief Consistency}: For all $i \in N_H$, the belief hierarchy $h_i^*$ satisfies Bayesian consistency

\item \textbf{Attribution Consistency}: For all $i \in N_H$ and $j \in N_A$,
   $$\tilde{h}_i^{*(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$$
\end{enumerate}
\end{definition}

\textbf{Key Innovation}: Unlike traditional equilibrium concepts where beliefs must be "correct" in some sense, attributed beliefs in ABE are governed by the attribution function $\phi$. They need not satisfy consistency with actual AI "mental states" (which don't exist) but rather with humans' psychological projections of those states.

This distinction is crucial: ABE accommodates the psychological reality that humans treat AI as if they have beliefs and expectations, even when those mental states are projected rather than genuine.

---

## Methodology

\subsection{Theoretical Approach}

Our theoretical analysis proceeds through four interconnected steps:

\begin{enumerate}
\item \textbf{Formal Extension of PGT}: We extend Battigalli and Dufwenberg (2009) to accommodate asymmetric player types, where only humans maintain genuine belief hierarchies while all players (humans and AI) maintain attributed beliefs about AI.

\item \textbf{Existence Analysis}: We prove existence of ABE using fixed-point arguments, extending the machinery of psychological game theory to our asymmetric setting. The key challenge is handling two distinct belief structures simultaneously.

\item \textbf{Characterization}: We analyze equilibria in canonical games—trust games, public goods games, and coordination games—to understand how attribution patterns affect outcomes.

\item \textbf{Welfare Analysis}: We examine how different attribution regimes (different $\phi$ functions) affect aggregate welfare and social optimality.
\end{enumerate}

\subsection{Key Technical Challenges}

\begin{enumerate}
\item \textbf{Attribution Specification}: The functional form of $\phi$ is theoretically unspecified. We must determine what assumptions on $\phi$ are necessary for equilibrium existence and what empirical evidence suggests about its shape.

\item \textbf{Equilibrium Multiplicity}: Different attribution functions can sustain different equilibria in the same game—the same human-AI interaction may result in cooperation or defection depending on how humans perceive AI expectations.

\item \textbf{Design Optimization}: Given $\phi$, what AI design parameters $(\theta, x)$ maximize welfare? This requires solving a bi-level optimization: humans optimize given $\phi$, AI designers optimize given human best responses.

\item \textbf{Type Heterogeneity}: Humans differ in psychological parameters ($\beta, \gamma, \omega_i$). How does this heterogeneity affect equilibrium selection and AI design?
\end{enumerate}

\subsection{Extensions and Variations}

Our framework accommodates several important extensions:
\begin{enumerate}
\item \textbf{Multiple AI Types}: When AI agents have different design parameters, how do humans attribute beliefs to heterogeneous AI populations?

\item \textbf{Learning Dynamics}: Do humans update their attribution functions $\phi_i$ over repeated interactions with the same or different AI?

\item \textbf{Design Interdependence}: How does AI design affect human attribution patterns, creating feedback loops between design and psychology?

\item \textbf{Dynamic Games}: Extending ABE to dynamic settings where attribution patterns evolve over time.
\end{enumerate}

---

## Related Literature

\subsection{Psychological Game Theory}

\begin{tabular}{|l|p{5cm}|p{4cm}|}
\hline
\textbf{Paper} & \textbf{Contribution} & \textbf{Extension to Human-AI} \\
\hline
Geanakoplos, Pearce \& Stacchetti (1989) & Introduced belief-dependent preferences & Add asymmetric belief structures \\
Battigalli \& Dufwenberg (2009) & Dynamic psychological games, SPE & All players have genuine beliefs vs. mixed genuine/attributed \\
Battigalli \& Dufwenberg (2016) & Partially specified psychological games & Partial specification extends to attribution functions \\
Mertens \& Zamir (1985) & Universal belief spaces & Extend to asymmetric belief types \\
Attanasi, Battigalli \& Manzoni (2016) & Incomplete information in psychological games & Type uncertainty vs. type asymmetry \\
\hline
\end{tabular}

\textbf{Canonical Examples}: Battigalli and Dufwenberg (2009) demonstrate belief-dependent preferences in several games:
\begin{itemize}
\item \textbf{Trust Game}: Guilt aversion induces positive returns to trustors
\item \textbf{Public Goods}: Indignation sustains higher contribution levels
\item \textbf{Ultimatum}: Second-mover rejections driven by perceived unfair expectations
\end{itemize}

These mechanisms provide the foundation for understanding how attributed beliefs about AI can generate similar psychological payoffs in human-AI contexts.

\subsection{Human-AI Interaction}

\begin{tabular}{|l|p{5cm}|p{4cm}|}
\hline
\textbf{Paper} & \textbf{Contribution} & \textbf{Game-Theoretic Gap} \\
\hline
Epley et al. (2007) & Anthropomorphism: humans attribute minds to non-humans & No equilibrium analysis \\
Rahwan et al. (2019) & Machine behavior: AI as social actors & No game-theoretic framework \\
Hancock et al. (2011) & Human-robot trust determinants & No belief-dependent preferences \\
Castelfranchi \& Falcone (2010) & Trust theory for artificial agents & Static trust, no dynamic beliefs \\
Złotowski et al. (2015) & Anthropomorphism in HRI & No formal equilibrium concept \\
\hline
\end{tabular}

This literature establishes that humans systematically attribute mental states to AI but lacks formal game-theoretic analysis. Our work fills this gap by providing equilibrium concepts that incorporate attributed beliefs.

\subsection{Evolutionary and Learning Dynamics}

\begin{tabular}{|l|p{5cm}|p{4cm}|}
\hline
\textbf{Paper} & \textbf{Connection to ABE} & \textbf{Extension} \\
\hline
Li (2026, GEB) & Indignation sustains cooperation in human games & Foundation for human psychological payoffs \\
Young (1993) & Stochastic stability in evolutionary games & P1 extends to heterogeneous mutation rates \\
Sandholm (2010) & Evolutionary game theory with complex populations & Add AI as separate evolutionary type \\
Li, Cui \& Zhang (2025, JME) & Spite in imitation dynamics & AI as reference point in spite payoffs \\
\hline
\end{tabular}

The evolutionary perspective is particularly relevant for understanding long-run outcomes in human-AI populations, where different player types may have different mutation rates and update rules.

---

## Main Contributions

Our work makes four primary contributions:

\begin{enumerate}
\item \textbf{Conceptual}: We introduce the first equilibrium concept explicitly designed for human-AI psychological asymmetry. This addresses a fundamental gap in game theory as AI becomes prevalent in economic interactions.

\item \textbf{Formal}: We prove existence of Attributed Belief Equilibrium under standard regularity conditions, extending the mathematical machinery of psychological game theory to asymmetric belief structures.

\item \textbf{Applied}: We characterize equilibria in canonical games (trust, public goods, coordination) and show how attribution patterns determine outcomes. This provides testable predictions for experiments.

\item \textbf{Design}: We analyze optimal AI design given human attribution patterns, providing guidance for practitioners on how to design AI systems that induce beneficial psychological responses.
\end{enumerate}

\textbf{Novelty}: The attributed belief concept is genuinely new to game theory. While psychology and HCI have documented anthropomorphism, we provide the first formal framework for incorporating these psychological projections into equilibrium analysis.

---

## Key Theoretical Results

\subsection{Existence}

\begin{theorem}[Existence of ABE]
\textbf{Conjecture}. Under assumptions of compact strategy spaces, continuous utility functions, and continuous attribution functions, an Attributed Belief Equilibrium exists.
\end{theorem}

\textbf{Intuition}: The existence proof extends Battigalli and Dufwenberg (2009) by constructing an extended game where humans' strategies are belief-contingent while AI strategies are design-contingent. Standard fixed-point arguments (Kakutani's theorem) apply given appropriate continuity conditions.

\textbf{Key Challenge}: Handling two distinct belief structures simultaneously—genuine beliefs about humans and attributed beliefs about AI.

\subsection{Equilibrium Multiplicity}

\begin{theorem}[Attribution-Dependent Equilibria]
\textbf{Conjecture}. Different attribution functions $\phi$ can sustain different equilibria in the same underlying game. The same human-AI interaction may result in cooperation or defection depending on how humans perceive AI expectations.
\end{theorem}

\textbf{Implications}: This multiplicity implies that AI design (through its effect on $\phi$) can fundamentally alter game outcomes, even when material payoffs are unchanged.

\subsection{Welfare}

\begin{theorem}[Attribution and Welfare]
\textbf{Conjecture}. Over-anthropomorphism (inflated attributed beliefs $\tilde{h}_i^{(2,j)}$) can improve welfare when AI is prosocially designed but reduce welfare when AI is materialistic. There exists an optimal attribution level given AI design.
\end{theorem}

\textbf{Design Implication}: Optimal AI design depends on human psychology—specifically, how humans attribute beliefs to AI systems.

---

## Applications

\subsection{Trust Game}

Consider a trust game where an AI trustor invests with a human trustee. The human experiences guilt from defection based on attributed beliefs about the AI's expectations.

\textbf{Setup}: AI trustor sends investment $x$; human trustee decides return $y$. The human's utility includes:
$$U^H = \pi(x, y) - \gamma \cdot \mathbf{1}_{y < \text{fair return}} \cdot \tilde{h}^{(2)}_{AI}(C)$$

where $\tilde{h}^{(2)}_{AI}(C)$ is the human's attributed belief that the AI expected cooperation.

\textbf{Prediction}: Higher anthropomorphism (stronger attributed beliefs) → higher guilt from defection → higher returns to AI → more investment by AI.

\textbf{Testability}: This prediction can be tested experimentally by varying AI interface design to manipulate $\phi$.

\subsection{Public Goods Game}

Consider a public goods game with mixed human-AI populations. Humans decide contributions; AI contribute based on design parameters.

\textbf{Question}: Does AI cooperation create normative pressure on humans through attributed beliefs about AI expectations?

\textbf{Prediction}: If humans include AI in their moral circle (attribute beliefs to AI), then AI cooperation creates indignation pressure toward human defection. However, this effect depends on anthropomorphism levels.

\textbf{Policy Implication}: AI design that signals prosociality may increase human cooperation even when AI have no genuine prosocial preferences.

\subsection{Coordination Game}

Consider a coordination game where AI choice may influence human coordination through attributed forward induction.

\textbf{Question}: If humans attribute intentions to AI choices, can AI "signal" equilibrium selection through its actions?

\textbf{Prediction}: AI design that encourages certain attributed beliefs may help coordinate on efficient equilibria even in games with multiple coordination failures.

---

## Open Questions and Future Directions

\subsection{Empirical Questions}

\begin{enumerate}
\item \textbf{Estimating $\phi$}: How can attribution functions be empirically estimated? What experimental manipulations best identify the psychological parameters of $\phi$?

\item \textbf{Learning Dynamics}: Do humans update their attribution functions $\phi_i$ over repeated interactions? How quickly do these psychological projections adapt to AI behavior?

\item \textbf{Individual Differences}: What psychological traits predict variation in $\omega_i$ (anthropomorphism tendency)? How do personality, experience with technology, and cultural factors affect attribution patterns?
\end{enumerate}

\subsection{Theoretical Extensions}

\begin{enumerate}
\item \textbf{Multiple AI Types}: When AI agents have heterogeneous design parameters, how do humans attribute beliefs to different AI simultaneously?

\item \textbf{Belief Upward Slopes}: What happens when humans attribute beliefs not just to AI's expectations but to AI's beliefs about humans' beliefs? (Higher-order attributed beliefs)

\item \textbf{Dynamic ABE}: How does ABE extend to dynamic games with learning and reputation formation?

\item \textbf{Bayesian Interpretation}: Can attributed beliefs be given a Bayesian interpretation? How does this relate to type uncertainty in Bayesian games?
\end{enumerate}

\subsection{Design and Policy}

\begin{enumerate}
\item \textbf{Optimal Design}: Given empirical estimates of $\phi$, what AI design maximizes social welfare?

\item \textbf{Manipulation Concerns}: If AI can manipulate attributed beliefs, what ethical constraints should guide AI design?

\item \textbf{Regulatory Implications}: How should policymakers think about AI that can exploit human psychological tendencies through attributed beliefs?
\end{enumerate}

\subsection{Connections to Other Fields}

\begin{enumerate}
\item \textbf{Mechanism Design}: How do attributed beliefs affect mechanism design problems? Can principals use AI to induce beneficial attributed beliefs?

\item \textbf{Multi-Agent Systems}: How do attributed beliefs affect cooperation in human-AI multi-agent systems?

\item \textbf{Computational Social Science}: How can ABE inform computational models of human-AI interaction at scale?
\end{enumerate}

---

## Conclusion

As AI systems become integral to economic interactions, we must develop equilibrium concepts that capture the psychological reality of human-AI engagement. Traditional game theory assumes symmetric belief structures, but human-AI interactions are inherently asymmetric: humans have genuine belief-dependent preferences while AI has design-dependent objectives.

Our attributed belief framework bridges this gap by formalizing how humans project mental states onto AI systems. The resulting Attributed Belief Equilibrium provides a foundation for understanding cooperation, trust, and conflict in human-AI contexts. This theory generates novel predictions about how AI design affects human behavior and offers guidance for creating AI systems that promote beneficial psychological responses.

The implications extend beyond individual games to broader questions about human-AI coexistence: How should we design AI that respects human psychology? What are the ethical implications of AI that can manipulate attributed beliefs? How do we ensure that AI serves human welfare rather than exploiting human psychological vulnerabilities?

These questions motivate continued theoretical development, experimental testing, and careful consideration of the ethical dimensions of human-AI interaction. Attributed Belief Equilibrium is a first step toward a game theory for the age of artificial intelligence.

---

*Draft: 2025-01-11*
