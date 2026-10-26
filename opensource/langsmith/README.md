# LangSmith SDK / evaluation concepts

LangSmith is useful for tracing, dataset-based evaluation, and comparing application runs.
The source comparison notes that the service is not fully open source; this module covers
the SDK and evaluation concepts, not a claim that the hosted service is open source.

## RAG metrics

- **Correctness** — answer compared with a reference or rubric.
- **Groundedness** — answer supported by retrieved documents.
- **Retrieval relevance** — retrieved documents answer the query.
- **Answer relevance** — response addresses the question.

## Agentic AI metrics

- **Task completion** — whether the run achieved the requested goal.
- **Tool trajectory correctness** — whether tools and ordering match the expected behavior.
- **Argument validity** — tool inputs satisfy schema and task requirements.
- **Efficiency / latency** — steps, retries, and runtime.

Use datasets with expected outputs and trace evaluators for the behavior you need. Log model,
prompt, dataset, and evaluator versions so comparisons are reproducible.

See [experiment.ipynb](./experiment.ipynb) for the experiment contract.
The notebook loads 10 shared RAG and 10 agentic AI examples from [the synthetic datasets](../datasets/README.md).
Each LangSmith evaluator has its own explanation and test-case code cell.
