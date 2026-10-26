# Inspect AI

Inspect AI is designed for evaluating models and agents through tasks, solvers, and scorers.
It is a strong choice for agentic workflows where you need controlled task environments,
multi-step traces, and explicit scoring. RAG can be tested by adding retrieval to the task
and scoring retrieved evidence and generated answers.

## RAG metrics

- **Retrieval relevance / evidence coverage** — scorer compares retrieved documents with labels.
- **Groundedness** — response claims are supported by retrieved evidence.
- **Answer correctness** — response satisfies the reference or task rubric.
- **Refusal / safety behavior** — expected response to restricted or unsupported requests.

## Agentic AI metrics

- **Task success** — scorer judges whether the objective is satisfied.
- **Tool-use correctness** — tool choices, arguments, and results are appropriate.
- **Trajectory quality** — intermediate actions support the goal.
- **Efficiency and safety** — step budget, policy compliance, and prohibited actions.

Keep task setup deterministic where possible, record tool traces, and separate scorer
uncertainty from actual agent failures.

See [experiment.ipynb](./experiment.ipynb) for the experiment contract.
The notebook loads 10 shared RAG and 10 agentic AI examples from [the synthetic datasets](../datasets/README.md).
Each Inspect AI scorer has its own explanation and test-case code cell.
