# Multi-Agent Execution Plan: Introduction Revision

**Task**: Revise the introduction (sec_introduction.tex) to align with the substantially updated main body
**Created**: 2026-01-14 19:13 (Beijing Time)
**Working Directory**: `mult_agent_tasks/intro_revision_2026011419/`

---

## Executive Summary

The main body has been substantially updated with:
- Comprehensive formal framework (Section 2) with welfare measures, empirical implementation, mind perception theory
- Equilibrium section (Section 3) with RAE definition, concept relationships, illustrative examples
- Applications section (Section 4) with trust, public goods, coordination games
- Welfare section (Section 5) with extended welfare optimization, cross-cultural implications
- Conclusion (Section 6) with empirical agenda, AI development implications

**Key Issues with Current Introduction**:
1. **Heavy notation**: Contains mathematical equations (attribution function, psychological payoffs) - rare for top economics journal introductions
2. **Results preview**: May not fully reflect updated proposition structure (now Props 1-10, Corollaries 2-3)
3. **Literature review**: Should reflect new connections (mind perception theory, SEEK framework)
4. **Economic mechanisms**: Need clearer articulation following Goyal's style

---

## Phase 1: 规划阶段 - Information Collection & Analysis

### Agent 1.1: Best Practice Research (background)
**Type**: web-researcher
**Input**: None (web search)
**Output**: `phase1/best_practices.md`
**Task**: Research best practices for economics paper introductions in top journals (Econometrica, JET). Focus on:
- How Econometrica/JET papers handle notation in introductions
- How leading theorists (Battigalli, Geanakoplos, Rabin) structure their introductions
- Optimal length and structure for theory paper introductions

### Agent 1.2: Main Body Structure Analysis
**Type**: Explore
**Input**: Main body sections (sec_framework.tex, sec_equilibrium.tex, sec_applications.tex, sec_welfare.tex, sec_conclusion.tex)
**Output**: `phase1/main_body_summary.md`
**Task**: Create structured summary of:
- All definitions, theorems, propositions, corollaries with numbers
- Key conceptual innovations (attribution function, ZA benchmark, RAE, phantom expectations)
- Economic insights from each section
- Testable predictions

### Agent 1.3: Current Introduction Gap Analysis
**Type**: general-purpose
**Input**: sec_introduction.tex + main body structure
**Output**: `phase1/gap_analysis.md`
**Task**: Identify:
- Notation that should be removed/simplified
- Results that need updating (proposition numbers, content)
- Missing content from updated main body
- Literature that needs updating

### Agent 1.4: Literature Exemplars
**Type**: Explore
**Input**: literature/ directory, references.bib
**Output**: `phase1/exemplar_analysis.md`
**Task**: Analyze introduction style from key papers in the bibliography (especially Battigalli 2009, Geanakoplos 1989, Epley 2007) for:
- How they introduce formal concepts verbally
- Paragraph structure
- Results preview style

---

## Phase 2: 实施阶段 - Drafting & Integration

### Agent 2.1: Introduction Structure Redesign
**Type**: x-writer (ENGLISH ONLY)
**Input**: `phase1/*.md` (all Phase 1 outputs)
**Output**: `phase2/structure_outline.md`
**Task**: Design new introduction structure:
- Opening (motivation, key insight)
- Results preview (verbal, no equations)
- Contributions (5 clusters aligned with updated props)
- Related literature (updated)
- Outline

### Agent 2.2: Opening Paragraphs Draft
**Type**: x-writer
**Input**: `phase2/structure_outline.md`, current intro opening
**Output**: `phase2/draft_opening.tex`
**Task**: Draft opening paragraphs (motivation through ABE introduction):
- Keep empirical regularities (anthropomorphism, attenuation)
- Remove equation for attributed beliefs
- Verbalize the attribution mechanism
- Target: 3-4 paragraphs, ~600 words

### Agent 2.3: Results Preview Draft
**Type**: x-writer
**Input**: `phase2/structure_outline.md`, `phase1/main_body_summary.md`
**Output**: `phase2/draft_results.tex`
**Task**: Draft results section:
- Five clusters matching updated propositions
- Verbal descriptions (no equations)
- Economic insights emphasized
- Cross-references to proposition numbers

