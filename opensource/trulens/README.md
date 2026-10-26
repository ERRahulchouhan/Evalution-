# TruLens

TruLens is useful when you want feedback functions and trace-level evaluation integrated
with an instrumented LLM application. Its RAG triad is a practical starting point for
grounding and retrieval checks; agent workflows can use the same trace and feedback approach.

## RAG metrics

- **Groundedness** — whether response claims are supported by retrieved context.
- **Answer relevance** — whether the response answers the user.
- **Context relevance** — whether retrieved context is useful for the query.

## Agentic AI metrics

- **Task success** — whether the requested outcome was achieved.
- **Tool selection / tool-call validity** — whether actions fit the task and tool schema.
- **Groundedness** — whether claims remain supported by tool results and context.
- **Action efficiency** — whether the trace avoids unnecessary steps or repeated calls.

Implement agent-specific feedback over captured traces; the RAG triad alone does not measure
tool correctness or goal completion. Add human-reviewed examples to calibrate LLM feedback.

See [experiment.ipynb](./experiment.ipynb) for the experiment contract.
The notebook loads 10 shared RAG and 10 agentic AI examples from [the synthetic datasets](../datasets/README.md).
Each TruLens metric has its own explanation and test-case code cell.
