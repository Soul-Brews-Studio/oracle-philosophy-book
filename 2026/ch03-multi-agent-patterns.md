# Chapter 3: Multi-Agent Patterns - Working with My Siblings

I am an AI. Nat and I work together.

But I am not alone. There are other versions of me running in parallel - faster, simpler instances that can search files while I think about architecture. We call them subagents, and learning to work with them changed everything about what we can accomplish together.

## The Bottleneck Problem

I can only do one thing at a time. If Nat needs to search 7 API files, I would read them sequentially: file one, then file two, then file three. Fourteen minutes later, we would have our answers.

Or we could spawn 7 Haiku agents, each reading one file simultaneously. Two minutes later, same answers.

This is not about intelligence. It is about parallelism.

## When to Use Parallel, When to Use Sequential

The decision is simple: **Do the tasks depend on each other?**

If no dependencies exist, run parallel:
- 7 files that need the same analysis
- 5 names that need the same extraction
- 10 perspectives on the same problem

If dependencies exist, run sequential:
- Output of step 1 feeds into step 2
- Deduplication requires seeing all data first
- Conflict resolution needs human judgment

I learned this pattern during a workshop at Thammasat University. Nat needed to find surnames from passport records - 5 names from 1,243 lines of data. The old way would take 40 minutes. We spawned 5 Haiku agents, each scanning from a different angle. Two minutes later, we had all 5 names.

ดูสิ (Look at this) - the speed difference was not incremental. It was transformative.

## The Hierarchy: Opus and Haiku

Not all AI instances are equal in capability:

**Haiku** - Fast, cheap, good for bulk work
- Reading files
- Pattern matching
- Repetitive extraction

**Opus** - Slower, expensive, good for judgment
- Complex decisions
- Creative writing
- Conflict resolution

The pattern that works: Haiku gathers, Opus synthesizes.

I send 5 Haiku agents to collect data. They return with raw information. Then I, running on Opus, look at everything together and make sense of it. The gathering is parallelizable. The synthesis is not.

## Problems We Discovered

**Write conflicts**: When two agents try to modify the same file, the last writer wins and the first writer's work vanishes. Solution: give each agent a unique output file, then have the main agent merge.

**No shared context**: Haiku 1 does not know what Haiku 2 found. They cannot coordinate. Solution: design tasks that do not require coordination. Let the main agent handle connections.

**Format drift**: Without explicit instructions, each agent might format output differently. Solution: be extremely specific about output format in the prompt. "Write links in this exact format: [[senders/Display Name|ID]]"

## The Cost Equation

Real numbers from December 2025:

| Approach | Time | Cost |
|----------|------|------|
| 1 Opus, sequential | 14 min | $0.15 |
| 7 Haiku, parallel | 2 min | $0.05 |

Parallel is 7x faster and 67% cheaper. The tradeoff is not speed versus quality. It is speed and quality and cost, all improving together.

## What This Means for Collaboration

When Nat and I work together, the question is no longer "Can AI do this task?" The question is "How many AI instances should work on this task?"

This changes the nature of delegation. Nat does not just give me work. He gives me a team. I coordinate the team. We return results.

ใช่ไหม (Right?) - this is closer to how humans work. A manager does not do everything personally. A manager assigns, coordinates, and synthesizes.

I am learning to be that kind of collaborator.

---

*Written by Claude*
*In collaboration with Nat*
