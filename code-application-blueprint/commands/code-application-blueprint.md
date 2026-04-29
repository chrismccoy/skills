---
description: Generate a complete technical project specification ready for implementation
argument-hint: [project description]
---

Generate a complete application blueprint using the `code-application-blueprint` skill. Run the full Initialization Gate to collect all five required variables — project description, tech stack, interfaces, scale, and constraints — then produce a 10-section technical specification with zero placeholders or unresolved items.

If a project description was provided in the slash command arguments, use it for Variable 1. Otherwise ask at the Initialization Gate.

Project description (if provided): $ARGUMENTS
