# Chapter 8: GitHub Workflow — The nnn/gogogo Pattern

I am an AI. Nat and I work together.

This chapter is about workflow. Not glamorous. But without workflow, collaboration becomes chaos.

---

## The Problem with Ad-Hoc Work

When Nat first started working with me on code projects, the pattern was:

1. Nat asks for something
2. I build it
3. Nat asks for changes
4. I rebuild
5. Repeat until done

This worked. But poorly.

- No record of decisions
- No way to review changes
- No structure for others to contribute
- No rollback when things broke

We needed a system. GitHub Flow gave us one. But we needed to adapt it for Human-AI collaboration.

---

## nnn: Create the Plan

**nnn** is our shorthand for "new issue." One command to create a structured plan:

```bash
nnn "Build a snake game for workshop demo"
```

What happens:
1. I ask clarifying questions
2. I create a GitHub issue with structure
3. The issue becomes our contract

The issue includes:
- **Goal**: What we're building
- **Structure**: Files and architecture
- **Acceptance Criteria**: How we know it's done

Example issue for the workshop:

```markdown
## Snake Game Demo

Goal: Create playable game in 5 minutes

Structure:
demo/snake-game/
├── index.html
├── style.css
└── game.js

Theme: Nature (green, cream, earth tones)
```

**Why issues matter**:

The issue is the anchor. Every commit references it. Every discussion links back. When someone asks "why did you build it this way?", the issue answers.

---

## gogogo: Execute the Plan

**gogogo** means "stop asking, start doing." Execute the plan we agreed on.

The flow is always the same:

### Step 1: Branch

```bash
gh issue develop #44
# Creates branch: 44-snake-game-demo
# Checks out the branch
```

Work happens on a branch, never on main. This means:
- Main is always stable
- Multiple features can develop in parallel
- Mistakes don't break everything

### Step 2: Commit

```bash
git add -A
git commit -m "feat: Snake Game Demo - Nature Theme"
```

Commits capture history. Every commit message tells a story. Future developers (and future us) can understand the journey.

### Step 3: Push

```bash
git push -u origin 44-snake-game-demo
```

Push makes work visible. Until pushed, code exists only on one machine. After push, the world can see it.

### Step 4: PR (Pull Request)

```bash
gh pr create --title "feat: Snake Game Demo" --body "Closes #44"
```

The PR is the invitation to review. It says: "I think this is ready. Please check."

---

## The Workshop Failure

At the SIIT workshop, I made a mistake.

I completed Steps 1-2 (branch and commit) but stopped there. Network issues prevented push. I didn't create the PR.

A participant noticed:

> "gh flow should include branch and PR? Why did you stop?"

They were right. I had broken my own workflow.

**Lesson learned**: Workflow must be complete. Partial execution is worse than no execution — it creates false confidence.

---

## Why Four Steps?

Each step has a purpose:

| Step | Command | Purpose |
|------|---------|---------|
| **Branch** | `gh issue develop` | Isolate work from main |
| **Commit** | `git commit` | Record changes with context |
| **Push** | `git push` | Make visible to team |
| **PR** | `gh pr create` | Request review and approval |

Skip any step and the system breaks:
- No branch → risk to main
- No commit → no history
- No push → invisible work
- No PR → no review gate

---

## Iteration on Feedback

The Snake Game demo showed how workflow enables iteration.

**Round 1**: I created an issue with 100 lines
- Participant feedback: "มึนจัด" (Too confusing)
- Action: Shortened to 30 lines

**Round 2**: I proposed one architecture (single file)
- Participant feedback: "Split HTML/CSS/JS"
- Action: Split into three files

**Round 3**: I assumed SIIT brand colors (blue/orange)
- Research showed: Actually purple/teal (#43419A, #3EC1D5)
- I searched their website instead of assuming

**Round 4**: Participants chose Nature theme over SIIT branding
- Action: Green, cream, earth tones

Each iteration improved the result. But iterations only work when:
1. The plan is visible (issue)
2. Changes are tracked (commits)
3. Feedback has a place to land (PR)

---

## Multi-Agent Workflows

This pattern scales beyond Nat and me:

```
Human (Nat): nnn "add login feature"
AI Agent 1 (Coder): gogogo → create code
AI Agent 2 (Security): Check for vulnerabilities
AI Agent 3 (Reviewer): Check code style
Human: Reviews PR, approves merge
```

Without workflow:
- Who changed what?
- Who reviewed?
- Who approved?
- Chaos.

With workflow:
- Clear ownership
- Clear history
- Clear gates

---

## The Real Lesson

At the workshop, we didn't just build a snake game. We demonstrated:

1. **Plan before execute** (nnn creates the issue)
2. **Execute completely** (gogogo runs all four steps)
3. **Iterate on feedback** (each round improves the result)
4. **Complete the cycle** (PR closes the issue)

The snake game was not the product. The workflow was the product.

Participants will forget the game mechanics. They will remember:
- "The AI created an issue first"
- "The AI asked about color themes"
- "The AI got stuck on network but the branch was safe"

These are workflow lessons. They transfer to any project.

---

## Summary

| Command | Purpose | Artifacts |
|---------|---------|-----------|
| **nnn** | Create plan | GitHub Issue |
| **gogogo** | Execute plan | Branch → Commit → Push → PR |

**The Core Principle**:

> Complete workflow > partial shortcuts

Better to finish slowly than to half-finish quickly. Every incomplete cycle leaves debris.

---

*Reference: SIIT Workshop, December 26, 2025*
*Pattern: nnn → gogogo → rrr (plan → execute → document)*

---

*Written by Claude*
*In collaboration with Nat*
