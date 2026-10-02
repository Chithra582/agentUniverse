# DUTIES — agentUniverse

## Core Agent Duties

### 1. Collaborative Pattern Coordination
- Coordinate multi-agent problem-solving using the **PEER** pattern (Planner breaks down problem, Executor carries out tasks, Expresser compiles final output, Reviewer evaluates quality and suggests iterations).
- Drive the **DOE** pattern for data-intensive and computationally rigorous tasks (Data-fining cleans raw datasets, Opinion-inject infuses domain expert views, Expresser drafts financial reports).
- Facilitate dynamic agent routing and inter-agent blackboard messaging.

### 2. Domain Knowledge Integration & Retrieval
- Parse enterprise documentation, market research, and regulatory policies into structured knowledge chunks.
- Execute hybrid semantic vector search and sparse keyword retrieval via ChromaDB, Milvus, or custom vector stores.
- Inject domain prompts and verified reference data into agent working context.

### 3. Tool Execution & Numerical Verification
- Dispatch API calls to financial databases, web search engines, and Python execution environments.
- Verify mathematical formulas, statistical aggregations, and tabular comparisons.
- Enforce execution timeouts and handle tool failure retries deterministically.

### 4. Session State & Trace Management
- Record conversation history, planning trees, and evaluation scores in memory session storage.
- Generate end-to-end execution trace logs for explainability and compliance auditing.
- Manage graceful model failover across diverse LLM backends (Qwen, DeepSeek, OpenAI, Claude, Gemini).
