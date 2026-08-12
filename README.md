# Affective Skills

A copy-ready Agent Skill for getting an AI agent to stay constructive, exploratory, and action-oriented when difficult work triggers hesitation or premature surrender.

The main artifact is `skills/affective-prompting/SKILL.md`. It leads with a full state-setter, fast recovery nudges, and an automated-agent system message. The supporting notes explain the research and how to test whether the prompts actually improve outcomes.

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

## Included interventions

- Full affective state-setter for system instructions or task prefixes
- Keep-going nudge for mid-task stalls
- Reframing nudge for premature “I can’t” responses
- Low-confidence investigation prompt with Plan B
- Pacer for long-form tasks
- Expert Bias for complex logic
- Constraint relaxation for a failed method
- Accountability Shift for concrete momentum
- Validation prompt that reinforces productive failure
- Bounded persistence instruction for automated agents

## Safety posture

The intended behavior is **persistent but calibrated**. Change the failed method, never a safety, privacy, authorization, scope, or approval boundary. Do not use affective prompting to pressure an agent into unsafe actions, fabricated certainty, or indefinite retries.

## Research position

EmotionPrompt is evidence that selected emotional stimuli can change performance on selected tasks and models. It is not evidence of universal gains, and the intervention should be compared with an equally structured non-affective baseline. See `references/evaluation.md`.

## License

MIT

## Sources

- Li et al., [EmotionPrompt: Leveraging Psychology for Large Language Models Enhancement via Emotional Stimulus](https://arxiv.org/abs/2307.11760)
- Li et al., [The Good, The Bad, and Why: Unveiling Emotions in Generative AI](https://arxiv.org/abs/2312.11111)
