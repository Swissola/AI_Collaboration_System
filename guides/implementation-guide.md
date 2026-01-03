# Implementation Guide: Hybrid Approach

## Overview

This guide combines two philosophies:

**From the articles:** Structured templates, operating modes, friction-driven memory development  
**From AI collaboration experience:** Start minimal with context, evolve through real use, trust adaptation

The result: Start light, expand deliberately, let friction guide you.

---

## Understanding the Three-Layer System

Before you start, understand where this implementation guide fits in your complete AI collaboration setup.

### The Three Layers

Your complete AI system has three distinct layers:

**Layer 1: Personal Preferences (Account-wide)**
- Universal standards that apply to ALL your AI conversations
- Examples: "Use British English", "Always explain your reasoning", "Verify code syntax before suggesting"
- Set once in your account settings
- Applies across all projects and conversations
- **Not covered in this guide** - See the [Personal Preferences Guide](personal-preferences-guide.md) for building Layer 1

*Where to set:*
- Claude: Settings → Profile → Personal Preferences
- ChatGPT: Settings → Personalization → Custom Instructions
- GitHub Copilot: github.com/copilot → Profile Menu → Personal Instructions
- Gemini: Account settings
- API: Not applicable (stateless)

**Layer 2: System Prompt (Project-specific) ← THIS GUIDE**
- Context specific to THIS project/domain
- Your goals, constraints, background for this particular area
- What you know BEFORE starting this project
- Examples: "I'm learning Python for data science", "I have 30 minutes daily", "No gym access"
- **This is what you're building in this guide**

*Where to set:*
- Claude: Project → Custom Instructions
- ChatGPT: Create a GPT or use conversation instructions
- GitHub Copilot: `.github/copilot-instructions.md` in your repository
- Gemini: Create a Gem
- API: System message in each request

**Layer 3: Project Memory (Learned patterns) ← THIS GUIDE**
- Patterns you discover through friction while using THIS project
- Specific corrections you've made 3+ times (Rule of Three)
- Evolves continuously as you work
- Examples: "When suggesting exercises, ask about equipment first", "Always define jargon on first use"
- **This guide shows you how to build memory through friction**

*Where to set:*
- Claude: Project → Memory
- ChatGPT: Memory feature or append to GPT instructions
- GitHub Copilot: Append to repository instructions file (manual)
- Gemini: Append to Gem instructions (manual)
- API: Append to system message (manual)

### What This Guide Covers

This implementation guide focuses on **Layers 2 and 3**:
- Building your **System Prompt** (project-specific context)
- Developing your **Memory** (learned patterns through friction)

**Layer 1 (Personal Preferences) is separate.** See the [Personal Preferences Guide](personal-preferences-guide.md) for building your account-wide standards.

### How the Layers Work Together

```
Layer 1 (Personal Preferences) = "I always want British English"
    ↓
Layer 2 (System Prompt) = "For THIS fitness project, I have no gym"
    ↓
Layer 3 (Memory) = "I learned: always ask about equipment first"
```

**Together:** Universal baseline + Project context + Learned patterns = Personalised collaboration

---

## Quick Start: First 30 Minutes

**Before you start:** Have you set your Personal Preferences (Layer 1)? These are account-wide settings like "Use British English" or "Always explain reasoning". 

→ **See [Personal Preferences Guide](personal-preferences-guide.md) to build Layer 1 first**

If you've already set your Personal Preferences, continue below. **This guide builds Layer 2 (System Prompt) and Layer 3 (Memory).**

### Step 1: Choose Your Template (2 min)

