# Implementation Guide: Hybrid Approach

## Overview

This guide combines two philosophies:

**From the articles:** Structured templates, operating modes, friction-driven memory development  
**From Claude's experience:** Start minimal with context, evolve through real use, trust adaptation

The result: Start light, expand deliberately, let friction guide you.

---

## Quick Start: First 30 Minutes

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

### Step 3: Add to Claude Project (5 min)

1. Copy your filled template
2. Open your Claude Project → Settings → Custom Instructions
3. Paste the template
4. Save

### Step 4: Test (3 min)

Ask 2-3 typical questions for your domain:
- Does Claude seem to understand your context?
- Is the response at the right level?
- Does the tone feel right?

If something's obviously wrong, adjust. Otherwise, move on to using it.

---

## The Evolution Cycle

### Week 1: Use & Observe

**Goal:** See how your starter setup actually works in practice.

**What to do:**
- Use Claude normally for your project tasks
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
- Claude assumes wrong skill level (too advanced or too simple)
- Suggestions ignore your constraints (equipment, time, budget)
- Response format doesn't match your preference
- Tone doesn't feel right (too formal, too casual, etc.)

**What NOT to do:**
- Don't update your system prompt after every single response
- Don't add complex frameworks you haven't tested
- Don't copy sections from advanced template "just in case"

### Week 2-3: Identify Patterns (Rule of Three)

**Goal:** Capture friction that's actually recurring, not one-offs.

**The Rule of Three:**
- First time: Could be a fluke, just correct and move on
- Second time: Might be a pattern, note it mentally
- Third time: Definitely a pattern, time to address it

**When you hit the third occurrence:**

Use this prompt with Claude:
```
"I've noticed I keep correcting [specific thing]. This is the third time. 
Can you help me identify the pattern and create either:
1. A memory instruction to prevent this, or
2. An addition to my system prompt if it's about context?"
```

Claude will help you articulate the pattern and craft appropriate instruction.

**Example patterns people discover:**
- "Claude keeps suggesting things that require [resource I don't have]"
- "Explanations use terms I don't know without defining them"
- "Responses are more complex than I need"
- "Tone doesn't match my preference"

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

**Add when:** You notice you interact with Claude differently for different types of tasks and those differences aren't being honored.

**Signs you need this:**
- You want detailed explanation when planning but quick answers when executing
- Strategic questions need different depth than tactical ones
- Analysis mode should be more critical than implementation mode

**How to add:**
1. Identify 2-4 distinct interaction types in your actual usage
2. For each, describe: when you're in this mode, how Claude should respond
3. Include trigger examples (phrases you naturally use)
4. Test with typical questions for each mode

**Don't add if:** Claude naturally adapts to context without explicit modes.

### Decision Framework

**Add when:** Claude's priorities don't match yours when suggesting options.

**Signs you need this:**
- Claude suggests things that technically work but aren't what you'd choose
- Advice doesn't reflect what actually matters to you
- You keep having to explain "but X is more important than Y"

**How to add:**
1. Think of a recent decision Claude helped with
2. What factors did you weigh? What order?
3. List 3-5 priorities explicitly
4. Give examples of how to resolve conflicts

**Don't add if:** Claude's suggestions generally align with what you'd choose.

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

**Don't add if:** Claude's advice generally aligns with your values.

### Success Metrics

**Add when:** You want help tracking progress and making data-driven adjustments.

**Signs you need this:**
- You're tracking data and want Claude to help analyze it
- You want systematic progress review
- You need help distinguishing signal from noise

**How to add:**
1. What 2-3 metrics actually indicate progress?
2. What supporting indicators matter?
3. What early signals predict later outcomes?
4. How often should each be reviewed?

**Don't add if:** Qualitative feedback suffices for your project.

### Response Structure

**Add when:** You're consistently reformatting Claude's responses.

**Signs you need this:**
- You keep editing response format (length, structure, style)
- Claude uses bullets when you want prose (or vice versa)
- Level of detail is consistently wrong

**How to add:**
1. Describe preferred structure explicitly
2. Give examples of good vs. bad formatting
3. Specify when different formats apply

**Don't add if:** Claude's format generally works for you.

### Common Pitfalls

**Add when:** You recognize patterns in your own mistakes that Claude should watch for.

**Signs you need this:**
- You have recurring tendencies that derail progress
- You'd benefit from being called out constructively
- Past patterns predict future behavior

**How to add:**
1. Identify 2-4 mistakes you tend to make
2. Describe what they look like and why you do them
3. How Claude should spot and address them

**Don't add if:** You don't have clear recurring patterns yet.

---

## Memory vs. System Prompt: Decision Guide

When you identify a pattern to address, where should it go?

### Add to System Prompt when:
- It's about **unchanging context** (who you are, core constraints)
- It's **background information** Claude needs for all interactions
- It's a **general preference** (British English, explanation style)
- It **won't change** unless your situation changes

**Examples:**
- "I have access to [specific equipment]"
- "I'm at beginner level in [domain]"
- "I prefer explanations that include why, not just what"

### Add to Memory when:
- It's a **specific correction** you've made repeatedly
- It's a **pattern** discovered through friction
- It's an **edge case** or nuance that wasn't obvious upfront
- It **might evolve** or need refinement

**Examples:**
- "When suggesting exercises, always check equipment first"
- "Don't use terminology without defining it on first use"
- "Suggest incremental improvements, not all at once"

### Rule of thumb:
If you knew it before using Claude → System Prompt  
If you learned it through using Claude → Memory

---

## Working with Memory Instructions

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

## Troubleshooting Common Issues

### "Claude's responses are still generic"

**Likely cause:** Context section too vague

**Fix:** Add specific details about your situation:
- Current skill level with examples (can do X, still learning Y)
- Specific constraints with numbers (4 hours/week, £50/month budget)
- Concrete goals with success criteria

**Test:** Ask a domain-specific question. Can Claude answer without asking clarifying questions?

### "Claude assumes wrong skill level"

**Likely cause:** Skill level description not calibrated

**Fix:** Be more specific:
- Not just "beginner" but "beginner who understands concepts but needs practice"
- Give examples: "I understand [X] but still learning [Y]"
- Specify what you can/can't do independently

**Test:** Ask Claude to explain something. Is it at the right level?

### "Suggestions ignore my constraints"

**Likely cause:** Constraints not emphasized enough

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
- Tell Claude about the pattern
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
- Learning how Claude responds to your setup

### Week 2-3
- Identifying recurring patterns
- Adding first memory instructions (2-3)
- System starting to feel personalized
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
- ✓ Productive working relationship with Claude

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
8. **Trust adaptation** - Claude can figure out a lot from context

---

## Next Steps

1. Choose your starting template (starter recommended)
2. Fill in the five essentials (20 min)
3. Add to Claude Project (5 min)
4. Use for one week without changes
5. Apply friction-driven improvements
6. Schedule first monthly review

**Remember:** Perfect is the enemy of good. Start with 80% and iterate to 100% through real use.

The best system is one that evolved through practice, not one that tried to anticipate everything upfront.

Good luck! 🚀
