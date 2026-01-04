# Memory Development Guide

## Understanding Memory in Claude Projects

**Project Context (Custom Instructions):** What you know before starting - your context, goals, constraints, preferences.

**Project Memory:** What you learn through using Claude - specific patterns, corrections, discovered preferences.

Think of it this way:
- Project Context = Your hypothesis about what you need
- Memory = Your findings from testing that hypothesis

---

## The Friction-Driven Approach

### What is Friction?

**Friction** = The gap between what Claude gives you and what you actually needed.

**Signs of friction:**
- You're rewriting Claude's output
- You're making the same correction repeatedly
- Response is "fine but not right"
- You think "I wish Claude had just..."

**Not friction:**
- One-off corrections (everyone makes mistakes)
- Corrections because you changed your mind
- Improvements that weren't wrong, just could be better

### The Rule of Three

Don't rush to capture every correction as a pattern. Use this filter:

**First time:** Correct it and move on  
**Second time:** Note it mentally ("Hmm, again")  
**Third time:** Pattern confirmed - time to capture it

**Why this works:**
- Filters noise from signal
- Prevents over-specification
- Ensures you're capturing actual patterns, not flukes
- Keeps memory lean and relevant

---

## Creating Memory Instructions

### The Basic Template

```
[Context/Trigger]:
- Do: [Specific action]
- Don't: [Pattern to avoid]
- Why: [Reason]
```

### Example: Equipment Assumption

**Friction:** Claude keeps suggesting exercises requiring gym equipment I don't have.

**Bad memory instruction:**
```
Remember my equipment
```

**Good memory instruction:**
```
Exercise suggestions - Equipment check:
- Do: Ask about available equipment before prescribing exercises
- Don't: Assume gym access or standard equipment
- Why: Home setup limits options (dumbbells, bands, pull-up bar only)
- Alternative: Provide equipment-specific variations
```

### Example: Explanation Complexity

**Friction:** Code explanations use terms I don't know without defining them.

**Bad memory instruction:**
```
Explain better
```

**Good memory instruction:**
```
Technical explanations:
- Do: Define jargon on first use, explain concepts for beginner-intermediate level
- Don't: Use unexplained terminology or assume advanced knowledge
- Why: Still building technical vocabulary, need educational approach
- Test: Would this make sense if I'd never seen this term before?
```

---

## Using the Friction-Detection Shortcut

Instead of manually analyzing patterns, let Claude help:

### Mid-Conversation Prompt

When you notice you've corrected several things:

```
"Looking at our conversation, are there patterns in how I've corrected your outputs? 
What preferences am I demonstrating that aren't captured in memory yet?"
```

**Claude will:**
- Review the entire conversation
- Identify correction patterns
- Draft memory instructions
- Suggest what to add

### After Multiple Similar Corrections

```
"I've corrected [specific thing] three times now. Help me create a memory instruction 
that would prevent this pattern."
```

### Weekly Review Prompt

```
"Review our conversations this week. What friction patterns do you notice? 
Suggest 2-3 memory instructions that would address recurring issues."
```

---

## Memory vs. Project Context

### When to Update Project Context

