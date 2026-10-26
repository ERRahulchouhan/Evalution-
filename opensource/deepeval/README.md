# DeepEval

DeepEval is useful for LLM unit tests and CI quality gates covering both RAG and agent
behavior. It provides reusable metric classes and test cases, so evaluation suites can be
run alongside application tests.

## RAG metrics

- **Faithfulness** — answer grounding in retrieved context.
- **Answer relevancy** — relevance of the response to the user input.
- **Contextual relevancy** — relevance of retrieved context to the input.
- **Contextual precision / recall** — ranking and completeness of retrieved evidence.
- **Hallucination** — unsupported claims against the provided context or reference.
- **GEval correctness** — rubric-based scoring against a reference or explicit criteria.

## Agentic AI metrics

- **Tool correctness** — whether the agent used the appropriate tools.
- **Argument correctness** — whether tool-call arguments are correct.
- **Task completion / GEval** — whether the requested goal was completed.
- **Step efficiency** — whether the agent used an appropriate number of steps.
- **Role adherence** — whether the agent stayed within its assigned role.

Use deterministic, versioned test cases in CI and separate model/API failures from score
failures. Select only metrics supported by the test-case fields you capture.

See [experiment.ipynb](./experiment.ipynb) for the experiment contract.
The notebook loads 10 shared RAG and 10 agentic AI examples from [the synthetic datasets](../datasets/README.md).
Each DeepEval metric has its own explanation and test-case code cell.
