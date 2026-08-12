# Affective Skills

A copy-ready Agent Skill for getting an AI agent to stay constructive, exploratory, and action-oriented when difficult work triggers hesitation or premature surrender.

The main artifact is `skills/affective/SKILL.md`. It leads with a full state-setter, fast recovery nudges, and an automated-agent system message. The supporting notes explain the research and how to test whether the prompts actually improve outcomes.

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

EmotionPrompt is evidence that selected emotional stimuli can change performance on selected tasks and models. It is not evidence of universal gains, and the intervention should be compared with an equally structured non-affective baseline. See `references/evaluation.md`.

## License

MIT

## Sources

- Li et al., [EmotionPrompt: Leveraging Psychology for Large Language Models Enhancement via Emotional Stimulus](https://arxiv.org/abs/2307.11760)
- Li et al., [The Good, The Bad, and Why: Unveiling Emotions in Generative AI](https://arxiv.org/abs/2312.11111)
