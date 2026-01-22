# Learning Sprints Framework

A structured, mentor-guided approach to learning programming concepts and skills. This framework provides templates and workflows for creating personalized learning sprints that emphasize deep understanding over surface-level completion.

## Overview

The Learning Sprints Framework is designed to:

- **Foster deep understanding** through guided investigation rather than passive tutorials
- **Promote active learning** where users write code and formulate answers themselves
- **Provide personalized feedback** through AI-assisted marking and question generation
- **Build professional habits** including documentation, version control, and code review

## Key Components

### Sprint Templates

Each sprint follows a consistent structure:

1. **Sprint Details & Goals** - Clear, measurable learning objectives
2. **Task List** - Step-by-step guidance with investigation prompts
3. **Understanding & Synthesis Questions** - Questions progressing from basic reinforcement to advanced stretch
4. **AI Marking & Feedback** - Personalized review and guidance

### Workflows

The framework supports six core workflows:

0. **Project Initialization** - Collaboratively define learning goals and create a roadmap
1. **Sprint Creation** - AI generates a new sprint based on project needs
2. **Sprint Walkthrough** - Interactive, step-by-step guidance through tasks
3. **Code Marking** - Review and feedback on implemented solutions
4. **Q&A Marking** - Evaluation and elaboration on conceptual answers
5. **Personalization** - Dynamic generation of new questions based on performance

## File Structure

```
learning-sprints/
├── AGENTS.md                           # AI operational context (read this first)
├── README.md                           # This file
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
```

## Getting Started

### For AI Assistants

1. Read `AGENTS.md` to understand your role and workflows
2. For new projects, use `docs/instructions/defining-learning-goals.md` to create `docs/learning-goals.md`
3. Consult `docs/learning-goals.md` to understand the project context and roadmap
4. Use `docs/templates/sprint-learning-template.md` when creating new sprints
5. Follow `docs/instructions/` for specific workflow guidance

### For Users

1. **Start here:** Ask your AI assistant to "help me set up learning goals for a [project type]"
2. **Review goals:** Your AI will guide you through defining your project vision and roadmap
3. **Begin sprinting:** Request to "start Sprint 1" once goals are set
4. **Submit work:** Ask for marking when you complete tasks or questions
5. **Iterate:** Review feedback and continue to the next sprint

## Question Progression

Every sprint contains an **Understanding & Synthesis Questions** section with questions ordered from basic to advanced:

### Reinforcing Questions (Foundation)
- Focus on recall, definition, and direct application
- Verify basic comprehension of concepts
- Example: "What is the difference between X and Y?"

### Stretch & Synthesis Questions (Advanced)
- Require synthesis, exploring trade-offs, and connecting concepts
- Push beyond basic understanding
- Example: "What are the trade-offs of X compared to Y? How do they relate to Z?"

## Customization

This framework is designed to be:

- **Language-Agnostic** - Works with any programming language
- **Framework-Agnostic** - Applicable to any technology stack
- **Domain-Agnostic** - Suitable for any programming domain

### Adapting for Different Languages

- Replace language-specific terminology with the target language's equivalent
- Adjust package management commands to the target ecosystem
- Modify database examples for the target database system

### Adapting for Different Domains

- **Web Development:** Emphasize HTTP, REST APIs, authentication, deployment
- **Data Science:** Focus on statistical concepts, data pipelines, model evaluation
- **Embedded Systems:** Cover hardware constraints, real-time requirements, memory management

## Core Principles

### The "Why" Before the "How"

Every sprint should compel the user to understand the reasoning behind concepts, not just the implementation.

### Investigation Over Instruction

Tasks should guide users to discover answers themselves through structured investigation, not provide direct solutions.

### Progressive Depth

Questions start with reinforcing basics and progress to stretch and synthesis, building understanding incrementally.

### Professional Practices

Every sprint includes documentation, version control, and code quality tasks to build professional habits.

## Example Sprint Flow

1. **AI creates learning goals** based on user's project vision and preferences
2. **User reviews** the learning goals document and confirms the roadmap
3. **AI creates sprint** based on roadmap, reading previous sprints for context
4. **User reads sprint** and requests to "begin walkthrough"
5. **AI guides** through each task, explaining concepts and prompting investigation
6. **User implements** code and answers questions (reinforcing first, then stretch)
7. **AI reviews** work and fills out marking section
8. **AI generates** personalized follow-up questions (reinforcing for gaps, stretch for interests)
9. **User completes** sprint and moves to the next concept

## References

- `AGENTS.md` - Complete AI operational context
- `docs/templates/learning-goals-template.md` - Master planning template
- `docs/templates/sprint-learning-template.md` - Sprint template
