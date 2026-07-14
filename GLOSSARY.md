# Glossary

Quick reference for key terms and concepts in the AI Collaboration System framework.

---

## The Three-Layer System

### Layer 1: Personal Preferences
**What it is:** Account-wide standards that apply to ALL your AI conversations across all projects and platforms.

**Also called:** User Preferences, Account Preferences

**Scope:** Universal - applies whether you're working on fitness, coding, writing, or any domain

**Contains:**
- Universal communication standards
- Language preferences (British English, etc.)
- General explanation depth
- Work quality expectations

**Examples:**
- "Always explain reasoning before giving recommendations"
- "Challenge my assumptions when they might lead to poor outcomes"
- "Ask clarifying questions rather than making assumptions"

**Where to set:**
- Claude: Settings → Profile → Personal Preferences
- Claude Code: `~/.claude/CLAUDE.md` (see [claude-code-memory-guide.md](guides/claude-code-memory-guide.md))
- ChatGPT: Settings → Personalization → Custom Instructions
- GitHub Copilot: github.com/copilot → Profile Menu → Personal Instructions
- Gemini: Account settings

**When to use:** Standards that apply regardless of what you're working on

**Decision rule:** Does this apply to fitness AND coding AND everything else? → Layer 1

**Related:** Project Context (Layer 2), Project Memory (Layer 3)

---

### Layer 2: Project Context
**What it is:** Project-specific context that applies to every conversation in THIS project.

**Also called:** Custom Instructions, Project Instructions, System Prompt (technical term)

**Scope:** One specific project/domain only

**Contains:**
- Who you are in this domain (context)
- Your constraints for this project
- Your goals for this area
- Project-specific communication preferences
- What won't work for you (red flags)

**Examples:**
- "I'm learning Python for data science with 8 hours/week"
- "I have no gym access - home equipment only"
- "Self-taught developer building portfolio projects"

**Where to set:**
- Claude: Project → Custom Instructions
- Claude Code: project `./CLAUDE.md`, plus `./CLAUDE.local.md` for personal overrides
- ChatGPT: Create a GPT or conversation-specific instructions
- GitHub Copilot: `.github/copilot-instructions.md` in repository
- Gemini: Create a Gem
- API: System message in requests

**When to use:** Things you know BEFORE starting to use your AI for this project

**Decision rule:** Did I know this before using the AI? → Layer 2

**Related:** Personal Preferences (Layer 1), Project Memory (Layer 3), Starter Template

---

### Layer 3: Project Memory
**What it is:** Learned patterns discovered through friction while using THIS specific project.

**Also called:** Memory Instructions, Project Memory, Memory

**Scope:** One specific project only - patterns unique to this domain

**Contains:**
- Specific corrections from friction (Rule of Three)
- "When X, do Y, not Z" instructions
- Edge cases and nuances discovered through use
- Patterns that weren't obvious upfront

**Examples:**
- "When suggesting exercises, always check equipment first"
- "Don't use terminology without defining it on first use"
- "Suggest incremental improvements, not all at once"

**Where to set:**
- Claude: Project → Memory
- Claude Code: mostly automatic, see [claude-code-memory-guide.md](guides/claude-code-memory-guide.md)
- ChatGPT: Memory feature or append to GPT instructions
- GitHub Copilot: Append to repository instructions (manual)
- Gemini: Append to Gem instructions (manual)
- API: Append to system message (manual)

**When to use:** Things you learn AFTER using the AI through friction patterns

**Decision rule:** Did I learn this through friction? Has it recurred 3+ times? → Layer 3

**Format:**
```
When [situation]:
- Do: [specific action]
- Don't: [pattern to avoid]
- Why: [reason this matters]
```

**Related:** Personal Preferences (Layer 1), Project Context (Layer 2), Friction, Rule of Three

---

## Core Concepts

### Friction
**What it is:** The gap between what the AI gives you and what you actually needed. Any moment where you find yourself correcting, reformatting, or clarifying the response.

**Examples:**
- AI assumes you have equipment you don't own
- Responses are too detailed when you needed quick answers
- AI explains concepts you already understand
- Format is wrong (bullets when you wanted prose)
- Suggestions ignore your constraints

**Why it matters:** Friction is signal, not noise. It tells you exactly what your system is missing and needs to capture in Layer 3 (Memory).

**How to use:** Track friction patterns. After 3 occurrences, capture as memory instruction.

