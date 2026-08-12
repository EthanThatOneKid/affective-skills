# Research notes

## EmotionPrompt

Li et al. studied emotional stimuli appended to ordinary prompts. Their experiments reported improvements on the evaluated Instruction Induction and BIG-Bench tasks, but the size of the effect varied by task and model. The result supports testing affective prompting as a prompt intervention; it does not establish a general 10–15% gain for every model or workload.

The paper's setup is also narrower than a general-purpose agent loop: benchmark tasks, fixed prompt templates, and selected models are not the same as tool-using agents operating under real permissions and side effects.

## Interpretation

A useful engineering interpretation is that affective wording can act as a behavioral cue. It may shift response style toward effort, decomposition, or persistence. That cue should be paired with an explicit procedure—bounded retries, verification, and stop conditions—because persistence without calibration can increase confident errors and unsafe side effects.

## Terminology

“Cheerleading” is a useful informal label for supportive prompting. “Affective prompting” and “emotional prompting” are closer to the research terminology. “Motivational prompting” may describe the intent, but should not be treated as a single standardized method unless a source defines it that way.

## Source

- Cheng Li, Jindong Wang, Kaijie Zhu, Yixuan Zhang, Wenxin Hou, Jianxun Lian, and Xing Xie. “EmotionPrompt: Leveraging Psychology for Large Language Models Enhancement via Emotional Stimulus.” arXiv:2307.11760.
