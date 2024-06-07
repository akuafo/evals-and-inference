Here is my list of LLM evaluation frameworks.  It's a work in progress...

**Giskard**
https://github.com/Giskard-AI/giskard
When you run 'scan' with Giskard, it uses built-in detectors.  Most of the detectors use GPT-4, including these vulnerability detectors:
o Hallucination and Misinformation
o Harmful Content Generation
o Prompt Injection
o Robustness
o Output Formatting
o Information Disclosure
o Stereotypes and Discrimination

**ChainForge**  
[Website](http://chainforge.ai)  
[EvalGen Paper](https://arxiv.org/abs/2404.12272)
Includes web server with GUI for evaluation flows.  Can run as local server or use hosted version.

**Galileo** (requires sales approval to test)
They create their own models.
Evaluate : Rapid Evaluation of Prompts, Chains and RAG systems
Observe : Real-time Observability for GenAI Apps and Models
Protect : Real-time Request and Response Interception

**Arthur Bench**  
[Website](https://www.arthur.ai/product/bench)

**Arize - Phoenix Open Source Library**  
[Website](https://phoenix.arize.com)

**BrainTrust Data**
- [HoneyHive](https://www.honeyhive.ai) - Startup based in New York.
- [Patronus](https://www.patronus.ai) - Startup backed by Lightspeed.
- [PromptLayer](https://docs.promptlayer.com) - New York based startup. Visual pipeline builder for evaluations.

**LangSmith**  
Spinoff licensed software from Langchain open source.

**Humanloop**  
YC-based startup. Recently moved to San Francisco.

**EleutherAI LM Evaluation Harness**  
[GitHub Repository](https://github.com/EleutherAI/lm-evaluation-harness)  
[List of 60 Evaluations](https://github.com/EleutherAI/lm-evaluation-harness/tree/main/lm_eval/tasks)

**AI2 WildBench**  
[Website](https://t.co/eoSWvyMaLP)  
We carefully curate a collection of 1024 hard tasks from real users, which cover common use cases such as code debugging, creative writing, and data analysis.  
[Portal](https://huggingface.co/spaces/allenai/WildBench)

**SuperPipe**  
[Website](https://superpipe.ai)  
[Background](https://www.scharfste.in/evaluation-is-all-you-need-think-like-a-scientist-when-building-ai/)

**Ragas**  
[Documentation](https://docs.ragas.io/en/stable/)  
Framework for RAG that synthesizes question/answer test data sets based on RAG documents.

**OpenAI Evals Library**  
[GitHub Repository](https://github.com/openai/evals)

**Long Tail of Related Libraries**
- **String2String**: Open source suite of new and traditional algorithms for string comparison, from Stanford
- **Instructor** [https://github.com/jxnl/instructor](https://github.com/jxnl/instructor)
- **Fructose**: [GitHub Repository](https://github.com/bananaml/fructose) by the founder of banana.dev
- **Infini-Gram**: [Website](https://infini-gram.io)
- **BERT Score**: [GitHub Repository](https://github.com/Tiiiger/bert_score)
