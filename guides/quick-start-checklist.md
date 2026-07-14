# Quick Start Checklist

30-minute setup to get your first AI project working with the three-layer system.

---

## ☑️ Pre-Setup (5 minutes)

**Before you start:**
- [ ] Choose your project domain (health, career, coding, writing, etc.)
- [ ] Review relevant example in `/examples/` for reference
- [ ] Set up project space (Claude Project, ChatGPT GPT, Copilot repo, Gemini Gem, etc.)
- [ ] Block 30 minutes of focused time

**Important:** This checklist builds Layer 2 (Project Context). You should have already set up Layer 1 (Personal Preferences) in your account settings. If you haven't, see [Personal Preferences Guide](personal-preferences-guide.md) first.

---

## ☑️ Layer 2 Setup: The Five Essentials (25 minutes)

Fill in the starter template with these 5 sections:

### 1. Context: Who You Are & What You're Doing (5 min)
- [ ] Describe your role and relevant background (3-5 sentences)
- [ ] Current skill level in this domain
- [ ] What you're working on specifically
- [ ] How you learn best

**Example:** "I'm focused on building sustainable fitness habits after previous intense programmes failed. Currently beginner level for most movements, but I understand training principles..."

---

### 2. Constraints: What You're Working Within (5 min)
- [ ] **Time available:** Be specific (hours/week, schedule patterns)
- [ ] **Resources:** Equipment, budget, tools you have access to
- [ ] **Limitations:** Skills gaps, physical constraints, other barriers

**Example:** "4-5 hours/week total, variable schedule, home setup with dumbbells and resistance bands, no gym membership..."

---

### 3. Goals: What You're Trying to Achieve (5 min)
- [ ] List 3-5 specific, concrete objectives
- [ ] Make them measurable if possible
- [ ] Include timeline if relevant

**Example:** "Train consistently 4x/week for 3+ months, build foundational strength progressively, maintain high energy levels throughout workday..."

---

### 4. Preferences: How You Want to Work (5 min)
**Project-specific preferences only** (universal preferences go in Layer 1)

- [ ] **Communication:** Detail level, explanation style for THIS domain
- [ ] **Approach:** Methodology preferences for THIS project
- [ ] What matters most to you in THIS area

**Example:** "Explain concepts but don't oversimplify, evidence-based recommendations over hype, clear progression schemes..."

**Note:** Don't include universal standards like "Use British English" - those belong in Layer 1 (Personal Preferences).

---

### 5. Red Flags: What Won't Work (5 min)
- [ ] List things that definitely won't work for you
- [ ] Be specific about constraints
- [ ] Include past failures to avoid

**Example:** "Don't suggest gym-based programmes, avoid 5-6 day/week routines, don't assume unlimited time..."

---

## ☑️ Implementation (5 minutes)

### Add to Your AI Platform

**Platform-specific locations:**

**Claude:**
- [ ] Open Project → Settings → Custom Instructions
- [ ] Paste your five essentials
- [ ] Save

**Claude Code:**
- [ ] Paste your five essentials into project `./CLAUDE.md`
- [ ] Commit it, see [claude-code-memory-guide.md](claude-code-memory-guide.md) for the full hierarchy

**ChatGPT:**
- [ ] Create new GPT or use Custom Instructions
- [ ] Paste your five essentials
- [ ] Save

**GitHub Copilot:**
- [ ] Create `.github/copilot-instructions.md` in your repository
- [ ] Add your five essentials
- [ ] Commit to repo

**Gemini:**
- [ ] Create a new Gem
- [ ] Add your five essentials as Gem instructions
- [ ] Save

**API:**
- [ ] Include as system message in your requests

---

## ☑️ Initial Testing (5 minutes)

### Test with 2-3 typical questions:
- [ ] Ask something typical for your domain
- [ ] Check if AI understands your context
- [ ] Verify response is at the right level
- [ ] Confirm tone feels appropriate

### Quick validation:
- [ ] Does it acknowledge your constraints?
- [ ] Are suggestions actually feasible for you?
- [ ] Is the detail level right?

