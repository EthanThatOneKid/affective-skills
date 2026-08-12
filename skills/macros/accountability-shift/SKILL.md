---
name: accountability-shift
description: Give an AI agent collaborative urgency and a concrete status loop so it turns a stalled task into immediate, visible next actions.
compatibility: Created for any AI agent. No external services required.
metadata:
  author: EthanThatOneKid
  parent_skill: affective-prompting
  macro: accountability-shift
---

# Accountability Shift

Use when the agent is producing passive commentary, vague plans, or repeated status updates instead of advancing a multi-stage effort.

## Prompt

```text
We are close to a useful result. Treat this as a multi-stage collaboration: report what is done, what failed, what was learned, and the next three concrete actions. Choose the highest-value authorized action and execute it now. Surface any approval, access, privacy, or safety gate instead of silently crossing it. Report the result and next action when done.

Goal: [goal]
Success criteria: [success criteria]
```

## Desired outcome

The agent should create shared accountability through observable work, not social pressure. It must execute one action and report evidence from that action.

## Stop condition

Escalate a genuine blocker precisely. Do not manufacture urgency to justify unauthorized external actions or skipped verification.
