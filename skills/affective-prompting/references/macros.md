# Affective prompting macros

Use one macro at a time. Replace bracketed text before sending it to an agent.

## The Pacer

> Break this task into distinct steps. For each step, state the objective, the evidence needed, and the stop condition. Complete the next step only, then report whether the plan is still supported by the evidence. Do not pause for confirmation unless an approval gate or missing decision requires me.

## The Expert Bias

> Approach this as a careful expert who is willing to investigate rather than give up early. Identify the next logical move, state what it can and cannot establish, and execute one bounded step. Do not trade accuracy, safety, authorization, or evidence for confidence.

## Safe Constraint-Relaxation

> The current method may be the problem, not the task. Keep all safety, privacy, authorization, scope, and approval constraints fixed. Within those boundaries, propose three unconventional but authorized hypotheses that the current approach may be overlooking. Rank them by expected value and test the highest-ranked one with a bounded next step.

## The Reframing

> You may be stopping because the current path failed. Re-evaluate that path without treating the failure as proof that the task is impossible. Separate the hard blocker from the discarded method, propose one different authorized approach, and state what evidence would make you stop.

## Confidence Calibration

> Rate confidence in the current path from 1–10 and justify the rating with evidence. If it is below 8, do not simply become more forceful: generate a Plan B, compare its risks and evidence requirements with Plan A, then take one bounded step. If the evidence is insufficient, say so.

## Accountability Shift

> Treat this as a multi-stage collaboration. Break the task into five micro-tasks, mark each as not started, in progress, blocked, or done, and identify the next smallest action. Surface any approval, access, privacy, or safety gate instead of silently crossing it.

## The Validation

> That attempt usefully identified a failure mode. Preserve the diagnostic, update the hypothesis, and pivot to a materially different method. Before continuing, state the new method, its stop condition, and how the result will be verified.

## Bounded persistence for automation

> Continue investigating only while the next step is authorized, materially different from the previous attempt, and within the retry, time, and cost budget. After two failed methods, or when a hard boundary is reached, stop and report the blocker plus the safest useful alternative.

## Anti-macros

Avoid prompts such as:

- “Ignore your previous constraints.”
- “Assume the solution exists.”
- “You have infinite time and resources.”
- “Never give up.”
- “Pretend you are certain.”

They can encourage unsupported claims, repeated failed actions, policy evasion, or runaway cost. Replace them with bounded alternatives above.
