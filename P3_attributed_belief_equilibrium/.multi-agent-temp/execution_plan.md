# Multi-Agent Execution Plan: PGT Literature Review & Introduction Update

**Task**: Update `/P3_attributed_belief_equilibrium/introduction.md` based on classical PGT literature conventions

**Created**: 2026-01-11
**Status**: Pending Approval

---

## Phase 1: 规划阶段 (Research & Planning)

### Agent 1.1: Classical PGT Literature Fetcher
**Type**: `web-researcher`
**Purpose**: Fetch key conventions from GPS 1989, Battigalli & Dufwenberg 2009
**Output**: `.multi-agent-temp/phase1_pgt_classics.md`

### Agent 1.2: Extended PGT Literature Fetcher
**Type**: `web-researcher`
**Purpose**: Fetch guilt/reciprocity papers (Dufwenberg & Kirchsteiger 2004, Charness & Dufwenberg 2006)
**Output**: `.multi-agent-temp/phase1_pgt_extended.md`

### Agent 1.3: Current Introduction Analyzer
**Type**: `general-purpose`
**Purpose**: Analyze current notation/terminology gaps vs PGT standards
**Output**: `.multi-agent-temp/phase1_current_analysis.md`

**Parallelization**: All 3 agents run in parallel

---

## Phase 2: 实施阶段 (Execution & Integration)

### Agent 2.1: Notation Standardizer
**Type**: `general-purpose`
**Purpose**: Create notation mapping (current → PGT standard) based on Phase 1 outputs
**Inputs**: Phase 1 outputs
**Output**: `.multi-agent-temp/phase2_notation_mapping.md`

### Agent 2.2: Introduction Rewriter
**Type**: `x-writer`
**Purpose**: Rewrite introduction.md using standard PGT notation
**Inputs**: Phase 1 outputs + notation mapping
**Output**: `.multi-agent-temp/phase2_introduction_draft.md`

### Agent 2.3: Framework.md Updater
**Type**: `general-purpose`
**Purpose**: Update theory/framework.md for consistency
**Output**: `.multi-agent-temp/phase2_framework_draft.md`

**Sequencing**: Agent 2.1 runs first → then Agents 2.2 & 2.3 in parallel

---

## Phase 3: 审阅阶段 (Review & Feedback)

### Agent 3.1: Technical Reviewer
**Type**: `paper-reviewer`
**Purpose**: Review notation consistency, mathematical rigor
**Inputs**: Phase 2 drafts
**Output**: `.multi-agent-temp/phase3_technical_review.md`

### Agent 3.2: Literature Alignment Checker
**Type**: `general-purpose`
**Purpose**: Verify alignment with PGT literature conventions
**Inputs**: Phase 1 + Phase 2 outputs
**Output**: `.multi-agent-temp/phase3_alignment_check.md`

**Parallelization**: Both agents run in parallel

---

## Phase 4: 修订阶段 (Revision)

### Agent 4.1: Final Reviser
**Type**: `x-writer`
**Purpose**: Incorporate all feedback, produce final introduction.md
**Inputs**: All Phase 3 feedback
**Output**: Final update to `introduction.md`

### Agent 4.2: Documentation Updater
**Type**: `general-purpose`
**Purpose**: Update CLAUDE.md with new notation conventions
**Output**: Update to `CLAUDE.md`

**Sequencing**: Agent 4.1 first → then Agent 4.2

---

## Key PGT Papers to Fetch

1. **GPS 1989**: "Games and Economic Behavior" - foundational belief-dependent utilities
2. **BD 2009**: Battigalli & Dufwenberg - dynamic psychological games, sequential rationality
3. **DK 2004**: Dufwenberg & Kirchsteiger - guilt and reciprocity
4. **CD 2006**: Charness & Dufwenberg - promises and guilt aversion
5. **ABM 2016**: Attanasi, Battigalli, Manzoni - incomplete information psychological games

## Expected Notation Updates

| Current | Expected PGT Standard |
|---------|----------------------|
| $E_i^{(2)}$ | Check BD 2009 notation for higher-order beliefs |
| $U_i^H(s, E_i)$ | Verify utility function form |
| $\phi_i$ (attribution) | Novel - needs proper integration |

## Output Files Summary

```
.multi-agent-temp/
├── execution_plan.md (this file)
├── phase1_pgt_classics.md
├── phase1_pgt_extended.md
├── phase1_current_analysis.md
├── phase2_notation_mapping.md
├── phase2_introduction_draft.md
├── phase2_framework_draft.md
├── phase3_technical_review.md
├── phase3_alignment_check.md
└── final_changes_log.md
```

---

**Awaiting user approval to proceed.**
