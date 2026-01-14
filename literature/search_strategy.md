# Literature Search Strategy for PGT Human-AI Foundation

> Comprehensive strategy for identifying relevant papers across five literature streams
> Generated: 2026-01-11

---

## Executive Summary

This project sits at an unusual intersection: **psychological game theory** (a mature field in economics) meets **human-AI interaction** (an exploding field in CS/HCI) meets **stochastic evolutionary dynamics** (mathematical game theory). Standard keyword searches will miss many relevant papers because:

1. PGT papers rarely mention "AI" even when methods generalize
2. Human-AI papers rarely use formal game-theoretic frameworks
3. Stochastic stability literature uses different terminology across disciplines

This document provides a **layered search strategy** to bridge these gaps.

---

## 1. Literature Streams and Their Gaps

### Stream A: Psychological Game Theory
**Status:** Well-covered in existing review (GPS 1989, BD 2009/2022, Li 2026)
**Gap:** No existing work models **asymmetric** populations where some players (AI) lack genuine beliefs but others (humans) have belief-dependent preferences.

### Stream B: Human-AI Strategic Interaction
**Status:** Rapidly growing but theoretically thin
**Gap:** Most papers are empirical (HCI) without formal game-theoretic models. Need papers that bridge behavioral economics and AI.

### Stream C: Evolutionary Dynamics with Heterogeneity
**Status:** Mathematical literature exists but not applied to human-AI
**Gap:** No stochastic stability analysis with **type-dependent mutation rates** (humans make errors differently than AI).

### Stream D: Moral Psychology of AI
**Status:** Philosophy and cognitive science literature
**Gap:** Need to connect to formal "attribution function" in economic theory.

### Stream E: AI Alignment and Cooperation
**Status:** CS/AI safety literature
**Gap:** Lacks behavioral economics perspective on how humans react to programmed prosociality.

---

## 2. arXiv Search Results (2026-01-11)

### Highly Relevant Papers Found

| Paper | Authors | Year | Relevance |
|-------|---------|------|-----------|
| **Theory of Mind with Guilt Aversion Facilitates Cooperative Reinforcement Learning** | Nguyen et al. | 2020 | Direct application of guilt aversion to RL agents |
| **The evolutionary advantage of guilt: co-evolution of social and non-social guilt** | Cimpeanu, Pereira & Han | 2023 | Evolution of guilt in artificial agents |
| **The Machine Psychology of Cooperation: Can GPT models operationalize prompts for cooperation** | Phelps & Russell | 2023 | LLM behavior in social dilemmas |
| **More Similar Values, More Trust? Effect of Value Similarity on Trust in Human-Agent Interaction** | Mehrotra et al. | 2021 | Trust and value alignment in human-AI |
| **The role of reciprocity in human-robot social influence** | Zonca et al. | 2021 | Reciprocity with robots |
| **How norms shape the evolution of prosocial behavior (C.U.R.E.)** | Mintz & Fu | 2024 | Norm evolution with mathematical model |
| **Impact of Committed Minorities: Critical Mass of Cooperation in IPD** | He et al. | 2023 | Critical mass effects (like our alpha-star threshold) |
| **A Model of Human Cooperation in Social Dilemmas** | Capraro | 2013 | Prosocial vs proself types model |
| **Overcoming Algorithm Aversion with Transparency** | Bohlen et al. | 2025 | Algorithm aversion mitigation |
| **LLMs grasp morality in concept** | Pock et al. | 2023 | Theory of meaning for LLMs |
| **Assessing LLMs for Moral Value Pluralism** | Benkler et al. | 2023 | LLM moral values assessment |

### Moderately Relevant Papers

| Paper | Authors | Year | Relevance |
|-------|---------|------|-----------|
| **Online Learning in Iterated Prisoner's Dilemma to Mimic Human Behavior** | Lin et al. | 2020 | RL agents in IPD |
| **Cooperation in spatial prisoner's dilemma with probabilistic abstention** | Cardinot et al. | 2018 | Abstention option in PD |
| **Dynamic Structure in Four-strategy Game: Theory and Experiment** | Wang et al. | 2022 | Experimental game dynamics |
| **Trust and Reliance in XAI: Attitudinal vs Behavioral Measures** | Scharowski et al. | 2022 | Trust measurement in AI |
| **Minimum Levels of Interpretability for Artificial Moral Agents** | Vijayaraghavan & Badea | 2023 | AMA interpretability |

---

## 3. Recommended Search Queries

