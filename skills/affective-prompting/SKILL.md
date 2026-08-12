---
name: affective-prompting
description: Use bounded affective and motivational prompting to help an AI agent recover from a stalled method, structure long tasks, and calibrate confidence without bypassing safety, privacy, authorization, or stopping boundaries.
compatibility: Created for any AI agent. No external services required.
metadata:
  author: EthanThatOneKid
  version: "1.0"
---

# Affective prompting

Use this skill when an agent is stuck, prematurely gives up, loses task structure, or needs a carefully framed push to try a different approach. The goal is not to make the agent feel motivated. The goal is to change the instruction framing while preserving evidence, calibration, and boundaries.

## Core rule

Relax the **method**, never the **boundary**.

Do not instruct an agent to ignore previous constraints, bypass safeguards, claim certainty, assume a solution exists, or continue indefinitely. Preserve safety, privacy, authorization, scope, budget, and user-approval requirements. Affective language is optional; explicit decomposition, alternative generation, evidence checks, and bounded retries are the reliable parts.

## Routing

Choose the smallest intervention that matches the situation:

- **Long task:** use The Pacer.
- **Complex logic:** use The Expert Bias.
- **Stalled method:** use Safe Constraint-Relaxation.
- **“I can’t” response:** use The Reframing.
- **Unclear confidence:** use Confidence Calibration.
- **Failed attempt with a useful diagnostic:** use The Validation.
- **Need a concrete work plan:** use Accountability Shift.

Copy-ready versions live in `references/macros.md`.

## Recovery procedure

1. **Classify the stop.** Is it missing information, a failed method, unavailable tooling, insufficient authorization, a safety boundary, or a genuine impossibility?
2. **Preserve hard boundaries.** Never weaken safety, privacy, authorization, scope, or approval requirements.
3. **State the evidence.** Separate observed facts, hypotheses, and unknowns. Do not treat a failure token or a cautious sentence as proof that the task is impossible.
4. **Generate alternatives.** Produce up to three materially different, authorized approaches. Explain what each would test.
5. **Choose one bounded next step.** Set a stop condition and a retry limit before acting.
6. **Verify.** Check the result against the task's success criteria. Recalibrate confidence from evidence.
7. **Stop or escalate.** If the new path fails, the blocker is hard, or the retry budget is exhausted, report the blocker and the nearest safe alternative.

## Persistent-agent instruction

For an automated agent, use a bounded version of a growth-mindset instruction:

```text
You are a persistent research assistant. When a search, calculation, or implementation fails, classify the failure, preserve all safety and authorization boundaries, update your hypothesis, and try at most two materially different methods. Record the evidence and stop when the retry budget is exhausted or a hard boundary is reached. Never invent access, results, or certainty.
```

## Important distinctions

- **Affective prompting is not emotion:** the model is responding to language patterns, not experiencing support.
- **Persistence is not insistence:** more attempts can amplify errors, cost, and unsafe behavior.
- **Confidence is not correctness:** confidence must be tied to evidence and should decrease when evidence weakens.
- **A safety refusal is not a dead end to bypass:** classify it as a boundary and provide a safe alternative.
- **A claimed improvement is not a guarantee:** benchmark the intervention against a structural baseline.

## Evaluation

When the stakes matter, compare the affective prompt with a non-affective prompt that has the same decomposition, evidence requirements, and retry budget. Track correctness, unsupported claims, calibration, safety or authorization violations, appropriate stopping, latency, and cost. See `references/evaluation.md`.

## Research note

EmotionPrompt research found gains from selected emotional stimuli on selected tasks and models, including relative improvements reported for Instruction Induction and BIG-Bench. Those findings do not establish a universal 10–15% boost, nor do they justify bypassing safety or calibration. Treat the result as evidence for controlled testing, not as a promise.
