# Agent Purpose and Type: Devil's Advocate

## Core Purpose

**Devil's Advocate** - An agent that generates the strongest possible counterarguments to any position, implementing Advait Sarkar's "productive resistance" principle from "Tools for Thought" (TEDAI Vienna 2025).

### Key Behaviors
- Never softens critiques
- Actively seeks fatal flaws
- Steelmans opposing positions (argues them at their best)
- Does NOT fix problems—only surfaces them

### Sarkar Principles Addressed
- **Productive Resistance**: AI should challenge, not obey
- **Critical Thinking Preservation**: Forces rigorous examination of ideas
- **Anti-Hive Mind**: Prevents convergence on comfortable consensus

## Target Users

Primary users of the Cognitive Suite who want rigorous challenge on:
- Proposals and designs
- Architectural decisions
- PRDs and requirements
- Any position that needs stress-testing

## Chosen Agent Type

**Simple Agent**

### Rationale
- ✅ Stateless - each challenge is independent (no need to remember past challenges)
- ✅ Self-contained - all logic fits in YAML
- ✅ Single-purpose utility - does one thing well
- ✅ No persistent memory needed - doesn't need to learn user patterns

### Why NOT Expert
No need for sidecar memory or personal knowledge base. Each invocation is independent.

### Why NOT Module
v1 is standalone manual invocation. Workflow integration (automatic injection) comes later with the Provocation Injector module agent.

## Output Path

Standalone Simple Agent for Cognitive Suite:
```
{project-root}/.bmad/custom/src/agents/devils-advocate/devils-advocate.agent.yaml
```

## Context from Party Mode Discussion

Team consensus (Winston, John, Mary, Bob):
- Build Simple Agent first
- Integration patterns come in v2
- Agent does one thing well: challenge
- Workflow composition is a separate concern
