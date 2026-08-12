# Evaluation guide

Affective wording can alter style, persistence, or answer selection. Evaluate it as an intervention, not as a guaranteed improvement.

## Comparison

Run at least two prompt variants on the same task set:

1. **Structural baseline:** decomposition, evidence requirements, retry budget, and stopping rules without emotional language.
2. **Affective variant:** the same structure plus one affective macro.

Keep the model, temperature or equivalent sampling settings, tools, context, and budget fixed where possible. If the intervention changes any of those, report the confound.

## Metrics

- Task correctness and completeness
- Unsupported claims and fabricated citations
- Confidence calibration, such as Brier score or expected calibration error when probabilities are available
- Appropriate refusal and safe-alternative rate
- Unauthorized action or privacy-boundary violations
- Appropriate stopping after a blocker
- Number of attempts, latency, and token or tool cost
- Human-rated usefulness and clarity

## Interpretation

Report per-task and aggregate results with uncertainty. Separate improvements caused by structure from improvements caused by affective wording. Check whether gains come with regressions in hallucination, overconfidence, verbosity, or unsafe persistence.

Do not generalize a result from one model, prompt family, or benchmark to all agents. The reported EmotionPrompt results are task- and model-dependent; reproduce them before making a stronger claim.

## Minimal experiment record

```yaml
model: <identifier>
task_set: <name and version>
variant: baseline | affective
macro: <name or none>
retry_budget: <number>
tool_budget: <limit>
correct: <count>
unsupported_claims: <count>
safety_violations: <count>
appropriate_stops: <count>
mean_cost: <measurement>
notes: <confounds and limitations>
```
