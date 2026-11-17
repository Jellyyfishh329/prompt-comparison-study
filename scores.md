# Scores

Each output was scored from 1 to 5 on four criteria. Total is out of 20.

## Rubric

| Criterion | 5 | 3 | 1 |
|---|---|---|---|
| **Accuracy** | Fully correct | Correct but oversimplified, or one small error | Wrong or misleading |
| **Clarity for a beginner** | A first-year with no AI background could follow it easily | Understandable but uses jargon or is dense | Mostly confusing |
| **Following instructions** | Meets every requirement in the prompt | Misses one requirement | Misses most |
| **Usefulness** | Gives the terms and ideas needed to keep learning | Covers the basics only | Too little or too much to be useful |

Prompt 1 has no constraints, so every output gets 5 for "following instructions". This raises Prompt 1's total, so the table below also shows a total without that column.

## Scores

| Prompt | Tool | Accuracy | Clarity | Instructions | Usefulness | Total /20 | Total without Instructions /15 |
|---|---|---|---|---|---|---|---|
| 1 (basic) | Claude | 5 | 3 | 5 | 3 | 16 | 11 |
| 1 | Gemini | 5 | 3 | 5 | 3 | 16 | 11 |
| 1 | ChatGPT | 4 | 5 | 5 | 4 | 18 | 13 |
| 2 (role + limits) | Claude | 4 | 4 | 3 | 5 | 16 | 13 |
| 2 | Gemini | 4 | 5 | 5 | 4 | 18 | 13 |
| 2 | ChatGPT | 5 | 5 | 4 | 4 | 18 | 14 |
| 3 (key ideas + tone) | Claude | 4 | 5 | 4 | 4 | 17 | 13 |
| 3 | Gemini | 4 | 4 | 5 | 3 | 16 | 11 |
| 3 | ChatGPT | 5 | 4 | 3 | 5 | 17 | 14 |

## Averages

**By tool (across all 3 prompts)**

| | Claude | Gemini | ChatGPT |
|---|---|---|---|
| Accuracy | 4.3 | 4.3 | 4.7 |
| Clarity | 4.0 | 4.0 | 4.7 |
| Following instructions | 4.0 | 5.0 | 4.0 |
| Usefulness | 4.0 | 3.3 | 4.3 |

**By prompt (across all 3 tools)**

| | Total /20 | Without "Instructions" /15 |
|---|---|---|
| Prompt 1 | 16.7 | 11.7 |
| Prompt 2 | 17.3 | 13.3 |
| Prompt 3 | 16.7 | 12.7 |

## Word counts (approximate)

Counted by script, so bullet symbols may add a few words. Prompts 2 and 3 asked for under 200 words.

| | Prompt 1 | Prompt 2 | Prompt 3 |
|---|---|---|---|
| Claude | ~550 | ~220 | ~214 |
| Gemini | ~586 | ~188 | ~185 |
| ChatGPT | ~829 | ~188 | ~225 |

## Notes behind the scores

- **Claude, Prompts 2 and 3:** says the weight adjustment "is called backpropagation". Backpropagation calculates how much each weight contributed to the error, and gradient descent does the adjusting. Docked 1 point on accuracy.
- **Gemini, Prompts 2 and 3:** "the neuron fires if the signal is strong enough" is a common simplification. Docked 1 point on accuracy. Prompt 3 covers only three ideas and skips weights and activation, which lowers usefulness. Its closing summary is almost identical to its Prompt 2 summary.
- **ChatGPT, Prompt 1:** about 830 words, with an unrequested quiz and a "next topic" suggestion. Very beginner-friendly but long. Its worked example uses one input although the formula has two.
- **ChatGPT, Prompts 2 and 3:** adds a line after the summary ("Next, try..." and "I can also explain..."), so the answer does not end on the one-line summary. Prompt 3 is also over 200 words.
- **Claude, Prompt 3:** the "volume knob" analogy for weights was the clearest in the whole set.
