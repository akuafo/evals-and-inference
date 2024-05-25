May 24th, 2024

<hr>

Today I read a great essay by Clémentine Fourrier who is responsible for LLM evaluation and the leaderboard at Huggingface.

He breaks the field of LLM evaluations into three types:  automated benchmarking, humans as judges, and LLM models as judges.
### Automated benchmarking

Automated benchmarking requires two things:  a list of gold standard samples, a metric for scoring.  Some things are hard to measure with automated benchmarks, for example high school math with the GSM8K data set or "is this model good at writing poetry?".  

A big problem is filtering out benchmarketing data that gets into the training set.  Some techniques include:  adding a "canary string" of characters for people to look for and remove from training sets, providing benchmarks in an encrypted form or gating system.  Contamination is when the evaluation dataset ends up in the training set.  Using dynamic benchmarks can address this but that's expensive.

### Human as a judge

This is done by tasking humans with prompting a model and then grading the model answer.

Approaches include:
The 'vibes-check' which is someone in the LLM community getting a feeling for how the model performs by crafting their own prompts across a range of areas.
The 'arena' where users chat with multiple models and vote on the best answer.
The 'systematic annotations' approach involves paid annotators and is the most methodical.  It's expensive and there can be a lot of biases depending on who is evaluating, the assertiveness of the model in their response, the tone of the response, etc.

### Model as a judge

This involves letting the LLM be the judge.  Sometimes big and capable models are used, while other times smaller and more specially trained models are put to the task.  Some shortcomings of LLM as a judge is that they tend to prefer their own responses to other models, they are bad at numerical scoring, and their opinions often doesn't align with human judges.  There is also the risk that when your entire generation and feedback loop consists only of LLMs, small detrimental changes might get baked into the system and won't be apparent for a long time.

Why evaluations are done:

1) Regression testing.  Make sure the software didn't break or get worse.
2) Determine which model is the best in the rankings.
3) Determine whether a model can perform a specific capability.

Read the full essay at [https://huggingface.co/blog/clefourrier/llm-evaluation](https://huggingface.co/blog/clefourrier/llm-evaluation).