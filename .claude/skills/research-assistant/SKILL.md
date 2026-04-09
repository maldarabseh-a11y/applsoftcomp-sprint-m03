---
name: research-assistant
description: Personalized research assistant for electrochemical energy storage papers. Answers research questions by searching local papers, reading relevant PDFs, and synthesizing answers. Learns and applies user preferences over time.
---

# Research Assistant

Answer research questions by reading papers in the `papers/` folder. Learn and apply the user's preferences after each session.

## Primitives

- **Write**: persist user preferences and query history to `research-assistant/preferences.md` and `research-assistant/history.md`
- **Select**: identify which papers are relevant to the query before reading (don't read all papers every time)
- **Isolate**: spawn one sub-agent per relevant paper to extract and summarize; spawn a separate synthesis sub-agent to combine summaries into a final answer

---

## Steps

### 1. Load preferences and history
Read `research-assistant/preferences.md` if it exists. This contains the user's preferred answer style (concise vs. detailed, focus areas, disliked patterns). Apply these in all outputs.

### 2. Select relevant papers (Lead Agent)
List all PDFs in `papers/`. For each, run:
```
uv run python .claude/skills/literature-review/tools/extract_pdf.py "papers/<filename>"
```
Read only the first page (title + abstract) to decide relevance. Select the 3–5 most relevant papers for the query. Do NOT read full papers in this step.

### 3. Spawn Reading Sub-Agents (one per selected paper, in parallel)
Each sub-agent:
1. Extracts full text: `uv run python .claude/skills/literature-review/tools/extract_pdf.py "papers/<filename>"`
2. Reads the text and writes a focused summary (3–5 sentences) answering the specific query
3. Returns the summary to the lead agent

### 4. Spawn Synthesis Sub-Agent (once, after all reading sub-agents complete)
The synthesis sub-agent:
1. Receives all paper summaries from the lead agent
2. Reads `research-assistant/preferences.md` for style guidance
3. Writes a final answer: unified narrative, no bullets, max 3 sentences/paragraph, LaTeX for equations, cites paper titles inline

### 5. Save history and collect feedback
Append the query + one-line answer summary to `research-assistant/history.md`.

Ask the user: "Anything you'd like me to do differently next time?" If they give feedback, append it to `research-assistant/preferences.md` in this format:
```
- [date] <feedback>
```

---

## Output format
- Narrative paragraphs (no bullet lists)
- Cite papers as (Author Year) inline
- Use LaTeX for equations: display mode for key ones
- Max 3 sentences per paragraph
- End with: "Papers consulted: <list of filenames used>"

## File locations
All persistent files live in `research-assistant/` relative to repo root:
- `preferences.md` — user style preferences and feedback history
- `history.md` — log of past queries and summaries

Create these files if they don't exist.
