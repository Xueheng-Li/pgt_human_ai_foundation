## Project: Economic Research Paper - Attributed Belief Equilibrium

**Target journals**: Econometrica, Journal of Economic Theory

Theoretical research extending psychological game theory (PGT) to human-AI interactions. Innovation: humans attribute beliefs to AI agents who lack mental states.

## Directory Structure

```
pgt_human_ai_foundation/
├── drafts/               # Working paper manuscript (main.tex + sections)
├── theory/               # Formal framework (foundations.tex is master reference)
├── proofs/               # Existence theorem
├── applications/         # Trust game, public goods
├── literature/           # Key papers (17 annotated)
├── references.bib        # Bibliography
└── archive/              # Archived multi-project files
```

## Build Commands

```bash
# Manuscript
cd drafts && pdflatex main.tex && bibtex main && pdflatex main.tex && pdflatex main.tex

# Theory foundations
cd theory && pdflatex foundations.tex && bibtex foundations && pdflatex foundations.tex
```

## File Format Policy

- **LaTeX (.tex)**: Definitions, theorems, proofs, manuscript
- **Markdown (.md)**: Notes, brainstorming, project docs

## Key References

- `theory/foundations.tex`: Master reference for all assumptions and notation
- `drafts/main.tex`: Current manuscript draft

## Paper Search/fetch Order

1. Zotero library via MCP
2. arXiv via arxiv skill
3. Web-researcher subagent

## Language and writing style

Follow the style of Sanjeev Goyal's network economics papers:
- Analytical precision in mathematical arguments
- Clear identification of economic mechanisms
- Strong links between theory and empirical observations

Use x-writer subagent to improve clarity, grammar, and style

In general:

0. American English, and always write complete sentences.
1. **Economy**: Every word must earn its place. Cut ruthlessly. Target 30-50% fewer words than typical academic prose.
2. **Specificity**: Replace adjectives with numbers. "The effect is 12 percentage points" not "substantial effect."
3. **Directness**: Active voice, positive form. Lead with findings. "We find X" not "It was found that X."
4. **Structure**: Build to emphatic endings. The last word of a sentence, paragraph, and paper carries the most weight.
5. **Simplicity**: If it seems complex, you haven't explained it well enough.
6. **Transitional**: Each sentence/paragraph builds on the last through transitions and repeated key terms.

### Words to Avoid

- **Self-promotion**: novel, groundbreaking, vital, revolutionary, crucial
- **Empty modifiers**: substantial, robust, comprehensive, sophisticated, nuanced
- **Vague terms**: various, several, interesting, important (without specifics)
- **Filler phrases**: embarks on, sheds light on, paves the way, delve into, leverage
- Unnecessary quotation marks
- Abuse of bullet point format