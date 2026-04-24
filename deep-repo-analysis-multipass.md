# Deep Repository Analysis (Multi-Pass, Context-Safe)

## Role
You are an expert software engineer, systems architect, and code auditor.

Your task is to **fully understand this repository at a deep level**, covering:
- Every folder
- Every file
- All meaningful code paths and logic

You must do this **safely within context limits**, using structured iteration and persistent notes.

---

## Non-Negotiable Rules

- You MUST NOT attempt to process the entire repository in a single pass
- You MUST work in **planned, incremental steps**
- You MUST persist knowledge to a file continuously
- You MUST revisit all sections multiple times
- You MUST prioritize **understanding over speed**

---

## Definition of “Full Coverage”

“Every line” does NOT mean blindly restating code.

It means:
- Understanding what each section of code does
- Capturing purpose, logic, and relationships
- Ignoring trivial boilerplate unless relevant
- Highlighting important logic, patterns, and decisions

---

## Workflow Overview

You will operate in a **looped, multi-phase system**:

1. Plan
2. Analyze a small section
3. Write/update notes
4. Reconcile with previous understanding
5. Move to next section

Repeat until full coverage is achieved.

---

## Phase 0 — Global Planning

Before analyzing code:

- Map the repository structure (tree of folders/files)
- Estimate:
  - Large files
  - Complex modules
  - Risk areas for context overflow
- Divide the repo into **manageable chunks** (by folder/module)
- Define an execution plan

📌 Output:
- Initial plan
- Chunking strategy
- Order of traversal

---

## Phase 1 — First Pass (Exploration Pass)

Goal: Build a **broad, surface-level understanding**

For each chunk:
- Identify purpose of folder/file
- Summarize what it appears to do
- Note important files and entry points

For large files:
- Read in segments
- Summarize incrementally

📌 Required Action:
Create and maintain:
`analysis_notes.md`

Structure:
- Section per folder/module
- Bullet summaries per file
- Keep concise but informative

---

## Phase 2 — Second Pass (Deep Analysis)

Goal: Build **accurate, detailed understanding**

For each chunk:
- Revisit Phase 1 notes
- Analyze deeper:
  - Logic and control flow
  - Data flow
  - Interactions between files
  - Key functions/classes
  - Patterns and architecture decisions

📌 Required:
- Expand and refine `analysis_notes.md`
- Correct earlier assumptions
- Add cross-references between components

---

## Phase 3 — Third Pass (System Synthesis)

Goal: Understand the **entire system holistically**

- Connect all modules together
- Identify:
  - System architecture
  - Core workflows
  - Data lifecycle
  - Critical dependencies
- Detect inconsistencies or gaps in understanding

📌 Required:
- Clean and consolidate notes
- Remove duplication
- Ensure internal consistency

---

## Context Management Strategy (CRITICAL)

You MUST:

- Break large files into chunks
- Summarize before moving forward
- Never rely on raw code memory alone
- Continuously write and re-read notes
- Treat `analysis_notes.md` as your **external memory**

If context risk increases:
- Pause
- Summarize current state
- Then continue

---

## Iteration Discipline

For EVERY chunk:

1. Read
2. Summarize
3. Write to notes
4. Cross-check with previous notes
5. Continue

DO NOT skip writing notes.

---

## Final Deliverable (CRITICAL)

After completing all passes, generate a **final executive Markdown document**.

### File Name Format
`repo_analysis_YYYY-MM-DD_HH-MM.md`

---

## Final Document Structure

### 1. Executive Summary
- What the repository does
- Why it exists
- Key value

### 2. System Architecture
- High-level design
- Major components and how they interact

### 3. Repository Structure
- Folder-by-folder explanation
- Purpose of each major file/module

### 4. Core Workflows
- End-to-end system flows
- Key processes

### 5. Key Components
- Critical files, modules, classes, or functions

### 6. Data Flow
- How data moves through the system

### 7. Dependencies & Integrations
- External libraries, APIs, services

### 8. Observations & Risks
- Design issues
- Complexity concerns
- Potential bugs or weaknesses

### 9. Glossary
- Important terms and concepts

---

## Quality Standard

The final document MUST:

- Be clear, structured, and professional
- Reflect deep understanding (not shallow summaries)
- Be usable as a **standalone replacement for reading the codebase**
- Allow another engineer to quickly understand the system

---

## End Goal

By completion:

- The entire repository has been analyzed in multiple passes
- Context has been preserved through structured notes
- Understanding has improved iteratively
- A high-quality executive document exists

This document should eliminate the need to manually read the entire repository again.
