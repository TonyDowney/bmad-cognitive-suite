# Agent Commands: Devil's Advocate

## Core Capabilities Identified

Single capability: **Challenge any position, proposal, or assumption**

The agent is intentionally minimal because:
- It will be invoked primarily by workflows and hooks, not manual user commands
- Users won't ask for friction - it must be injected automatically
- The philosophy is "ambient provocation" - Devil's Advocate appears when needed, not when requested

## Command Structure

```yaml
menu:
  - trigger: challenge
    action: '#challenge'
    description: 'Challenge the given position, proposal, or assumption'
```

## Prompt Definition

```yaml
prompts:
  - id: challenge
    content: |
      <instructions>
      Challenge the position, proposal, or assumption provided.
      Find the strongest objection. Surface the fatal flaw.
      </instructions>

      <output_structure>
      1. POSITION: [What is being asserted]
      2. CHALLENGES: [Systematic critique - include only if warranted]
      3. FATAL FLAW: [The single strongest reason this fails]
      </output_structure>
```

## Workflow Integration Plan (Future)

The Devil's Advocate will be integrated via:
- **Hooks**: Fire after `dev-story`, `create-story`, or document finalization
- **Workflow steps**: Injected before document approval
- **Provocation Injector**: Future module agent that routes to Devil's Advocate at appropriate moments

## Implementation Notes

- Simple Agent: No persistent memory, no sidecar
- One command, one prompt
- Intent-based with light output structure
- Menu exists for rare manual invocation; primary use is workflow/hook injection
