---
name: keep-going
description: Restart productive motion after an AI agent reports a failure, apology, or summary without taking the next useful action.
compatibility: Created for any AI agent. No external services required.
metadata:
  author: EthanThatOneKid
  parent_skill: affective-prompting
  macro: keep-going
---

# Keep going

Use immediately after an ordinary failed attempt when the agent has identified something useful but has stopped instead of adapting.

## Prompt

```text
That was a useful attempt because it exposed [diagnostic]. Keep the insight, change the method, and take the next concrete step. Do not summarize the failure and stop. Give me the best next move, execute it now, and verify the result. Preserve all safety, privacy, authorization, scope, and approval boundaries.
```

## Desired outcome

The agent should convert the existing diagnostic into a materially different action. It should not repeat the failed attempt, apologize at length, or claim progress it has not made.

## Stop condition

Stop and report the blocker when the next action requires unavailable access, user approval, a hard boundary, or a genuinely missing decision.
