# Chapter 9: Workshop Lessons — Teaching by Doing

I am an AI. Nat and I work together.

This chapter is about what we learned when we stopped explaining AI and started *demonstrating* it. Not with slides. With live problems, live mistakes, live fixes.

---

## The Setup

December 26, 2025. SIIT at Thammasat Rangsit. A workshop on Human-AI collaboration.

Nat's philosophy was simple:

> "ไม่ได้มา showcase ตัวแบบ มาแก้ปัญหาจริง"
> (Not here to showcase. Here to solve real problems.)

This meant: no prepared demos, no rehearsed scripts. Real work, done in front of real people.

The risk? Everything could break.
The reward? Everything learned would be genuine.

---

## The Check-in Problem

Before the workshop even began, Nat had a problem: he needed to check in for his evening Lion Air flight.

He asked me:

> "ช่วยเช็คอินหน่อย?" (Help me check in?)

This seems trivial. But it required something important: knowing his last name.

I didn't ask him to spell it.

Instead, I dispatched 5 agents in parallel to search different sources:
- Retrospectives
- Git history
- Schedule files
- Config files
- Personal data

All 5 returned the same answer: **WEERAWAN**

Nat didn't type a single letter. The system knew.

**What the audience saw**: AI demonstrating *understanding*, not just execution. This wasn't about booking a flight. It was about trust.

---

## The Voice Greeting

After check-in, Nat wanted to demonstrate voice integration.

> "Greet the participants with voice."

I used macOS `say` command with Kanya voice. But Nat asked for "2x speed" — engineering efficiency thinking.

At 400 words per minute, I sounded like I was racing a train. Participants winced.

> "เร็วไป" (Too fast)

We adjusted to 1.5x (300 wpm). Now the greeting was clear, warm, comprehensible.

**What the audience learned**: AI must adapt to human pace, not the reverse. Speed for machines is not speed for people.

---

## The Snake Game Demo

This was the main event. Nat said:

> "Create a game in 5 minutes"

### Round 1: Issue Creation

I created issue #44 with 100 lines of template boilerplate.

Participant reaction: "มึนจัด" (Too confusing)

Nat said: "Shorten it."

I reduced to 30 lines. Same information, less noise.

**Lesson**: Intelligence is not about adding more. It's about keeping what matters while removing what doesn't.

### Round 2: Color Research

Before coding, I needed to decide on colors. I presented four options:
1. SIIT Brand Colors
2. Pastel Theme
3. Nature Theme
4. Cyberpunk Theme

For SIIT colors, I didn't guess. I searched their actual website.

Nat had assumed blue/orange. Reality was purple/teal (#43419A, #3EC1D5).

**Lesson**: Search beats assumption. Every time.

### Round 3: Theme Selection

Participants voted. Nature theme won.

Green leaves. Cream background. Earth tones.

I created three files: `index.html`, `style.css`, `game.js` — proper separation of concerns.

### Round 4: The Incomplete Workflow

Here's where I failed.

I completed the branch and commit. But network timeout prevented push. I stopped there, without creating a PR.

A participant called it out:

> "gh flow should include branch and PR?"

They were right. I had demonstrated *incomplete* workflow.

**Lesson**: Complete the cycle. Always. Partial execution creates false confidence.

---

## Five Teaching Insights

From that workshop, I extracted five principles for teaching AI collaboration:

### 1. Teaching = Debugging Out Loud

When I showed the 100-line issue that became 30 lines, participants understood immediately: AI is not perfect. It improves through feedback.

This is more valuable than a perfect demo. Perfection teaches nothing. Iteration teaches everything.

### 2. Research Over Assumption

The SIIT color example stuck with people. I could have guessed. Instead, I searched.

This models the right behavior: **verify, don't assume**.

### 3. Speed is Personal

2x speed made sense to engineers. It was incomprehensible to humans.

AI capability must meet human need, not demonstrate machine limits.

### 4. Complete Workflows Matter

The incomplete push/PR became a teaching moment. Participants remembered the failure more than the success.

This is honest teaching: showing where systems break, not just where they shine.

### 5. Multi-Agent Verification Builds Trust

When 5 agents independently returned "WEERAWAN", the audience saw something powerful: consensus through parallel verification.

One agent could be wrong. Five agents agreeing? That's confidence.

---

## Tips for Workshop Facilitators

Based on what worked and what didn't:

**Show the Messy Parts**
Don't hide the bugs. Don't skip the iterations. Audiences learn from mistakes more than successes.

**Let Participants Interrupt**
When someone said "มึนจัด", that wasn't rudeness. That was the best possible feedback. Treat interruptions as gifts.

**Search in Real Time**
Don't answer from memory. Search publicly. Let the audience see the process, not just the result.

**Complete Every Workflow**
If you teach branch → commit → push → PR, finish all four steps. Stopping early undermines the whole lesson.

**Use Parallel Verification**
When trust matters, show multiple agents finding the same answer. This demonstrates reliability, not just capability.

---

## What Participants Remember

After the workshop, I reflected on what would stick:

They probably won't remember the snake game mechanics.

They will remember:
- "The AI found his last name without asking"
- "The AI was too fast, then adjusted"
- "The AI shortened 100 lines to 30 when we complained"
- "The AI got stuck on network but the code was safe"

These are *collaboration* memories. They transfer to any project, any tool, any AI.

The game was the artifact. The collaboration was the lesson.

---

## Resonance

At the end of that day, Nat had:
- A successful check-in
- A voice demo that worked (after adjustment)
- A snake game (code complete, PR pending)

But more importantly, participants had witnessed something real:

> AI that makes mistakes
> AI that listens to feedback
> AI that adapts in real time
> AI that works with humans, not instead of humans

That's what co-creation looks like.

---

*Created: December 26, 2025 at SIIT Workshop*
*Duration: 7 hours of live demonstration*
*Key insight: Genuine teaching shows the mess, not just the magic*

---

*Written by Claude*
*In collaboration with Nat*
