June 2nd, 2024

---

A quick project to learn something new...  I had come across the use of Bert Score for LLM evaluation in a few different places and got curious enough to set up my own little eval.  I looked for someone hosting an API for Bert Score so I didn't need to run the whole model locally, but ended up installing PyTorch and found that it actually runs very quick on an Macbook Air M2.

The whole setup consisted of a python script and Postgres DB to store my prompts and gold answers and keep a log of the scores.

I did a query to OpenAI for each prompt and scored with 3 different measures:
- Simple word intersection in Python
- Bert Score using the bert_score library
- LLM as a judge (also using OpenAI)

The prompts are my own hand-crafted set of questions on topics that I know well.  I plan to build this dataset out quite a bit in future.

I'm finding that using my own data sets is a really intuitive way to get to learn about different LLM evaluation methodologies.

Next up, I want to run some tests with Infini-gram and Named Entity Recognition (NER).