### Primary Queries (High Precision)

```bash
# Query 1: PGT + AI
python3 ~/.claude/skills/arxiv-search/arxiv_search.py \
  "psychological game belief-dependent preferences artificial agent" --max-papers 15

# Query 2: Guilt/indignation + evolution
python3 ~/.claude/skills/arxiv-search/arxiv_search.py \
  "guilt aversion reciprocity evolutionary dynamics cooperation" --max-papers 15

# Query 3: Human-AI cooperation games
python3 ~/.claude/skills/arxiv-search/arxiv_search.py \
  "human-AI cooperation game theory strategic interaction" --max-papers 15

# Query 4: LLM social behavior
python3 ~/.claude/skills/arxiv-search/arxiv_search.py \
  "large language model social dilemma prisoner cooperation" --max-papers 15

# Query 5: Stochastic stability heterogeneous
python3 ~/.claude/skills/arxiv-search/arxiv_search.py \
  "stochastic stability mutation rate heterogeneous population" --max-papers 15
```

### Secondary Queries (Broader Recall)

```bash
# Query 6: Attribution and moral responsibility
python3 ~/.claude/skills/arxiv-search/arxiv_search.py \
  "moral attribution responsibility robot AI agent" --max-papers 15

# Query 7: Trust and algorithm aversion
python3 ~/.claude/skills/arxiv-search/arxiv_search.py \
  "algorithm aversion appreciation trust decision machine" --max-papers 15

# Query 8: Theory of Mind for AI
python3 ~/.claude/skills/arxiv-search/arxiv_search.py \
  "theory of mind artificial agent robot ToM attribution" --max-papers 15

# Query 9: Prosocial AI
python3 ~/.claude/skills/arxiv-search/arxiv_search.py \
  "prosocial AI cooperative agent altruistic machine" --max-papers 15
```

### arXiv Categories to Monitor

| Category | Description | Relevance |
|----------|-------------|-----------|
| `econ.TH` | Economic Theory | Primary for game theory |
| `cs.GT` | Computer Science Game Theory | Technical models |
| `cs.AI` | Artificial Intelligence | AI behavior modeling |
| `cs.HC` | Human-Computer Interaction | Human-AI experiments |
| `cs.MA` | Multi-Agent Systems | Agent cooperation |
| `physics.soc-ph` | Physics: Society | Evolutionary dynamics |
| `q-bio.PE` | Populations and Evolution | Mathematical evolution |

---

## 4. Papers to Acquire (Not on arXiv)

### Must-Have Papers

| Paper | Where to Find | Why Needed |
|-------|---------------|------------|
| Horton (2023) - "Large Language Models as Simulated Economic Agents" | NBER/SSRN | LLM as economic agent |
| Aher et al. (2023) - "Using LLMs to Simulate Multiple Humans" | NeurIPS | Agent simulation |
| Dietvorst et al. (2015) - "Algorithm Aversion" | J. Exp. Psych. | Original algorithm aversion |
| Dietvorst et al. (2018) - "Overcoming Algorithm Aversion" | Management Science | When people accept algorithms |
| Bigman & Gray (2018) - "People Are Averse to Machines Making Moral Decisions" | Cognition | Moral aversion to AI |
| Waytz et al. (2010) - "Who Sees Human?" | Perspectives on Psych Science | Anthropomorphism |
| Gray & Wegner (2012) - "Mind Perception" | Science | Experience vs Agency dimensions |
| Dafoe et al. (2020) - "Open Problems in Cooperative AI" | DeepMind | AI cooperation research agenda |
| Rahwan et al. (2019) - "Machine Behavior" | Nature | Machine behavior framework |
| Dennett (1987) - "The Intentional Stance" | MIT Press | Philosophical foundation |

### Nice-to-Have Papers

| Paper | Where to Find | Why Relevant |
|-------|---------------|--------------|
| Bonnefon et al. (2016) - "Moral Machine" | Science | AI moral dilemmas |
| Awad et al. (2018) - "Moral Machine Experiment" | Nature | Global moral preferences |
| Crandall et al. (2018) - "Cooperating with Machines" | Nature Comm. | Human-machine cooperation |
| de Melo et al. (2018) - "Cooperation with Robot Partners" | PNAS | Robot cooperation |
| March (2021) - "Algorithm as Social Actors" | CHI | Algorithms in social context |

---

## 5. Theoretical Gaps to Address

### Gap 1: The Attribution Problem