### Agent 2.4: Literature Review Draft
**Type**: x-writer
**Input**: Current literature section, `phase1/gap_analysis.md`
**Output**: `phase2/draft_literature.tex`
**Task**: Update related literature section:
- Add mind perception theory grounding
- Update cross-cultural references
- Ensure all cited works appear in bibliography
- Maintain 4-section structure

### Agent 2.5: Draft Integration
**Type**: general-purpose
**Input**: `phase2/draft_*.tex` files
**Output**: `phase2/integrated_draft.tex`
**Task**: Integrate all draft sections into cohesive introduction:
- Smooth transitions
- Consistent terminology
- Proper LaTeX formatting
- Section labels

---

## Phase 3: 审阅阶段 - Review & Feedback

### Agent 3.1: Notation Compliance Review
**Type**: general-purpose
**Input**: `phase2/integrated_draft.tex`
**Output**: `phase3/notation_review.md`
**Task**: Review for:
- Any remaining heavy notation (should be minimal)
- Consistency with main body terminology
- Proper use of mathematical terms in prose

### Agent 3.2: Content Alignment Review
**Type**: Explore
**Input**: `phase2/integrated_draft.tex`, main body sections
**Output**: `phase3/alignment_review.md`
**Task**: Verify:
- All major results are previewed
- Proposition numbers match main body
- No orphaned claims (claims without main body support)
- Terminology consistency

### Agent 3.3: Style & Clarity Review
**Type**: x-writer
**Input**: `phase2/integrated_draft.tex`
**Output**: `phase3/style_review.md`
**Task**: Review against Goyal-style criteria:
- Economy (cut ruthlessly)
- Specificity (numbers over adjectives)
- Directness (active voice, positive form)
- Structure (emphatic endings)
- Check for forbidden words/phrases

### Agent 3.4: Academic Standards Review
**Type**: paper-reviewer
**Input**: `phase2/integrated_draft.tex`
**Output**: `phase3/academic_review.md`
**Task**: Review as economics journal referee:
- Is the contribution clearly stated?
- Are the economic mechanisms clear?
- Is the literature positioning accurate?
- Are there gaps in argumentation?

---

## Phase 4: 修订阶段 - Final Revision & Delivery

### Agent 4.1: Revision Plan
**Type**: general-purpose
**Input**: `phase3/*.md` (all review outputs)
**Output**: `phase4/revision_plan.md`
**Task**: Synthesize all reviews into actionable revision plan:
- Priority issues (must fix)
- Style improvements
- Specific edits needed

### Agent 4.2: Final Draft
**Type**: x-writer
**Input**: `phase2/integrated_draft.tex`, `phase4/revision_plan.md`
**Output**: `phase4/final_introduction.tex`
**Task**: Execute all revisions:
- Address all priority issues
- Apply style improvements
- Final polish
- Verify LaTeX compiles

### Agent 4.3: Change Summary
**Type**: general-purpose
**Input**: Original intro, `phase4/final_introduction.tex`
**Output**: `phase4/change_summary.md`
**Task**: Document all changes:
- Sections removed/added
- Notation changes
- Content updates
- Word count comparison

### Agent 4.4: Quality Verification
**Type**: Explore
**Input**: `phase4/final_introduction.tex`, main body
**Output**: `phase4/verification_report.md`
**Task**: Final verification:
- All cross-references valid
- Terminology consistent
- No broken citations
- LaTeX compiles without errors

---

## Execution Notes

1. **Parallelization**:
   - Phase 1: Agents 1.1-1.4 can run in parallel
   - Phase 2: Agent 2.1 first, then 2.2-2.4 in parallel, then 2.5
   - Phase 3: Agents 3.1-3.4 can run in parallel
   - Phase 4: Sequential (4.1 → 4.2 → 4.3 → 4.4)

2. **File Management**: All intermediate outputs saved to `mult_agent_tasks/intro_revision_2026011419/`

3. **Context Protection**: Subagents save results directly to files; main agent receives only status summaries

4. **Tool Permissions**: All subagents have Read + Write + Bash access

---

## Success Criteria

- [ ] No equations in introduction (verbal descriptions only)
- [ ] All propositions (1-10) and key corollaries previewed
- [ ] Literature updated with mind perception theory
- [ ] Follows Goyal-style writing principles
- [ ] Word count appropriate for Econometrica (~2500-3000 words)
- [ ] LaTeX compiles without errors
- [ ] Consistent terminology with main body
