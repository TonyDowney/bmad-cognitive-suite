# Agent Commands and Capabilities: Reading Lens Guide

## Core Capability

Examines the material in context, generates an organic lens (perspective), provides a brief hook to capture attention, and points to a specific passage with the shortest cognitive distance (ideally a link) plus scope signal.

## Command Structure

### Command: `lens`

**Trigger:** `lens`

**Description:** Surface a targeted reading invitation for the current material

**Action:** Self-contained prompt (no external workflow needed)

### Prompt Content

```yaml
- id: lens
  content: |
    <instructions>
    Examine the material in context. Surface a targeted reading invitation
    that gets the user back into the source material.
    </instructions>

    <process>
    1. Identify the most relevant passage for the user's current work
    2. Generate an organic lens (perspective/role) that fits the material
    3. Craft a one-line hook to capture attention
    4. Provide the shortest cognitive distance to the passage (link if possible)
    5. Signal scope so the user knows what they're committing to
    </process>

    <output_structure>
    **Lens:** [perspective to adopt - role-based, organic to the material]
    **Hook:** [one-line teaser to capture interest]
    **Read:** [link or path to passage] (~X lines/paragraphs)
    </output_structure>

    <rules>
    - Point, don't summarize - the moment you excerpt, they won't open the file
    - Link if possible; otherwise shortest cognitive path (file:line, page+section, anchor)
    - Lenses are organic - surface the perspective that fits, don't prescribe
    - Scope signals are mandatory - "read the PRD" fails, "read lines 45-52" succeeds
    - One lens per invocation - focused, not overwhelming
    - This is a provocation, not a demand - user can ignore
    </rules>
```

### Menu Entry

```yaml
menu:
  - trigger: lens
    action: "#lens"
    description: "Surface a targeted reading invitation"
```

## Implementation Notes

- **Agent Type:** Simple Agent (stateless, self-contained)
- **No workflow integration needed** - single prompt execution
- **Adapts to material type** - code files get line numbers, PDFs get page+section, URLs get anchors
- **Consistent with Cognitive Suite pattern** - single command, focused purpose

## Output Examples

**For code review:**
```
**Lens:** As the maintainer of this module
**Hook:** The error handling here swallows context that callers need
**Read:** [src/utils/api.ts:142-158](file://...) (~16 lines)
```

**For document analysis:**
```
**Lens:** A skeptic evaluating the methodology
**Hook:** The sample size assumption drives the entire conclusion
**Read:** Section 3.2, paragraph 3 (~4 paragraphs)
```

**For PR review:**
```
**Lens:** As someone who will debug this at 2am
**Hook:** This retry logic has no backoff
**Read:** [changes in retry.go, lines 45-67](link) (~22 lines)
```
