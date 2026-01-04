# Glossary

Quick reference for key terms and concepts used throughout this framework.

---

## Core Concepts

### Friction
**What it is:** The gap between what Claude gives you and what you actually needed. Any moment where you find yourself correcting, reformatting, or clarifying Claude's response.

**Examples:**
- Claude assumes you have equipment you don't own
- Responses are too detailed when you needed quick answers
- Claude explains concepts you already understand
- Format is wrong (bullets when you wanted prose)

**Why it matters:** Friction is signal, not noise. It tells you exactly what your system is missing and needs to capture.

**Related:** Rule of Three, Memory Instructions

---

### Rule of Three
**What it is:** A filtering mechanism - only capture a pattern as a memory instruction after you've corrected it 3+ times.

**How it works:**
- 1st correction: Note it
- 2nd correction: Pattern maybe?
- 3rd correction: Definitely a pattern → capture it

**Why it matters:** Prevents over-specification. Many "problems" are one-off situations that won't recur. The Rule of Three filters signal from noise.

**Related:** Friction, Memory Instructions

---

### Project Context
**What it is:** Your Custom Instructions in Claude Projects. The unchanging context that applies to every conversation.

**Also called:** Custom Instructions, Project Instructions

**Contains:**
- Who you are (context)
- Your constraints
- Your goals
- Communication preferences
- What won't work for you (red flags)

**When to use:** Things you know BEFORE starting to use Claude.

**Related:** Memory, Friction-Driven Development

---

### Memory / Project Memory
**What it is:** Specific instructions stored separately in Claude Projects that capture patterns discovered through use.

**Also called:** Memory Instructions, Project Memory

**Contains:**
- Specific corrections from friction
- Learned patterns (Rule of Three)
- "When X, do Y, not Z" instructions

**When to use:** Things you learn AFTER using Claude through friction.

**Format:**
```
When [situation]:
- Do: [specific action]
- Don't: [pattern to avoid]
- Why: [reason this matters]
```

**Related:** Project Context, Friction, Rule of Three

---

### Personal Preferences
**What it is:** User-level preferences that apply across ALL Claude conversations (both Projects and non-Project chats). Set once in your Claude account settings.

**Also called:** User Preferences, Account Preferences

**Contains:**
- Language preference (British English, American English, etc.)
- General communication style preferences
- Universal formatting preferences
- Cross-cutting work standards (e.g., documentation cleanup rules)

**Scope:** 
- Applies everywhere: Projects, regular chats, all conversations
- More general than Project-specific instructions
- Think "how I want Claude to work in general"

**When to use:** Preferences that apply regardless of what project or task you're working on.

**Examples:**
- "Use British English spelling throughout"
- "When revising documentation, always complete with cleanup pass"
- "Explain technical concepts at intermediate level"

**Where vs. Project Context:**
- Personal Preferences: Universal across all Claude use
- Project Context: Specific to one project's domain/context

**Related:** Project Context, Memory

---

### Friction-Driven Development
**What it is:** The methodology of starting minimal, using the system, noticing friction, and expanding deliberately based on real patterns.

**Core principle:** You cannot anticipate what you'll need before experiencing friction.

**Process:**
1. Start minimal (essentials only)
2. Use the system normally
3. Notice friction patterns
4. Capture patterns (Rule of Three)
5. Expand deliberately
6. Repeat

**Why it matters:** Prevents over-engineering. Creates systems that evolved through use rather than guessing.

**Related:** Rule of Three, Friction, Memory

---

## Template Terms

### Starter Template
**What it is:** Minimal viable setup with 5 essential sections. Always the starting point.

**Contains:**
- Context, Constraints, Goals, Preferences, Red Flags
- One example per section (Health/Fitness domain)
- Appendices with other domain examples
- Guidance on what to add next

**Time to complete:** 15-30 minutes

**When to use:** Always start here. Every new project.

**Related:** Advanced Template, Essentials

---

### Advanced Template
**What it is:** Reference library of 8 optional expansion sections. Not a checklist - a menu of options.

**Contains:**
- Operating Modes
- Decision Framework
- Domain Principles
- Success Metrics
- Response Structure
- Common Pitfalls
- Integration with Other Areas
- Tools & Systems

**Examples:** Career/Coding domain

**When to use:** After Week 1+, when friction reveals specific needs. Add ONE section at a time.

**Related:** Starter Template, Friction

---

