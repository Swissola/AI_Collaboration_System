# AI Project Starter Template

## Understanding What You're Building

**This template builds Layer 2: Project Context**

Before using this template, make sure you've set up **Layer 1 (Personal Preferences)** in your AI platform's account settings. Layer 1 contains universal standards that apply to ALL your AI conversations. See the [Personal Preferences Guide](../guides/personal-preferences-guide.md) if you haven't done this yet.

**The Three-Layer System:**
- **Layer 1: Personal Preferences** - Account-wide standards (set once, applies everywhere)
- **Layer 2: Project Context** - Project-specific context (what you're building with this template)
- **Layer 3: Project Memory** - Friction-learned patterns (built after using Layer 2 for a week)

---

## Quick Start: The Five Essentials (20-30 minutes)

This is your minimal viable Layer 2 setup. Fill in these five sections, use your AI for a week, then expand based on friction patterns you discover.

All examples use Health/Fitness domain for consistency.

---

### 1. Context: Who You Are & What You're Doing

```
[Describe your actual situation - not aspirational, but real]

What to include:
- Your role or focus area
- Current skill/experience level (be honest)
- What you're working on or towards
- Relevant background that affects your approach
```

**Why this matters:** Context enables the AI to understand who it's working with. The more specific you are about your actual situation (not who you wish you were), the more useful responses will be.

**Example:**
```
I'm focused on building sustainable fitness habits. Beginner level currently, with good understanding of how things should work structurally but limited practical experience. Working around a busy schedule with limited equipment access.
```

**Key pattern:** Be specific about what you CAN do and what you're STILL LEARNING. This calibrates AI responses appropriately.

*See [Appendix A](#appendix-a-additional-context-examples) for other domain examples.*

---

### 2. Constraints: What You're Working Within

```
[The reality of your situation - this is crucial for useful advice]

Time available:
- [Actual hours per day/week, not what you wish you had]

Resources:
- [Money, equipment, tools you actually have access to]
- [What you DON'T have that people might assume]

Limitations:
- [Skills you're still learning]
- [Things you've tried that didn't work]
- [Non-negotiable boundaries]
```

**Why this matters:** Constraints enable creativity. When the AI knows what you CAN'T do, it can suggest what you CAN do within those limits. Unrealistic suggestions waste time.

**Example:**
```
Time: 4-5 hours per week total, schedule varies week to week
Resources: Home equipment only (dumbbells 5-25kg, resistance bands), no gym access
Budget: £50/month maximum for equipment or guidance
Limitations: Previous attempts at intense 6-day programmes failed due to unsustainability. Must work around occasional lower back sensitivity (no current injury, just need to watch form).
```

**Critical insight:** Include what HASN'T worked before. This prevents the AI from suggesting things you've already tried and failed at.

*See [Appendix B](#appendix-b-additional-constraints-examples) for other domain examples.*

---

### 3. Goals: What You're Actually Trying to Achieve

```
[3-5 specific, concrete goals - not vague aspirations]

What makes a good goal here:
- Specific enough that you'd know if you achieved it
- Actually achievable within your constraints
- Prioritised (what matters most?)
```

**Why this matters:** Vague goals get vague advice. "Get fit" → generic fitness advice. "Train 4x/week consistently for 3 months" → specific sustainability strategies.

**Example:**
```
1. Train consistently 4x per week for 3 months (prove I can sustain a routine)
2. Increase strength on key movements (squat, deadlift, press) progressively without injury
3. Maintain high energy levels throughout workday (no afternoon crashes)
4. Build enough knowledge to understand training decisions independently (not just following blindly)
5. Create a system that adapts when my schedule changes
```

**Key pattern:** Notice how good goals are measurable (you'll know if you hit them) and realistic (they acknowledge your constraints).

*See [Appendix C](#appendix-c-additional-goals-examples) for other domain examples.*

---

### 4. Preferences: How You Want to Work

**IMPORTANT:** Only include project-specific preferences here. Universal preferences (like "Use British English") belong in Layer 1 (Personal Preferences), not here.

```
[2-4 things specific to THIS project - add more as you discover them]

Communication:
- [Technical level to assume for THIS domain]
- [What annoys you in responses for THIS type of work]

Approach:
- [What style works for you in THIS area - challenging? supportive? data-driven?]
- [Do you want explanations or just answers for THIS domain?]
```

**Why this matters:** Project-specific preferences prevent friction before it starts. These are things that matter for THIS domain but might be different in another project.

**Example:**
```
Communication:
- I'm a beginner but understand concepts - explain without talking down
- Avoid fitness industry hype and pseudoscience

Approach:
- Evidence-based recommendations over trends
- Challenge unrealistic expectations constructively
- I want to understand WHY things work, not just WHAT to do
- Sustainable > optimal; consistency > intensity
```

**Key pattern:** Include what annoys you in THIS domain. "Avoid X" is as helpful as "Do Y" for preventing friction.

**Remember:** "Use British English spelling" is Layer 1 (Personal Preferences), not here. "Avoid fitness industry hype" is Layer 2 because it's specific to the fitness domain.

*See [Appendix D](#appendix-d-additional-preferences-examples) for other domain examples.*

---

### 5. Red Flags: What Won't Work For Me

```
[What to avoid based on past experience or known preferences]

This prevents the AI from suggesting things that sound good but won't work for your situation.
```

**Why this matters:** Red flags are often more informative than goals. They tell the AI about past failures and hard boundaries, preventing wasted suggestions.

**Example:**
```
- Don't suggest gym-based programmes (no access, not getting membership)
- Don't recommend 5-6 day/week routines (tried before, can't sustain)
- Avoid suggesting I "just" do advanced movements without progression
- Don't assume unlimited time or that fitness is my top priority
- Don't recommend cutting/restrictive diets (unsustainable for me)
```

**Key pattern:** Red flags often stem from past failures. "Don't suggest X" usually means "tried X, it didn't work, learned that lesson." Share those lessons.

*See [Appendix E](#appendix-e-additional-red-flags-examples) for other domain examples.*

---

## That's Your Layer 2 Starting Point

**Next steps:**

1. Copy the above five sections
2. Fill them in for your project (20-30 minutes)
3. Add to your AI platform's project context storage:

**Where to add Layer 2 (Project Context):**
- **Claude:** Project → Custom Instructions
- **ChatGPT:** Create a GPT, or use custom instructions for conversation
- **GitHub Copilot:** Create `.github/copilot-instructions.md` file in your repository
- **Gemini:** Create a Gem with these instructions
- **API:** Include as system message in your requests

4. Use for a week
5. Track friction patterns
6. Build Layer 3 (Memory) from recurring issues

---

## The Evolution Process

### Week 1: Just Use It
- Work with your AI normally using your Layer 2 setup
- Notice when responses miss the mark
- Don't fix everything immediately - just note patterns
- Track friction using the Rule of Three

### Week 2-3: Build Layer 3 (Memory)
When you find yourself correcting the same thing 3+ times:
1. Recognize the pattern
2. Create a memory instruction (Layer 3)
3. Add it to your platform's memory storage
4. Test if it resolves the friction

**Where to add Layer 3 (Project Memory):**
- **Claude:** Project → Memory
- **ChatGPT:** Memory feature or append to GPT instructions
- **GitHub Copilot:** Append to `.github/copilot-instructions.md` (manual)
- **Gemini:** Append to Gem instructions (manual)
- **API:** Append to system message (manual)

### Monthly: Light Review
- What's working well? (keep it)
- What causes friction? (fix it in Layer 3)
- Has context changed? (update Layer 2)
- Any new patterns? (capture in Layer 3)

---

## Layer 3: Friction → Memory Instructions

When you notice a pattern worth capturing (3+ occurrences):

**Template for memory instructions:**
```
When [situation/trigger]:
- Do: [specific action]
- Don't: [pattern to avoid]
- Why: [reason this matters]
```

**Why this works:** Memory instructions (Layer 3) are surgical fixes for recurring problems. Not "be better generally" but "do X instead of Y in situation Z."

**Example - Equipment assumptions:**
```
When suggesting exercises:
- Do: Always ask about available equipment first
- Don't: Assume gym access or specific equipment
- Why: Prevents suggesting workouts I can't complete
```

**Layer 2 vs Layer 3:**
- **Layer 2 (Project Context):** What you knew BEFORE using the AI - "I have home equipment only"
- **Layer 3 (Memory):** What you learned AFTER using the AI - "Always ask about equipment first"

**The Pattern:** Most memory instructions follow this structure:
1. Trigger/situation (when this happens...)
2. What to do (do this...)
3. What not to do (not that...)
4. Why it matters (because...)

*See [Appendix F](#appendix-f-additional-memory-instruction-examples) for other domain examples.*

---

## What to Add Next (After Month 1+)

After using your Layer 2 essentials for a month and building some Layer 3 memory instructions, you might need to expand Layer 2 with optional sections from the [Advanced Template](advanced-template.md).

**Add ONE section at a time when friction reveals the need:**

### Consider adding if you notice:
- **Operating Modes:** You interact differently for different types of work (planning vs. execution)
- **Decision Framework:** AI suggestions work but don't align with your priorities
- **Domain Principles:** AI keeps suggesting things that violate how you think work should be done
- **Success Metrics:** You want help analyzing progress and adjusting based on data
- **Response Structure:** Specific format preferences keep recurring
- **Common Pitfalls:** You have recurring mistakes the AI should help you avoid
- **Integration:** This project connects with other areas needing coordination
- **Tools & Systems:** External tools/workflows the AI should reference

**Don't add sections "just in case" - wait for friction to reveal genuine needs.**

See [Advanced Template](advanced-template.md) for details on each optional section.

---
## Appendix A: Additional Context Examples

### Career/Coding
```
I'm transitioning into software development through self-study. No CS degree but 3 years in project management (understand working methodologies). Currently learning Python and web fundamentals. Good at picking up concepts, struggle with practical application (too much consuming, not enough building). Full-time job limits learning time.
```

### Content Creation
```
I'm building a technical writing practice focused on developer tools. Background in software but new to content creation. Understand technical subjects deeply, still developing ability to explain them clearly to varied audiences. Comfortable with written content, less so with video/audio formats.
```

### Research/Learning
```
I'm researching AI applications in education for a thesis project. Academic background but new to this specific field. Good at literature review and analysis, still developing ability to synthesise across disciplines. Working part-time, so need efficient research strategies.
```

### Business/Entrepreneurship
```
I'm a solo founder building a SaaS product. Technical background (can code) but new to business side - pricing, marketing, sales. Bootstrap mode, no funding. Strong on execution, less experienced with strategy and positioning.
```

---

## Appendix B: Additional Constraints Examples

### Career/Coding
```
Time: 8-12 hours per week outside work for learning/practice
Resources: Decent computer, VS Code, GitHub, basic dev tools. No formal mentorship currently.
Budget: ~£50/month for courses/books/tools
Limitations: No CS degree (self-taught path). Limited professional network in tech. Tendency toward tutorial hell rather than building projects.
```

### Content Creation
```
Time: 10 hours per week for content (research, writing, distribution)
Resources: Basic setup (laptop, internet, free tools). Small existing audience (~500).
Budget: Minimal - relying on free tools mostly
Limitations: No design skills (can't create complex graphics). No video/audio setup. Past attempts at daily posting led to burnout. Must balance with full-time job.
```

### Research/Learning
```
Time: 15-20 hours per week (part-time student schedule)
Resources: University library access, academic databases, supervisor meetings monthly
Budget: Student budget - minimal spending capacity
Limitations: New to this research field (strong methodology, limited domain knowledge). No lab access. Supervisor has limited availability. Thesis deadline in 8 months.
```

### Business/Entrepreneurship
```
Time: 20-25 hours per week (still have part-time job for runway)
Resources: Can code, have domain expertise. No team. Basic digital tools.
Budget: Bootstrap - £500/month for tools/services maximum
Limitations: No marketing experience. Small network. Solo founder (no cofounder). Can't afford to quit job yet. Previous startup failed (learned from it but scarred by experience).
```

---

## Appendix C: Additional Goals Examples

### Career/Coding
```
1. Build 3-4 portfolio projects demonstrating real skills (not just tutorials)
2. Develop proficiency in Python and web fundamentals to employable level
3. Make 5-10 open source contributions (build experience and visibility)
4. Land first developer role or substantial freelance projects within 12 months
5. Establish sustainable learning practice (avoid burnout whilst making progress)
```

### Content Creation
```
1. Grow from 500 to 2,000 subscribers in 6 months
2. Publish consistently (1-2x per week) for 6 months without burnout
3. Develop distinctive voice that differentiates from other creators in niche
4. Build engaged community (not just passive readers - active commenters)
5. Create content system that's sustainable long-term
```

### Research/Learning
```
1. Complete comprehensive literature review of 50+ papers in 3 months
2. Develop original framework synthesizing findings across disciplines
3. Write 60-page thesis draft by Month 6 (leaving 2 months for revision)
4. Present preliminary findings at departmental seminar
5. Build foundation for potential PhD applications (if I decide to continue)
```

### Business/Entrepreneurship
```
1. Launch MVP to 50-100 beta users within 3 months
2. Validate willingness to pay (get 10 paying customers at any price point)
3. Achieve £2,000 MRR within 9 months (enough to consider full-time)
4. Build sustainable development pace (20 hours/week, no burnout)
5. Develop basic marketing/sales competency (currently weakest area)
```

---

## Appendix D: Additional Preferences Examples

### Career/Coding
```
Communication:
- Beginner-intermediate level - explain concepts but don't oversimplify
- Avoid unexplained jargon (define terms on first use)

Approach:
- Push me toward building over consuming tutorials
- Be direct about code quality issues (I want honest feedback)
- Help me distinguish "good enough to ship" from "needs improvement"
- Challenge me when I'm overthinking instead of acting
```

### Content Creation
```
Communication:
- Assume marketing background, but new to content creation specifics
- Avoid generic writing advice - I need strategies specific to my niche

Approach:
- Be direct about what's not working (honest feedback helps me improve)
- Focus on sustainable practices over viral tactics
- Help me develop distinctive voice (not copy others)
- Encourage shipping over perfecting
```

### Research/Learning
```
Communication:
- Academic writing style acceptable
- Technical depth welcome (I can handle it)

Approach:
- Help me synthesise, not just summarise
- Challenge my assumptions and methodology
- Point out gaps in my thinking
- Balance thoroughness with efficiency (time-bound project)
```

### Business/Entrepreneurship
```
Communication:
- Technical founder - comfortable with technical topics
- Less comfortable with business/marketing jargon (explain when needed)

Approach:
- Balance ambition with realism (bootstrap constraints matter)
- Push me to talk to users (I avoid this)
- Be direct about opportunity costs
- Help me prioritise ruthlessly (I try to do too much)
```

---

## Appendix E: Additional Red Flags Examples

### Career/Coding
```
- Don't suggest bootcamps or full-time study (not financially viable)
- Don't recommend I learn 5 frameworks before building projects (leads to paralysis)
- Avoid assuming I have mentors or senior dev friends (I don't)
- Don't suggest networking events as if they're easy (I find them draining)
- Don't compare my timeline to people with CS degrees or different circumstances
```

### Content Creation
```
- Don't suggest posting daily (tried it, burned out immediately)
- Don't recommend complex video/podcast setups (no equipment, no skills, no budget)
- Avoid growth hacks that require large existing audience
- Don't suggest I "just" be more active on social media (it's draining)
- Don't recommend copying successful creators' styles (want to develop my own)
```

### Research/Learning
```
- Don't suggest methods requiring lab equipment (don't have access)
- Don't recommend extensive field research (time and budget constrained)
- Avoid suggesting I "just" email 20 experts for interviews (response rate is terrible)
- Don't assume I can extend my deadline (it's fixed)
- Don't suggest paying for expensive databases (have university access but limited)
```

### Business/Entrepreneurship
```
- Don't suggest hiring/outsourcing (bootstrap budget can't afford it yet)
- Don't recommend complex tech stack (solo founder, need to ship fast)
- Avoid suggesting I "just" raise funding (not the path I'm taking)
- Don't assume I can work 80-hour weeks (have part-time job still)
- Don't recommend enterprise sales strategies (going after SMBs)
```

---

## Appendix F: Additional Memory Instruction Examples

These are Layer 3 examples - patterns learned through friction, not part of initial Layer 2 setup.

### Code complexity:
```
When explaining code:
- Do: Assume beginner-intermediate level, define jargon on first use
- Don't: Use unexplained terminology or assume advanced knowledge
- Why: Still building technical vocabulary, need educational approach
```

### Content scope:
```
When suggesting content ideas:
- Do: Keep scope achievable for single 1,500-word post
- Don't: Suggest topics requiring 5,000-word deep dives
- Why: Need to maintain weekly publishing pace, comprehensive pieces take too long
```

### Research depth:
```
When recommending sources:
- Do: Prioritise recent peer-reviewed papers (last 5 years)
- Don't: Suggest reading entire books (no time)
- Why: Thesis needs current evidence, time-bound research window
```

### Feature prioritisation:
```
When suggesting product features:
- Do: Focus on MVP core functionality first
- Don't: Suggest nice-to-have features before basics work
- Why: Solo founder, need to ship and validate before expanding scope
```

---

## Quick Reference

**Layer 1 (Personal Preferences):** Account settings - applies everywhere
- Example: "Use British English spelling"

**Layer 2 (Project Context):** This template - project-specific context
- Example: "I'm learning Python with 8 hours/week"

**Layer 3 (Project Memory):** Built through friction - learned patterns
- Example: "When explaining code, define jargon on first use"

**Decision guide:**
- Universal across all projects? → Layer 1
- Knew it before using AI? → Layer 2
- Learned through friction (3+ times)? → Layer 3

**Next steps:**
1. Set up Layer 1 if you haven't (see [Personal Preferences Guide](../guides/personal-preferences-guide.md))
2. Fill in this template for Layer 2 (20-30 minutes)
3. Use for Week 1, track friction
4. Build Layer 3 from patterns (Week 2+)
5. Expand Layer 2 if needed (Month 1+, see [Advanced Template](advanced-template.md))

Good luck building your AI collaboration system! 🚀
