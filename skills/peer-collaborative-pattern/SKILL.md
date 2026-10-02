---
name: "peer-collaborative-pattern"
description: "Multi-agent orchestration following the Plan-Execute-Express-Review pipeline for structured reasoning and iterative review."
license: Apache-2.0
---

# PEER Collaborative Pattern

## Overview
This skill implements the PEER multi-agent collaboration pattern developed by Ant Group, decomposing complex analytical questions into a 4-stage pipeline: Plan, Execute, Express, and Review.

## Key Capabilities
- **Planner Agent**: Decomposes complex problems into structured subtasks with clear dependency sequences.
- **Executor Agent**: Executes individual subtasks utilizing domain tools, calculators, and knowledge queries.
- **Expresser Agent**: Synthesizes intermediate subtask results into a coherent, professional narrative.
- **Reviewer Agent**: Evaluates the output against accuracy and completeness rubrics, issuing feedback loops if quality thresholds are unmet.

## Operational Workflow
1. **Planning**: Planner agent generates subtask execution graph from user inquiry.
2. **Execution**: Executor agent carries out subtasks sequentially using `tool_caller` and `knowledge_retriever`.
3. **Expression**: Expresser agent compiles draft synthesis.
4. **Review Loop**: Reviewer agent evaluates draft; if quality score $< 0.80$ and loop count $< 3$, feedback is routed back to Executor/Expresser for refinement.
