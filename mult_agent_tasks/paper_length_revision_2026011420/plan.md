# Multi-Agent Execution Plan: Paper Length Revision

**Task**: Address reviewer concerns about paper length (~55 pages, ~30,690 words)
**Date**: 2026-01-14 20:00 (Beijing Time)
**Working Directory**: `mult_agent_tasks/paper_length_revision_2026011420/`

---

## Reviewer Length Concerns Summary

| Journal | Quote |
|---------|-------|
| **Econometrica** | "At approximately 55 pages including appendix, the paper is long. The proofs could be shortened by relegating topology details to a technical appendix. The framework section (Section 2) is thorough but could be tightened; the mind perception psychology section (2.6.2) is perhaps excessive." |
| **JET** | "The paper is long (55+ pages with appendix); some proofs could be shortened without loss" |
| **GEB** | "The paper is long (~50 pages). Consider moving technical material (e.g., detailed proof of Theorem 1, attribution function specification) to supplementary appendix." |

## Current Word Counts

| Section | Words | Priority |
|---------|-------|----------|
| **Proofs Total** | **16,560** | HIGH |
| - prop_optimal_design | 4,377 | Cut heavily |
| - prop_over_anthropomorphism | 2,810 | Cut |
| - thm_existence | 1,975 | Move topology to supplement |
| **Main Sections** | **13,788** | MEDIUM |
| - sec_framework | 3,709 | Tighten (Section 2.6.2 specifically) |
| - sec_welfare | 2,812 | Moderate cuts |
| - sec_equilibrium | 2,516 | Moderate cuts |
| - sec_conclusion | 1,676 | Tighten |
| - sec_applications | 1,566 | Keep mostly intact |
| - sec_introduction | 1,509 | Keep concise |

**Target**: Reduce by 20-25% (aim for ~23,000-24,000 words)

---

## Multi-Agent Architecture (10 Agents, 4 Phases)

### Phase 1: Analysis & Information Gathering (3 Parallel Agents)

| Agent | Task | Input | Output |
|-------|------|-------|--------|
| **Agent-1** (opus) | Analyze reviewer length concerns; extract specific actionable items | review_20260115/*.md | `phase1_reviewer_analysis.md` |
| **Agent-2** (opus) | Section-by-section content analysis; identify verbose passages, redundancies | drafts/*.tex | `phase1_content_analysis.md` |
| **Agent-3** (opus) | Analyze proofs; identify what can move to supplementary | drafts/proofs/*.tex | `phase1_proof_analysis.md` |

### Phase 2: Strategy Development (2 Parallel Agents)

| Agent | Task | Input | Output |
|-------|------|-------|--------|
| **Agent-4** (opus) | Develop section tightening strategy | Phase 1 outputs | `phase2_section_strategy.md` |
| **Agent-5** (opus) | Develop proof reorganization plan | Phase 1 outputs | `phase2_proof_strategy.md` |

### Phase 3: Execution (4 Parallel Agents)

| Agent | Task | Input | Output |
|-------|------|-------|--------|
| **Agent-6** (opus) | Revise Introduction & Framework | sec_introduction.tex, sec_framework.tex | Direct file edits + `phase3_intro_framework_log.md` |
| **Agent-7** (opus) | Revise Equilibrium & Applications | sec_equilibrium.tex, sec_applications.tex | Direct file edits + `phase3_equilibrium_apps_log.md` |
| **Agent-8** (opus) | Revise Welfare & Conclusion | sec_welfare.tex, sec_conclusion.tex | Direct file edits + `phase3_welfare_conclusion_log.md` |
| **Agent-9** (opus) | Reorganize proofs; create supplementary appendix | drafts/proofs/*.tex | Direct file edits + `phase3_proofs_log.md` |

### Phase 4: Review & Integration (2 Agents)

| Agent | Task | Input | Output |
|-------|------|-------|--------|
| **Agent-10** (opus) | Review all revisions for quality, consistency, academic rigor | All revised files | `phase4_review_report.md` |
| **Main Agent** | Integrate feedback, make final adjustments | Review report | Final revised manuscript |

---

## Execution Rules

1. **Context Protection**: Each subagent writes results to local files immediately; only status summaries return to main agent
2. **Model**: All subagents use `opus` model
3. **File Operations**: Subagents have full Read + Write + Edit + Bash access
4. **No Returns**: Subagents must NOT return full content to main agent
5. **Word Count Tracking**: Each Phase 3 agent reports before/after word counts

---

## Success Criteria

- [ ] Total word count reduced by 20-25%
- [ ] Proofs reorganized with supplementary appendix created
- [ ] Framework Section 2.6.2 (mind perception) tightened
- [ ] Existence theorem topology details moved to supplement
- [ ] All LaTeX compiles without errors
- [ ] Academic rigor maintained

---

## Timeline

| Phase | Duration | Status |
|-------|----------|--------|
| Phase 1 | Parallel execution | Pending |
| Phase 2 | After Phase 1 complete | Pending |
| Phase 3 | Parallel execution | Pending |
| Phase 4 | After Phase 3 complete | Pending |