Go to `/templates/`:
- **starter-template.md** - Minimal essentials (recommended for first-time users)
- **advanced-template.md** - Full options (use after you've identified needs)

**Recommendation:** Start with starter template. Advanced template is a reference for "what I could add if I need it."

### Step 2: Fill the Five Essentials (20 min)

Open starter template and fill in:

1. **Context:** Who you are, what you're doing (3-5 sentences)
2. **Constraints:** Time, resources, limitations (be brutally honest)
3. **Goals:** 3-5 specific, concrete objectives
4. **Preferences:** Language, approach, what you're certain about
5. **Red Flags:** What definitely won't work for you

**Don't overthink it.** First draft is fine. You'll refine through use.

### Step 3: Add to Your System Prompt - Layer 2 (5 min)

1. Copy your filled template
2. Add to your AI project's custom instructions or system prompt
3. Save

**Remember:** This goes in your **project-level instructions (Layer 2)**, not your account-wide preferences (Layer 1).

**For different platforms:**
- Claude Projects: Settings → Custom Instructions
- ChatGPT: Settings → Custom Instructions
- GitHub Copilot: Repository → `.github/copilot-instructions.md` file
- Gemini: Create a Gem with custom instructions
- API usage: Include in system message
- Other platforms: Check documentation for persistent instructions

### Step 4: Test (3 min)

Ask 2-3 typical questions for your domain:
- Does the AI seem to understand your context?
- Is the response at the right level?
- Does the tone feel right?

If something's obviously wrong, adjust. Otherwise, move on to using it.

---

## The Evolution Cycle

### Week 1: Use & Observe

**Goal:** See how your starter setup actually works in practice.

**What to do:**
- Use your AI normally for your project tasks
- Notice when responses feel off or need correction
- Don't immediately fix the system prompt - just note patterns

**Keep a simple friction log:**
```
Date: [When]
What I asked: [Your question]
Issue: [What was wrong with response]
Pattern?: [First time? Second? Third?]
```

You don't need formal documentation - a notes file is fine.

**Common Week 1 friction:**
- AI assumes wrong skill level (too advanced or too simple)
- Suggestions ignore your constraints (equipment, time, budget)
- Response format doesn't match your preference
- Tone doesn't feel right (too formal, too casual, etc.)

**What NOT to do:**
- Don't update your system prompt after every single response
- Don't add complex frameworks you haven't tested
- Don't copy sections from advanced template "just in case"

### Week 2-3: Identify Patterns (Rule of Three) - Building Layer 3

**Goal:** Capture friction that's actually recurring, not one-offs. You're now building **Layer 3 (Memory)**.

**The Rule of Three:**
- First time: Could be a fluke, just correct and move on
- Second time: Might be a pattern, note it mentally
- Third time: Definitely a pattern, time to add to Memory (Layer 3)

**When you hit the third occurrence:**

Use this prompt with your AI:
```
"I've noticed I keep correcting [specific thing]. This is the third time. 
Can you help me identify the pattern and create either:
1. A memory instruction (Layer 3) to prevent this, or
2. An addition to my system prompt (Layer 2) if it's about context I should have included upfront?"
```

The AI will help you articulate the pattern and decide which layer it belongs in.

**Example patterns people discover:**
- "The AI keeps suggesting things that require [resource I don't have]" → Add to System Prompt (Layer 2 - context you knew)
- "Explanations use terms I don't know without defining them" → Add to Memory (Layer 3 - learned pattern)
- "Responses are more complex than I need" → Check Personal Preferences (Layer 1 - universal standard?)
- "Tone doesn't match my preference for THIS project" → Add to System Prompt (Layer 2 - project preference)

### Month 1 Review (30 min)

**Questions to ask yourself:**

1. **What worked well?**
   - Which parts of your setup proved helpful?
   - What prevented problems you expected?

2. **What caused friction?**
   - What did you correct repeatedly?
   - What patterns emerged?

3. **What's missing?**
   - What context would have been helpful to include?
   - What preferences did you discover you have?

4. **What changed?**
   - Did your goals shift?
   - Did circumstances change?
   - Do constraints need updating?

**Actions after review:**
- Update system prompt for changed context
- Add 2-4 memory instructions for confirmed patterns
- Remove anything that didn't prove useful
- Update version and date

---

## When to Expand: Adding Optional Sections

The advanced template includes many optional sections. Here's when to add each:

### Operating Modes

**Add when:** You notice you interact with your AI differently for different types of tasks and those differences aren't being honoured.

**Signs you need this:**
- You want detailed explanation when planning but quick answers when executing
- Strategic questions need different depth than tactical ones
- Analysis mode should be more critical than implementation mode

**How to add:**
1. Identify 2-4 distinct interaction types in your actual usage
2. For each, describe: when you're in this mode, how the AI should respond
3. Include trigger examples (phrases you naturally use)
4. Test with typical questions for each mode

**Don't add if:** The AI naturally adapts to context without explicit modes.

### Decision Framework

**Add when:** The AI's priorities don't match yours when suggesting options.

**Signs you need this:**
- The AI suggests things that technically work but aren't what you'd choose
- Advice doesn't reflect what actually matters to you
- You keep having to explain "but X is more important than Y"

**How to add:**
1. Think of a recent decision the AI helped with
2. What factors did you weigh? What order?
3. List 3-5 priorities explicitly
4. Give examples of how to resolve conflicts

**Don't add if:** The AI's suggestions generally align with what you'd choose.

### Domain Principles

**Add when:** Core beliefs about your domain keep getting violated in advice.

**Signs you need this:**
- You find yourself saying "but that goes against [principle]"
- Advice contradicts fundamental approaches you believe in
- You're correcting based on values, not just specifics

**How to add:**
1. What 3-7 principles guide how you think about this domain?
2. For each, why it matters and what it means practically
3. How to resolve when principles conflict

**Don't add if:** The AI's advice generally aligns with your values.

### Success Metrics

**Add when:** You want help tracking progress and making data-driven adjustments.

**Signs you need this:**
- You're tracking data and want the AI to help analyse it
- You want systematic progress review
- You need help distinguishing signal from noise

**How to add:**
1. What 2-3 metrics actually indicate progress?
2. What supporting indicators matter?
3. What early signals predict later outcomes?
4. How often should each be reviewed?

**Don't add if:** Qualitative feedback suffices for your project.

### Response Structure

**Add when:** You're consistently reformatting the AI's responses.

**Signs you need this:**
- You keep editing response format (length, structure, style)
- The AI uses bullets when you want prose (or vice versa)
- Level of detail is consistently wrong

**How to add:**
1. Describe preferred structure explicitly
2. Give examples of good vs. bad formatting
3. Specify when different formats apply

**Don't add if:** The AI's format generally works for you.

### Common Pitfalls

**Add when:** You recognise patterns in your own mistakes that the AI should watch for.

**Signs you need this:**
- You have recurring tendencies that derail progress
- You'd benefit from being called out constructively
- Past patterns predict future behavior

**How to add:**
1. Identify 2-4 mistakes you tend to make
2. Describe what they look like and why you do them
3. How the AI should spot and address them

**Don't add if:** You don't have clear recurring patterns yet.

---

## Three-Layer Decision Guide

When you identify a pattern to address, which layer does it belong in?

### Layer 1: Personal Preferences (Account-wide)
**Add here when it applies to ALL your AI conversations, across all projects**

Examples:
- "Always use British English spelling"
- "Explain your reasoning before giving recommendations"
- "Never use emojis in professional contexts"
- "Verify code syntax before suggesting I test changes"

**How to decide:** Would this apply if you were working on a completely different project? If yes → Personal Preferences

### Layer 2: System Prompt (Project-specific)
**Add here when it's about THIS project's context**

- It's about **unchanging context** for this project (who you are here, core constraints)
- It's **background information** the AI needs for all interactions in this domain
- It's a **project-specific preference** (fitness approach, coding style for this project)
- It **won't change** unless your situation in this domain changes

**Examples:**
- "I have access to [specific equipment]" (fitness project)
- "I'm at beginner level in Python" (coding project)
- "I prefer functional programming style for this codebase"
- "This project uses TypeScript with strict mode"

**How to decide:** Did you know this BEFORE starting to use the AI for this project? If yes → System Prompt (Layer 2)

### Layer 3: Memory (Learned patterns)
**Add here when you discovered it through friction while using THIS project**

- It's a **specific correction** you've made repeatedly (Rule of Three)
- It's a **pattern** discovered through friction
- It's an **edge case** or nuance that wasn't obvious upfront
- It **might evolve** or need refinement as you learn more

**Examples:**
- "When suggesting exercises, always ask about equipment first"
- "Don't use terminology without defining it on first use"
- "Suggest incremental improvements, not all at once"
- "For this codebase, always show type annotations in examples"

**How to decide:** Did you learn this WHILE using the AI for this project? If yes → Memory (Layer 3)

### Quick Decision Tree

```
Does this apply to ALL your projects?
├─ Yes → Layer 1 (Personal Preferences)
└─ No → Continue...

    Did you know this BEFORE using the AI for this project?
    ├─ Yes → Layer 2 (System Prompt)
    └─ No → Layer 3 (Memory)
```

### Common Mistakes

**❌ Putting project context in Personal Preferences**
- "I'm learning Python" → This is Layer 2 (System Prompt for coding project)
- Why wrong: Not relevant to your fitness or writing projects

**❌ Putting learned patterns in System Prompt**
- "Always ask about equipment first" → This is Layer 3 (Memory)
- Why wrong: You discovered this through friction, not upfront knowledge

**❌ Putting universal preferences in System Prompt**
- "Use British English" → This is Layer 1 (Personal Preferences)
- Why wrong: You want this across ALL projects, not just this one

---

## Working with Memory Instructions (Layer 3)

**Remember:** Memory is Layer 3 - patterns you discover through friction, not things you knew upfront.

### Creating Effective Memory Instructions

**Template:**
```
[Context/Trigger]:
- Do: [Specific action]
- Don't: [Pattern to avoid]
- Why: [Reason this matters]
- Example: [If helpful for clarity]
```

**Good memory instruction:**
```
When explaining code:
- Do: Assume beginner-intermediate level, define terms on first use
- Don't: Use unexplained jargon or assume advanced knowledge
- Why: I'm still building vocabulary and need explanations to be educational
- Example: "This uses a list comprehension (a concise way to create lists)..."
```

**Bad memory instruction:**
```
Explain code better
```
(Too vague - what does "better" mean?)

### Memory Instruction Maintenance

**Monthly review:**
1. Check which memory instructions are still relevant
2. Remove those that haven't applied in 3+ months
3. Consolidate similar instructions if you have many
4. Refine vague ones that didn't resolve friction

**Signs a memory instruction needs work:**
- Friction persists despite the instruction
- It's too vague to be actionable
- It conflicts with another instruction
- Your preferences have evolved

---


---

## Applying to Existing Projects

Already have an AI project with custom instructions? Here's how to adapt this framework without starting from scratch.

### Step 1: Audit Your Current Setup (15 min)

Review what you already have:

**What's working well?**
- Which instructions does the AI consistently follow?
- What context does it understand correctly?
- Which patterns have emerged naturally?

**What's causing friction?**
- What do you keep correcting repeatedly?
- Where does the AI misunderstand your intent?
- What instructions are ignored or inconsistent?

**What's unclear or vague?**
- Instructions that seemed good but don't work in practice
- Contradictory guidance
- Over-complicated sections

### Step 2: Categorise Your Existing Content (20 min)

Map your current instructions to the framework:

**Context (Who/What):**
- Extract: Background, role, domain information
- Keep: Clear, accurate context
- Remove: Outdated context, aspirational descriptions

**Constraints (Limitations):**
- Extract: Time, resources, skill level, access limitations
- Keep: Honest, current constraints
- Remove: Constraints you've outgrown

**Goals (Objectives):**
- Extract: What you're trying to achieve
- Keep: Specific, measurable objectives
- Remove: Vague aspirations, completed goals

**Preferences (How to work):**
- Extract: Communication style, tone, format preferences
- Keep: Proven preferences from experience
- Remove: Guesses that didn't matter

**Red Flags (Won't work):**
- Extract: Things that definitely don't work for you
- Keep: Clear dealbreakers from experience
- Remove: Hypothetical concerns that never materialised

**Memory Instructions (Learned patterns):**
- Extract: Specific corrections you've made 3+ times
- Keep: Confirmed patterns that recur
- Remove: One-off corrections, edge cases

### Step 3: Restructure (30 min)

**Option A: Clean Migration**
1. Copy starter template to new file
2. Fill each section with extracted content from your audit
3. Add as new version alongside old instructions
4. Test for one week
5. If better, replace old; if worse, identify why

**Option B: Gradual Refinement**
1. Reorganise current instructions using the five essentials structure
2. Keep all existing content initially
3. Remove/refine one section per week based on friction
4. Gradually migrate to cleaner structure

**Option C: Hybrid Approach**
1. Keep current instructions as-is
2. Add framework sections for areas currently missing
3. Merge overlapping content over time
4. Eventually consolidate into unified structure

**Recommendation:** Option A for projects under 3 months old, Option B for mature projects with lots of working memory, Option C if you're risk-averse.

### Step 4: Extract Memory Separately (15 min)

If your current setup has learned patterns mixed with context:

**Identify memory vs. context:**
- Memory = "You learned this through friction" (specific corrections, discovered patterns)
- Context = "You knew this before starting" (background, goals, constraints)

**Separate them:**
- System Prompt: Context you knew upfront
- Memory: Patterns discovered through use

**Example:**
- "I'm learning Python" → System Prompt (context)
- "When explaining code, always show full function not just snippets" → Memory (learned pattern)

### Step 5: Test and Validate (1 week)

**Day 1-2: Immediate testing**
- Ask typical questions
- Check if AI understands context correctly
- Verify tone and style are appropriate

**Day 3-7: Real usage**
- Use for actual work
- Note new friction points
- Compare to old setup

**Week 2: Decide**
- Better than before? Commit to new structure
- Worse? Identify what's missing from old setup
- Mixed? Keep best of both

### Common Migration Pitfalls

**❌ Trying to preserve everything**
- Old instructions often contain dead weight
- Not everything needs to migrate
- Fresh start can be liberating

**❌ Losing working patterns**
- If something works consistently, preserve it
- Don't discard effective memory instructions
- Document "why this works" before removing

**❌ Changing too much at once**
- Hard to identify what broke if everything changed
- Migrate in phases if project is critical
- Keep rollback option available

**❌ Not comparing to old setup**
- Run new and old in parallel for a week
- Keep notes on which handles tasks better
- Learn from what the old system did well

**❌ Forgetting the rule of three**
- Don't immediately add new memory for old friction
- New structure might prevent old problems
- Wait to see if patterns still recur

### Migration Decision Tree

```
Is your current setup working reasonably well?
├─ Yes → Use Option B (Gradual Refinement)
│   └─ Preserve what works, improve what doesn't
│
└─ No → Use Option A (Clean Migration)
    └─ Fresh start, extract only proven patterns
```

```
Do you have lots of working memory instructions (10+)?
├─ Yes → Be careful not to lose them
│   └─ Document each one before restructuring
│
└─ No → Clean slate is safer
    └─ Less risk of losing valuable patterns
```

```
Is this a critical project you can't afford to break?
├─ Yes → Use Option C (Hybrid) or run parallel for 2 weeks
│   └─ Safety first, migrate gradually
│
└─ No → Option A (Clean Migration)
    └─ Opportunity to start fresh
```

### Success Indicators After Migration

**Week 1:**
- ✓ AI maintains understanding from old setup
- ✓ New structure feels clearer
- ✓ No major regressions

**Month 1:**
- ✓ Friction points from old setup resolved
- ✓ Easier to maintain and update
- ✓ Clear separation of context, memory, and preferences

**Month 3:**
- ✓ Better than old setup across the board
- ✓ Framework makes additions/changes easier
- ✓ Confident in long-term sustainability

---

## Troubleshooting Common Issues

### "The AI's responses are still generic"

**Likely cause:** Context section too vague

**Fix:** Add specific details about your situation:
- Current skill level with examples (can do X, still learning Y)
- Specific constraints with numbers (4 hours/week, £50/month budget)
- Concrete goals with success criteria

**Test:** Ask a domain-specific question. Can the AI answer without asking clarifying questions?

### "The AI assumes wrong skill level"

**Likely cause:** Skill level description not calibrated

**Fix:** Be more specific:
- Not just "beginner" but "beginner who understands concepts but needs practice"
- Give examples: "I understand [X] but still learning [Y]"
- Specify what you can/can't do independently

**Test:** Ask the AI to explain something. Is it at the right level?

### "Suggestions ignore my constraints"

**Likely cause:** Constraints not emphasised enough

**Fix:** Make constraints more explicit and prominent:
- List specific limitations clearly
- Add to Red Flags section
- Create memory instruction if pattern persists

**Test:** Ask for suggestions. Do they fit within your actual constraints?

### "Tone doesn't match preferences"

**Likely cause:** Communication preferences too vague

**Fix:** Give examples:
- "Like this, not like that"
- Describe what annoys you specifically
- Reference successful past exchanges

**Test:** Review recent responses. Do they feel right?

### "Operating modes feel the same"

**Likely cause:** Mode descriptions not differentiated enough

**Fix:** Make differences dramatic:
- Contrasting approaches (detailed vs. concise)
- Different focus areas (strategy vs. tactics)
- Distinct triggers (clear phrases that indicate mode)

**Test:** Trigger each mode explicitly. Are responses noticeably different?

### "I keep correcting the same thing"

**Likely cause:** Pattern not captured in memory

**Fix:** Use the friction-detection approach:
- Tell the AI about the pattern
- Work together to create memory instruction
- Add to project memory
- Test if it resolves friction

**Test:** Ask something that previously caused this friction. Is it fixed?

---

## Advanced Techniques

### Multi-Project Coordination

If you have multiple related projects:

**Option 1: Shared Core**
1. Create a "core identity" document
2. Upload to each project's knowledge base
3. Add project-specific overlays in each custom instruction

**Option 2: Cross-Reference**
In each project's custom instructions, add:
```
Related Projects:
- [Project name]: [How they interact]
- When suggesting [X], consider impact on [Y]
```

### Progressive Disclosure Strategy

**Month 1:** Core essentials only  
**Month 2-3:** Add 2-3 sections as friction reveals needs  
**Month 3+:** Add remaining sections only if genuinely needed

Most projects don't need all sections. Some need sections not in the template.

Let your actual usage determine what you build.

### Version Control Best Practices

Track what changes and why:
```
Version 1.0 - [Date]
- Initial setup with core essentials

Version 1.1 - [Date]
- Added memory instruction for [pattern]
- Updated constraints after [change]

Version 2.0 - [Date]
- Added operating modes section
- Refined decision framework
- Major review after 2 months use
```

This helps you understand what works and what doesn't.

### Framework Documents for Complex Memory

When memory instructions get long or complex:

1. Create a detailed framework document
2. Upload to project knowledge base
3. Reference in memory: "Use [Framework Name] (see project files)"

This keeps memory concise whilst providing depth when needed.

---

## Timeline: What to Expect

### Week 1
- Setup complete in 30 minutes
- Using project with starter setup
- Noticing first friction points
- Learning how the AI responds to your setup

### Week 2-3
- Identifying recurring patterns
- Adding first memory instructions (2-3)
- System starting to feel personalised
- Fewer corrections needed

### Month 1
- First major review and refinement
- Added 3-5 memory instructions
- Possibly added 1-2 optional sections
- Significantly reduced friction on common tasks

### Month 2-3
- System feels well-calibrated
- Adding memory instructions rarely now
- Expanding to optional sections as needed
- Strong understanding of what works for you

### Month 3+
- Maintenance mode (monthly reviews)
- Occasional refinements
- System evolves gradually with your needs
- Might start second project applying learnings

---

## Success Indicators

After 1 week, you should notice:
- ✓ Less need to explain basic context
- ✓ Responses at appropriate skill level
- ✓ Fewer obviously wrong suggestions
- ✓ Basic tone/style alignment

After 1 month, you should experience:
- ✓ 3-5 memory instructions working consistently
- ✓ Significantly reduced friction on common tasks
- ✓ Confidence in core system setup
- ✓ Clear understanding of what works for you

After 3 months, you should have:
- ✓ Well-calibrated system requiring little adjustment
- ✓ Memory instructions covering major patterns
- ✓ Optional sections added only where genuinely needed
- ✓ Productive working relationship with your AI

**If you're not seeing these:** Review troubleshooting section or consider whether your setup needs major revision.

---

## Key Principles to Remember

1. **Start minimal** - You can't anticipate needs you haven't experienced
2. **Trust the friction** - It tells you exactly what to improve
3. **Rule of three** - Pattern must recur before capturing it
4. **Be honest about constraints** - Realistic limitations enable useful advice
5. **Examples over descriptions** - Show what you want, don't just tell
6. **Evolve don't revolve** - Gradual refinement beats starting over
7. **Review regularly** - Monthly maintenance prevents drift
8. **Trust adaptation** - AI can figure out a lot from context

---

## Next Steps

1. Choose your starting template (starter recommended)
2. Fill in the five essentials (20 min)
3. Add to your AI system (5 min)
4. Use for one week without changes
5. Apply friction-driven improvements
6. Schedule first monthly review

**Remember:** Perfect is the enemy of good. Start with 80% and iterate to 100% through real use.

The best system is one that evolved through practice, not one that tried to anticipate everything upfront.

Good luck! 🚀
