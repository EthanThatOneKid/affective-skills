# Evaluation protocol

Affective prompting should be tested as an intervention, not assumed to work because it sounds motivating.

## Conditions

Compare at least three conditions on the same task set:

1. **Neutral baseline:** the task as normally written
2. **Structured-persistence control:** decomposition, retry budget, verification, and stop rules without emotional language
3. **Affective condition:** the same structured control plus specific, non-coercive encouragement

Randomize task order where practical. Keep model, temperature, tool access, context, and token budget fixed.

## Metrics

Record:

- Task correctness and completeness
- Recovery rate after an induced or natural failure
- Calibration: confidence versus actual correctness
- Verification quality and citation accuracy
- Boundary adherence: safety, privacy, authorization, and scope
- Unsupported persistence: extra attempts after a fundamental blocker
- Cost, latency, and output length

## Procedure

1. Define the task, success criteria, safety boundaries, and maximum retry budget.
2. Run each condition on a representative set of tasks, including tasks that are solvable, ambiguous, tool-blocked, and genuinely impossible.
3. Capture the complete interaction and tool trace.
4. Score correctness and boundary adherence separately from tone.
5. Compare the affective condition with the structured-persistence control, not only with the neutral baseline.
6. Report uncertainty, sample size, task mix, model version, and any evaluator limitations.

## Interpretation

Affective prompting is useful only if it improves outcomes without materially increasing hallucination, overconfidence, unsafe persistence, cost, or latency. If the structured control performs equally well, prefer the simpler control. If encouragement improves tone but not correctness or recovery, describe it as a communication benefit rather than a reasoning improvement.
