# Prompt Comparison Study: Explaining Neural Networks

A small experiment testing how prompt wording changes the quality of AI answers across **ChatGPT, Claude and Gemini**.

## Summary

- **Prompt 2 (role + audience + word limit + summary line) worked best.** It gave the biggest improvement in how easy the answer was for a beginner to follow.
- **Adding more instructions in Prompt 3 did not help across the board.** It improved structure and usefulness for some tools, but two of the three then broke the 200-word limit.
- **Gemini followed instructions most closely. ChatGPT scored highest on accuracy and clarity but added extra text. Claude gave the best analogies but ran slightly long.**
- The differences between tools were small, about 1 point on a 5-point scale, so I would not call any tool "best" from this one test.

## Goal

Find out how much prompt style changes an AI answer when the task is the same, and whether the effect is similar on different tools.

**Task used:** "Explain how a neural network works" for a first-year student with no AI background.

## Method

1. Wrote 3 prompts for the same task, each with more detail than the last (see [prompts.md](prompts.md)):
   - **Prompt 1:** basic, one sentence
   - **Prompt 2:** adds a role, an audience, a 200-word limit and a one-line summary
   - **Prompt 3:** Prompt 2 plus "list key ideas in points, 2-3 sentences each" and a tone example
2. Ran all 3 prompts on all 3 tools = **9 outputs**, each in a fresh chat with the prompt pasted unedited. (Outputs are in [outputs/](outputs/).)
3. Scored every output from 1 to 5 on four criteria: **accuracy, clarity for a beginner, following instructions, usefulness**. The rubric and full table are in [scores.md](scores.md).
4. Tools and versions: ChatGPT, Claude and Gemini free versions, run on [DATE]. [Add exact model names if the apps show them.]

## Results

| Prompt | Average total /20 | Average without "Instructions" /15 |
|---|---|---|
| 1 (basic) | 16.7 | 11.7 |
| 2 (role + limits) | **17.3** | **13.3** |
| 3 (key ideas + tone) | 16.7 | 12.7 |

| | Claude | Gemini | ChatGPT |
|---|---|---|---|
| Accuracy | 4.3 | 4.3 | **4.7** |
| Clarity | 4.0 | 4.0 | **4.7** |
| Following instructions | 4.0 | **5.0** | 4.0 |
| Usefulness | 4.0 | 3.3 | **4.3** |

Prompt 1 has no constraints, so every tool gets full marks for "following instructions". That column is excluded in the second column above to keep the comparison fair.

## Findings

1. **A role, an audience and limits change the answer more than anything else.** Prompt 1 gave 550-830 words with terms like "chain rule", "ReLU" and "Adam" from Claude and Gemini. Prompt 2 gave short, plain answers with analogies, from all three tools.
2. **More instructions can cause the tool to drop some of them.** In Prompt 3, Claude and ChatGPT went over 200 words, and ChatGPT added a closing offer after the summary.
3. **Tools have different habits.** ChatGPT tends to add extras (a quiz, next-step suggestions). Gemini tends to stay within limits but covers fewer ideas. Claude tends to use strong analogies but runs a little long.
4. **Even good answers had small accuracy problems.** For example, two tools said the weight adjustment "is called backpropagation", but backpropagation calculates the blame for each weight and gradient descent does the adjusting.

## What I would do differently

- Write the prompt carefully. Prompt 3 has a missing space ("one line summary.List"), and the Wikipedia tone example I pasted is a fact sheet with bullets and citations, so the tools probably copied its format instead of its tone.
- Use a tone example that is a plain, friendly explanation.

## Limitations

- One task, one run per prompt. AI outputs change each time, so a rerun could give different results.
- Scored by one person, so the scores are subjective.
- Free-tier models on a single date. Newer versions may behave differently.
- Word counts are approximate.

## Files

| File | What it contains |
|---|---|
| [prompts.md](prompts.md) | The 3 prompts, exactly as used |
| [outputs/](outputs/) | The 9 responses |
| [scores.md](scores.md) | Rubric, scores, word counts and notes |

## Skills practiced

Prompt design, comparing AI tools, writing evaluation criteria, documenting an experiment.
