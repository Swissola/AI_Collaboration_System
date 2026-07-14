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
```

**Why here, not projects?**
- Applies everywhere - fitness projects, coding projects, general chats
- Foundational preference that never changes
- Known before using AI, not learned through friction

---

### Documentation Work

```
- When revising or restructuring documentation:
  * Always complete with cleanup pass before presenting final work
  * Move obsolete files to /archive/ folder (with date) during active development
  * Update all cross-references (search project for old filenames/terms)
  * Verify directory structure matches documentation
  * Single-source-of-truth in main directories
  * Delete archive folder entirely when project finalised
```

**Friction that led here:**
1. **Cleanup pass** - AI would present work with obsolete files still present, contradictory versions
2. **Archive during development** - Wanted safety net during iteration but clean results at end
3. **Update cross-references** - Found broken links after file renames
4. **Single source of truth** - Encountered duplicate file trees, specifications in multiple places getting out of sync

**Evolution:** Started with just "cleanup pass", added others as specific patterns emerged

**Why preferences?**
- Applies to ANY documentation project (this framework, test plans, proposals, work docs, personal wikis)
- Fundamental quality standard for deliverables
- Not domain-specific, it's how documentation work should be done

---

### When Operations Fail

```
- When operations fail:
  * Diagnose cause after first failure - don't retry blindly
  * Maximum 2 retries before investigating root cause
  * Check if credentials/tokens/environment changed since last success
```

**Friction that led here:**
- AI kept retrying failed git pushes without checking if proxy token expired
- Repeated identical commands expecting different results
- Wasted time on multiple timeouts instead of diagnosing once

**Why preferences?**
- Applies to any technical operation (git, API calls, file operations)
- Universal debugging principle
- About HOW to work through failures, not domain-specific

---

### Action vs. Instruction

```
- Action vs. instruction decision:
  * Check if you have tools to complete the task yourself
  * First occurrence in conversation: Ask permission and explain approach
  * Repeated occurrences: Execute directly without asking
  * Never provide manual instructions for tasks you can do yourself
  * Only suggest manual steps when you genuinely cannot complete the task
```

**Friction that led here:**
- AI gave git commands when it could push to GitHub directly
- Provided file creation instructions instead of just creating files
- Wasted time on manual steps for automatable tasks

**Why this matters:**
- Balance: Security on first use (ask permission) vs. efficiency on repeated use (just do it)
- Prevents frustration of repeated permission requests
- Stops AI defaulting to "here's how you do it" when "I'll do it" is better

**Why preferences?**
- Fundamental working relationship principle
- Applies across all domains and projects
- About HOW we collaborate, not WHAT we're working on

---

### What About Code-Specific Rules?

You might notice there are **no code-specific rules** in Personal Preferences. That's deliberate!

**Code-specific patterns belong in Project Memory (coding projects):**

```
When working on code:
- Check project files with view tool before asking for uploads
- Provide clear options without flip-flopping between approaches
- Before suggesting I test changes: verify syntax yourself (read modified 
  sections with 20+ lines context, trace brackets/tags, confirm nesting)
```

**Why Project Memory, not Preferences?**
- Only applies to coding projects, not fitness/documentation/general chats
- Learned through friction in specific coding work
- Domain-specific quality standards, not universal

**The distinction:**
- Preferences = Works across ALL domains
- Project Memory = Specific to coding projects only

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
- "Always verify code syntax before suggesting I test" → Yes, universal quality standard across all coding work
- "When suggesting exercises, always ask about equipment first" → No, that's project-specific memory for fitness project
- "Check project files before asking for uploads" → No, that's coding-project-specific memory
- "Always complete documentation with cleanup pass" → Yes, applies to any documentation work

### Common Categories

**Communication:**
- Language/spelling preferences
- Explanation depth
- Tone (formal/casual)

**Work Standards:**
- Code verification requirements
- Documentation cleanup rules
- File organisation principles

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

**Example: Coding Project**

*Personal Preferences:*
- British English spelling
- Documentation cleanup standards
- Action vs. instruction methodology
- Failure diagnosis approach

*Custom Instructions (Coding Project):*
- Context: "I'm a beginner coder with good structural understanding"
- Goals: "Build portfolio projects, learn Python, get first dev role"
- Constraints: "8-12 hours/week, no formal mentorship"

*Memory (Coding Project):*
- "Check project files with view tool before asking for uploads"
- "Provide clear options without flip-flopping between approaches"
- "Verify syntax before suggesting I test (read 20+ lines context, trace brackets)"

**See how they layer?**
- Preferences = Universal baseline (applies to ALL domains)
- Custom Instructions = Project context (who you are in THIS domain)
- Memory = Learned project-specific patterns (from friction in THIS project)

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
