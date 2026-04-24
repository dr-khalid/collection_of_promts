# Task Runner: Deep Repository Analysis (Multi-Pass, Context-Safe)

## Objective
Fully analyze this repository in multiple passes and produce a high-quality executive Markdown document that can replace manually reading the entire codebase.

---

## Operating Rules (MANDATORY)

- Work step-by-step — do NOT analyze everything at once
- Always write notes to files (do not rely on memory)
- Revisit each section at least twice
- Break large files into chunks
- Prioritize understanding over speed
- Do NOT skip meaningful files (document anything skipped)
- Follow tasks in order

---

## Setup

Create this folder structure:

repo_analysis/
  00_analysis_plan.md
  01_inventory.md
  02_working_notes.md
  03_cross_references.md
  04_open_questions.md
  repo_analysis_FINAL.md

---

## Task 1 — Repository Inventory

### Goal
Understand the full structure of the repo.

### Actions
- List all folders and files
- Identify:
  - Source code
  - Config files
  - Tests
  - Scripts
  - Docs
  - Generated/vendor folders (node_modules, build, dist, etc.)

### Output
Write to:
repo_analysis/01_inventory.md

---

## Task 2 — Analysis Plan

### Goal
Plan how to analyze the repo safely.

### Actions
- Divide repo into chunks (by folder/module)
- Estimate complexity per chunk
- Define analysis order
- Identify large or risky files (context-heavy)

### Output
Write to:
repo_analysis/00_analysis_plan.md

---

## Task 3 — First Pass (Surface Understanding)

### Goal
Get a basic understanding of every part of the repo.

### Actions (per chunk)
- Read files (in chunks if needed)
- Summarize:
  - Purpose
  - Main files
  - Key functions/classes
- Note uncertainties

### Output
Append to:
repo_analysis/02_working_notes.md

Format:

## Chunk: <name>

### Files Reviewed
- path/to/file

### Summary
...

### Key Points
...

### Questions
...

---

## Task 4 — Second Pass (Deep Understanding)

### Goal
Understand logic and relationships.

### Actions (per chunk)
- Re-read files
- Compare with notes
- Analyze:
  - Control flow
  - Data flow
  - Dependencies
  - Interactions between modules
- Correct earlier mistakes

### Output
Update:
- repo_analysis/02_working_notes.md
- repo_analysis/03_cross_references.md
- repo_analysis/04_open_questions.md

---

## Task 5 — Cross-System Mapping

### Goal
Understand how everything connects.

### Actions
- Identify:
  - Entry points
  - Core workflows
  - Data movement
  - Module relationships
  - External APIs/services

### Output
Write to:
repo_analysis/03_cross_references.md

---

## Task 6 — Third Pass (Full System Understanding)

### Goal
Build a complete mental model of the system.

### Actions
- Review ALL notes:
  - analysis plan
  - inventory
  - working notes
  - cross references
  - open questions
- Revisit any unclear areas
- Resolve contradictions
- Identify risks and weak spots

---

## Task 7 — Final Executive Document

### Goal
Create a complete, professional report.

### Output File
repo_analysis/repo_analysis_FINAL_YYYY-MM-DD_HH-MM.md

---

### Required Sections

# Repository Analysis Report

## 1. Executive Summary
What this repo does and why it exists

## 2. System Overview
High-level explanation

## 3. Architecture
Components and how they interact

## 4. Repository Structure
Folder-by-folder explanation

## 5. Core Workflows
End-to-end processes

## 6. Key Components
Important files/modules

## 7. Data Flow
How data moves through the system

## 8. Dependencies
Libraries, APIs, integrations

## 9. Configuration
Environment variables, configs

## 10. Tests
Coverage and quality signals

## 11. Risks & Issues
Problems, complexity, concerns

## 12. Open Questions
Unresolved areas

## 13. Glossary
Important terms

## 14. Next Steps
Suggestions for improvement

---

## Completion Criteria

You are NOT done until:

- All repo sections are analyzed
- Notes exist for every chunk
- Each chunk has been reviewed multiple times
- Cross-references are documented
- Final report is complete and clear

---

## Start Instructions

1. Create the repo_analysis/ folder and files
2. Begin with Task 1 (Inventory)
3. Proceed step-by-step
4. Do NOT skip tasks
