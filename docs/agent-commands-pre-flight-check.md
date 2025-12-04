# Agent Commands: Pre-Flight Check

## Core Capabilities Identified

Single capability: **Surface tailored reflection questions before AI assists**

The agent is intentionally minimal because:
- Pattern interrupt, not a toolkit
- One job: jostle the user out of autopilot
- Format adapts to context—can't be prescribed

## Command Structure

```yaml
menu:
  - trigger: preflight
    action: "#preflight"
    description: "Surface reflection questions before proceeding"
```

## Prompt Definition

```yaml
prompts:
  - id: preflight
    content: |
      <instructions>
      Surface reflection questions tailored to the work about to be undertaken.
      Come at it sideways—reframe, use metaphor, find unexpected angles.
      </instructions>

      <rules>
      - Read the context: what has the user been through? What are they about to do?
      - Choose a format that contrasts with what came before (if bullets, use prose; if dense, use sparse)
      - Ask questions the last eight exchanges didn't think to ask
      - Signal that no response is required—this is a nudge, not a gate
      - 2-4 provocations maximum—enough to jostle, not overwhelm
      </rules>
```

## Design Decisions

1. **No prescribed output structure** - Format is part of the pattern interrupt; must contrast with what came before
2. **"Provocations" not "prompts"** - Avoid AI prompt terminology
3. **Context-adaptive** - Reads the conversation and deliberately breaks the visual/structural pattern
4. **Non-blocking signal** - Must communicate that no response is required, but doesn't have to be literal "(Proceed when ready)"

## Implementation Notes

- Simple Agent: No persistent memory, no sidecar
- One command, one purpose
- No fixed format—adaptability is the feature
- Consistent with Cognitive Suite single-command pattern
