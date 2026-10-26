# OpenAI Evals

OpenAI Evals is an open-source evaluation framework for defining and running evaluation
sets. It is useful when custom graders or structured test cases fit your stack. The README
comparison marks it as limited for the specific RAG and agent use cases, so treat both as
custom integrations rather than assuming built-in domain-specific metrics.

## RAG metrics to implement

- **Answer correctness and relevance** — custom grader against references/rubrics.
- **Groundedness / hallucination** — grader compares response claims with retrieved context.
- **Retrieval precision / recall** — custom scorer using labeled relevant documents.

## Agentic AI metrics to implement

- **Task completion** — grader against expected outcome.
- **Tool-call correctness and argument validity** — compare captured trace with expected actions.
- **Safety and policy compliance** — deterministic checks plus rubric-based grading.
- **Step efficiency** — custom scoring over trace length, retries, and latency.

Confirm compatibility with your model/runtime and maintain labeled examples. This framework
does not automatically instrument an arbitrary production RAG or agent application.

See [experiment.ipynb](./experiment.ipynb) for the experiment contract.
The notebook loads 10 shared RAG and 10 agentic AI examples from [the synthetic datasets](../datasets/README.md).
Each custom evaluation metric has its own explanation and test-case code cell.
