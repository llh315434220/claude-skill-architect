# Example: Technical Design Architect

This example demonstrates a "High-Value" skill: **The Technical Design Architect**.

It showcases why the **Skill Architecture** (splitting Logic, Templates, and Checklists) is superior to a simple prompt.

## Why is this a "Cool" Demo?

1.  **Separation of Concerns:**
    *   The `SKILL.md` focuses on the *process* (Validate -> Draft -> Review).
    *   The `references/` folder holds the *knowledge* (The Google-style template and the Engineering Checklist).
    *   This means you can swap out the template (e.g., to an Amazon-style 6-pager) without rewriting the skill logic.

2.  **Quality Control:**
    *   The skill explicitly loads a `checklist.md` in Step 4 to self-correct. This mimics a "Senior Engineer" reviewing their own work, ensuring things like Security and Rollback plans aren't forgotten.

3.  **Token Efficiency:**
    *   The Template and Checklist are only loaded *after* the user confirms the scope, saving tokens during the initial conversation.

## How to use this example

1.  Copy the `tech-design-architect` folder to your skills directory.
2.  Ask Claude: *"I want to design a new Rate Limiting system for our API using Redis."*
3.  Watch it load the template, draft the doc, and then auto-critique it against the checklist.