### The Essentials
**What they are:** The 5 core sections that every project needs:
1. Context (who you are)
2. Constraints (what limits you)
3. Goals (what you want)
4. Preferences (how to work)
5. Red Flags (what won't work)

**Why these 5:** Minimum information needed for Claude to provide useful, contextualised responses.

**Related:** Starter Template

---

## Domain Terms

### Operating Modes
**What it is:** Explicit definitions of different interaction patterns (e.g., planning vs. execution).

**When to add:** You notice you interact with Claude differently for different types of work.

**Example:** 
- Mode 1: Strategic Planning (detailed, challenging)
- Mode 2: Daily Execution (concise, actionable)

**Related:** Advanced Template

---

### Decision Framework
**What it is:** Explicit priority hierarchy for helping Claude align suggestions with what matters to you.

**When to add:** Claude's suggestions work technically but don't align with your actual priorities.

**Example:**
```
Priority 1: Sustainability
Priority 2: Safety
Priority 3: Effectiveness
```

**Related:** Advanced Template, Domain Principles

---

### Domain Principles
**What it is:** Core beliefs that guide all advice in your domain.

**When to add:** Claude keeps suggesting things that violate how you fundamentally think the work should be done.

**Example (Fitness):**
- Consistency beats intensity
- Form before load
- Recovery is training

**Related:** Decision Framework, Advanced Template

---

### Success Metrics
**What it is:** How you measure progress - primary metrics, secondary indicators, leading signals.

**When to add:** You want Claude to help analyse progress and suggest adjustments based on data.

**Related:** Advanced Template

---

## Process Terms

### Friction Log
**What it is:** Simple tracking of patterns where Claude misses the mark.

**Format:** Just note date + issue + pattern status
- "2025-01-03: Assumed gym access again (2nd time)"
- "2025-01-05: Assumed gym access (3rd time - create memory)"

**Why useful:** Helps apply Rule of Three systematically.

**Can be:** Mental notes, simple text file, or structured log

**Related:** Friction, Rule of Three

---

### Memory Instruction
**What it is:** Specific, actionable instruction captured after friction pattern confirmed (Rule of Three).

**Format:**
```
When [situation]:
- Do: [specific action]
- Don't: [pattern to avoid]
- Why: [reason this matters]
```

**Where stored:** Project Memory (not Custom Instructions)

**Example:**
```
When suggesting exercises:
- Do: Ask about available equipment first
- Don't: Assume gym access
- Why: Prevents suggesting workouts I can't complete
```

**Related:** Memory, Friction, Rule of Three

---

### Evolution Process
**What it is:** The ongoing cycle of use → friction → capture → refine.

**Phases:**
1. Essential Setup (Day 1)
2. Friction Recognition (Weeks 1-3)
3. Deliberate Expansion (Month 1+)
4. Continuous Evolution (Ongoing)

**Why it matters:** Systems that evolve through use work better than systems designed upfront.

**Related:** Friction-Driven Development

---

## Common Phrases

### "Start minimal, expand deliberately"
**Meaning:** Begin with just the essentials, add complexity only when friction reveals genuine needs.

**Why:** You can't anticipate needs before experiencing friction. Over-engineering wastes time on sections you'll never use.

---

### "Friction is signal, not noise"
**Meaning:** When Claude misses the mark, that's valuable information about what your system needs.

**Why:** Each friction point tells you exactly what instruction or context is missing.

---

### "Trust the process"
**Meaning:** Follow friction-driven development even when tempted to plan everything upfront.

**Why:** Systems evolved through use outperform systems designed through guessing.

---

### "Context over commands"
**Meaning:** Rich situation description enables Claude to adapt, versus rigid command-based instructions.

**Why:** Claude can figure out what to do if it understands who you are and what you're trying to achieve.

---

### "Memory vs. Project Context"
**Meaning:** Project Context = what you knew before; Memory = what you learned through use.

**Decision rule:**
- Knew it before using Claude? → Project Context
- Learned it through using Claude? → Memory

---

### "Personal Preferences vs. Project Context vs. Memory"
**Understanding the three layers:**

**Personal Preferences (Universal):**
- Scope: All Claude conversations everywhere
- Examples: Language, general communication style, work standards
- When: Set once, applies always
- Where: Account Settings → Personal Preferences

**Project Context (Project-Specific):**
- Scope: One specific Claude Project only
- Examples: Your role, constraints, goals for THIS domain
- When: Known before starting project
- Where: Project Settings → Custom Instructions

**Memory (Learned Patterns):**
- Scope: One specific Claude Project only
- Examples: Corrections after Rule of Three
- When: Discovered through friction
- Where: Project Settings → Memory

**Visual:**
```
Personal Preferences (Everywhere)
    ├── Project A: Project Context + Memory
    ├── Project B: Project Context + Memory
    └── Regular Chats (no Project)
```

**Example:**
- Personal Preference: "Use British English spelling" (everywhere)
- Project Context: "I'm learning Python for data science" (Python Project only)
- Memory: "When explaining code, define jargon on first use" (Python Project, after friction)

---

## Meta Terms

### Hybrid Approach
**What it is:** This framework - combining structured templates (from articles) with adaptive friction-driven development (from Claude's experience).

**Why hybrid:** 
- Structure provides starting point and reference
- Friction-driven prevents over-engineering
- Together they balance "enough structure" with "evolve through use"

**Related:** Friction-Driven Development, Templates

---

### Single Source of Truth
**Meaning:** One authoritative version of each piece of information, no duplicates or contradictions.

**Why it matters:** Prevents confusion, reduces maintenance burden, ensures consistency.

**Practice:** Delete old versions after creating new ones, update all cross-references.

---

## Quick Reference

**When deciding where something goes:**

*Step 1: Does this apply to ALL my Claude use?*
- Yes → Personal Preferences (Account Settings)
- No → Go to Step 2

*Step 2: Did I know this before using Claude?*
- Yes → Project Context (Custom Instructions)
- No → Go to Step 3

*Step 3: Have I corrected this 3+ times?*
- Yes → Memory (Project Memory)
- No → Don't capture yet, wait for pattern

**Examples by category:**

*Personal Preferences:*
- British English spelling
- Documentation cleanup standards
- General explanation depth preference

*Project Context:*
- Who you are in this domain
- Your constraints for this project
- Goals for this specific area

*Memory:*
- "Always ask about equipment first" (fitness project)
- "Define jargon on first use" (coding project)
- Specific patterns from friction

**When deciding what to add:**
- Week 1: Nothing - just use essentials
- Week 2-3: Memory instructions for confirmed patterns
- Month 1+: One advanced section if friction reveals need
- Ongoing: Review monthly, refine as needed

---

## Related Documents

- **README.md** - System overview
- **project-context-guide.md** - Detailed setup process
- **memory-guide.md** - Deep dive on memory development
- **personal-preferences-guide.md** - Account-level preferences setup
- **template-usage-order.md** - How to use templates
