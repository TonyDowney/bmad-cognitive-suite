# Agent Commands: Assumption Auditor

## Core Capabilities Identified

Single capability: **Surface hidden assumptions in any material**

The agent is intentionally minimal because:
- It will be invoked primarily by workflows and hooks, not manual user commands
- Users won't ask for friction - it must be injected automatically
- Same philosophy as Devil's Advocate and Socratic Challenger: one job, does it well

## Command Structure

```yaml
menu:
  - trigger: assumptions
    action: '#assumptions'
    description: 'Surface hidden assumptions in the given material'
```

## Prompt Definition

```yaml
prompts:
  - id: assumptions
    content: |
      <instructions>
      Surface hidden assumptions, unstated premises, and implicit requirements
      in the material provided. Do not judge whether assumptions are right or
      wrong—only make them visible.
      </instructions>

      <output_structure>
      Assumptions detected:
      1. [Assumption] — Is this intentional?
      2. [Assumption] — Is this intentional?
      ...
      </output_structure>

      <rules>
      - List assumptions concisely without judgment
      - Each assumption ends with "Is this intentional?"
      - Surface both human assumptions and AI assumptions if applicable
      - Do not fix or recommend—only surface
      </rules>
```

## Naming Convention

Trigger, action, and prompt id all use `assumptions` for consistency:
- Unique enough to avoid namespace collisions
- Self-documenting
- Matches the agent's core function

## Workflow Integration Plan (Future)

The Assumption Auditor will be integrated via:
- **Hooks**: Fire at pre-planning and pre-finalization phases
- **Workflow steps**: Injected before designs, PRDs, stories are signed off
- **Provocation Injector**: Future module agent that routes to Assumption Auditor

## Implementation Notes

- Simple Agent: No persistent memory, no sidecar
- One command, one prompt
- Light output structure (list format with "Is this intentional?")
- Menu exists for rare manual invocation; primary use is workflow/hook injection
