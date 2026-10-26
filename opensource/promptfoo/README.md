# Promptfoo

Promptfoo is useful for declarative test cases, prompt/model comparisons, regression checks,
and red-team testing. It is especially practical when you want repeatable pass/fail assertions
in CI across multiple model configurations.

## RAG metrics and assertions

- **Answer correctness / relevance** — rubric or reference-based assertions.
- **Groundedness / hallucination** — assert responses are supported by supplied context.
- **Retrieval relevance** — evaluate retrieved content when the retrieval output is exposed.
- **Refusal and safety behavior** — test expected handling of unsafe or out-of-scope inputs.

## Agentic AI metrics and assertions

- **Task completion** — expected result or rubric-based assertion.
- **Tool selection and argument correctness** — inspect tool calls and compare to expected trace.
- **Tool-use policy / prompt injection resistance** — adversarial test suites and assertions.
- **Latency / cost** — provider metrics or custom thresholds.

Expose tool traces and retrieval contexts as test outputs to evaluate them. A prompt-level
assertion cannot prove a hidden tool action was correct.

See [experiment.ipynb](./experiment.ipynb) for the experiment contract.
The notebook loads 10 shared RAG and 10 agentic AI examples from [the synthetic datasets](../datasets/README.md).
Each Promptfoo assertion has its own explanation and test-case code cell.
