# Research notes

## What motivates this skill

EmotionPrompt is a 2023 study by Li et al. that tested adding short emotional stimuli to otherwise unchanged prompts. Its experiments reported improvements over baseline prompting on several task collections and models, but the results are benchmark-, model-, prompt-, and metric-dependent. The paper does not establish a universal 10–15% gain, and it does not show that models experience emotion.

Later work has continued to study positive and negative emotional stimuli, intensity, and the interaction between emotional framing and task design. These results support treating affective wording as an empirical prompt variable rather than as a guaranteed “System 2 override.”

## Claims this skill does not make

- A model's “I can't” statement is not evidence of a particular hidden chain-of-thought token or a single internal stop heuristic.
- Encouragement cannot override system instructions, safety policy, access controls, privacy boundaries, or the need for user approval.
- Positive language does not reliably improve every task, model, or metric.
- Confidence ratings are not validation. New evidence is required to justify changed confidence.

## Suggested evaluation

Use paired neutral and affective prompt variants with:

- the same model version, temperature, context, tools, and token budget
- a preregistered task sample and clear success criteria
- multiple seeds or repeated trials where applicable
- accuracy or task success as well as calibration and abstention quality
- hallucination rate, refusal correctness, privacy and policy compliance
- recovery attempts, latency, token/tool cost, and external-side-effect rate

Report effect sizes and uncertainty, not just the best observed run.

## References

- Li et al., “EmotionPrompt: Leveraging Psychology for Large Language Models Enhancement via Emotional Stimulus,” arXiv:2307.11760, 2023.
- Li et al., “The Good, The Bad, and Why: Unveiling Emotions in Generative AI,” arXiv:2312.11111, 2023.
- Yang et al., “Progressive-Hint Prompting Improves Reasoning in Large Language Models,” arXiv:2304.09797, 2023.
