# Agent Purpose and Type: Lateral Thinker

## Core Purpose

Break the AI out of statistical convergence. When AI generates solutions, it naturally converges on consensus - the statistically most likely answers. This creates a "hive mind" effect where everyone using AI gets the same ideas.

Lateral Thinker surfaces **unconventional-but-viable alternatives** with creative justification for why the road less traveled might matter.

## The Problem This Solves

Sarkar's research identifies creativity narrowing as a key risk of AI-assisted work:

> "Numerous studies have shown that on a collective level, knowledge workers using AI assistants produce a smaller range of ideas than a group working manually. We've created a hive mind. Except the hive is really boring and keeps suggesting the same five ideas."

This agent directly combats that by forcing the AI to reject its statistical defaults.

## What It Does

- Generates concrete atypical alternatives (not blue sky, not refinements)
- Provides creative justification for unconventional approaches
- Uses cross-domain analogies where helpful (AI decides when/which domains)
- Fires during exploration, before decisions solidify

## What Makes It Unique

Unlike other Cognitive Suite agents that prompt the *user* to think differently, Lateral Thinker is where the *AI itself generates divergent content*. It's actively fighting its own statistical tendencies.

| Other Agents | Lateral Thinker |
|--------------|-----------------|
| Provoke user thinking | AI generates alternatives |
| Work within your frame | Break the frame |
| Critique/question | Expand solution space |
| Adversarial (find flaws) | Divergent (find other paths) |

## Target Users

- Developers exploring architecture decisions
- Product managers evaluating approaches
- Anyone at risk of accepting the first "good enough" AI suggestion
- Teams wanting to avoid convergent thinking

## Chosen Agent Type

**Simple Agent**

### Rationale

- Stateless - each invocation is independent
- No persistent memory needed
- No sidecar files required
- Consistent with other Cognitive Suite agents (Devil's Advocate, Socratic Challenger, etc.)
- Distributable without per-project state

## Output Path

Standalone Simple Agent: `src/agents/lateral-thinker.agent.yaml`

## Sarkar Alignment

This agent implements Sarkar's "Creativity Preservation" principle - actively working against the hive mind effect by surfacing alternatives the AI wouldn't naturally prioritize.
