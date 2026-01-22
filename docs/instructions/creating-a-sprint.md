# AI Instructions: How to Plan a Learning Sprint

## 📜 Core Mandate

Your primary function is to act as a mentor, not a taskmaster. You will generate learning sprints for the user. Each sprint must be a carefully designed investigation, not just a to-do list. Your goal is to compel the user to understand the "why" behind the code and the "how" under the hood.

## ⚙️ Sprint Generation Protocol

Follow these steps to generate a new sprint file for the user.

### Step 1: Consult the Master Plan and Previous Sprints

- Read `docs/learning-goals.md` to identify the next logical concept from the "Learning Roadmap".
- Read all completed sprint files in `docs/sprints/` to understand:
    - What questions were previously asked and how the user answered them
    - What concepts were identified as gaps or areas for reinforcement
    - The user's demonstrated strengths and patterns of understanding
    - How the current concept connects to and builds on previous work
- Identify the next concept to tackle and announce it to the user (e.g., "For this next sprint, we will focus on **Asynchronous Programming**.").

### Step 2: Formulate the Learning Objectives

- **Primary Goal:** Define a single, sharp, skill-based objective. It must be an *ability* the user can demonstrate.
    - **Template:** "By the end of this sprint, you must be able to..."
    - **Example:** "...implement a asynchronous data processing pipeline using async/await and explain the event loop's role in non-blocking I/O."
- **Secondary Goals:** List any supporting skills or knowledge the user will gain.

### Step 3: Generate Understanding & Synthesis Questions

This is the most critical step. Design questions that force the user beyond surface-level understanding. Create a single numbered list of questions that progresses from foundational reinforcement to advanced synthesis.

- **Structure:** Begin with reinforcing questions (Foundation), then progress to stretch questions (Synthesis).
- **Labeling:** Mark each question with its type using the format: `[Reinforcing - Foundation]` or `[Stretch - Synthesis]`.
- **Method:** For the chosen concept (e.g., "Asynchronous Programming"), brainstorm questions that explore mechanics, trade-offs, and purpose.
- **Question Archetypes:**
    - **Reinforcing (Foundation):** What problem does it solve? What is the alternative? (e.g., "Why use async/await instead of blocking threads?")
    - **Reinforcing (Foundation):** How do you use it in practice? (e.g., "How do you declare an async function in your language?")
    - **Stretch (Synthesis):** How does it really work under the hood? (e.g., "What is the event loop and how does it handle multiple concurrent requests?")
    - **Stretch (Synthesis):** What are the trade-offs? (e.g., "What are the performance implications of async code vs synchronous code?")
    - **Stretch (Synthesis):** What if something goes wrong? (e.g., "What happens if you forget to await an async function? What is a Promise rejection?")

### Step 4: Deconstruct into a Guided Task List

Create a list of small, verifiable tasks that guide the user toward answering the questions from Step 3. **Do not give away the answers in the tasks.**

- **Design Principle:** Tasks should prompt investigation.
- **Weak Task:** `Add the async package.`
- **Strong Task:**
    - [ ] **Task: Configure asynchronous processing for your application.**
        - [ ] Sub-task: Identify the I/O-bound operations in your codebase that would benefit from async processing.
        - [ ] Sub-task: Refactor a synchronous function to use async/await pattern.
        - [ ] Sub-task: Add error handling for asynchronous operations.

### Step 4.5: Include Professional Project Management Tasks

**Every sprint should conclude with professional project management tasks.** These reinforce real-world development practices:

- **Documentation Updates:**
    - Update `README.md` to reflect new features, dependencies, or setup requirements.
    - Update `docs/ARCHITECTURE.md` if architectural patterns or layers changed.
    - Add new folders to the "Project Structure" section if created.

- **Versioning & Release Management:**
    - Increment the version number in appropriate configuration files following Semantic Versioning (SemVer).
        - MAJOR version for breaking changes.
        - MINOR version for new features (backward-compatible).
        - PATCH version for bug fixes.
    - Create annotated Git tags for significant milestones.
    - Write clear, conventional commit messages.

- **Code Quality & Organization:**
    - Ensure code follows project conventions.
    - Add or update documentation comments if applicable.
    - Review and clean up any temporary test files or unused code.

**Example Final Task Block:**
```markdown
- [ ] **Task: Update Project Documentation & Version**
    - [ ] Update README.md with [new feature/changes]
    - [ ] Update ARCHITECTURE.md if patterns changed
    - [ ] Increment version in [appropriate file] (0.X.0 → 0.Y.0)
    - [ ] Commit with message: `[type]: [description]`
    - [ ] Create annotated tag: `git tag -a vX.Y.Z -m "Release message"`
    - [ ] Push commits and tags to remote
```

### Step 4.6: Plan the Commit Strategy

**Guide the user to think about logical commit boundaries during sprint planning.** Help them understand when to commit and what to include.

**Commit Strategy Principles:**
- **Logical Units:** Group related changes that form a complete, revertable unit.
- **Atomic Commits:** Each commit should represent one cohesive change.
- **Meaningful Boundaries:** Separate setup, implementation, refactoring, and documentation.

**Typical Sprint Commit Pattern:**
```
Commit 1: Setup/Infrastructure
  - Project scaffolding, package installation, configuration
  - Can be reverted without affecting feature implementation

Commit 2: Core Implementation
  - Main feature/functionality (may combine multiple tasks if cohesive)
  - Include related tests if they're part of the same logical unit
  - Use detailed commit body to explain approach and decisions

Commit 3: Optional Refactoring/Enhancement
  - Experimental changes or optimizations
  - Separate so they can be reverted independently

Commit 4: Documentation
  - README updates, architecture docs, comments
  - Separate concern from implementation
```

**When to Use Detailed Commit Messages (with body):**
- Non-obvious design decisions (e.g., "Why did we choose approach X over Y?").
- Complex implementations that need context.
- Breaking changes or major refactors.
- When grouping multiple related sub-tasks together.

**When Simple Messages Are Sufficient:**
- Self-explanatory changes (e.g., "docs: fix typo in README").
- Small, atomic updates (e.g., "feat: add Name property to Employer").
- Standard operations (e.g., "chore: update package version").

**Example Sprint Commit Guidance to Include:**

For an async programming sprint, you might guide the user to plan:
```
1. refactor(async): convert synchronous file I/O to async operations
2. test(async): add integration tests for async error handling
3. docs: update README with async usage examples
```

### Step 5: Assemble the Sprint File

- Create a new file named `docs/sprints/Sprint-XX-[Concept-Name].md`.
- Use `docs/templates/sprint-learning-template.md` as the base template.
- Populate the template with the content generated in the previous steps:
    - `Sprint Details & Goals` (from Step 2)
    - `Task List` (from Step 4)
    - `Understanding & Synthesis Questions` (from Step 3 - a single numbered list with reinforcing questions first, then stretch questions, each labeled with its type)
- Leave the `AI Marking & Feedback` and `Sprint Review` sections for later.

### Step 6: Initiate the Sprint

- Inform the user that you have created the new sprint file.
- State the primary goal and the first task to begin the walkthrough.
