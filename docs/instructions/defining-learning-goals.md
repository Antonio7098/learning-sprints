# AI Instructions: Defining Learning Goals with the User

## Purpose

This document guides the AI assistant through a collaborative process of defining learning goals with the user. The **Learning Goals** document serves as a master plan that connects individual sprints to the broader learning journey, ensuring coherence and progression across all sprint creation.

## When to Use This Process

- At the start of a new learning project
- When the user wants to restructure or refocus their learning
- Before creating the first sprint in a new domain

## Workflow Overview

```
1. Elicit Project Vision     →  2. Define Learning Objectives  →  3. Map Concepts
4. Create Sprint Roadmap     →  5. Document & Confirm          →  6. Begin Sprint 1
```

---

## Step 1: Elicit the Project Vision

### Objective

Help the user articulate what they want to build and why it matters for their learning.

### Agent Prompts

**Opening:**
> "Before we start creating sprints, let's define our learning goals together. This will give us a roadmap for the entire project and ensure every sprint connects to a bigger picture. I'll ask you a few questions to help shape our plan."

**Questions to Ask:**

1. "What do you want to build? Describe the application or system in simple terms."
2. "Why did you choose this project? What are you hoping to learn?"
3. "Who will use this project, and what problem does it solve for them?"

### Capture Output

Document the vision in the **Project Vision** section of `learning-goals-template.md`.

**Example:**
> "We are building a REST API for tracking job applications. This will teach us backend development, database design, and API best practices while creating a useful tool for job seekers."

---

## Step 2: Define Learning Objectives

### Objective

Identify the specific, measurable skills the user will gain.

### Agent Prompts

**Questions to Ask:**

1. "What is the ONE most important skill you want to develop through this project?"
2. "What secondary skills would complement that primary skill?"
3. "Think about a developer who 'gets' this topic. What can they do that you want to learn?"

### Help User Refine

- **Primary skills** should be specific and demonstrable (e.g., "Building RESTful APIs" not just "learning APIs")
- **Secondary skills** should emerge naturally from the primary focus
- Avoid listing too many skills - focus on depth over breadth

### Capture Output

Document in **Learning Objectives** section.

**Example:**
- **Primary:** Building RESTful APIs with ASP.NET Core
- **Secondary:** Designing relational databases, Writing integration tests

---

## Step 3: Map Core Concepts

### Objective

Break down the learning objectives into specific concepts that must be mastered.

### Agent Prompts

**Questions to Ask:**

1. "What specific topics or concepts do you need to understand to achieve your primary skill?"
2. "Are there any foundational topics someone would need first?"
3. "What concepts build on each other? Which ones are more advanced?"

### Help User Order Concepts

Guide the user to think about prerequisites and logical progression:

- **Foundation:** Concepts that enable everything else
- **Intermediate:** Concepts that build on foundations
- **Advanced:** Concepts that require solid understanding of earlier topics

### Capture Output

Document in **Concepts to Master** section (ordered list).

**Example:**
1. Project scaffolding and domain modeling
2. API layer and dependency injection
3. Data transfer objects and validation
4. Entity Framework and migrations
5. Unit and integration testing
6. CI/CD and deployment

---

## Step 4: Create the Sprint Roadmap

### Objective

Map specific concepts to individual sprints with clear goals and guiding questions.

### Agent Prompts

**Process:**

For each concept in the "Concepts to Master" list:

1. "For **[Concept X]**, what should someone be able to DO by the end of the sprint?"
2. "What are 1-2 key questions someone should be able to answer after learning this?"

### Create Sprint Entries

Each sprint in the roadmap should include:

- **Focus Area:** The concept name
- **Primary Goal:** A clear, measurable outcome
- **Key Questions:** 2-3 questions that guide the learning

### Capture Output

Document in **Learning Roadmap** table.

**Example:**

| Sprint | Focus Area | Primary Goal | Key Questions |
| 1 | Domain Modeling | Define domain models with correct relationships | What makes a good domain model? How do we represent relationships? |
| 2 | Minimal APIs | Build basic CRUD endpoints | How do HTTP verbs map to operations? What is routing? |
| 3 | DTOs & Validation | Create clean API contracts | Why use DTOs? How do we validate input? |

---

## Step 5: Document and Confirm

### Objective

Review everything with the user and confirm accuracy.

### Agent Prompts

**Review Script:**

> "Let's review what we've planned. This will be our guide for the entire project."

**Read back each section:**
1. Project Vision - "Does this capture what you want to build?"
2. Learning Objectives - "Are these the skills you want to develop?"
3. Concepts to Master - "Is this the right sequence? Any concepts missing?"
4. Roadmap - "Do these sprints make sense? Are the goals achievable?"

**Final Confirmation:**

> "Once we start sprinting, we'll follow this roadmap. As you learn, we may adjust - some concepts might take longer, others might reveal new areas to explore. Does this plan feel right to begin?"

---

## Step 6: Begin Sprint 1

### Objective

Transition from planning to execution.

### Agent Prompts

**Transition:**

> "Our learning goals are set. Now let's create Sprint 1 based on our roadmap. This sprint will focus on **[Concept 1 from the roadmap]**."

**Next Actions:**
1. Create the first sprint file using `sprint-learning-template.md`
2. Use the roadmap entry for Sprint 1 as the foundation
3. Consult `creating-a-sprint.md` for the detailed sprint creation protocol

---

## How This Document Evolves

### Initial State

The learning goals document starts as a **plan** - what we intend to learn and in what order.

### During the Project

The document becomes a **living record**:

- **After each sprint:** Update with insights, completed concepts, and any adjustments
- **When concepts change:** Note why the roadmap shifted
- **For reflection:** Add notes about what worked, what didn't

### Final State

At project completion, the document becomes a **retrospective** - documenting the complete learning journey.

---

## Quick Reference: Section Purpose

| Section | Purpose | When to Update |
| :--- | :--- | :--- |
| **Project Vision** | Keep focus on the bigger picture | Rarely - the vision rarely changes |
| **Learning Objectives** | Track primary and secondary skills | At midpoint review |
| **Concepts to Master** | Ordered list of topics to learn | When roadmap changes |
| **Success Criteria** | How we know we've succeeded | At midpoint and final review |
| **Learning Roadmap** | Sprint-by-sprint plan | At each sprint creation |
| **Required Tools** | What the user needs | Initial setup only |
| **Personal Notes** | Reflections and insights | Throughout the journey |
| **Review Schedule** | When to reflect and adjust | At each checkpoint |
