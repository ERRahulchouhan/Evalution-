# RAGAS

RAGAS is a good fit when you need repeatable, reference-aware evaluation of a RAG pipeline,
including retrieval quality and answer grounding. It also has agent-oriented metrics, so it
can assess tool-using workflows when you record the agent's tool calls and expected behavior.

## RAG metrics

- **Faithfulness** — whether answer claims are supported by retrieved context.
- **Answer relevancy** — whether the answer addresses the question.
- **Context precision** — whether relevant retrieved chunks rank above irrelevant chunks.
- **Context recall** — whether retrieval includes evidence needed by the reference answer.
- **Answer correctness** — answer alignment with the reference.
- **Noise sensitivity** — whether irrelevant context causes errors.

## Agentic AI metrics

- **Tool-call accuracy** — whether the selected tools and calls match the expected trace.
- **Agent goal accuracy** — whether the agent completes the requested goal.
- **Tool-call argument accuracy** — whether arguments are valid and grounded in the task.
- **Trajectory quality** — whether the sequence of actions is appropriate and efficient.

Use representative production traces, references, and expected tool behavior. Define pass
thresholds from a measured baseline; do not treat example thresholds as universal.

See [experiment.ipynb](./experiment.ipynb) for the RAG and agent evaluation plan.
The notebook loads 10 shared RAG and 10 agentic AI examples from [the synthetic datasets](../datasets/README.md).
Each RAGAS metric has its own explanation and test-case code cell.
