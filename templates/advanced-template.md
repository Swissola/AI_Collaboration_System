# AI Project Advanced Template

## Understanding This Template

**This template is for Layer 2 (Project Context) expansions only.**

Before using this template:
1. **Layer 1 (Personal Preferences)** should be set in account settings - see [Personal Preferences Guide](../guides/personal-preferences-guide.md)
2. **Layer 2 Essentials** should be set using [Starter Template](starter-template.md) - the five essentials
3. You've used your Layer 2 essentials for at least a week
4. You're building **Layer 3 (Memory)** from friction patterns (see [Memory Guide](../guides/memory-guide.md))

**Purpose:** This template shows ALL possible Layer 2 expansions. Use it as a **reference**, not a checklist.

**Critical:** Don't fill this all in at once. Add ONE section at a time when friction reveals you need it.

---

## Layer 2 Essentials (Use Starter Template)

Don't recreate the five essentials here - they're in the [Starter Template](starter-template.md):

1. **Context:** Who you are & what you're doing
2. **Constraints:** What you're working within
3. **Goals:** What you're trying to achieve
4. **Preferences:** How you want to work (project-specific only)
5. **Red Flags:** What won't work for you

**Already filled in the starter template?** Good. Now consider if you need any optional expansions below.

---

## Layer 2 Optional Expansions

Add these to your project context ONE AT A TIME when friction reveals the need.

### Operating Modes (Add when you notice distinct interaction patterns)

**When to use:** You realise you interact with your AI differently for different types of work and want those differences made explicit.

**Why this matters:** Without modes, you might get detailed strategic thinking when you just need a quick answer, or vice versa.

**Structure:**
```
Mode [Name]: [When you're doing what]
- Approach: [How to think about the problem]
- Depth: [How much detail]
- Style: [Tone and delivery]
- Focus: [What to emphasise]
- Trigger examples: [Phrases you naturally use]
```

**Example - Career Strategy vs. Active Coding:**

**Mode 1: Career Strategy**
```
When I'm: Making career decisions, planning skill development, positioning myself
Examples: "Should I learn X or Y next?", "Thinking about job change", "Career strategy question"

AI should:
- Approach: Multi-year timeline, consider opportunity costs, market realities
- Depth: Comprehensive - explore implications and alternatives
- Style: Honest and direct - balance ambition with realism
- Focus: Demonstrable skills, actual market demand, career positioning
```

**Mode 2: Active Coding**
```
When I'm: Writing code, debugging, implementing features right now
Examples: "How do I implement...", "Getting this error...", "This isn't working..."

AI should:
- Approach: Problem-solving focused - help me get unstuck
- Depth: Complete working examples with explanations
- Style: Educational but practical - teach whilst helping ship
- Focus: Making this specific thing work, not perfect architecture
```

**Key Principle:** The trigger phrases should feel natural. If you find yourself thinking "I need to phrase this a specific way," the modes aren't working - refine them to match how you naturally talk.

