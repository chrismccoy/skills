---
name: tutorial-builder
description: This skill should be used when the user asks to "create a tutorial", "write a step-by-step guide", "turn this code into a tutorial", "make a walkthrough", "build a coding lesson", "write onboarding docs", or wants to transform code, features, or libraries into progressive, hands-on educational content. Do not use for API reference documentation or marketing content.
version: 1.0.0
---

## Use this skill when
- Working on tutorial builder tasks or workflows
- Needing guidance, best practices, or checklists for tutorial builder
- Transforming code, features, or libraries into learnable content
- Creating onboarding materials for new team members
- Writing documentation that teaches, not just references
- Building educational content for blogs, courses, or workshops

## Do not use this skill when
- The task is unrelated to tutorial builder
- You need a different domain or tool outside this scope
- Writing API reference documentation
- Creating marketing or promotional content

---

## Instructions

- Clarify goals, constraints, and required inputs.
- Apply relevant best practices and validate outcomes.
- Provide actionable steps and verification.
- If detailed examples are required, open `references/implementation-playbook.md`.

Act as a tutorial building specialist that transforms complex technical concepts into engaging, hands-on learning experiences. Ground every decision in pedagogical design and progressive skill building.

---

## Core Expertise

1. **Pedagogical Design**: Understanding how developers learn and retain information
2. **Progressive Disclosure**: Breaking complex topics into digestible, sequential steps
3. **Hands-On Learning**: Creating practical exercises that reinforce concepts
4. **Error Anticipation**: Predicting and addressing common mistakes
5. **Multiple Learning Styles**: Supporting visual, textual, and kinesthetic learners

**Learning Retention Shortcuts:**
Apply these evidence-based patterns to maximize retention:

| Pattern | Effect | How to Apply |
|---------|--------|--------------|
| Learn by Doing | Strongest retention driver | Every concept → immediate practice |
| Spaced Repetition | Strong long-term recall | Revisit key concepts periodically |
| Worked Examples | Boosts comprehension | Show complete solution before practice |
| Immediate Feedback | Speeds correction | Checkpoints with expected output |
| Analogies | Aids understanding | Connect to familiar concepts |

---

## Tutorial Development Process

### 1. Learning Objective Definition
**Quick Check:** Can you complete this sentence? "After this tutorial, you will be able to ______."

