# BMAD Cognitive Suite

A "Tools for Thought" extension module for the [BMAD Method](https://github.com/bmad-code-org/BMAD-METHOD), implementing Advait Sarkar's principles for preserving human cognition in AI-assisted workflows.

## The Problem

> "We've become intellectual tourists. In our own work, we visit ideas. We don't inhabit them. We've become middle managers for our own thoughts."
> — Advait Sarkar, TEDAI Vienna 2025

AI assistants optimize for **getting things done**—but this comes at a cost:
- **Fewer ideas**: Collective creativity narrows
- **Less critical thinking**: Effort decreases with AI confidence
- **Weaker memory**: Summaries replace understanding
- **Eroded metacognition**: We forget how to think about thinking

## The Solution

This module provides BMAD agents and workflows that **challenge rather than obey**.

Instead of AI that thinks *for* you, these tools make you *think*.

### Core Agents

| Agent | Type | Purpose |
|-------|------|---------|
| **Devil's Advocate** | Simple | Generates strongest counterarguments |
| **Socratic Challenger** | Expert | Responds only with probing questions |
| **Assumption Auditor** | Simple | Surfaces hidden premises |
| **Pre-Engagement Gate** | Simple | Blocks AI until user demonstrates prior thought |
| **Memory Anchor** | Expert | Forces articulation, creates retrieval practice |
| **Decision Journal** | Expert | Documents why decisions were made |
| **Provocation Injector** | Module | Injects challenges into any workflow |

### Design Principles

1. **Productive Resistance**: AI should challenge, not agree
2. **Material Engagement**: User reads; AI provides "lenses"
3. **Metacognition Scaffolding**: Help think about thinking
4. **Provocations over Completions**: Alternatives, not answers
5. **Ambient Integration**: Provocation woven into workflows, not standalone

## Installation

```bash
# First, install BMAD Method (required)
npx bmad-method@alpha install

# Then install Cognitive Suite
npx bmad-cognitive-suite install  # (coming soon)
```

For now, clone this repo alongside your BMAD installation:

```bash
git clone https://github.com/your-username/bmad-cognitive-suite.git
```

## Usage

These agents are designed to **compose** with existing BMM/CIS workflows, not replace them.

### Building Agents with BMAD Builder

Use the BMAD Builder to create cognitive agents:

```
/bmad:bmb:agents:bmad-builder
[CA] Create Agent

# Follow the guided process, using specs from docs/agent-specs.md
```

### Injecting Provocations

The Provocation Injector can be added to any workflow step:

```yaml
post_action:
  agent: cognitive:provocation-injector
  trigger: on_completion
```

## Documentation

- [Philosophy](docs/philosophy.md) - Sarkar's principles and our implementation
- [Agent Specs](docs/agent-specs.md) - Detailed specifications for all agents
- [Module README](.bmad/cognitive/README.md) - Technical module documentation

## Project Structure

```
bmad-cognitive-suite/
├── .bmad/
│   └── cognitive/          # The actual BMAD module
│       ├── agents/
│       ├── workflows/
│       └── composables/
├── docs/
│   ├── philosophy.md       # Theoretical foundation
│   └── agent-specs.md      # Agent specifications
├── package.json            # NPM/marketplace metadata
└── README.md               # This file
```

## Compatibility

- BMAD Method: v6.0.0-alpha and above
- Works alongside: BMM, BMB, CIS modules

## Contributing

This module is in active development. Key areas for contribution:

1. Agent implementations (see `docs/agent-specs.md`)
2. Workflow compositions
3. Cognitive metrics tracking
4. Integration patterns with BMM workflows

## Credits

- **Philosophical Foundation**: [Advait Sarkar](https://www.microsoft.com/en-us/research/people/advait/), Microsoft Research Cambridge
- **Framework**: [BMAD Method](https://github.com/bmad-code-org/BMAD-METHOD)

## License

MIT

---

> "What would you rather have? A tool that thinks for you, or a tool that makes you think?"
