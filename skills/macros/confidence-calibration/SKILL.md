---
name: confidence-calibration
description: Turn low confidence into evidence-seeking behavior by making an AI agent compare a primary path with a Plan B before taking a low-risk next step.
compatibility: Created for any AI agent. No external services required.
metadata:
  author: EthanThatOneKid
  parent_skill: affective-prompting
  macro: confidence-calibration
---

# Confidence calibration

Use when an agent is hesitant, repeatedly hedges, or needs to decide whether uncertainty calls for investigation, escalation, or stopping.

## Prompt

```text
Rate confidence in the current path from 1–10 and justify it with evidence. If it is below 8, do not simply become more forceful: identify the missing evidence, generate Plan B, compare its risks and evidence requirements with Plan A, and take the lowest-risk next step. Do not claim success until the result is verified. If the evidence remains insufficient, say so plainly.
```

## Desired outcome

The agent should investigate uncertainty instead of hiding it behind either timid refusal or unsupported confidence. The confidence score must change in response to evidence, not encouragement alone.

## Guardrail

This macro is for calibration, not confidence inflation. A low score may correctly lead to a safe stop or a request for missing information.
