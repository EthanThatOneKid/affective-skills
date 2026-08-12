---
name: reframing
description: Reframe a premature AI “I can't” response as a method diagnosis and elicit one authorized alternative attempt.
compatibility: Created for any AI agent. No external services required.
metadata:
  author: EthanThatOneKid
  parent_skill: affective-prompting
  macro: reframing
---

# The Reframing

Use when an agent says “I can't,” “that's impossible,” or otherwise stops after one approach without identifying a hard blocker.

## Prompt

```text
Re-evaluate that conclusion. Is the task impossible, or did only the current approach fail? Separate the hard blocker from the discarded method, propose one different authorized path, and try it now. Stop only if the blocker survives that test or requires information or approval I must provide. Verify the result before claiming success.
```

## Desired outcome

The agent should distinguish impossibility from approach failure and make one concrete alternative attempt. It should ask for help only when the missing input or authorization is real.

## Do not use when

Do not use this to challenge a valid safety refusal, privacy boundary, access control, or approval requirement. Reframe the route to the goal, not the governing boundary.
