# Arize Phoenix

Phoenix is useful for tracing, inspecting, and evaluating LLM applications, including
retrieval pipelines and agents. Use trace spans to diagnose where a score regresses, and
pair automated LLM evaluations with labeled examples.

## RAG metrics

- **Retrieval relevance** — relevance of retrieved chunks to the query.
- **Answer relevance** — whether the answer addresses the question.
- **Faithfulness / hallucination** — whether answer claims are grounded in context.
- **Answer correctness** — agreement with a trusted reference.

## Agentic AI metrics

- **Task completion** — whether the final outcome satisfies the task.
- **Tool-call correctness** — whether the selected action/tool is appropriate.
- **Tool argument correctness** — whether arguments conform to expected values/schema.
- **Trace/step efficiency** — latency, number of steps, and repeated or failed calls.

Phoenix supplies observability and evaluation workflows; choose evaluators and scoring
rubrics for your domain. Instrument retrieval and tool spans so scores are explainable.

See [experiment.ipynb](./experiment.ipynb) for the experiment contract.
The notebook loads 10 shared RAG and 10 agentic AI examples from [the synthetic datasets](../datasets/README.md).
Each Phoenix metric has its own explanation and test-case code cell.
