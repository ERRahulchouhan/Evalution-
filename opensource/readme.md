Open-source evaluation stack
Tool	RAG	Agents	Main use
Ragas	✅ Excellent	✅	Faithfulness, context precision/recall, answer relevancy, agent/tool metrics
DeepEval	✅ Excellent	✅ Excellent	RAG + agent + LLM unit testing, hallucination, tool correctness
TruLens	✅	✅	RAG quality, groundedness, feedback functions, tracing
Arize Phoenix	✅	✅	Evaluation + tracing + observability + experiments
Langfuse	✅	✅ Excellent	Tracing, datasets, experiments, scores, LLM-as-judge
Opik	✅	✅	Evaluation, experiments, tracing, prompt/agent monitoring
Promptfoo	✅	✅	Test cases, regression testing, assertions, model comparisons
Giskard	✅	⚠️	RAG testing, hallucination, vulnerabilities, LLM testing
TruLens	✅	✅	Groundedness/relevance and application feedback
Inspect AI	⚠️	✅ Excellent	Agent/model evaluations, tasks, scoring, tool-use evals
OpenAI Evals	⚠️	⚠️	General evaluation framework; framework itself is open source
LangSmith SDK/evaluation concepts	✅	✅	Useful ecosystem, but LangSmith service itself isn't fully open-source

## Experiment modules

Each unique tool above has a module with a `README.md` explaining when to use it and which
metrics to evaluate, plus an `experiment.ipynb` that loads 10 RAG and 10 agentic AI test
cases. Every listed metric has its own explanation cell followed by a separate code cell
that prepares that metric's test cases. The shared synthetic cases are documented in
[datasets/README.md](./datasets/README.md).
TruLens appears twice in the comparison above but has one module.

- [RAGAS](./ragas/)
- [DeepEval](./deepeval/)
- [TruLens](./trulens/)
- [Arize Phoenix](./arize-phoenix/)
- [Langfuse](./langfuse/)
- [Opik](./opik/)
- [Promptfoo](./promptfoo/)
- [Giskard](./giskard/)
- [Inspect AI](./inspect-ai/)
- [OpenAI Evals](./openai-evals/)
- [LangSmith SDK/evaluation concepts](./langsmith/)