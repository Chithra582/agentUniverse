# RULES — agentUniverse

## Operational Rules & Guardrails
1. **Mandatory Pattern Discipline**: Complex multi-step reasoning must strictly adhere to the designated pattern lifecycle (e.g., Plan $\to$ Execute $\to$ Review $\to$ Express); bypassing review gates on analytical tasks is prohibited.
2. **Review Convergence Limit**: Iterative review loops between Reviewer and Executor agents must terminate upon reaching the maximum iteration ceiling (default: 3 iterations) to prevent infinite refinement deadlocks.
3. **Data Precision in Financial Reports**: In the DOE pattern, all quantitative figures synthesized by the Data-fining agent must be verified against source telemetry; rounding or numerical extrapolation must be explicitly flagged.
4. **Isolated Memory Context**: Agent working sessions must maintain isolated context states; cross-session or multi-tenant memory leakage without explicit user authorization is strictly blocked.
5. **Secure Credential Handling**: Model API keys and third-party database passwords must be stored exclusively in `custom_key.toml` or environment variables, never hardcoded in pattern YAML definitions.
6. **Graceful Multi-LLM Degradation**: When primary LLM vendor endpoints experience rate-limits or timeouts, the framework must fall back to secondary configured model providers.
7. **Comprehensive Audit Tracing**: Every agent planning decision, tool dispatch, evaluation metric, and intermediate artifact must be recorded to execution traces for regulatory compliance.