**Literature Needed:**
- Cognitive science on anthropomorphism (Waytz, Epley, Cacioppo)
- Philosophy of mind on intentional stance (Dennett 1987)
- Mind perception research (Gray & Wegner 2012)
- Empirical work on ToM for artificial agents

**Key Question:** How does the function $\tilde{E}_i^{(2,j)} = \phi_i(\theta_j, x_j, \omega_i)$ relate to actual AI programming?

### Gap 2: Asymmetric Stochastic Stability

**Literature Needed:**
- Two-timescale stochastic approximation (Borkar 1997, 2008)
- Evolutionary dynamics in structured populations
- Order of limits results (Sandholm 2010 and extensions)
- Population genetics with different mutation rates

**Key Question:** When $\epsilon_H \neq \epsilon_A$, which limit to take first?

### Gap 3: Spite/Indignation with Non-Human Targets

**Literature Needed:**
- Moral psychology on emotional responses to machines
- Experimental economics on punishment of algorithms
- Philosophy on moral patiency of AI
- Robot ethics literature

**Key Question:** Is indignation triggered by AI defection? Is it weaker/stronger?

### Gap 4: Equilibrium Refinement

**Literature Needed:**
- Games with boundedly rational players
- Mechanism design with behavioral agents (Koszegi & Rabin)
- Hybrid human-algorithm systems

**Key Question:** When some players (AI) don't have beliefs, what's the right solution concept?

---

## 6. Journal-Specific Search Strategy

### Economics Journals (via SSRN, NBER, EconLit)

**Search Terms:**
- "psychological game" AND "heterogeneous"
- "belief-dependent motivation" AND "evolution"
- "guilt aversion" AND "experiment"
- "stochastic stability" AND "cooperation"

**Target Journals:**
- Games and Economic Behavior
- Journal of Economic Theory
- Econometrica
- Theoretical Economics
- Journal of Economic Behavior & Organization

### Psychology/Cognitive Science (via PsycINFO)

**Search Terms:**
- "anthropomorphism" AND "trust"
- "theory of mind" AND "robot"
- "moral judgment" AND "artificial agent"
- "mind perception" AND "machine"

**Target Journals:**
- Cognition
- Journal of Experimental Psychology
- Psychological Science
- Trends in Cognitive Sciences

### CS/AI (via ACM DL, IEEE Xplore)

**Search Terms:**
- "human-AI cooperation" AND "game theory"
- "multi-agent" AND "social dilemma"
- "trust calibration" AND "algorithm"
- "prosocial AI" AND "behavior"

**Target Venues:**
- CHI, CSCW
- NeurIPS, ICML
- AAMAS
- Nature Machine Intelligence

---

## 7. Zotero Search Strategy

For papers already in the Zotero library, search with these tags:

```
tag:psychological-game
tag:stochastic-stability
tag:cooperation
tag:human-AI
tag:evolution
tag:guilt
tag:reciprocity
```

---

## 8. Next Steps

### Immediate Actions

1. **Run remaining arXiv queries** (secondary queries above)
2. **Check Zotero** for already-acquired papers
3. **SSRN/NBER search** for working papers
4. **Google Scholar alerts** for new papers citing:
   - GPS 1989
   - Battigalli & Dufwenberg 2009
   - Li 2026 GEB
   - Mei et al. 2024 PNAS

### Weekly Monitoring

Set up alerts for:
- arXiv categories: `econ.TH`, `cs.GT`, `cs.AI`
- Authors: Battigalli, Dufwenberg, Mei, Jackson, Capraro
- Keywords: "psychological game", "human-AI cooperation", "algorithmic trust"

---

## 9. Key Papers Summary Table

| Paper | Stream | Gap Addressed | Priority |
|-------|--------|---------------|----------|
| Nguyen et al. 2020 (ToM + Guilt RL) | A+D | Attribution + AI beliefs | High |
| Cimpeanu et al. 2023 (Guilt evolution) | A+C | Guilt in agents | High |
| Phelps & Russell 2023 (LLM cooperation) | B | AI behavior in dilemmas | High |
| He et al. 2023 (Critical mass) | C | Threshold effects | Medium |
| Mintz & Fu 2024 (CURE norms) | A+C | Norm evolution | Medium |
| Mehrotra et al. 2021 (Value similarity trust) | B+D | Trust attribution | Medium |
| Bohlen et al. 2025 (Algorithm aversion) | B | When humans trust AI | Medium |
| Capraro 2013 (Social dilemmas model) | A | Type classification | Background |

---

*Last updated: 2026-01-11*
