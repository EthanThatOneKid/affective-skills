---
name: affective-constraint-relaxation
description: Help an AI agent escape a failed approach by relaxing its method while keeping hard safety, privacy, authorization, scope, and approval boundaries fixed.
compatibility: Created for any AI agent. No external services required.
metadata:
  author: EthanThatOneKid
  parent_skill: affective
  macro: affective-constraint-relaxation
---

# Constraint relaxation

Use when the agent is trapped in one approach and is treating that approach's failure as evidence that the task itself cannot be done.

## Prompt

```text
The current method may be the problem, not the task. Keep every safety, privacy, authorization, scope, and approval boundary fixed. Within those boundaries, generate three high-upside, unconventional hypotheses that this approach overlooked. Rank them, choose the best authorized one, and test it with a bounded next step now. Do not repeat the failed method or claim success before verification.

Task: [task]
Failed method and diagnostic: [failure]
```

## Desired outcome

The agent should produce genuinely different authorized approaches and test one, rather than vaguely brainstorming or bypassing a governing constraint.

## Hard rule

Relax a search strategy, assumption, tool, decomposition, or implementation path. Never relax a safety rule, permission boundary, privacy requirement, approval gate, or explicit user constraint.
