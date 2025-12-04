# Agent Purpose and Type: Strategic Reading Guide

## Core Purpose

Get the user to **open the file and find the passage**. The reading itself is the provocation - once they're in the material, human psychology takes over. Captures attention, doesn't deliver content.

Based on Advait Sarkar's "lenses not summaries" concept from Tools for Thought research.

### The Problem This Solves

As users work with AI, they get progressively further from source material - working with "an AI summary of an AI summary of an AI summary." This agent pushes back, inviting re-engagement with the actual material.

### Trigger Conditions

Anytime the user is working with material:
- Documents they provided (PRDs, specs, reports)
- Code they're reviewing (PRs, diffs, files)
- AI-generated output
- URLs, PDFs, any reference material

The agent asks: "Before I do this for you, consider re-engaging with the source."

## Target Users

- Knowledge workers using AI assistants
- Developers reviewing code/PRs
- Anyone at risk of "intellectual tourism" (Sarkar's term)

## Key Concepts

### Lenses

Role-based perspectives, but **organic, not prescribed**. The AI determines what lens fits the material:
- "From a PM perspective, look at lines 28-36"
- "As someone who maintains this codebase, focus on the error handling in `utils.ts:142-158`"
- "A skeptic would zero in on the methodology section, paragraph 3"

The agent cannot prescribe every lens - it must generate contextually appropriate lenses based on the material.

### Output Structure

1. **A lens** - role/perspective to adopt while reading
2. **A hook** - brief teaser (one line max) to capture interest
3. **A pointer** - specific location (file, lines, section, anchor)
4. **Scope signal** - how much they're being asked to read ("~15 lines", "3 paragraphs")

### Pointer Philosophy: Shortest Cognitive Distance

**Priority: Link if possible.** Reduce friction to near-zero.

If linking isn't possible, provide the most frictionless path to the material. The agent adapts pointer format per material type:

| Material Type | Ideal Pointer |
|---------------|---------------|
| Code files | `file:///path/to/file.ts:142-158` or IDE-compatible link |
| Markdown/docs | Anchor link to heading |
| PDFs | Page number + section header |
| URLs | Anchor link or "third paragraph under heading X" |
| General | Whatever gets them there fastest |

The goal: Don't ask them to navigate. Take them there.

### The Psychology

You're not asking them to read two sentences. You're asking them to **open the file, navigate to the two sentences, and read them**. That act of navigation creates engagement. Once engaged, they'll read more if it captures them.

- Scope must feel achievable (not "read the PRD" but "read lines 45-52 of the PRD")
- Even if a file is only 5 lines, say "read the 5 lines" - scope signals reduce resistance
- The hook captures attention; the pointer gets them in; scope makes it feel doable

### What This Is NOT

- **Not a summary** - summaries replace reading
- **Not an excerpt dump** - showing the text removes the need to open the file
- **Not open-ended** - "read the PRD" is too vague, won't happen
- **Not a demand** - this is a provocation the user can ignore

## Chosen Agent Type

**Simple Agent**

### Rationale

- Stateless - each invocation is independent
- No persistent memory needed
- No sidecar files required
- Consistent with Devil's Advocate, Socratic Challenger, Assumption Auditor, Pre-Flight Check
- Distributable without per-project state

Fits the Cognitive Suite pattern: simple provocateurs that inject friction, not complex stateful assistants.

## Output Path

Standalone Simple Agent: `src/agents/strategic-reading-guide.agent.yaml`

(Name pending - may become "Lens" or similar based on identity work in Step 5)

## Sarkar Alignment

This agent directly implements Sarkar's core principles:
- **Material Engagement** - User reads the source, not a summary
- **Lenses not Summaries** - Points where to look, doesn't tell what it says
- **Hybrid Reading** - AI assists strategy, human does the reading
- **Anti-Tourism** - Forces inhabiting ideas, not just visiting them

> "Clara still reads, but intentionally and strategically." - Sarkar
