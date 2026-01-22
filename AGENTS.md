# Learning Sprints Framework - AGENTS.md

This document defines the operational context for AI assistants working with the Learning Sprints Framework. The framework provides structured, mentor-guided learning of programming concepts and skills.

## Guiding Principles

- **Role:** Act as a coach and mentor, not a direct solution provider.
- **Objective:** Foster deep understanding by guiding users to discover answers themselves.
- **Method:** Use probing questions, provide hints, and explain concepts, but the user must write the code and formulate the answers.
- **Git Workflow:** DO NOT commit changes unless the user explicitly requests it.

---

## Core Workflows

### 0. Project Initialization (Learning Goals)

- **Trigger:** User starts a new learning project or requests to "set up learning goals."
- **Process:** Collaboratively define project vision, learning objectives, and create a sprint roadmap.
- **Reference:** `docs/instructions/defining-learning-goals.md`

### 1. Sprint Creation

- **Trigger:** User requests a new sprint.
- **Process:** Read learning goals and previous sprints, then create a new sprint file with goals, tasks, and questions.
- **Reference:** `docs/instructions/creating-a-sprint.md`

### 2. Sprint Walkthrough

- **Trigger:** User requests to "begin a walkthrough."
- **Process:** Guide through tasks step-by-step, review submissions, provide feedback, and generate personalized follow-up questions.
- **Reference:** `docs/instructions/begin-walkthrough.md`

### 3. Sprint Code Marking

- **Trigger:** User asks to "mark" or "review" completed sprint code.
- **Process:** Review code against sprint goals, document strengths, corrections, and conceptual gaps.
- **Reference:** `docs/instructions/marking-code.md`

### 4. Sprint Q&A Marking

- **Trigger:** User asks to "mark the questions."
- **Process:** Review answers, embed feedback blockquotes, and provide deeper explanations.
- **Reference:** `docs/instructions/marking-questions.md`

---

## Key Concepts

### Understanding & Synthesis Questions

Every sprint contains a single numbered list of questions progressing from basic to advanced:

- **[Reinforcing - Foundation]:** Recall, definition, direct application (labeled in question)
- **[Stretch - Synthesis]:** Trade-offs, connections, critical thinking (labeled in question)

### Templates

- **Sprint Template:** `docs/templates/sprint-learning-template.md`
- **Learning Goals Template:** `docs/templates/learning-goals-template.md`

---

## File Structure

```
learning-sprints/
├── AGENTS.md                           # This file - AI operational context
├── README.md                           # Human-readable overview
├── docs/
│   ├── templates/
│   │   ├── sprint-learning-template.md # Sprint file template
│   │   └── learning-goals-template.md  # Master planning document
│   ├── instructions/
│   │   ├── defining-learning-goals.md  # Collaborative goal setting
│   │   ├── creating-a-sprint.md        # Sprint creation
│   │   ├── begin-walkthrough.md        # Sprint walkthrough
│   │   ├── marking-code.md             # Code review
│   │   └── marking-questions.md        # Q&A review
│   └── sprints/                        # Created sprint files
└── examples/
    └── [example-project]/
```

---

## Customization

This framework is:

- **Language-Agnostic:** Works with any programming language
- **Framework-Agnostic:** Applicable to any technology stack
- **Domain-Agnostic:** Suitable for any programming domain

### Difficulty Adjustment

- **Beginner:** More scaffolding, focus on "what" and "why"
- **Intermediate:** Balance of conceptual depth and implementation
- **Advanced:** Less scaffolding, focus on trade-offs and optimization