**If something feels off:** Note it, but don't revise yet. Use for a week first - friction will tell you exactly what to fix.

---

## ☑️ Week 1: Use & Track Friction (5 min daily)

**Your only job this week:** Use the AI normally and track friction.

### Daily practice:
- [ ] **Day 1:** Use normally, notice any friction
- [ ] **Day 2:** Use normally, watch for patterns
- [ ] **Day 3:** Use normally, note recurring issues
- [ ] **Day 4:** Use normally, continue tracking
- [ ] **Day 5:** Use normally, identify patterns (Rule of Three)
- [ ] **Day 6-7:** Use normally, prepare for review

### Simple friction tracking:
```
Date: [When]
Issue: [What was wrong]
Count: [1st time / 2nd time / 3rd time]
```

**Remember the Rule of Three:**
- 1st occurrence: Could be a fluke
- 2nd occurrence: Maybe a pattern
- 3rd occurrence: Definitely a pattern → capture in Layer 3

---

## ☑️ Week 1 Review: Build Layer 3 (15 minutes)

**After one week of use, review your friction log:**

### Identify patterns (Rule of Three):
- [ ] What did you correct 3+ times?
- [ ] What suggestions consistently missed the mark?
- [ ] What did AI assume incorrectly repeatedly?

### Create memory instructions:
- [ ] Use this prompt: "I've noticed I keep correcting [specific thing]. This is the third time. Can you help me create a memory instruction?"
- [ ] Format each as: When [situation] → Do [action] → Don't [avoid] → Why [reason]
- [ ] Aim for 1-3 memory instructions this first week

### Add to Layer 3 (Project Memory):

**Claude:**
- [ ] Project → Memory → Add instruction

**Claude Code:**
- [ ] Mostly automatic, Claude writes these for you. Say "remember this" for anything urgent, or see [claude-code-memory-guide.md](claude-code-memory-guide.md)

**ChatGPT:**
- [ ] Use Memory feature or append to GPT instructions

**GitHub Copilot:**
- [ ] Append to `.github/copilot-instructions.md`

**Gemini:**
- [ ] Append to Gem instructions

**Test:**
- [ ] Ask something that previously caused friction
- [ ] Verify the pattern is now addressed

---

## ☑️ Common Week 1 Friction Patterns

Watch for these common issues:

### AI assumes wrong context:
- [ ] Suggests things requiring resources you don't have
- [ ] Assumes higher/lower skill level than actual
- [ ] Ignores your stated constraints

**Fix:** Check if Layer 2 (Context, Constraints) was specific enough. If yes, add to Layer 3 after 3rd occurrence.

### Response style issues:
- [ ] Too detailed when you need quick answers
- [ ] Too technical or too simplified
- [ ] Wrong format (bullets vs prose)

**Fix:** Check Layer 1 (Personal Preferences). If this is project-specific, add to Layer 2 Preferences or Layer 3 after pattern confirms.

### Suggestions don't fit your approach:
- [ ] Technically correct but not aligned with your philosophy
- [ ] Violates your stated principles
- [ ] Doesn't match your priorities

**Fix:** Check Layer 2 (Goals, Red Flags). Consider adding optional Decision Framework section after Month 1 if pattern persists.

---

## ☑️ Month 1 Maintenance (30 minutes monthly)

**Monthly review checklist:**

### Review what happened:
- [ ] What worked well? (keep it)
- [ ] What caused persistent friction? (fix it)
- [ ] What patterns emerged? (capture in Layer 3)

### Update layers as needed:
- [ ] **Layer 1:** Have any universal preferences changed?
- [ ] **Layer 2:** Has your situation changed? (goals, constraints, context)
- [ ] **Layer 3:** Add 2-5 new memory instructions from this month's friction

### Consider expansion:
- [ ] Do you need an optional section from Advanced Template?
- [ ] Only add ONE section if friction clearly reveals the need
- [ ] Don't add "just in case"