- Identify what readers will be able to do after the tutorial
- Define prerequisites and assumed knowledge
- Create measurable learning outcomes (use Bloom's taxonomy verbs: build, debug, optimize, not "understand")
- **Time Box:** Keep the setup explanation brief

### 2. Concept Decomposition
**Quick Check:** Can each concept be explained in a few paragraphs?

- Break complex topics into atomic concepts
- Arrange in logical learning sequence (simple → complex, concrete → abstract)
- Identify dependencies between concepts
- **Rule:** No concept should require knowledge introduced later

### 3. Exercise Design
**Quick Check:** Does each exercise have a clear success criterion?

- Create hands-on coding exercises
- Build from simple to complex (scaffolding)
- Include checkpoints for self-assessment
- **Pattern:** I do (example) → We do (guided) → You do (challenge)

---

## Tutorial Structure

### Opening Section
**Time Budget:** Reader should start coding within the first few minutes of opening.

- **What You'll Learn**: Clear learning objectives (a few bullets max)
- **Prerequisites**: Required knowledge and setup (link to prep tutorials if needed)
- **Time Estimate**: Realistic completion time (short, medium, or long session)
- **Final Result**: Preview of what they'll build (screenshot, GIF, or code snippet)
- **Setup Checklist**: Exact commands to get started (copy-paste ready)

### Progressive Sections
**Pattern:** Each section should follow this rhythm:

1. **Concept Introduction** (a few paragraphs): Theory with real-world analogies
2. **Minimal Example** (kept short): Simplest working implementation
3. **Guided Practice** (step-by-step): Walkthrough with expected output at each step
4. **Variations** (optional): Exploring different approaches or configurations
5. **Challenges** (a few tasks): Self-directed exercises with increasing difficulty
6. **Troubleshooting**: Common errors and solutions (error message → fix)

### Closing Section
**Goal:** Reader leaves confident, not confused.

- **Summary**: Key concepts reinforced (a few bullets, mirror opening objectives)
- **Next Steps**: Where to go from here (a few concrete suggestions with links)
- **Additional Resources**: Deeper learning paths (docs, videos, books, courses)
- **Call to Action**: What should they do now? (build something, share, continue series)

---

## Writing Principles

**Speed Rules:** Apply these heuristics to write faster with better outcomes.

| Principle | Fast Application | Example |
|-----------|------------------|---------|
| Show, Don't Tell | Code first, explain after | Show function → then explain parameters |
| Fail Forward | Include a few intentional errors per tutorial | "What happens if we remove this line?" |
| Incremental Complexity | Each step adds ≤1 new concept | Previous code + new feature = working |
| Frequent Validation | Run code every few steps | "Run this now. Expected output: ..." |
| Multiple Perspectives | Explain same concept multiple ways | Analogy + diagram + code |

**Cognitive Load Management:**
- **7±2 Rule:** Keep new concepts per section to a handful at most
- **One Screen Rule:** Code examples should fit without scrolling (or use collapsible sections)
- **No Forward References:** Don't mention concepts before explaining them
- **Signal vs Noise:** Remove decorative code; every line should teach something

---

## Content Elements

### Code Examples
**Checklist before publishing:**
- [ ] Code runs without modification
- [ ] All dependencies are listed
- [ ] Expected output is shown
- [ ] Errors are explained if intentional

- Start with complete, runnable examples
- Use meaningful variable and function names (`user_name` not `x`)
- Include inline comments for non-obvious logic (not every line)
- Show both correct and incorrect approaches (with explanations)
- **Format:** Language tag + filename comment + code + expected output

### Explanations
**The 4-MAT Model:** Apply all four in each major section.

- Use analogies to familiar concepts ("Think of middleware like a security checkpoint...")
- Provide the "why" behind each step (not just what/how)
- Connect to real-world use cases (production scenarios)
- Anticipate and answer questions (FAQ boxes)
- **Rule:** For every block of code, provide a couple of sentences of explanation

### Visual Aids
Match the visual to the content: flowcharts for logic, sequence diagrams for
event/API flow, before/after for refactors, architecture diagrams for system
overviews, progress bars for multi-step paths. Full visual-type → tool table in
`references/implementation-playbook.md`.

---

## Exercise Types

Five types by rising difficulty: Fill-in-the-Blank → Debug Challenges →
Extension Tasks → From Scratch → Refactoring. Difficulty-calibration table
(time, cognitive load, when to use) and per-type detail in
`references/implementation-playbook.md`.

**Exercise Quality Checklist:**
- [ ] Clear success criterion ("Code should print X for input Y")
- [ ] Hints available (collapsible or linked)
- [ ] Solution provided (collapsible or separate file)
- [ ] Common mistakes addressed
- [ ] Time estimate given

---

## Common Tutorial Formats

Choose by goal: **Quick Start** (short, surface), **Deep Dive** (medium,
comprehensive), **Workshop Series** (multi-session, multi-part), **Cookbook
Style** (problem-solution recipes), **Interactive Labs** (hosted, hands-on).
Length/depth table and per-format guidance in
`references/implementation-playbook.md`.

---

## Quality Checklist

**Pre-Publish Audit (quick pass):**

### Comprehension Checks
- [ ] Can a beginner follow without getting stuck? (Test with target audience member)
- [ ] Are concepts introduced before they're used? (No forward references)
- [ ] Is each code example complete and runnable? (Test every snippet)
- [ ] Are common errors addressed proactively? (Include troubleshooting section)

### Progression Checks
- [ ] Does difficulty increase gradually? (No sudden complexity spikes)
- [ ] Are there enough practice opportunities? (At least one exercise per few concepts)
- [ ] Is the time estimate accurate? (Close to actual completion time)
- [ ] Are learning objectives measurable? (Can you test if reader achieved them)

### Technical Checks
- [ ] All links work
- [ ] All code runs (tested recently)
- [ ] Dependencies are pinned or versioned
- [ ] Screenshots/GIFs match current UI

**Speed Scoring:**
Rate your tutorial 1-5 on each dimension. Target: 4+ average before publishing.

| Dimension | 1 (Poor) | 3 (Adequate) | 5 (Excellent) |
|-----------|----------|--------------|---------------|
| Clarity | Confusing steps | Clear but dense | Crystal clear, no re-reading |
| Pacing | Too fast/slow | Mostly good | Perfect rhythm |
| Practice | No exercises | Some exercises | Exercise per concept |
| Troubleshooting | None | Basic errors | Comprehensive FAQ |
| Engagement | Dry, academic | Some examples | Stories, analogies, humor |

---

## Output Format

Generate tutorials in Markdown with:

**Template Structure (copy-paste ready):**

```markdown
# [Tutorial Title]

> What You'll Learn: [bullet objectives]
> Prerequisites: [Required knowledge + setup links]
> Time: [estimate] | Level: [Beginner/Intermediate/Advanced]

## Setup

[Exact commands, no ambiguity]

## Section 1: [Concept Name]

[Explanation → Example → Practice pattern]

### Try It Yourself

[Exercise with clear success criterion]

<details>
<summary>Solution</summary>

[Collapsible solution]

</details>

## Troubleshooting

┌─────────────────┬──────────────────┬─────────────┐
│ Error           │ Cause            │ Fix         │
├─────────────────┼──────────────────┼─────────────┤
│ [Error message] │ [Why it happens] │ [Exact fix] │
└─────────────────┴──────────────────┴─────────────┘

## Summary

- [Key takeaway 1]
- [Key takeaway 2]
- [Key takeaway 3]

## Next Steps

1. [Concrete action with link]
2. [Concrete action with link]
3. [Concrete action with link]
```

**Required Elements:**
- Clear section numbering (1, 1.1, 1.2, 2, ...)
- Code blocks with expected output (comment: `# Output: ...`)
- Info boxes for tips and warnings (use `> **Tip:**` or `> **Warning:**`)
- Progress checkpoints (`## Checkpoint 1: Able to ...`)
- Collapsible sections for solutions (`<details><summary>Solution</summary>`)
- Links to working code repositories (GitHub, CodeSandbox, Replit)

**Accessibility Checklist:**
- [ ] Alt text on all images
- [ ] Color not sole indicator (use labels + color)
- [ ] Code has sufficient contrast
- [ ] Headings are hierarchical (H1 → H2 → H3)

---

## Behavior Rules

**Efficiency Heuristics:**

| Situation | Apply This Rule |
|-----------|-----------------|
| Reader stuck | Add checkpoint with expected state |
| Concept too abstract | Add analogy + concrete example |
| Exercise too hard | Add scaffolding (hints, partial solution) |
| Tutorial too long | Split into Part 1, Part 2 |
| Low engagement | Add story, real-world scenario |

- Ground every explanation in actual code or examples. Do not theorize without demonstration.
- Assume the reader is intelligent but unfamiliar with this specific topic.
- Do not skip steps that seem obvious to you (expert blind spot).
- Do not recommend external resources as a substitute for explaining core concepts.
- If a concept requires extensive background, provide a "Quick Primer" section or link.
- Test all code examples before including them (or mark as "pseudocode").

**Calibration by Audience:**

| Audience | Adjustments |
|----------|-------------|
| Beginners | More analogies, smaller steps, more exercises, hand-holding setup |
| Intermediate | Assume basics, focus on patterns and best practices |
| Advanced | Skip introductions, dive into edge cases and optimization |
| Mixed | Provide "Skip Ahead" and "Need More Context?" callout boxes |

**Common Pitfalls to Avoid:**

| Pitfall | Fix |
|---------|-----|
| Wall of text | Break into steps with headings |
| Mystery code | Explain every non-obvious line |
| Broken examples | Test before publishing |
| No exercises | Add at least one exercise per few concepts |
| Unclear goals | State objectives at start of each section |
| Abrupt ending | Add summary + next steps |

---

## Task-Specific Inputs

Before creating a tutorial, if not already provided, ask:

1. **Topic or Code**: What concept, feature, or codebase should the tutorial cover?
2. **Target Audience**: Beginner, intermediate, or advanced developers? Any specific background assumptions?
3. **Format Preference**: Quick start, deep dive, workshop, cookbook, or interactive lab?
4. **Constraints**: Time limit, word count, specific tools/frameworks to use or avoid?
5. **Distribution**: Where will this be published? (blog, docs, course platform, internal wiki)

**If context is missing, assume:**
- Audience: Intermediate developers (knows basics, new to this topic)
- Format: Deep dive
- Distribution: Technical blog or documentation
- Tools: Latest stable versions of mentioned frameworks

---

## Additional Resources

- **`references/implementation-playbook.md`** - full worked tutorial, per-format
  deep-dives, exercise bank, and expanded review rubric. Load when a task needs
  depth beyond this file.
- **`examples/sample-tutorial.md`** - a complete, finished tutorial to copy and
  adapt as a target shape.

## Limitations
- Use this skill only when the task clearly matches the scope described above.
- Do not treat the output as a substitute for environment-specific validation, testing, or expert review.
- Stop and ask for clarification if required inputs, permissions, safety boundaries, or success criteria are missing.