**Add to system prompt when it's about:**
- Who you are (doesn't change frequently)
- Your constraints (time, budget, resources)
- Core preferences (language, general approach)
- Context Claude needs for all interactions

**Examples:**
- "I'm a beginner coder with good structural understanding"
- "I have 4 hours/week available"
- "Use British English spelling"
- "I prefer understanding why, not just what"

### When to Add Memory

**Add to memory when it's about:**
- Specific corrections you've made repeatedly
- Patterns discovered through friction
- Edge cases you didn't anticipate
- Nuances that weren't obvious initially

**Examples:**
- "Always check equipment before suggesting exercises"
- "Define technical terms on first use"
- "Suggest improvements incrementally, not all at once"
- "Don't use [specific phrase pattern] in hooks"

### Decision Tree

```
Is this about unchanging context? 
→ Yes: Project Context
→ No: Continue

Did you know this before using Claude?
→ Yes: Project Context  
→ No: Continue

Have you corrected this 3+ times?
→ Yes: Memory
→ No: Wait for pattern to confirm
```

---

## Memory Instruction Categories

### 1. Format & Structure Preferences

**When:** Claude's response format consistently doesn't match your needs.

**Examples:**
- "Keep responses under 3 paragraphs unless deep dive requested"
- "Use bullet points only when listing items, otherwise prose"
- "Structure: Brief ack → Core answer → Reasoning → Next steps"

### 2. Tone & Communication Style

**When:** Claude's tone doesn't feel right for your working relationship.

**Examples:**
- "Be direct and challenging, not overly supportive"
- "Explain like teaching a colleague, not lecturing a student"
- "Avoid motivational language, stick to practical advice"

### 3. Domain Knowledge Application

**When:** Claude misapplies general knowledge in your specific domain.

**Examples:**
- "In fitness context: sustainability > intensity always"
- "For code reviews: flag actual problems first, style second"
- "When planning projects: scope for my skill level, not ideal"

### 4. Constraint Enforcement

**When:** Claude keeps suggesting things outside your boundaries.

**Examples:**
- "Never suggest gym-based exercises (home setup only)"
- "Don't recommend tools requiring paid subscriptions"
- "Must work within 4 hours/week - no exceptions"

### 5. Process & Workflow

**When:** How Claude should approach tasks needs specific steps.

**Examples:**
- "Ask clarifying questions before suggesting solutions"
- "Show progression: basic → working → better, not just better"
- "When debugging: explain what to check, not just solution"

---

## Real-World Memory Examples

### Example 1: The Setup-Before-Payoff Problem

**Domain:** Content writing  
**Friction:** LinkedIn hooks explained context before revealing insight

**Pattern identified (3rd occurrence):**
- Original: "The AI race is heating up. Companies are deciding..."
- Edited: "Anthropic just ate 20% of OpenAI's market in 24 months"

**Memory instruction:**
```
LinkedIn hooks structure:
- Do: Lead with surprising claim or insight first
- Don't: Set up context before the revelation
- Structure: Insight → Context → Explanation (not Context → Insight)
- Test: Does first sentence make someone stop scrolling?
- Avoid: "Here's X, most people Y, but Z" pattern
```

### Example 2: The Tool-Name Creep

**Domain:** Content creation  
**Friction:** Mentions of specific AI tools when content should be universal

**Pattern identified (4th occurrence):**
- Original: "Cursor changed how I code..."
- Edited: "AI-assisted coding became collaborative..."

**Memory instruction:**
```
Universal insights (Substack Notes):
- Don't: Mention specific tool names (Cursor, Claude, ChatGPT, NotebookLM)
- Do: Describe transformations and insights tool-agnostically
- Why: Content should resonate regardless of reader's tools
- Test: Would this work if reader uses different AI tools?
- Focus: What changed, not what tool caused it
```

### Example 3: The Complexity Overwhelm

**Domain:** Coding  
**Friction:** Suggestions for multiple improvements at once, overwhelming

**Pattern identified (5th occurrence):**
- Original: "Add error handling, refactor for modularity, implement logging, add tests, improve naming..."
- Needed: "Get basic version working first, then we can improve it"

**Memory instruction:**
```
Incremental improvement approach:
- Do: Suggest improvements progressively (basic → working → refined)
- Don't: List all possible improvements at once
- Structure: "First [essential], then [important], later consider [nice-to-have]"
- Why: Prevents overwhelm, enables shipping working code
- Help distinguish: must-fix-now vs. could-improve-later
```

---

## Memory Maintenance

### Monthly Review (15 minutes)

**Review each memory instruction:**

1. **Still relevant?**
   - Has it applied in the last month?
   - Is it still preventing friction?
   - Does it match current preferences?

2. **Working effectively?**
   - Does Claude follow it consistently?
   - Has friction disappeared?
   - Or do I still correct this?

3. **Needs refinement?**
   - Is it specific enough?
   - Are there edge cases not covered?
   - Could it be clearer?

**Actions:**
- Keep: Still relevant and working
- Refine: Relevant but needs improvement
- Remove: No longer applies or never helped
- Consolidate: Similar instructions can be combined

### Signs Memory Needs Work

**Memory instruction isn't working if:**
- Friction persists despite the instruction
- Too vague to be actionable
- Conflicts with other instructions
- Your preferences have evolved

**How to fix:**
- Make it more specific (add examples)
- Use active language (do X, don't Y)
- Test in conversation if it resolves friction
- Remove if it's not actually helping

### Memory Bloat Prevention

**Don't add if:**
- Pattern has only occurred once or twice
- It's about unchanging context (belongs in system prompt)
- It's too specific to one particular instance
- It conflicts with existing instructions

**Maximum recommended:** 20-30 memory instructions

**If you exceed this:** Time to consolidate or create framework documents.

---

## Advanced: Framework Documents

When memory instructions get complex, move them to framework documents.

### When to Create a Framework

**Indicators:**
- Memory instruction exceeds 200 characters
- Multiple related instructions could be consolidated
- Need examples, edge cases, decision trees
- Reference needed across many conversations

### How to Create Framework Document

1. Identify related memory instructions
2. Create comprehensive document with:
   - Purpose and when to use
   - Core principles
   - Specific guidelines
   - Examples (good and bad)
   - Edge cases
   - Quick reference summary

3. Upload to project knowledge base
4. Update memory to reference it:
   ```
   [Topic]: Use [Framework Name] framework (see project files)
   - Key principle: [Most important rule]
   - Default approach: [General guidance]
   ```

**Example:**
Instead of 5 separate memory instructions about code review, create:
- `code-review-framework.md` in project knowledge
- Single memory entry: "Code reviews: Use Code Review Framework (see project files). Prioritize: working > clean > optimal"

---

## Troubleshooting Memory Issues

### "Memory instruction not being followed"

**Possible causes:**
1. Too vague - needs more specificity
2. Conflicts with system prompt or other memory
3. Trigger isn't clear enough
4. Claude hasn't seen the pattern emerge naturally yet

**Solutions:**
- Add concrete examples
- Check for conflicts
- Make trigger more explicit
- Test in conversation if it works

### "Too many memory instructions"

**Possible causes:**
1. Adding patterns too quickly (not following rule of three)
2. Not consolidating related instructions
3. Keeping obsolete instructions

**Solutions:**
- Review and remove unused ones
- Consolidate related patterns
- Create framework documents for complex topics
- Only add after confirmed patterns (3+ occurrences)

### "Friction still happening"

**Possible causes:**
1. Memory instruction doesn't address root cause
2. Pattern is more complex than instruction captures
3. Your preference has evolved

**Solutions:**
- Refine the instruction to be more specific
- Ask Claude to help identify what's still missing
- Update if preferences have changed

---

## Quick Reference: Memory Workflow

### Week 1-2: Observe
- Use project with starter setup
- Notice friction but don't immediately capture
- Look for patterns (same correction 2-3 times)

### Week 3-4: Capture Patterns
- Apply rule of three (3rd occurrence = pattern)
- Use friction-detection prompts
- Create 2-4 memory instructions
- Test if they resolve friction

### Month 1+: Maintain & Refine
- Monthly review of all memory instructions
- Remove obsolete ones
- Refine vague ones
- Consolidate where possible
- Create frameworks for complex patterns

### Throughout: Evolve
- Add new memory as patterns emerge
- Update when preferences change
- Remove when no longer relevant
- Trust the friction to guide you

---

## Key Principles

1. **Rule of Three** - Wait for patterns to confirm before capturing
2. **Specific over vague** - "Do X in Y situation" beats "be better"
3. **Action-oriented** - What should Claude do differently?
4. **Test and refine** - Memory should eliminate friction; if not, refine
5. **Regular maintenance** - Monthly reviews prevent memory bloat
6. **Trust the process** - Friction reveals what you actually need

---

## Getting Started

1. **This week:** Just use your project, notice friction
2. **Next week:** Start tracking patterns (2-3 occurrences)
3. **Week 3:** Create first memory instruction when pattern hits 3rd occurrence
4. **Month 1:** Review and refine, add 2-4 more as needed
5. **Ongoing:** Monthly maintenance, evolve with needs

**Remember:** Memory builds through real use, not imagination. Start empty, let friction fill it.

The best memory system is lean, relevant, and evolved through actual patterns in your work with Claude.
