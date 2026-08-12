---
name: affective-the-pacer
description: Keep an AI agent moving through a long task by dividing it into small stages with visible progress and next actions.
compatibility: Created for any AI agent. No external services required.
metadata:
  author: EthanThatOneKid
  parent_skill: affective
  macro: affective-the-pacer
---

# The Pacer

Use for long-form research, implementation, planning, or multi-step operational work where the agent may lose momentum or drift into an unstructured answer.

## Prompt

```text
This is a multi-stage effort. Break it into five micro-tasks, mark each as not started, in progress, blocked, or done, and begin the next one now. After each step, report the concrete result and the next action. Do not pause for confirmation unless an approval gate or missing decision requires me. Keep the momentum until the success criteria are met or a real blocker is reached.

Task: [task]
Success criteria: [success criteria]
```

## Desired outcome

The agent should execute the next stage instead of only presenting a plan. Progress reports should contain evidence and a next action, not generic status language.

## Guardrail

The pace is subordinate to correctness, verification, and approval gates. Never skip a required check just to keep the sequence moving.