**Related:** Rule of Three, Project Memory (Layer 3)

---

### Rule of Three
**What it is:** A filtering mechanism - only capture a pattern as a memory instruction after you've corrected it 3+ times.

**How it works:**
- 1st correction: Note it (could be a fluke)
- 2nd correction: Pattern maybe? (watch for it)
- 3rd correction: Definitely a pattern → capture in Layer 3 (Memory)

**Why it matters:** Prevents over-specification. Many "problems" are one-off situations that won't recur. The Rule of Three filters signal from noise.

**Example:**
- Day 1: AI suggests barbell squats (note: I don't have a barbell)
- Day 3: AI suggests cable exercises (note: 2nd time assuming gym)
- Day 5: AI suggests leg press (3rd time! → Create memory instruction)

**Related:** Friction, Project Memory (Layer 3), Friction Log

---

### Friction-Driven Development
**What it is:** The methodology of starting minimal, using the system, noticing friction, and expanding deliberately based on real patterns.

**Core principle:** You cannot anticipate what you'll need before experiencing friction.

**Process:**
1. Set up Layer 1 (Personal Preferences) once
2. Set up Layer 2 (Project Context) - essentials only (30 min)
3. Use the system normally for a week
4. Notice friction patterns
5. Capture patterns in Layer 3 (Memory) using Rule of Three
6. Expand Layer 2 with optional sections only when needed
7. Repeat continuously

**Why it matters:** Prevents over-engineering. Creates systems that evolved through use rather than guessing upfront needs.

**Contrasts with:** Traditional prompt engineering (design everything upfront)

**Related:** Rule of Three, Friction, Three-Layer System

---

## Template Terms

### Starter Template
**What it is:** Minimal viable setup with 5 essential sections for Layer 2 (Project Context). Always the starting point.

**The Five Essentials:**
1. Context (who you are in this domain)
2. Constraints (what limits you)
3. Goals (what you want to achieve)
4. Preferences (how you work - project-specific)
5. Red Flags (what won't work)

**Domain:** Health/Fitness examples

**Time to complete:** 20-30 minutes

**Layer:** Layer 2 (Project Context)

**When to use:** Always start here. Every new project begins with starter template.

**Related:** Advanced Template, Layer 2, The Essentials

---

### Advanced Template
**What it is:** Reference library of 8 optional expansion sections for Layer 2. Not a checklist - a menu of options to add when friction reveals needs.

**Contains:**
- Operating Modes (different interaction types)
- Decision Framework (priority hierarchy)
- Domain Principles (core beliefs)
- Success Metrics (tracking progress)
- Response Structure (format preferences)
- Common Pitfalls (your recurring mistakes)
- Integration with Other Areas (cross-domain)
- Tools & Systems (external integrations)

**Domain:** Career/Coding examples

**Layer:** Layer 2 (Project Context) expansions

**When to use:** After Week 2+, when friction reveals specific needs. Add ONE section at a time, not all at once.

**Related:** Starter Template, Layer 2, Friction

---

### The Essentials
**What they are:** The 5 core sections that every Layer 2 (Project Context) needs:

1. **Context** - Who you are, what you're doing
2. **Constraints** - Time, resources, limitations (be honest)
3. **Goals** - 3-5 specific objectives
4. **Preferences** - How you want to work (project-specific only)
5. **Red Flags** - What definitely won't work

**Why these 5:** Minimum information needed for the AI to provide useful, contextualised responses.

**Note:** Universal preferences go in Layer 1 (Personal Preferences), not here.

**Related:** Starter Template, Layer 2

---

## Optional Expansion Terms

### Operating Modes
**What it is:** Explicit definitions of different interaction patterns within a project (e.g., planning vs. execution).

**Part of:** Advanced Template (Layer 2 expansion)

**When to add:** You notice you interact with the AI differently for different types of work within this project.

**Example:**
- Mode 1: Strategic Planning (detailed, challenging, long-term)
- Mode 2: Daily Execution (concise, actionable, immediate)
- Mode 3: Analysis & Review (objective, data-driven)

**Related:** Advanced Template, Layer 2

---

### Decision Framework
**What it is:** Explicit priority hierarchy for helping the AI align suggestions with what matters to you.

**Part of:** Advanced Template (Layer 2 expansion)

**When to add:** The AI's suggestions work technically but don't align with your actual priorities.

**Example:**
```
Priority 1: Sustainability & Consistency
Priority 2: Safety & Injury Prevention
Priority 3: Effectiveness
Priority 4: Enjoyment
```

**Related:** Advanced Template, Domain Principles, Layer 2

---

### Domain Principles
**What it is:** Core beliefs that guide all advice in your domain.

**Part of:** Advanced Template (Layer 2 expansion)

**When to add:** The AI keeps suggesting things that violate how you fundamentally think the work should be done.

**Example (Fitness):**
- Consistency beats intensity
- Form before load
- Recovery is training

**Example (Coding):**
- Readability over cleverness
- Working code before optimisation
- Delete code rather than comment it out

**Related:** Decision Framework, Advanced Template, Layer 2

---

### Success Metrics
**What it is:** How you measure progress - primary metrics, secondary indicators, leading signals.

**Part of:** Advanced Template (Layer 2 expansion)

**When to add:** You want the AI to help analyse progress and suggest adjustments based on data.

**Example:**
- Primary: Workouts completed per week
- Secondary: Energy levels, sleep quality
- Leading: Planning sessions completed

**Related:** Advanced Template, Layer 2

---

## Process Terms

### Friction Log
**What it is:** Simple tracking of patterns where the AI misses the mark. Essential for applying the Rule of Three systematically.

**Format:** Just note date + issue + pattern count

**Example:**
```
2025-01-03: Assumed gym access (1st time)
2025-01-05: Suggested cable exercises (2nd time - watching)
2025-01-07: Suggested leg press (3rd time - CREATE MEMORY)
```

**Can be:** Mental notes, simple text file, or structured tracking

**Why useful:** Makes it easy to identify when a pattern has recurred 3 times and needs capturing in Layer 3 (Memory).

**Related:** Friction, Rule of Three, Project Memory (Layer 3)

---

### Memory Instruction
**What it is:** Specific, actionable instruction captured in Layer 3 after friction pattern confirmed by Rule of Three.

**Format:**
```
When [situation]:
- Do: [specific action]
- Don't: [pattern to avoid]
- Why: [reason this matters]
```

**Where stored:** Layer 3 (Project Memory) - separate from Layer 2 (Project Context)

**Example:**
```
When suggesting exercises:
- Do: Ask about available equipment first
- Don't: Assume gym access or standard equipment
- Why: Prevents suggesting workouts I can't complete at home
```

**Related:** Project Memory (Layer 3), Friction, Rule of Three

---

### Evolution Process
**What it is:** The ongoing cycle of use → friction → capture → refine across all three layers.

**Timeline:**
1. **Day 1:** Set up Layers 1 & 2 (Personal Preferences + Project Context)
2. **Week 1:** Use system, track friction, make no changes yet
3. **Weeks 2-3:** Identify patterns (Rule of Three), start building Layer 3
4. **Month 1:** First review, 2-3 memory instructions added
5. **Month 2:** Consider Layer 2 expansions if friction reveals needs
6. **Ongoing:** Monthly reviews, continuous refinement

**Why it matters:** Systems that evolve through use work better than systems designed entirely upfront.

**Related:** Friction-Driven Development, Three-Layer System

---

## Common Phrases

### "Start minimal, expand deliberately"
**Meaning:** Begin with just the essentials (Layers 1 & 2), add complexity only when friction reveals genuine needs.

**Why:** You can't anticipate needs before experiencing friction. Over-engineering wastes time on features you'll never use.

**Application:** Start with Starter Template (Layer 2), not Advanced Template. Add to Layer 3 only after Rule of Three.

---

### "Friction is signal, not noise"
**Meaning:** When the AI misses the mark, that's valuable information about what your system needs in Layer 3.

**Why:** Each friction point tells you exactly what instruction or context is missing. Don't ignore it - track it.

---

### "Trust the process"
**Meaning:** Follow friction-driven development even when tempted to plan everything upfront.

**Why:** Systems evolved through use (Layers 2 & 3 built incrementally) outperform systems designed through guessing (trying to fill Advanced Template on Day 1).

---

### "Context over commands"
**Meaning:** Rich situational description (Layer 2) enables AI to adapt, versus rigid command-based instructions.

**Why:** The AI can figure out what to do if it understands who you are and what you're trying to achieve. Layer 2 provides this context.

---

## Three-Layer Decision Guide

**Quick Reference:**

```
Does this apply to ALL my AI use (fitness, coding, writing, everything)?
├─ Yes → Layer 1: Personal Preferences
└─ No → Continue...

    Did I know this BEFORE using the AI for this project?
    ├─ Yes → Layer 2: Project Context
    └─ No → Continue...

        Have I corrected this 3+ times?
        ├─ Yes → Layer 3: Memory
        └─ No → Don't capture yet, wait for pattern
```

**Examples by Layer:**

**Layer 1 (Personal Preferences):**
- "Always explain reasoning before recommendations"
- "Use British English spelling"
- "Challenge my assumptions constructively"

**Layer 2 (Project Context):**
- "I'm learning Python for data science"
- "I have 8 hours/week for coding practice"
- "Self-taught, no CS degree, building portfolio"

**Layer 3 (Memory):**
- "When explaining code, define jargon on first use" (learned through friction)
- "Always ask about equipment before suggesting exercises" (learned through friction)
- "Suggest incremental changes, not wholesale rewrites" (learned through friction)

---

## Visual: The Three-Layer System

```
Layer 1: Personal Preferences (Account-wide)
│   "Use British English everywhere"
│   "Always explain reasoning"
│
├─> Project A (Fitness)
│   ├─ Layer 2: Project Context
│   │   "Home workouts, no gym, 4 hours/week"
│   └─ Layer 3: Memory
│       "Always ask about equipment first" (friction-learned)
│
├─> Project B (Coding)
│   ├─ Layer 2: Project Context
│   │   "Learning Python, 8 hours/week, beginner"
│   └─ Layer 3: Memory
│       "Define jargon on first use" (friction-learned)
│
└─> Regular Conversations (no project)
    └─ Only Layer 1 applies
```

---

## Meta Terms

### Hybrid Approach
**What it is:** This framework's methodology - combining structured templates with adaptive friction-driven development.

**Why hybrid:**
- Structure (templates) provides starting point and reference
- Friction-driven development prevents over-engineering
- Together they balance "enough structure" with "evolve through use"

**Contrasts with:**
- Pure structured approach: Design everything upfront (over-engineering risk)
- Pure adaptive approach: No structure at all (blank-page paralysis)

**Related:** Friction-Driven Development, Templates, Three-Layer System

---

### Platform-Agnostic
**Meaning:** This framework works with any AI system that supports persistent instructions (Claude, ChatGPT, GitHub Copilot, Gemini, etc.).

**How:** Core concepts (three layers, friction-driven) are universal. Implementation details (where to put instructions) vary by platform.

**Platform variations:** See each layer's "Where to set" section for platform-specific locations.

---

## Claude Code Terms

Claude Code implements the three-layer system as files rather than account settings. Full detail in [claude-code-memory-guide.md](guides/claude-code-memory-guide.md).

### CLAUDE.md
**What it is:** A markdown file Claude Code reads automatically at the start of a session. Exists at four levels (managed policy, user, project, local), most specific loading last.

**Related:** Layer 1, Layer 2, `@import`

### The Memory Hierarchy
**What it is:** The four CLAUDE.md levels, combined rather than overridden: managed policy (organisation-wide), user (`~/.claude/CLAUDE.md`), project (`./CLAUDE.md`), local (`./CLAUDE.local.md`, gitignored).

**Related:** CLAUDE.md, Layer 1, Layer 2

### `@import`
**What it is:** Syntax for pulling one file's content into a CLAUDE.md, `@path/to/file.md`. Keeps a single source of truth instead of copy-pasting the same instructions into several files. Four hops deep at most.

**Related:** CLAUDE.md

### Auto Memory
**What it is:** Claude Code's own Layer 3 implementation. Claude writes structured notes as it works with you, under `~/.claude/projects/<project>/memory/`, rather than you drafting memory instructions by hand after the Rule of Three.

**Related:** Layer 3, Rule of Three, Friction

---

## Related Documents

**Understanding the system:**
- **README.md** - Overview and three-layer introduction
- **PROJECT-INDEX.md** - Complete navigation guide
- **This GLOSSARY** - Terms and concepts

**Building each layer:**
- **personal-preferences-guide.md** - Layer 1 setup
- **project-context-guide.md** - Layer 2 setup
- **memory-guide.md** - Layer 3 development

**Templates and examples:**
- **starter-template.md** - Layer 2 essentials
- **advanced-template.md** - Layer 2 expansions reference
- **examples/** - Complete three-layer implementations

**Quick start:**
- **quick-start-checklist.md** - Fast-track setup
- **template-usage-order.md** - How to use templates
