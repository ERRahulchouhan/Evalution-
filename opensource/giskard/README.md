# Giskard

Giskard is useful for systematic LLM/RAG testing, including quality checks and security
oriented probes. Use its RAG evaluation capabilities to find retrieval and generation
failures, and use agent workflows only where your agent's observable inputs, outputs, and
actions can be tested.

## RAG metrics

- **Retrieval precision / recall / hit rate** — whether the retriever finds relevant evidence.
- **Answer relevance** — whether the response addresses the question.
- **Groundedness / hallucination** — whether answers stay within retrieved evidence.
- **Robustness and security probes** — test prompt injection and sensitive-data leakage.

## Agentic AI metrics

- **Task success** — completion of a defined scenario.
- **Tool policy compliance** — whether actions stay within allowed tool boundaries.
- **Argument validity** — schema and business-rule checks on tool inputs.
- **Prompt-injection robustness** — whether untrusted content can redirect actions.

Do not equate vulnerability probes with a complete agent evaluation: include normal task
success and tool-trace assertions as well as security tests.

See [experiment.ipynb](./experiment.ipynb) for the experiment contract.
The notebook loads 10 shared RAG and 10 agentic AI examples from [the synthetic datasets](../datasets/README.md).
Each Giskard metric has its own explanation and test-case code cell.
