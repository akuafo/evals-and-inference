# LLM Evaluations

Perhaps you've read about the landmark court ruling against an airline that had inadequately tested their AI chatbot.  A customer of Air Canada successfully sued the airline for an overcharge due to bad advice from the chatbot.  The impact of this court ruling is making companies think more deeply about the risks of AI services.  The reality is that no one has prepared for this moment.  The evaluation of large language models (LLMs) is a problem that has not yet been solved.

Software development of an LLM application is quite different from anything that has come before.  In the initial steps of application building, the development process might be deceptively easy.  For instance, when creating a simple chatbot, very little programming is required since the LLM accepts human language as the input.  Add a simple basic website template and a few API calls and a fully functional chatbot can be created in an hour or so.

But the creators of this LLM application will have no easy way to determine if it's good enough to become customer-facing.  Today's state of the art LLMs do not come packaged with any standard testing method or automated evaluation.  There are no industry protocols and few guidelines.  It's new territory for even the most experienced developers.

The reason is that LLMs are probabilistic.  The randomness in these responses does not lend itself to an easy quantified assessment.  An LLM may provide two different responses if asked the exact same question two times.  And its responses may change and evolve over time.  Even worse, if the LLM vendor makes a scheduled release, or does an unannounced 'internal alignment', the responses for entire categories of prompts can change significantly.

The good news is that there are a growing number of innovative approaches for addressing the hard parts of LLM evaluation.

It might seem obvious, but in order to do an LLM evaluation, it's necessary to have a good data set for testing.  For those who specialize in machine learning (ML) and data science, it's standard practice to start with the process of obtaining the data, preparing the data, and splitting the data into training and test sets.  For non-ML engineers, this process might be part of the learning curve.

One technique to get started quickly is to create a small hand-crafted data set with manual-labels.  With this small data set in hand, an evaluation pipeline can be set up quickly.  While this initial evaluation data set might not be large enough to be meaningful, it facilitates the setup of an evaluation pipeline.  It also encourages a habit of investigating individual evaluation findings in detail.

As a further step, there are many open source ML data sets that can be useful for a more general evaluation of LLM applications.  For example, the Eleuther evaluation framework includes over 60 standard benchmarks for LLMs with hundreds of subtasks and variants.  There are datasets that focus on logical reasoning, computer programming, academic examinations, and identifying bias or inappropriate behavior.

If the LLM application is intended for use in a specialized domain (law, medical, internal corporate, etc), obtaining a domain specific data set for evaluation is crucial but can be challenging.  For example, in medicine there are a number of open data sets that can be freely downloaded.  There are others that require a certificate demonstrating knowledge of patient privacy before they can be obtained.  But most of the data is in fact locked inside various institutional entities and can only be acquired by a very long process of signing an agreement with a hospital or healthcare company.

###### Synthetic data for evaluation
Once a data set is in hand, it's often useful to make it larger and more varied by a process of generating synthetic data.  For example, words in the data can be replaced by variables which results in many variations of prompts generated from the same data set.  To create more complex synthetic data sets, an increasingly popular approach is to use an LLM that is external to the application to generate the data.  Synthetic data sets can be created for purpose of creating sets of question answer pairs, multiple variations of prompts, assessing the impact of text changes like verb tenses and misspellings, or system changes like adjusting the temperature or randomness parameter of the LLM response.

###### Orchestration 
In the LLM application workflow, there are typically a number of different steps, each of which can be logged and evaluated separately.  For the logging itself, there are a number of companies and open source projects that specialize in AI tracing and observability of steps in the application workflow.  An example of a workflow would be if an application uses Retrieval Augmented Generation (RAG) to retrieve text from a vector database with embeddings from internal documents, an evaluation step can be inserted after the text retrieval to provide a score of the match quality. This score can be used on its own or in combination with other metrics for an aggregated quality score.

###### Scoring
In the world of LLMs, there is not always a correct answer.  In many cases the ground truth for a given question may have a large degree of interpretation.  While sometimes the answer is binary or multiple choice, other times there may be multiple correct answers with different words, phrasings, and shades of meaning.  Options for scoring these text responses include algorithmic text comparison, calculations of embedding distance, and prompting external LLMs to be a judge of the response.  If using an LLM as a judge, be mindful of the fact that LLMs are not very good at numerical scoring.

###### Human testing
Due to the challenges of automated LLM evaluation, it's standard practice to design any evaluation with a human in the loop.  The human may be there only to spot check data or the human may be judging responses and generating quality scores.

###### Alignment and Bias
There have been many academic papers demonstrating problematic behavior by LLM foundational models.  These models are only as good as the data they have been trained on, which includes a lot of questionable content as well as content that represents existing inequalities in society.  While the LLMs models have generally been fine-tuned to improve their behavior and prevent illegal and offenses responses, it's still often necessary to do further evaluation of quality.  There are open source data sets and commercial tools to assist with general alignment evaluation.  But for any specific domain, it's important to involve the people who have the deepest knowledge of that domain to validate that the system is not doing something bad.

###### Final thoughts
`Don't put prototype LLM applications directly into production with customers.` Instead, spend some time evaluating it.

###### Future
There are a number of software packages available to assist with AI evaluation, including open source libraries, new startup products, and offerings from big tech.  That's a topic for the next writing session.
