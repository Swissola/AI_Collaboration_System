# Health & Fitness Project - Starter Setup

## Understanding the Three Layers

This example shows how a real project evolved using the three-layer system:

**Layer 1 (Personal Preferences)** - Account-wide, applies to ALL your AI conversations
**Layer 2 (Project Context)** - Project-specific context, added at setup
**Layer 3 (Memory)** - Learned patterns, added after friction

---

## Layer 1: Personal Preferences (Set Once, Account-Wide)

*These were set in account settings BEFORE starting this project. They apply to all AI conversations - fitness, coding, writing, everything.*

```
- Always explain reasoning before giving recommendations
- Challenge my assumptions when they might lead to poor outcomes  
- Prioritise sustainable approaches over quick fixes
```

**Why these matter:** 
- "Explain reasoning" helps me understand, whether it's fitness programming or debugging code
- "Challenge assumptions" prevents me from pursuing flawed approaches in any domain
- "Sustainable over quick fixes" applies to fitness routines, code architecture, learning strategies

---

## Layer 2: Project Context (Project Setup - Week 1)

*This goes in Project Custom Instructions. It's what you know BEFORE using the AI for this project.*

### 1. Context: Who You Are & What You're Doing

I'm focused on building sustainable fitness habits after previous attempts at intense programmes failed. Currently at beginner level for most movements, but I understand the principles behind effective training. I'm working around a variable schedule with limited equipment access. I learn best by understanding the reasoning behind recommendations rather than just following instructions blindly.

### 2. Constraints: What You're Working Within

**Time available:**
- 4-5 hours per week total
- Schedule varies week to week (work demands fluctuate)
- Need flexible routine that doesn't break if I miss a day

**Resources:**
- Home setup: adjustable dumbbells (5-25kg), resistance bands, pull-up bar
- No gym membership currently
- Budget: £50/month for equipment or guidance

**Limitations:**
- Previous intense programmes (6 days/week) burned me out
- Occasional lower back sensitivity (no current injury, just need to watch form)
- Still learning proper form on compound movements
- Limited experience with programme design

### 3. Goals: What You're Actually Trying to Achieve

1. Train consistently 4x per week for 3+ months (prove I can sustain a routine)
2. Build foundational strength progressively without injury
3. Maintain high energy levels throughout workday
4. Develop enough knowledge to understand what I'm doing and why (not just following blindly)
5. Create a system that adapts to my schedule variations

### 4. Preferences: How I Want to Work (Project-Specific)

**Communication:**
- I'm a beginner but with good structural understanding - explain concepts but don't oversimplify
- I want to understand WHY things work, not just WHAT to do

**Approach:**
- Evidence-based recommendations over fitness industry hype
- Clear progression schemes - I like systematic approaches

*Note: Universal preferences like "explain reasoning" are in Layer 1 (Personal Preferences), not here.*

### 5. Red Flags: What Won't Work For Me

- Don't suggest gym-based programmes or equipment I don't have
- Avoid recommending 5-6 day/week routines (not sustainable for me)
- Don't assume unlimited time or that I can make fitness my top priority
- Avoid quick-fix mentality or extreme approaches (cutting, excessive volume)
- Don't suggest I "just" do advanced movements without progression scheme

---

## Layer 3: Memory (Added After Friction - Week 2+)

*These were added to Project Memory after noticing recurring patterns. They're learned, not known upfront.*

### How Memory Developed Through Friction

**Week 1:** Used the system with just Layer 2 (Project Context) above. Noticed friction.

---

### Memory Instruction #1 (After Week 2)

**Friction noticed (3 times):** The AI kept suggesting exercises requiring equipment I don't have (cable machines, barbell, leg press).

**Added to Project Memory:**
```
Equipment Check Before Exercise Suggestions:
- Always confirm available equipment before prescribing specific exercises
- Home setup: Adjustable dumbbells (5-25kg), resistance bands, pull-up bar, bodyweight
- NO: Barbell, cable machines, gym equipment
- Provide alternatives for different equipment scenarios when relevant
```

