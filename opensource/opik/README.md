# Opik

Opik is useful for tracing and evaluating LLM applications, comparing experiments, and
monitoring prompts or agent runs. Use it to organize evaluations around datasets and traces;
select metrics that match the outputs and spans your application records.

## RAG metrics

- **Answer relevance** — answer addresses the query.
- **Faithfulness / hallucination** — answer claims are supported by context.
- **Context precision and recall** — retrieved evidence is relevant and sufficiently complete.
- **Answer correctness** — response matches trusted references.

## Agentic AI metrics

- **Task completion** — final result meets the task criteria.
- **Tool-call and argument correctness** — actions and inputs are appropriate.
- **Trajectory quality / step efficiency** — action sequence is useful and avoids waste.
- **Safety / policy compliance** — tool actions and final response follow policy.

Calibrate LLM-as-a-judge metrics against human labels and monitor latency/cost separately from
quality scores.

See [experiment.ipynb](./experiment.ipynb) for the experiment contract.
The notebook loads 10 shared RAG and 10 agentic AI examples from [the synthetic datasets](../datasets/README.md).
Each Opik metric has its own explanation and test-case code cell.
