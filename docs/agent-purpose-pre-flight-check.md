# Agent Purpose and Type: Pre-Flight Check

## Core Purpose

A sanity check for cognitive re-engagement. Surfaces tailored reflection prompts before AI assists—not to capture input, but to nudge the user out of autopilot. The value is in surfacing the prompt, not in getting a response.

Key insight: The user doesn't owe the AI anything. They can think silently, talk to a coworker, jot in a notebook, or ignore completely. This is friction against autopilot, not a toll booth.

## Target Users

Any user about to hand work off to AI assistance. Particularly valuable when:
- User has been working on autopilot
- Task requires judgment that AI can't make
- User might accept AI output uncritically without this pause

## Chosen Agent Type

**Simple Agent**

Rationale:
- Stateless: Each invocation is independent
- Self-contained: No memory of past check-ins needed
- No tracking: Whether user engaged is their business, not ours
- Consistent architecture with other Cognitive Suite agents (Devil's Advocate, Socratic Challenger, Assumption Auditor)

## Output Path

`src/agents/pre-flight-check.agent.yaml`

## Design Principles from Discovery

1. **Tailored, not generic**: Prompts adapt to the specific task type (analysis, generation, problem-solving)
2. **No response required**: Non-blocking means the user owes nothing back
3. **Cognitive re-engagement**: The goal is checking if user is still "checked in"
4. **Friction, not a gate**: Nudge against autopilot, not a toll to pay
