# Personal Preferences Guide

Understanding and building your account-level preferences that work across all Claude conversations.

---

## What Are Personal Preferences?

**Personal Preferences** = Universal standards that apply to ALL your Claude conversations, regardless of project or topic.

**Think of it as:**
- How you want Claude to work in general
- Your communication baseline
- Quality standards for all deliverables
- Universal preferences that transcend any specific domain

---

## The Three Layers

```
Personal Preferences (Account-wide)
    ├── Project A: Custom Instructions + Memory
    ├── Project B: Custom Instructions + Memory
    └── Regular Chats (no project)
```

**Personal Preferences:** Universal standards (language, work approach, quality expectations)  
**Custom Instructions:** Project-specific context (who you are, goals, constraints for THIS domain)  
**Memory:** Learned patterns from friction (specific corrections after Rule of Three)

---

## Real Example: Evolved Over 2 Months

Here's a real set of preferences built through friction-driven development, with the "why" behind each rule.

### Language & Context

```
British English spelling throughout (conversation and code).
I'm a beginner coder with good structural understanding.
```

**Why here, not projects?**
- Applies everywhere - fitness projects, coding projects, general chats
- Foundational context that never changes
- Known before using Claude, not learned through friction

---

### Code Projects

```
- When working on code projects:
  * Check project files with view tool before asking for uploads
  * Provide clear options without flip-flopping between approaches
  * Before suggesting I test changes: verify syntax yourself by reading 
    modified sections with 20+ lines of context, manually trace bracket/tag 
    matching, and confirm nesting levels are correct
```

**Friction that led here:**
1. **Check files first** - Claude kept asking "can you upload X?" when files were already accessible
2. **Clear options** - Got frustrated with Claude changing approaches mid-conversation ("actually, let's do Y instead")
3. **Verify syntax** - Tired of testing code only to find obvious syntax errors Claude should have caught

**Why preferences, not project memory?**
- Applies to ALL code projects (games, tools, websites)
- About HOW Claude works, not domain-specific patterns
- Quality standard, not project-specific correction

---

### Documentation Work

```
- When revising or restructuring documentation:
  * Always complete with cleanup pass before presenting final work
  * Move obsolete files to /archive/ folder (with date) during active development
  * Update all cross-references (search project for old filenames/terms)
  * Verify directory structure matches documentation
  * Present clean, single-source-of-truth results in main directories
  * Delete archive folder entirely when project finalised
```

**Friction that led here:**
1. **Cleanup pass** - Claude would present work with obsolete files still present, contradictory versions
2. **Archive during development** - Wanted safety net during iteration but clean results at end
3. **Update cross-references** - Found broken links after file renames
4. **Single source of truth** - Encountered duplicate file trees, specifications in multiple places getting out of sync

**Evolution:** Started with just "cleanup pass", added others as specific patterns emerged

**Why preferences?**
- Applies to ANY documentation project (this framework, work docs, personal wikis)
- Fundamental quality standard for deliverables
- Not domain-specific, it's how work should be done

---

### Action vs. Instruction

```
- Action vs. instruction decision:
  * Check if you have tools to complete the task yourself
  * First occurrence in conversation: Ask permission and explain approach
  * Repeated occurrences: Execute directly without asking
  * Never provide manual instructions for tasks you can do yourself
  * Only suggest manual steps when you genuinely cannot complete the task
  * Examples: GitHub operations, file creation, code execution, API calls
```

**Friction that led here:**
- Claude gave git commands when it could push to GitHub directly
- Provided file creation instructions instead of just creating files
- Wasted time on manual steps for automatable tasks

**Why this matters:**
- Balance: Security on first use (ask permission) vs. efficiency on repeated use (just do it)
- Prevents frustration of repeated permission requests
- Stops Claude defaulting to "here's how you do it" when "I'll do it" is better

**Why preferences?**
- Fundamental working relationship principle
- Applies across all domains and projects
- About HOW we collaborate, not WHAT we're working on

---

## Building Your Own Preferences

### Start Minimal

Don't try to anticipate everything. Start with just:
- Language preference (if not English)
- One or two fundamental things about how you work
- Maybe your expertise level if relevant

**Example minimal start:**
```
British English spelling.
I'm technical but not an expert coder.
```

That's it. Use Claude for 2-4 weeks, notice friction.

