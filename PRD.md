# PRD: Research Paper Assistant

## Overview
A personalized AI assistant that answers research questions by searching and reading papers in the local `papers/` folder. The assistant learns the user's preferences (answer style, focus areas, formatting) over time and applies them without being told twice.

Designed for a researcher in electrochemical energy storage / 3D printing for batteries.

---

## Task 1: Paper Selection (Select primitive)
- Implemented: true
- Test Passed: true
- Goal: Given a research question, identify the 3–5 most relevant papers from `papers/` without reading all full texts
- Inputs: User query string; list of PDFs in `papers/`
- Outputs: List of selected PDF filenames
- Specification 1: Extract only the first page (title + abstract) of each PDF to assess relevance
- Specification 2: Select based on keyword and topic match to the query
- Specification 3: Never read more than 5 full papers per query (performance constraint)
- Test Case: Query "what techniques exist for 3D printing battery electrodes?" → should select Cheng2019, Mottaghi2024, Egorov2020, and at least one experimental paper
- Evaluation Criteria: Selected papers are topically relevant to the query; no obviously irrelevant papers included

## Task 2: Parallel Paper Reading (Isolate primitive)
- Implemented: true
- Test Passed: true
- Goal: Spawn one sub-agent per selected paper to extract a focused summary answering the query
- Inputs: Selected PDF filenames; user query
- Outputs: Per-paper summaries (3–5 sentences each)
- Specification 1: Each sub-agent reads the full paper text and summarizes only what is relevant to the query
- Specification 2: Sub-agents run in parallel (spawned via Task tool simultaneously)
- Specification 3: Each sub-agent returns its summary to the lead agent
- Test Case: 3 selected papers → 3 sub-agents spawn simultaneously → 3 summaries returned
- Evaluation Criteria: Summaries are query-focused, not generic paper abstracts

## Task 3: Synthesis (Isolate primitive — synthesis sub-agent)
- Implemented: true
- Test Passed: true
- Goal: Combine per-paper summaries into a coherent final answer
- Inputs: All paper summaries; user query; preferences.md
- Outputs: Final answer as narrative paragraphs
- Specification 1: Synthesis sub-agent reads preferences.md before writing
- Specification 2: Output is narrative (no bullets), cites papers inline, uses LaTeX for equations
- Specification 3: Ends with "Papers consulted: <list>"
- Test Case: Query about DIW electrode performance → answer synthesizes findings from 3+ papers into coherent narrative
- Evaluation Criteria: Answer is coherent, cites sources, applies user preferences

## Task 4: Preference Learning (Write primitive)
- Implemented: true
- Test Passed: true
- Goal: After each query, ask for feedback and persist it to preferences.md; log query to history.md
- Inputs: User feedback (optional); query text; answer summary
- Outputs: Updated preferences.md; updated history.md
- Specification 1: Append feedback to preferences.md under "Feedback History" with date
- Specification 2: Append query + one-line summary to history.md
- Specification 3: On next run, read preferences.md and apply feedback without user repeating it
- Test Case: User says "be more concise" → preferences.md updated → next answer is shorter
- Evaluation Criteria: Feedback persists across sessions; behavior changes accordingly
