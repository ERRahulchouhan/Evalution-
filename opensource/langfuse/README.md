# Langfuse

Langfuse is useful for production tracing, datasets, experiment runs, and score tracking.
It helps compare model/prompt versions and inspect regressions over traces. Treat metric
definitions as your responsibility: Langfuse records scores and experiments, while evaluators
or human review produce the scores.

## RAG metrics

- **Faithfulness / groundedness** — support of answer claims by retrieved evidence.
- **Answer relevance** — relevance to the question.
- **Retrieval relevance / context precision** — usefulness and ranking of retrieved chunks.
- **Context recall** — coverage of evidence needed for the reference.
- **Answer correctness** — comparison to a trusted reference.

## Agentic AI metrics

- **Task success** — completion against an expected outcome.
- **Tool-call correctness and argument validity** — expected tool and arguments vs. trace.
- **Step efficiency / latency** — steps and time to completion.
- **Policy adherence** — domain-specific rubric or deterministic checks.

Use versioned datasets and attach scorer name/version to each score. Do not interpret a logged
score as a built-in Langfuse evaluator unless you configured one.

See [experiment.ipynb](./experiment.ipynb) for the experiment contract.
The notebook loads 10 shared RAG and 10 agentic AI examples from [the synthetic datasets](../datasets/README.md).
Each Langfuse metric has its own explanation and test-case code cell.