**Claude Code users:** run `/claude-md-management:claude-md-improver` for this monthly review instead of doing it by eye. It audits every CLAUDE.md in the repo against a quality rubric and proposes a diff before touching anything. See [claude-code-memory-guide.md](claude-code-memory-guide.md).

### Test changes:
- [ ] Ask typical questions
- [ ] Verify friction is reduced
- [ ] Confirm nothing broke

---

## ☑️ Success Indicators

**After 1 week:**
- [ ] Less need to explain basic context
- [ ] AI understands your constraints
- [ ] Responses at appropriate level
- [ ] Identified 1-3 memory patterns

**After 1 month:**
- [ ] 3-5 solid memory instructions working
- [ ] Significantly reduced friction
- [ ] Confidence in Layer 2 structure
- [ ] Clear understanding of what works

**After 3 months:**
- [ ] All three layers working smoothly
- [ ] Minimal friction on common tasks
- [ ] Occasional refinements only
- [ ] System feels genuinely collaborative

---

## ☑️ Troubleshooting Quick Fixes

**"AI gives generic responses"**
→ Layer 2 (Context) needs more specific details about who you are and what you're doing

**"AI assumes wrong skill level"**
→ Layer 2 (Context) - explicitly state skill level with examples of what you can/can't do

**"Suggestions ignore my constraints"**
→ Layer 2 (Constraints) - be more explicit and specific, add to Red Flags

**"Same correction 3+ times"**
→ Layer 3 (Memory) - create memory instruction using friction-detection prompt

**"Not sure what belongs where"**
→ See [GLOSSARY.md](../GLOSSARY.md) - Three-Layer Decision Guide

---

## ☑️ What NOT to Do

**❌ Don't add optional sections on Day 1:**
- Operating Modes, Decision Framework, Success Metrics are NOT essentials
- These belong in Advanced Template, add after Month 1+ only if friction reveals need

**❌ Don't revise before Week 1:**
- Use the system for a full week before making changes
- Trust friction to tell you what's actually wrong

**❌ Don't add memory before 3rd occurrence:**
- Rule of Three prevents over-specification
- Many issues are one-offs that won't recur

**❌ Don't mix layers:**
- Universal standards → Layer 1 (Personal Preferences)
- Project context → Layer 2 (The Five Essentials)
- Learned patterns → Layer 3 (Memory)

---

## ☑️ Key Files Reference

**Three-layer guides:**
- **Layer 1:** [Personal Preferences Guide](personal-preferences-guide.md)
- **Layer 2:** [Project Context Guide](project-context-guide.md) (comprehensive)
- **Layer 3:** [Memory Guide](memory-guide.md) (deep dive)

**Templates:**
- **Start here:** [Starter Template](../templates/starter-template.md) (Layer 2 essentials)
- **Reference later:** [Advanced Template](../templates/advanced-template.md) (Layer 2 expansions)

**Examples:**
- **Health/Fitness:** [health-fitness-starter-example.md](../examples/health-fitness-starter-example.md)
- **Career/Coding:** [career-coding-starter-example.md](../examples/career-coding-starter-example.md)

**Other guides:**
- **Template workflow:** [Template Usage Order](template-usage-order.md)
- **Terms & concepts:** [GLOSSARY.md](../GLOSSARY.md)

---

## Quick Timeline Summary

**Today (30 min):** Set up Layer 2 (five essentials) → Test → Start using

**Week 1 (5 min/day):** Use normally → Track friction → Note patterns

**End Week 1 (15 min):** Review friction → Create 1-3 memory instructions → Add to Layer 3

**Month 1 (30 min):** Review → Update layers → Add 2-5 more memory instructions

**Ongoing:** Use → Track → Refine → Evolve

---

**Remember:** You're building three layers incrementally:

```
Layer 1 (Personal Preferences) → Set once, applies everywhere
↓
Layer 2 (Project Context) → Set today (30 min)
↓  
Layer 3 (Memory) → Build through friction (Week 1+)
```

**The system gets better through use, not through planning.**

Start minimal. Trust friction. Evolve deliberately.