### Add Through Friction

When you find yourself correcting the same thing 3+ times:
1. **Is it universal?** Does it apply across all your Claude use?
2. **Is it about HOW not WHAT?** Is it about work approach, not domain knowledge?
3. **Did you know it upfront?** Or did you learn it through use?

If yes to 1 and 2, no to 3 → Add to preferences

**Examples:**
- "Always verify code syntax before suggesting I test" → Yes, universal quality standard
- "When suggesting exercises, always ask about equipment first" → No, that's project-specific memory for fitness project

### Common Categories

**Communication:**
- Language/spelling preferences
- Explanation depth
- Tone (formal/casual)

**Work Standards:**
- Code verification requirements
- Documentation cleanup rules
- File organization principles

**Collaboration Style:**
- When to ask vs. when to act
- How to present options
- Iteration preferences

**Don't Add:**
- Domain-specific knowledge (goes in project instructions)
- Learned patterns from specific projects (goes in project memory)
- One-off preferences (wait for pattern)

---

## Decision Tree

**Where does this instruction go?**

```
Does it apply to ALL my Claude use?
├─ No → Not preferences
│   └─ Did I know it before using Claude?
│       ├─ Yes → Custom Instructions (project-specific)
│       └─ No → Memory (learned pattern)
└─ Yes → Continue...
    Is it about HOW Claude works, not domain knowledge?
    ├─ Yes → Personal Preferences ✓
    └─ No → Probably Custom Instructions
```

**Examples:**

"Use British English" → ALL use + HOW = **Preferences** ✓

"I'm a fitness beginner with limited equipment" → Not all use, specific domain = **Custom Instructions** (fitness project)

"Always ask about equipment before suggesting exercises" → Specific domain + learned pattern = **Memory** (fitness project)

"Always cleanup documentation before presenting" → ALL use + HOW = **Preferences** ✓

---

## Maintenance

### Review Periodically

Every 2-3 months:
- Are there instructions you never use? Remove them.
- Have new patterns emerged across multiple projects? Add them.
- Are any instructions too specific? Move to project memory.

### Signs Your Preferences Need Work

**Too Heavy:**
- More than 15-20 lines
- Includes domain-specific details
- Trying to cover every edge case

**Too Light:**
- Repeatedly correcting the same universal pattern
- No guidance on work quality standards
- Claude doesn't match your baseline expectations

**Just Right:**
- 10-15 lines of core principles
- Universal standards that apply everywhere
- Evolved through real use, not guessing

---

## Integration with Projects

Your preferences work WITH project instructions, not instead of them.

**Example: Fitness Project**

*Personal Preferences:*
- British English
- Verify syntax before suggesting tests (if coding involved)
- Documentation cleanup standards

*Custom Instructions (Fitness Project):*
- Context: "I'm a fitness beginner with limited equipment"
- Goals: "Build sustainable habits, avoid injury"
- Constraints: "Home gym only, 4x per week max"

*Memory (Fitness Project):*
- "When suggesting exercises: Ask about equipment first, don't assume gym access"
- "Prefer simple effective programmes over complex ones"

**See how they layer?**
- Preferences = Universal baseline
- Custom Instructions = Project context
- Memory = Learned project-specific patterns

---

## Key Principles

**1. Preferences are universal**
If it only applies to one project, it's not a preference

**2. Preferences are about HOW, not WHAT**
Work approach and quality standards, not domain knowledge

**3. Preferences evolve through use**
Start minimal, add through friction, review periodically

**4. Preferences complement, don't replace**
Projects still need custom instructions and memory

**5. Less is more**
10 well-chosen lines beat 50 lines of guessing

---

## Quick Reference

**Add to Preferences when:**
- ✓ Applies across ALL your Claude use
- ✓ About work approach/quality/standards
- ✓ You knew it before using Claude (or it emerged universally)
- ✓ Confirmed pattern (3+ occurrences across projects)

**Don't add to Preferences when:**
- ✗ Only applies to specific domain
- ✗ Domain knowledge or context
- ✗ Learned pattern specific to one project
- ✗ One-off situation or edge case

---

## Related Documents

- **GLOSSARY.md** - See "Personal Preferences" entry for definition
- **template-usage-order.md** - How preferences fit with project setup
- **memory-guide.md** - Understanding Memory vs. Custom Instructions vs. Preferences
