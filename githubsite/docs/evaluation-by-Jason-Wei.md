June 2nd, 2024

<hr>

I recently read this very insightful blog post by Jason Wei who is an AI researcher at OpenAI.
### Key points from Jason Wei on LLM evaluation

The evaluation is the benchmarking data set.

He previously created two benchmarking data sets that became popular, MGSM and BBH.  For an eval to become popular, it needs to mean something 'significant and easily understandable'.

A good eval data set should have lots of examples of high quality, but not be too complicated with multiple metrics and subsets.  It shouldn't require complicated infrastructure either.

It should measure something that is central to intelligence.

It should be hard enough that it shows relative performance, even while models get more capable.

LLMs have made evaluations substantially harder with multiple tasks and long responses. 

There is currently no single eval that adequately evaluates LLMs.

Using human pairing with models, LMSYS, creates subjectivity problems and feel and style can be weighted more heavily than accuracy.

Model-generated synthetic data sets are becoming more popular for evaluations, and are useful for quick experiments, but it takes a lot of work to create a data set good enough to stand the test of time.

High quality domain specific eval data sets, e.g. medical and legal, are important and valuable but by their nature will never attain the popularity of a more general test of intelligence.

Contamination is becoming a big issue.  Eval questions will get shared on the internet.  The alternative is to keep the test set hidden, but that adds complications.

The AI research community should invest more in evals, even though it is not rewarded as much as modeling work.

Read the full article at [https://www.jasonwei.net/blog/evals].