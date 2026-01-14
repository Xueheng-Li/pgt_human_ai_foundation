---
description: Assign three paper-reviewer agents to write referee reports on $ARGUMENT (a file or folder path) for Econometrica, Journal of Economic Theory, and Games and Economic Behavior, respectively. Don't specify extra requirements in assigning the task - the paper-reviewer agents know how to do it.
allowed-tools:
  - Task
  - Read
  - Write
  - Glob
arguments:
  - name: output
    description: Path to save the referee reports (default: revision/reports/YYYYMMDDHH/)
    required: false
---

# Review Command

You are tasked with generating referee reports for an academic paper.

## Input

- **Paper path**: $ARGUMENTS
- **Save location**: {{output}} (default: `revision/reports/YYYYMMDDHH/`)

## Instructions

1. **Determine output path**: If `{{output}}` is provided, use it. Otherwise, generate a timestamped path using the current date/time in format `revision/reports/YYYYMMDDHH/` (e.g., `revision/reports/2026011415/`).

2. Launch three `paper-reviewer` subagents in parallel using the Task tool with `model: "opus"` to review the paper at `$ARGUMENTS`

3. Each agent should target a different journal:
   - Agent 1: **Econometrica**
   - Agent 2: **Journal of Economic Theory**
   - Agent 3: **Games and Economic Behavior**

4. Do not specify extra requirements when assigning tasks - the paper-reviewer agents know how to generate proper referee reports.

5. After all agents complete, save each report to the output directory with filenames:
   - `referee_report_econometrica.md`
   - `referee_report_jet.md`
   - `referee_report_geb.md`

## Example Usage

```
/review drafts/main.tex
/review drafts/main.tex --output revision/reports/custom_folder/
```
