# Affective Skills

[![skills.sh](https://skills.sh/b/EthanThatOneKid/affective-skills)](https://skills.sh/EthanThatOneKid/affective-skills)

A copy-ready set of Agent Skills for helping AI agents keep working when a task gets difficult.

The idea is simple: encouragement can keep an agent from treating its first failed attempt as a reason to stop. This project turns that informal “keep going” tactic into a modular, situation-aware, bounded prompt methodology. Each macro pairs an affective cue with a specific behavior: take the next action, change methods, investigate missing evidence, verify the result, or report a real blocker.

Anthropic has described a related mathematical investigation in which repeated “keep going” and “believe in yourself” prompts seemed to help Claude continue after its initial ideas failed. `affective-skills` packages that kind of encouragement into short, reusable skills with explicit outcomes, guardrails, and stop conditions.

The main entrypoint is `skills/affective/SKILL.md`. Use it when the situation is unclear, or use one of the focused `affective-*` skills when the failure mode is known.

## Install

```bash
npx skills add https://github.com/EthanThatOneKid/affective-skills
```

## Desired behavior

The skill is designed to elicit an agent that:

- treats setbacks as diagnostics rather than reasons to stop
- produces the next concrete action instead of only apologizing or summarizing
- switches methods instead of repeating the same failed attempt
- stays optimistic and collaborative without pretending to be certain
- continues until success is verified, useful paths are exhausted, or a real blocker needs human input

## Macro subskills

Use the default skill when the situation is unclear or several interventions are needed. Use one focused subskill when the situation and desired outcome are known.

| Situation | Subskill | Desired outcome |
|---|---|---|
| Beginning a difficult task | [`affective-full-state-setter`](skills/affective-full-state-setter/) | Energetic, collaborative, persistent working state |
| Ordinary mid-task failure | [`affective-keep-going`](skills/affective-keep-going/) | Immediate next action instead of apology or summary |
| Long-form work | [`affective-the-pacer`](skills/affective-the-pacer/) | Visible stages, momentum, and concrete progress |
| Complex reasoning | [`affective-expert-bias`](skills/affective-expert-bias/) | Expert-like investigation and hypothesis generation |
| One method is stuck | [`affective-constraint-relaxation`](skills/affective-constraint-relaxation/) | Different authorized approaches without weakening boundaries |
| Premature “I can’t” | [`affective-reframing`](skills/affective-reframing/) | Distinguish method failure from true impossibility |
| Low confidence | [`affective-confidence-calibration`](skills/affective-confidence-calibration/) | Evidence-seeking and a compared Plan B |
| Passive status updates | [`affective-accountability-shift`](skills/affective-accountability-shift/) | Shared status translated into immediate action |
| A useful failed attempt | [`affective-validation`](skills/affective-validation/) | Preserve the diagnostic and pivot productively |
| Automated retry loop | [`affective-bounded-persistence`](skills/affective-bounded-persistence/) | Adaptive retries with explicit stop conditions |

Each subskill is copy-ready and includes its trigger, prompt, desired outcome, and guardrails.

## Safety posture

The intended behavior is **persistent but calibrated**. Change the failed method, never a safety, privacy, authorization, scope, or approval boundary. Do not use affective prompting to pressure an agent into unsafe actions, fabricated certainty, or indefinite retries.

## Research position

This is not a claim that encouragement guarantees breakthroughs. EmotionPrompt and related work suggest that emotional wording can change model behavior on some tasks, but the effect depends on the model, prompt, and task. The evaluation protocol compares an affective prompt with an equally structured non-affective baseline, including checks for correctness, calibration, unsafe persistence, and cost.

## License

MIT

## Sources

- Li et al., [EmotionPrompt: Leveraging Psychology for Large Language Models Enhancement via Emotional Stimulus](https://arxiv.org/abs/2307.11760)
- Li et al., [The Good, The Bad, and Why: Unveiling Emotions in Generative AI](https://arxiv.org/abs/2312.11111)
