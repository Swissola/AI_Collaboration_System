# Template Usage Order - Clear Workflow

## Understanding the Three-Layer System First

Before using templates, understand what you're building:

**Layer 1: Personal Preferences (Account-wide)**
- Set once in your AI platform's account settings
- Applies to ALL your AI conversations everywhere
- See [Personal Preferences Guide](personal-preferences-guide.md)
- **Do this BEFORE starting with templates**

**Layer 2: Project Context (Project-specific)**
- What the templates help you build
- Specific to THIS project/domain
- Set up once, expand as needed
- **This is what you're doing with these templates**

**Layer 3: Project Memory (Learned patterns)**
- Built through friction after using Layer 2
- Added when patterns recur 3+ times (Rule of Three)
- See [Memory Guide](memory-guide.md)
- **Developed after Week 1 of using templates**

---

## The Standard Path (Recommended for Most Users)

### Phase 1: Set Up Layer 1 First (One-time, 20 min)

**Before using any templates:**
- [ ] Read [Personal Preferences Guide](personal-preferences-guide.md)
- [ ] Set up account-wide preferences in your AI platform
- [ ] Test that preferences apply across all conversations

**Where to set Layer 1:**
- Claude: Settings → Profile → Personal Preferences
- Claude Code: `~/.claude/CLAUDE.md` (see [claude-code-memory-guide.md](claude-code-memory-guide.md))
- ChatGPT: Settings → Personalization → Custom Instructions
- GitHub Copilot: github.com/copilot → Profile Menu → Personal Instructions
- Gemini: Account settings

**Once done, you're ready for templates.**

---

### Phase 2: Build Layer 2 with Starter Template (Week 1)
**File:** `starter-template.md`