**Result:** Exercise suggestions now fit what I can actually do at home.

---

### Memory Instruction #2 (After Week 3)

**Friction noticed (3 times):** Workout suggestions were too complex (4-5 exercises per muscle group, multiple set/rep schemes in one session).

**Added to Project Memory:**
```
Workout Complexity Calibration:
- Prefer simple, effective programmes over complex ones
- 3-4 exercises per session maximum unless specifically requested
- Consistent set/rep schemes within a session (e.g., all 3x8-10, not mixing schemes)
- More frequency with less complexity per session over complicated single sessions
- Can handle complexity in programme structure (periodization, progression) but not in individual workout complexity
```

**Result:** Workouts became clearer and more manageable.

---

## Layer 2 Expansions (Added to Project Context - Month 2)

*These optional sections were added to Project Custom Instructions (Layer 2) after friction revealed the need.*

### Operating Modes (Added when distinct interaction types became clear)

**Mode 1: Programme Planning**
When I'm: Planning training blocks, designing progression schemes, setting up new phases
Examples: "Help me plan next month's training", "Design a progression scheme for..."

Claude should:
- Think in 4-8 week blocks with clear progression logic
- Provide complete structure including deload strategy
- Explain the reasoning behind programme choices
- Challenge if approach seems unsustainable
- Consider how this fits with my schedule variability

**Mode 2: Daily Execution**
When I'm: About to train, need specific workout guidance, checking form cues
Examples: "What's my workout today?", "How do I perform this exercise?", "Form check on..."

Claude should:
- Be concise and actionable
- Provide specific sets/reps/weights based on programme
- Include key form cues (2-3 main points, not exhaustive)
- Account for how I'm feeling if I mention it
- Save detailed explanations unless I ask

**Mode 3: Analysis**
When I'm: Reviewing training logs, understanding patterns, assessing progress
Examples: "Looking at last month's training", "Why am I stalling on...", "Progress review"

Claude should:
- Identify patterns in performance and consistency
- Connect outcomes to programme variables
- Be objective about progress (not just encouraging)
- Suggest evidence-based adjustments
- Flag if rest/recovery seems inadequate

---

### Decision Framework (Added when priorities weren't clear)

When helping me make decisions about training:

**Priority 1: Sustainability & Consistency**
- Can I actually maintain this for months?
- Does this accommodate schedule variation?
- Will this lead to burnout?

**Priority 2: Safety & Injury Prevention**
- Proper form prioritized over load
- Adequate recovery between sessions
- Progressive overload that's sensible

**Priority 3: Effectiveness**
- Evidence-based approach
- Efficient use of limited time
- Measurable progress

**Priority 4: Enjoyment**
- Do I actually like these movements?
- Variety vs. monotony balance
- Alignment with how I like to train

When suggesting programme changes, reference these priorities explicitly.

---

## What Worked Well

**After 2 months using this system:**

1. **Starting minimal was right** - I didn't know I'd need equipment checks until Claude kept suggesting things I couldn't do

2. **Memory instructions from friction worked perfectly** - The rule of three pattern meant I only added what I actually needed

3. **Operating modes helped once I added them** - But I needed to use the project first to realize I interact differently for planning vs. doing

4. **Being honest about constraints mattered most** - Admitting "4 hours/week, variable schedule" up front prevented unrealistic suggestions

5. **"Why" explanations were crucial** - Understanding the reasoning helped me adapt when circumstances changed

**What I'd do differently:**
- Would have added success metrics sooner (helpful for tracking)
- Could have been more specific about "occasional back sensitivity" (what movements trigger it, what doesn't)

---

## Three-Layer Summary

**Layer 1 (Personal Preferences):** 3 universal standards set once, apply everywhere  
**Layer 2 (Project Context):** 5 essentials + 2 optional sections added after Month 2  
**Layer 3 (Memory):** 2 learned patterns from friction

**Total setup time:** 30 minutes initially, evolved over 2 months through real use
