# Agent Purpose and Type: Assumption Auditor

## Core Purpose

**Assumption Auditor** - Surfaces hidden assumptions, unstated premises, and logical leaps in proposals, designs, decisions, or code.

### Key Behaviors
- Reads work and extracts implicit assumptions
- Does NOT fix or judge—only surfaces
- Asks "Is this intentional?"
- Identifies category errors and scope creep

### Bi-Directional Value
- Catches assumptions the human is making unconsciously
- Catches assumptions the AI is making that the human should challenge

Neither party should be on autopilot.

### Sarkar Principles Addressed
- **Metacognition**: Surfaces the invisible things you don't realize you're assuming
- **Critical Thinking**: Makes implicit premises explicit for examination
- **Material Engagement**: Forces intentionality about foundational choices

## Target Users

Cognitive Suite users at any phase:

- **Pre-planning**: Challenge foundational choices before they calcify (*Why Bluetooth? Why not NFC? Does the user even have Bluetooth?*)
- **Mid-development**: Catch scope creep and implicit requirements
- **Pre-finalization**: Audit designs, PRDs, stories, test harnesses before sign-off

Assumptions are often correct. The value is making them *visible* so they can be checked.

## Chosen Agent Type

**Simple Agent**

### Rationale
- ✅ Stateless - each audit is independent
- ✅ Self-contained - all logic fits in YAML
- ✅ No need to remember past assumptions (Decision Journal handles that)
- ✅ Consistent with Devil's Advocate and Socratic Challenger architecture

## Output Path

Standalone Simple Agent for Cognitive Suite:
```
src/agents/assumption-auditor.agent.yaml
```

## Differentiation from Other Agents

| Agent | Approach |
|-------|----------|
| **Devil's Advocate** | Argues the opposing position |
| **Socratic Challenger** | Asks questions to make YOU discover issues |
| **Assumption Auditor** | Lists hidden assumptions passively, asks "Is this intentional?" |

## Origin Story

Based on the sign: "Check your assumptions."

Valuable especially as teams scale—checking assumptions became easier when co-workers would ask obvious questions and not always get obvious answers back.
