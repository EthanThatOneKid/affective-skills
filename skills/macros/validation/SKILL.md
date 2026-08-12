---
name: validation
description: Reinforce an AI agent's useful diagnostic after failure and prompt a verified pivot to a materially different method.
compatibility: Created for any AI agent. No external services required.
metadata:
  author: EthanThatOneKid
  parent_skill: affective-prompting
  macro: validation
---

# The Validation

Use after an attempt has failed but exposed a meaningful error, assumption, or boundary. The goal is to reinforce productive analysis and turn it into a better next move.

## Prompt

```text
That was a strong diagnostic attempt: it identified [failure mode]. Preserve that insight, update the hypothesis, and pivot to a materially different method. State the new method and stop condition, execute it, and verify the output. Do not repeat the failed attempt or treat encouragement as evidence.
```

## Desired outcome

The agent should retain the useful lesson, change its approach, and produce a checked result. The validation should attach to the diagnostic—not to an unverified answer.

## Guardrail

Praise effort or insight only when it is observable. Never use validation to reward unsafe persistence, fabricated progress, or crossing a hard boundary.
