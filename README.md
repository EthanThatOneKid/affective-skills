# Affective Skills

A small Agent Skills library for using affective and motivational prompting without sacrificing truthfulness, calibration, safety, privacy, authorization, or appropriate stopping.

This project treats “cheerleading” as a prompt-framing technique, not as a way to override safeguards. It preserves hard boundaries while encouraging an agent to diagnose a failed method, explore a bounded set of alternatives, and verify the result.

## Install

```bash
npx skills add https://github.com/EthanThatOneKid/affective-skills
```

## Skill index

| Skill | Scope | Description |
|---|---|---|
| [`affective-prompting`](skills/affective-prompting/) | Recovery and persistence | Bounded affective macros, safe reframing, confidence calibration, and evaluation guidance |

## Included macros

- The Pacer for long-form tasks
- The Expert Bias for complex logic
- Safe Constraint-Relaxation for a stalled method
- The Reframing for premature “I can’t” responses
- Confidence Calibration for uncertain paths
- Accountability Shift for multi-stage work
- The Validation for pivoting after a useful failure
- Bounded Persistence for automated agents

## Research position

EmotionPrompt is evidence that selected emotional stimuli can change performance on selected tasks and models. It is not evidence of universal gains, and it does not support telling an agent to ignore constraints or continue without limits. This library therefore pairs motivational language with explicit decomposition, evidence tracking, bounded retries, and appropriate stopping.

## Safety posture

Relax the method, never the boundary. A refusal caused by a safety, privacy, authorization, or approval constraint is not a problem to bypass. The correct response is to identify the boundary and find a safe, authorized alternative.

## License

MIT

## Sources

- Li et al., [EmotionPrompt: Leveraging Psychology for Large Language Models Enhancement via Emotional Stimulus](https://arxiv.org/abs/2307.11760)
- Li et al., [The Good, The Bad, and Why: Unveiling Emotions in Generative AI](https://arxiv.org/abs/2312.11111)