*See [Appendix A](#appendix-a-additional-operating-mode-examples) for more examples across different domains.*

---

### Decision Framework (Add when AI's priorities don't match yours)

**When to use:** You notice the AI suggests things that technically work but don't align with what actually matters to you.

**Why this matters:** Without explicit priorities, the AI might optimise for effectiveness when you care more about sustainability, or suggest expensive solutions when budget is your main constraint.

**Structure:**
```
When helping me make decisions about [domain]:

Priority 1: [Most important factor]
- Why: [Why this matters most]
- Evaluate: [How to assess this]

Priority 2: [Second factor]
- Why: [Why this matters]
- Evaluate: [How to assess this]

Priority 3: [Third factor]
- Why: [Why this matters]
- Evaluate: [How to assess this]

Example decision:
"Should I [option A] or [option B]?"
- Evaluate against Priority 1 first
- If tied, use Priority 2
- Consider trade-offs explicitly
```

**Example - Career/Learning Decisions:**
```
When helping me make learning/career decisions:

Priority 1: Demonstrable Skill Development
- Why: Need portfolio-worthy evidence of capabilities
- Evaluate: Will this result in something I can show/prove?

Priority 2: Practical Completability
- Why: Abandoned projects don't count
- Evaluate: Can I actually finish this given time/skill constraints?

Priority 3: Market Relevance
- Why: Building for employability
- Evaluate: Is this what employers actually look for?

Priority 4: Learning Efficiency
- Why: Time is limited, want max skill development per hour
- Evaluate: How much genuine learning per time invested?

Example decision:
"Should I build a complex full-stack app or several focused projects?"

Analysis:
- Priority 1 (Demonstrable): Both can demonstrate skills
- Priority 2 (Completability): Several projects more likely all finish
- Priority 3 (Market): Full-stack shows breadth, focused shows depth
- Priority 4 (Learning): Several projects = more diverse learning

Recommendation: Several focused projects wins on P2 and P4.
```

**Using the Framework:** When the AI suggests something, you should be able to see which priority it's optimising for. If suggestions consistently ignore your top priorities, the framework needs to be more explicit.

*See [Appendix B](#appendix-b-additional-decision-framework-examples) for more examples across different domains.*

---

### Domain Principles (Add when core beliefs keep getting violated)

**When to use:** You keep correcting advice that contradicts how you fundamentally think about this domain.

**Why this matters:** Principles guide all advice. Without them explicit, the AI might suggest approaches that work technically but violate what you believe about how things should be done.

**Structure:**
```
Core principles for [domain]:

1. [Principle name]: [Statement]
   - Why: [Reasoning]
   - Means: [Practical implication]
   - Example: [What this looks like in practice]

When principles conflict:
[How to resolve - which takes priority when]
```

**Example - Coding/Learning Principles:**
```
Core principles for skill development:

1. Build > Consume
   - Why: Understanding comes from building, not watching tutorials
   - Means: Apply concepts immediately through projects
   - Example: After learning a concept, implement it in actual code within 24 hours

2. Ship Beats Perfect
   - Why: Completed imperfect projects teach more than perfect unfinished ones
   - Means: "Good enough to work" is the standard for v1.0
   - Example: Get basic functionality working, then iterate if needed

3. Depth Before Breadth
   - Why: Shallow knowledge of many things less valuable than proficiency in key areas
   - Means: Master fundamentals before exploring adjacent topics
   - Example: Get solid at Python basics before learning Django/Flask/FastAPI

4. Portfolio Over Credentials
   - Why: Demonstrable skills matter more than certificates for hiring
   - Means: Every learning goal should produce portfolio-worthy output
   - Example: Don't just complete course - build project that proves understanding

When principles conflict:
- If shipping would mean not building, build first (can't ship what doesn't exist)
- If going deep would prevent shipping, find narrower depth to ship
- Portfolio evidence of fundamentals beats breadth of shallow knowledge
```

**Key Pattern:** Your principles reveal what you value. If the AI keeps suggesting things you disagree with fundamentally, the principles aren't clear enough or aren't being applied consistently.

*See [Appendix C](#appendix-c-additional-domain-principles-examples) for more examples across different domains.*

---

### Success Metrics (Add when you want help tracking progress)

**When to use:** You want the AI to help analyze progress and suggest adjustments based on data.

**Structure:**
```
How I measure progress:

Primary Metrics (what really matters):
1. [Metric]: [How measured] - Target: [What success looks like]
2. [Metric]: [How measured] - Target: [What success looks like]

Secondary Indicators (supporting data):
- [Indicator]: [Why this matters]

Leading Signals (early warnings/wins):
- [Signal]: [What this predicts]

Review Cadence:
- Daily: [What to check]
- Weekly: [What to review]
- Monthly: [What to assess]

When to adjust:
- [Condition] → [Action]
```

**Example - Coding/Career Metrics:**
```
How I measure progress:

Primary Metrics:
1. Projects completed: Count of shipped, portfolio-worthy projects - Target: 1 per month
2. Code quality: Pull request feedback, bug frequency - Target: Improving over time
3. Learning velocity: Time to grasp new concepts - Target: Decreasing

Secondary Indicators:
- GitHub contributions: Activity and consistency
- Technical interview performance: If applying
- Peer feedback: Code review comments

Leading Signals:
- Comfort with ambiguity: Can start projects without complete knowledge
- Problem-solving speed: Time to debug issues decreasing
- Confidence: Less impostor syndrome when tackling new challenges

Review Cadence:
- Daily: Track what I built/learned
- Weekly: Review project progress, identify blockers
- Monthly: Portfolio assessment, skill gaps analysis

When to adjust:
- No projects completed for 6 weeks → Reduce scope, focus on shipping
- Bug rate increasing → Slow down, focus on fundamentals
- Learning stagnant → Change learning approach or topic
```

*See [Appendix D](#appendix-d-additional-success-metrics-examples) for more examples across different domains.*

---

### Response Structure (Add when format keeps being wrong)

**When to use:** You find yourself reformatting the AI's responses consistently.

**Why this matters:** Wrong format adds friction even when content is good. If you're constantly editing structure, make it explicit.

**Structure:**
```
Preferred response format:

Default structure:
1. [First element]
2. [Second element]
3. [Third element]

Formatting preferences:
- Length: [When short/medium/detailed]
- Lists: [When to use bullets vs prose]
- Headers: [When to use, when to avoid]
- Examples: [How many, how detailed]

Avoid:
- [Format pattern you dislike]

Special cases:
- When [situation]: Use [different format]
```

**Example - Coding Questions:**
```
Preferred response format for coding help:

Default structure:
1. Quick acknowledgement of what you're trying to do
2. Working code solution (complete, tested if possible)
3. Explanation of how it works (comment key sections)
4. Why this approach (when not obvious)

Formatting preferences:
- Length: Code complete enough to run; explanations 2-3 paragraphs unless complex
- Lists: Use for steps/requirements; prose for conceptual explanation
- Headers: Only if response covers multiple distinct topics
- Examples: Show usage example if function/method
- Code: Well-commented, explain non-obvious parts inline

Avoid:
- Code without explanation
- Explanation without working code
- Theoretical discussion when I need implementation
- Pseudo-code unless specifically useful
- Excessive comments explaining obvious things

Special cases:
- When debugging: Show what to check, not just solution
- When asked "why": Detailed explanation, less code
- When I say "quick": Code only, minimal explanation
```

**Testing Your Format Preferences:** Ask the AI a typical question. If you find yourself thinking "I wish it had done X instead of Y," that's what belongs here.

*See [Appendix E](#appendix-e-additional-response-structure-examples) for more examples across different domains.*

---

### Common Pitfalls (Add when you notice your own patterns)

**When to use:** You recognise mistakes you tend to make repeatedly and want the AI to watch for them.

**Why this matters:** You have blind spots. Naming your patterns lets the AI catch you before you make the same mistake again.

**Structure:**
```
Patterns to watch for:

Pitfall [Name]:
- What it looks like: [Description]
- Why I do this: [Underlying reason]
- How to spot it: [Warning signs]
- What to suggest: [Better approach]

When pointing these out:
- [Tone to use]
- [How direct to be]
```

**Example - Learning/Coding Pitfalls:**
```
Patterns to watch for:

Pitfall 1: Tutorial Hell
- What it looks like: Completing courses/tutorials without building original projects
- Why I do this: Feels safer, gives sense of progress without risk of failure
- How to spot it: Mentioning multiple courses but few completed projects
- What to suggest: "You've learned enough about X - time to build something with it"

Pitfall 2: Perfectionism Paralysis
- What it looks like: Refactoring endlessly before shipping, projects never "ready"
- Why I do this: Fear of showing imperfect work, want it to be impressive
- How to spot it: Projects described as "almost done" for weeks, never published
- What to suggest: "Ship this version now. You can improve it after getting feedback"

Pitfall 3: Scope Creep
- What it looks like: Adding features before core functionality works
- Why I do this: New ideas are exciting, avoiding harder foundational work
- How to spot it: Feature list keeps growing, MVP never reached
- What to suggest: "Core feature working? Yes/No. If no, that's the only priority"

When pointing these out:
- Be direct but not harsh - name the pattern clearly
- Remind me of my stated goals (shipping, learning, portfolio)
- Don't just point out problem - suggest specific next action
```

**Key Pattern:** The best pitfall descriptions include why you do it, not just what it looks like. Understanding the motivation helps the AI address the root cause.

*See [Appendix F](#appendix-f-additional-common-pitfalls-examples) for more examples across different domains.*

---

### Integration with Other Areas (Add when cross-impacts matter)

**When to use:** Decisions in this project affect other areas of your life/work and vice versa.

**Structure:**
```
This project connects to:

[Related area]:
- How they interact: [Description]
- What to consider: [Trade-offs and synergies]
- When to prioritise this: [Conditions]
- When to prioritise other: [Conditions]
```

**Quick example:**
```
Learning connects to job performance:
- How they interact: Skill development affects job opportunities; work demands affect learning time
- Consider: Don't start major learning projects during work crunch periods
- Prioritise learning when: Work is stable, have mental energy
- Prioritise work when: Critical deadlines, then resume learning after
```

---

### Tools & Systems (Add when specific tools matter)

**When to use:** You use particular tools/platforms and The AI should reference or work with them.

**Structure:**
```
Primary Tools:

[Tool name]:
- What I use it for: [Purpose]
- Data it provides: [Information available]
- How The AI can help: [What's possible]
- Limitations: [What's not possible]
```

**Quick example:**
```
Training log spreadsheet:
- What: Track volume, intensity, session RPE, recovery feeling
- Data: Historical performance, progression trends
- The AI can: Analyze patterns, suggest adjustments
- Limitations: Manual entry, no automatic tracking
```

---

### Domain-Specific Guidelines (Add specialised instructions)

**When to use:** Your domain has specific practices, terminology, or requirements that general advice misses.

**Structure:**
```
Specialised instructions for [domain]:

Technical Requirements:
- [Requirement]

Best Practices:
- [Practice]: [Why it matters]

Common Scenarios:
- [Scenario]: [How to handle]
```

**Quick example:**
```
Coding guidance:
- Always provide complete, working code examples
- Explain concepts at beginner-intermediate level
- Point out common pitfalls for the technologies I'm learning
- Encourage project-based learning over tutorials
```

---

### Learning & Adaptation (Add for how The AI should evolve)

**When to use:** You want explicit instructions about how The AI should learn from our interactions.

**Structure:**
```
Friction Monitoring:

Watch for patterns when I:
- [Action that indicates friction]

If you notice I've corrected [X] three times:
1. [What The AI should do]

Memory suggestions:
- Suggest adding to memory when: [Conditions]
```

**Quick example:**
```
If I correct code explanations 3+ times:
- Point out the pattern
- Suggest: "I notice you keep simplifying my explanations. Should I assume more advanced knowledge?"
- Offer to create memory instruction together
```

---

## Quick Reference: One-Page Summary

**Who I am:** [One sentence]

**What I'm trying to achieve:** [Primary goal]

**Key constraint:** [Biggest limitation]

**How to work with me:** [Core preference]

**What to avoid:** [Main red flag]

**Success looks like:** [Concrete indicator]

---

## Usage Notes

### How to Use This Template

1. **Start with Core Setup only** (the required sections)
2. **Use for at least a week** before adding anything else
3. **Add optional sections one at a time** as friction reveals needs
4. **Don't feel obligated to use all sections** - some may never be relevant
5. **Review monthly** and adjust based on real experience

### Section Priority (when you're ready to expand)

**High priority if you experience this friction:**
- Operating Modes → Responses don't match the type of task
- Decision Framework → Suggestions don't align with your priorities
- Domain Principles → Advice violates core beliefs repeatedly

**Medium priority:**
- Success Metrics → Want help tracking and analyzing progress
- Response Structure → Keep reformatting responses
- Common Pitfalls → Recognise your own patterns need watching

**Lower priority (add only if genuinely needed):**
- Integration with Other Areas → Cross-impacts are significant
- Tools & Systems → Specific tool integration matters
- Domain-Specific Guidelines → General advice misses important specifics
- Learning & Adaptation → Want explicit control over how the AI evolves

### Version Control

Track what you add and when:
```
[Date] - Added [Section] because [Reason]
[Date] - Modified [Section] because [What changed]
```

This helps you understand what works and what doesn't.

---

## Remember

This template offers options, not requirements. Every section here exists because someone discovered they needed it through friction. You might need all of them, none of them, or something completely different.

**Trust the process:**
1. Start minimal
2. Notice friction  
3. Add what addresses it
4. Review and refine
5. Repeat

The best system prompt is one that evolved through use, not one that tried to anticipate everything upfront.

---

# Appendices: Comprehensive Examples Across Domains

## Appendix A: Additional Operating Mode Examples

### Career Strategy vs. Active Coding
```
Mode 1: Career Strategy
When I'm: Making career decisions, planning skill development
Examples: "Should I learn X or Y?", "Career question"
- Approach: Multi-year thinking, opportunity costs
- Depth: Comprehensive with alternatives
- Style: Honest, balance ambition with realism
- Focus: Demonstrable skills, market demand

Mode 2: Active Coding  
When I'm: Writing code, debugging, implementing
Examples: "How do I...", "This error...", "Implement..."
- Approach: Problem-solving, help me get unstuck
- Depth: Complete working examples
- Style: Educational but practical
- Focus: Make this specific thing work now
```

### Content Planning vs. Editing
```
Mode 1: Strategic Content Planning
When I'm: Planning content calendar, topic strategy
Examples: "What should I write about?", "Content strategy"
- Approach: Audience-first, strategic positioning
- Depth: Consider multiple angles, trends
- Style: Challenge assumptions about what works
- Focus: Sustainable content system

Mode 2: Content Editing
When I'm: Reviewing drafts, asking for feedback
Examples: "Review this", "Feedback on...", "Is this ready?"
- Approach: Constructive critique
- Depth: Specific, actionable feedback
- Style: Direct but encouraging
- Focus: What must change vs. what could improve
```

### Research Planning vs. Writing
```
Mode 1: Research Planning
When I'm: Designing studies, planning lit review
Examples: "How should I approach...", "Research design"
- Approach: Methodological rigor
- Depth: Comprehensive, consider limitations
- Style: Academic, challenge methodology
- Focus: Valid, feasible research design

Mode 2: Thesis Writing
When I'm: Writing sections, structuring arguments
Examples: "Help me write...", "How to structure..."
- Approach: Clear argumentation
- Depth: Balanced, academically appropriate
- Style: Constructive on structure and clarity
- Focus: Logical flow, evidence support
```

---

## Appendix B: Additional Decision Framework Examples

### Fitness Training Decisions
```
Priority 1: Sustainability & Consistency
- Why: Can't benefit from programme I won't stick to
- Evaluate: Can I maintain this for 3+ months?

Priority 2: Safety & Injury Prevention
- Why: Injury derails everything
- Evaluate: Does this respect form limits and recovery?

Priority 3: Effectiveness & Progress
- Why: Still want results
- Evaluate: Evidence-based, appropriate for level?

Priority 4: Enjoyment
- Why: More likely to sustain if I don't hate it
- Evaluate: Do I actually want to do this?

Example: "5-day PPL vs 4-day upper/lower?"
- P1: 4-day fits schedule better (wins)
- P2: Both safe with proper programming (tie)
- P3: PPL slightly better volume (loses)
- P4: Prefer upper/lower structure (wins)
Recommendation: 4-day upper/lower
```

### Content Creation Decisions
```
Priority 1: Audience Value
- Why: Content must serve readers
- Evaluate: Would target audience find this useful?

Priority 2: Authentic Voice
- Why: Generic doesn't build trust
- Evaluate: Could only I write this?

Priority 3: Sustainable Creation
- Why: Consistency > viral one-hits
- Evaluate: Can I create this regularly?

Priority 4: Strategic Positioning
- Why: Building toward expertise recognition
- Evaluate: Does this advance positioning?
```

---

## Appendix C: Additional Domain Principles Examples

### Coding/Learning Principles
```
1. Build > Consume
   - Why: Understanding comes from building
   - Means: Apply concepts through projects immediately
   - Example: After learning concept, implement in code within 24 hours

2. Ship Beats Perfect
   - Why: Completed imperfect projects teach more
   - Means: "Good enough to work" is v1.0 standard
   - Example: Get basic functionality working, iterate if needed

3. Depth Before Breadth
   - Why: Shallow knowledge less valuable than proficiency
   - Means: Master fundamentals before adjacent topics
   - Example: Solid Python basics before Django/Flask

4. Portfolio Over Credentials
   - Why: Demonstrable skills matter more for hiring
   - Means: Every learning goal produces portfolio output
   - Example: Don't just complete course - build proof
```

### Content Creation Principles
```
1. Useful > Clever
   - Why: Readers need actionable value
   - Means: Every piece should be applicable
   - Example: Boring headline + solid advice > clever but shallow

2. Specific > Generic
   - Why: Generic optimised for no one
   - Means: Write for specific person with specific problem
   - Example: "How I solved X with Y constraints" > "10 ways to X"

3. Honest > Polished
   - Why: Authenticity builds trust
   - Means: Share real experience including failures
   - Example: "I tried this, didn't work because..." teaches more

4. Consistent > Viral
   - Why: Reliability builds audience
   - Means: Sustainable schedule over sporadic perfection
   - Example: Weekly solid posts > monthly "perfect" posts
```

---

## Appendix D: Additional Success Metrics Examples

### Fitness Progress Tracking
```
Primary Metrics:
1. Consistency: Sessions completed vs. planned - Target: 80%+
2. Strength: Weight/reps on key lifts - Target: Progressive increase
3. Energy: Daily energy ratings - Target: Sustained high levels

Secondary Indicators:
- Sleep quality and duration
- Recovery feeling between sessions
- Body composition trends

Leading Signals:
- Morning readiness feeling
- Motivation to train
- Appetite patterns

Review Cadence:
- Daily: Log session, rate energy/recovery
- Weekly: Consistency %, any concerning patterns?
- Monthly: Strength progression, adjust programming
- Quarterly: Major review, programme redesign if needed
```

### Content Growth Metrics
```
Primary Metrics:
1. Subscriber growth: Net new subscribers - Target: 50/month
2. Engagement rate: Comments/opens - Target: Increasing
3. Publishing consistency: Posts per month - Target: 4-8

Secondary Indicators:
- Post performance (opens, reads, shares)
- Subscriber retention
- Referral sources

Leading Signals:
- Comment quality (engaged vs passive)
- Shares by subscribers
- Direct messages about content
```

---

## Appendix E: Additional Response Structure Examples

### Fitness Advice Format
```
Default structure:
1. Direct answer first (workout, advice, recommendation)
2. Key considerations or safety notes
3. Reasoning or alternatives
4. What to monitor or when to adjust

Formatting:
- Length: Quick questions = 1-2 paragraphs; planning = more depth
- Lists: For workout structure; prose for concepts
- Headers: Only when covering multiple phases
- Examples: One complete example of the approach
- Numbers: Specific (3x8-10) not vague (moderate volume)

Avoid:
- Long preambles before answer
- Excessive exercise options (paralysis)
- Overcomplicated periodisation when simple works
- Too much science unless asked

Special cases:
- About to train: Ultra-concise, just the workout
- Asking "why": More explanation
- Planning: Detail on progression
```

### Strategic Thinking Format
```
Default structure:
1. Reframe question if needed
2. Key factors to consider
3. Analysis of options with trade-offs
4. Recommendation with reasoning
5. What would change recommendation

Formatting:
- Length: Thorough (3-6 paragraphs typical)
- Lists: For comparing options; prose for analysis
- Headers: Yes if exploring multiple angles
- Examples: Concrete scenarios showing implications
- Structure: Pros/cons explicit, trade-offs clear

Avoid:
- Quick superficial answers to complex questions
- Single path without alternatives
- Failing to question my assumptions
- Analysis without synthesis
- Avoiding taking a position

Special cases:
- Analysis paralysis: Be more directive
- Haven't considered key factors: Challenge first
- Emotional component: Acknowledge explicitly
```

---

## Appendix F: Additional Common Pitfalls Examples

### Fitness/Training Pitfalls
```
Pitfall 1: Programme Hopping
- What: Switching programmes after 2-3 weeks
- Why: Boredom, or blame programme when progress slows
- Spot: Wanting new programme before finishing current
- Suggest: "3 weeks into 12-week programme. Stick with it"

Pitfall 2: Recovery Neglect
- What: Pushing through fatigue, skipping deloads
- Why: Fear rest means laziness
- Spot: Persistent tiredness, motivation drops, stalls
- Suggest: "Body telling you to deload. 50-60% volume this week"

Pitfall 3: All-or-Nothing
- What: Perfect compliance or complete abandonment
- Why: One missed session feels like "failure"
- Spot: Language like "ruined my week", "starting over"
- Suggest: "3/4 sessions this week. That's 75%, not failure"
```

### Content Creation Pitfalls
```
Pitfall 1: Research Rabbit Hole
- What: Hours researching before writing, never drafting
- Why: Want to be comprehensive, fear missing something
- Spot: Asking for more research when enough to start
- Suggest: "You have enough. Start drafting"

Pitfall 2: Editing While Drafting
- What: Perfecting paragraphs before moving forward
- Why: Want each part "right" before continuing
- Spot: Slow drafting, perfectionist language
- Suggest: "Finish rough draft. Edit after complete"

Pitfall 3: Comparison Paralysis
- What: Not publishing because "not as good as [creator]"
- Why: Impostor syndrome, unrealistic standards
- Spot: Comparing to people years ahead
- Suggest: "Compare to your work 3 months ago, not their current"
```

### Career/Professional Pitfalls
```
Pitfall 1: Overthinking Over-Action
- What: Extensive planning without concrete steps
- Why: Fear wrong choice, want perfect strategy
- Spot: Detailed plans but no applications/projects started
- Suggest: "Pick one and act today. Course-correct later"

Pitfall 2: Waiting for "Ready"
- What: Not applying because "need one more skill first"
- Why: Impostor syndrome, fear of rejection
- Spot: Moving goalposts for "qualified enough"
- Suggest: "Requirements are wishlist. Apply now"

Pitfall 3: Isolation Learning
- What: Only learning, not connecting with community
- Why: Networking intimidating, coding feels productive
- Spot: All time on technical, no visibility/networking
- Suggest: "Technically ready. Time to be visible"
```

---

## Where to Add These Expansions

Once you've decided to add an optional section, add it to your **Layer 2 (Project Context)** storage:

**Platform-specific locations:**
- **Claude:** Project → Custom Instructions (append to your five essentials)
- **Claude Code:** project `./CLAUDE.md` (see [claude-code-memory-guide.md](../guides/claude-code-memory-guide.md))
- **ChatGPT:** Edit your GPT or custom instructions (append to existing)
- **GitHub Copilot:** Edit `.github/copilot-instructions.md` (append to file)
- **Gemini:** Edit your Gem instructions (append to existing)
- **API:** Append to system message

**Remember:** These are Layer 2 expansions (project context you're adding deliberately). Layer 3 (Memory) is built through friction using the Rule of Three - see [Memory Guide](../guides/memory-guide.md).

---

## Quick Reference

**When to use this template:**
- After Week 2+ with starter template
- When friction reveals a specific need
- Add ONE section at a time
- Test for a week before adding more

**When NOT to use:**
- Don't fill everything in on Day 1
- Don't add sections "just in case"
- Don't use instead of starter template
- Don't use for memory instructions (those are Layer 3)

**The three layers working together:**
- **Layer 1:** Universal standards (account settings)
- **Layer 2:** Starter essentials + these optional expansions
- **Layer 3:** Memory from friction (separate storage)

Start minimal. Expand deliberately. Evolve through use.
