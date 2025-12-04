# BMAD Cognitive Suite

**Version 0.1.0**

AI agents that challenge you to think, not think for you.

## Installation

**Requires:** [BMAD Method v6](https://github.com/bmadcode/bmad-method)

```bash
# 1. Ensure BMAD v6 is installed in your project
npx bmad-method

# 2. Install Cognitive Suite (coming soon - for now, copy src/ contents)
# npx bmad-cognitive-suite

# 3. Activate cognitive mode at session start
/bmad:cognitive:tasks:init
```

Run `/bmad:cognitive:tasks:init` at any time to enter cognitive mode.

## What This Is

Six AI agents implementing Advait Sarkar's "productive resistance" principle from his TED talk [How to Stop AI from Killing Your Critical Thinking](https://www.ted.com/talks/advait_sarkar_how_to_stop_ai_from_killing_your_critical_thinking).

The core idea: AI should preserve your role as the primary thinker. These agents add friction—not to slow you down, but to keep you engaged.

| Agent | Name | Purpose |
|-------|------|---------|
| Devil's Advocate | Lucy | Surfaces strongest counterarguments |
| Socratic Challenger | Sora | Responds only with probing questions |
| Assumption Auditor | Vera | Surfaces hidden assumptions |
| Pre-Flight Check | Jett | Pattern interrupt before major work |
| Reading Lens Guide | Lenny | Points to source material (lenses, not summaries) |
| Lateral Thinker | Ziggy | Surfaces unconventional alternatives |

## How It Works

After running `/bmad:cognitive:tasks:init`, agents surface provocations during your BMAD workflows:

- Brief, non-blocking observations or questions
- You can ignore any that don't resonate
- The value is in what they surface, not in answering them

The system monitors engagement signals and adapts frequency—more provocations during strategic work, fewer during mechanical execution.

## Philosophy

> "The goal is not to make AI maximally helpful, but to preserve the human's role as the primary thinker."
> — Advait Sarkar

Sarkar's research shows AI-assisted work has 40% lower recall and comprehension. When we defer to AI, we become "intellectual tourists"—visiting ideas but never truly inhabiting them.

These agents implement his concept of "provocations": short commentary, critiques, and questions that stimulate critical thinking without blocking workflow.

**Design principles:**
- Friction is the feature, not the bug
- Non-blocking: user can always ignore
- Light mental burden: suggestions to ignore, not homework
- Never apologize for making you think

## Status

Work in progress. Currently tested for personal use with Claude Code and BMAD v6.

## Credits

Based on [Advait Sarkar](https://advait.org/)'s "Tools for Thought" research at Microsoft Research, presented at TEDAI Vienna 2025.

Built with [BMAD Method](https://github.com/bmadcode/bmad-method).
