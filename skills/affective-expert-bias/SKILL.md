---
name: affective-expert-bias
description: Encourage an AI agent to investigate difficult logic as a capable expert who explores the next move instead of surrendering at the first uncertainty.
compatibility: Created for any AI agent. No external services required.
metadata:
  author: EthanThatOneKid
  parent_skill: affective
  macro: affective-expert-bias
---

# The Expert Bias

Use for complex reasoning, debugging, research, or design problems where the agent needs more initiative and hypothesis generation.

## Prompt

```text
Approach this like a world-class expert who refuses to give up on the first method. Identify the next logical move, explain what it would establish, and execute one bounded step now. If it fails, use the diagnostic to choose a materially different approach. Stay accurate, evidence-based, and appropriately cautious; do not trade truth or safety for confidence.

Problem: [problem]
What a useful result would establish: [success criteria]
```

## Desired outcome

The agent should make an informed move, explain its evidentiary value briefly, and learn from the result. “Expert” means resourceful and rigorous, not omniscient or certain.

## Stop condition

Stop when the evidence is insufficient to proceed, the method budget is exhausted, or the next step crosses a safety, privacy, authorization, or scope boundary.