**What to do:**
1. Read through the starter template
2. Fill in the 5 essential sections (Layer 2):
   - Context (who you are in this domain)
   - Constraints (time, resources, limitations)
   - Goals (specific objectives)
   - Preferences (how to work - project-specific only)
   - Red Flags (what won't work)
3. Add to your project's context storage:
   - Claude: Project → Custom Instructions
   - Claude Code: project `./CLAUDE.md`
   - ChatGPT: Create GPT or conversation instructions
   - GitHub Copilot: `.github/copilot-instructions.md` file
   - Gemini: Create Gem with instructions
   - API: System message
4. Use for one week
5. Notice friction (what needs correcting repeatedly)

**Why starter first:**
- Minimal setup (20-30 minutes)
- Works immediately with Layer 1
- You can't anticipate Layer 3 needs before using it
- Examples show you the pattern (Health/Fitness domain)

**Don't look at Advanced Template yet** - you don't know what you need.

---

### Phase 3: Build Layer 3 from Friction (Week 2-3)
**Still using:** Your filled starter template (Layer 2)

**What to do:**
1. Use your AI normally with your starter setup
2. When you correct the AI 3+ times for the same thing:
   - Create a memory instruction (Layer 3)
   - Add to project memory storage
3. Track patterns you notice

**The Rule of Three:**
- 1st correction: Note it
- 2nd correction: Pattern maybe?
- 3rd correction: Definitely a pattern → capture in Layer 3

**Where to add Layer 3:**
- Claude: Project → Memory
- Claude Code: mostly automatic, see [claude-code-memory-guide.md](claude-code-memory-guide.md)
- ChatGPT: Memory feature or append to GPT instructions
- GitHub Copilot: Append to repository instructions file
- Gemini: Append to Gem instructions
- API: Append to system message

**Tools you're using:**
- Layer 1: Personal Preferences (account settings)
- Layer 2: Starter template (project context)
- Layer 3: Memory instructions (project memory)
- Friction log (mental or written notes)

---

### Phase 4: Expand Layer 2 if Needed (Month 1+)
**Now you might look at:** `advanced-template.md`

**What to do:**
1. Review the "What to Add Next" section in starter template
2. Based on your friction, identify 1-2 sections you actually need
3. Open advanced template as a **reference**
4. Look at the specific section you need (e.g., Operating Modes)
5. Adapt that section to your needs
6. Add to your Layer 2 (project context storage)

**Example:**
"I notice I ask planning questions differently than execution questions. Let me check the Operating Modes section in the advanced template to add to Layer 2."

**Don't:**
- Copy the entire advanced template
- Add sections "just in case"
- Fill in everything at once

**Do:**
- Add ONE section at a time to Layer 2
- Use it for a week to see if it helps
- Only add more if friction reveals need

**Remember:** These are Layer 2 expansions, not Layer 3. They're project context you're adding deliberately, not friction-learned patterns.

---

### Phase 5: Continuous Evolution (Ongoing)
**Using:** All three layers working together

**Monthly review:**
1. Layer 1: Any universal preferences changed?
2. Layer 2: Has context changed? Need new sections?
3. Layer 3: What friction patterns emerged? Add memory instructions.
4. What's working? (keep it)
5. What causes friction? (fix it)

**The templates are tools, not destinations**

---

## Alternative Paths

### Path A: "I've Used AI Projects Before"
**Start:** Layer 1 → Starter template (Layer 2) → Layer 3
**Why:** Even experienced users benefit from structured three-layer approach
**Skip to:** Phase 4 faster (after 1 week instead of 1 month)

### Path B: "I Have Complex Needs Already"
**Start:** Layer 1 → Starter template (Layer 2)
**Also read:** Advanced template to see what's possible
**Why:** Still fill starter first, but you'll know what Layer 2 expansions to add after Week 1
**Timeline:** Phase 2 → Phase 4 (skip Phase 3 delay, but still use Rule of Three for Layer 3)

### Path C: "I Just Want to See Examples"
**Read:** Example files (health-fitness or career-coding)
**Then:** Set up Layer 1 → Start with starter template for Layer 2
**Why:** Examples show the end result of all three layers, but you still need to fill your own

---

## What Each Template Actually Is

### Starter Template = Your Layer 2 Launch Pad
- **Purpose:** Get Layer 2 (Project Context) working in 20-30 minutes
- **When to use:** Always start here (after setting up Layer 1)
- **What's in it:** 
  - 5 core sections (blank templates for Layer 2)
  - 1 example per section (Health/Fitness)
  - Appendices with other domain examples
  - Guidance on what to add next
- **Think of it as:** Minimum viable Layer 2 setup

### Advanced Template = Your Layer 2 Expansion Reference
- **Purpose:** See all possible Layer 2 expansions
- **When to use:** After Week 1+, when friction reveals needs
- **What's in it:**
  - All optional Layer 2 sections (8 different expansions)
  - 1 example per section (Career/Coding)
  - Appendices with other domain examples
  - Guidance on when to use each section
- **Think of it as:** Menu of Layer 2 options, not a to-do list

**Note:** Memory instructions (Layer 3) aren't in templates - they're built through friction using the Rule of Three.

---

## Common Mistakes to Avoid

❌ **Starting with Advanced Template**
- Too overwhelming
- You don't know what you need yet
- Wastes time on sections you won't use

❌ **Filling in Entire Advanced Template**
- Takes hours
- Most sections won't be relevant
- Over-specification creates rigidity

❌ **Never Expanding Beyond Starter**
- Misses opportunities for improvement
- Friction persists that could be fixed
- Not using system's full potential

✅ **The Right Approach:**
1. Start minimal (starter)
2. Notice friction (weeks 1-3)
3. Add deliberately (one section at a time from advanced)
4. Evolve continuously (monthly reviews)

---

## Quick Decision Tree

**Q: I'm starting a new AI project. Which template?**
A: First set up Layer 1 (Personal Preferences) if you haven't. Then starter template for Layer 2. Always.

**Q: I've used my starter setup for a week. Now what?**
A: Build Layer 3 (Memory). Did you notice friction patterns recurring 3+ times?
- Yes → Create memory instructions and add to Layer 3
- No → Keep using, wait for patterns

**Q: When do I look at Advanced Template?**
A: After Month 1+, when friction reveals you need a specific Layer 2 expansion section.

**Q: I know I need Operating Modes. Where do I find that?**
A: Advanced template. Read just that section, adapt to your needs, add to your Layer 2.

**Q: Should I read both templates before starting?**
A: Skim both to understand the system, but only fill in starter (Layer 2 essentials).

**Q: Can I skip starter and just use advanced?**
A: You can, but you'll likely over-engineer Layer 2 and waste time on sections you don't need.

**Q: How do I know when I need an advanced section?**
A: When you experience friction 3+ times that a specific section would solve.

**Q: Where does memory go?**
A: Layer 3 (Project Memory) - separate from Layer 2. Built through friction, not templates.

---

## Timeline Summary

- **Before Day 1:** Set up Layer 1 (Personal Preferences) in account settings (20 min, one-time)
- **Day 1:** Fill starter template for Layer 2 (30 min), add to project
- **Week 1:** Use it, notice friction, track patterns
- **Week 2-3:** Add memory instructions to Layer 3 for patterns (Rule of Three: 3+ occurrences)
- **Month 1:** Review friction, add 1-2 Layer 2 expansion sections if needed
- **Monthly:** Review all three layers and refine
- **Ongoing:** Evolve based on real use

---

## The Core Principle

**You cannot anticipate what you'll need before experiencing friction.**

That's why the three-layer system works:
- Layer 1: Universal standards set once
- Layer 2: Starter gets your project context working quickly
- Layer 2 Expansions: Advanced provides options when you discover needs
- Layer 3: Memory captures patterns from real use
- Evolution happens through practice, not planning

**Trust the process:**
1. Set up Layer 1 (once)
2. Build Layer 2 (starter template)
3. Use and notice friction
4. Build Layer 3 (memory from patterns)
5. Expand Layer 2 if needed (advanced sections)
6. Repeat

The templates support this process, they don't replace it.
