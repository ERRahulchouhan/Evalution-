# Shared synthetic evaluation cases

The framework experiment notebooks load these local, synthetic datasets:

- `rag_cases.json` — 10 RAG examples with question, retrieved contexts, response, reference,
  and expected grounding/relevance labels. Includes supported, irrelevant/noisy, and
  deliberately unsupported answer cases.
- `agent_cases.json` — 10 agent examples with task, tool trace, expected tools/outcome,
  final response, expected task/tool/argument/policy labels, step budgets, and latency.
  Includes incorrect tool selection/arguments, failed completion, unsupported claims,
  redundant calls, a privacy-safe refusal, and an unsafe disclosure/policy failure case.

They are illustrative test fixtures, not production customer data or calibrated score
thresholds. Judge-based metrics still require the framework's evaluator and model setup.
Each framework notebook gives every listed metric its own explanation and code cell. That
cell prepares the metric-specific inputs for all 10 examples and reports available expected
labels; it does not claim a framework score until an evaluator is configured.
