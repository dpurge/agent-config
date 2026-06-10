---
name: start-project
description: Start in empty directory, create new project structure.
---

If the current directory is not empty, do nothing.

If the current directory is empty, perform these steps in order:

1. initialize git repository
2. create AGENTS.md file
3. create GitHub Spec-Driven Development structure

## Initialize git repository

TODO

## Create AGENTS.md file

TODO

## Create GitHub Spec-Driven Development structure

```sh
specify init --here --ai claude
specify check
```

```txt
project-name/
├── .speckit/
│   ├── constitution.md      # Project principles
│   ├── features/
│   │   └── 001-feature-name/
│   │       ├── specify.md    # Requirements
│   │       ├── plan.md       # Technical plan
│   │       ├── tasks.md      # Task breakdown
│   │       └── checklist.md  # Quality gates
│   └── .claude/
│       └── commands/         # Slash commands
└── [application code]
```

Each feature gets its own directory with three files:

- *spec.md*: What the feature does (requirements, acceptance criteria)
- *plans.md*: How to build it (architecture decisions, implementation order)
- *tasks.md*: Granular checklist that hydrates into Claude Tasks

