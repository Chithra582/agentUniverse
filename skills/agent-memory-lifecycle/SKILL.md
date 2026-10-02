---
name: "agent-memory-lifecycle"
description: "Manages conversational memory, session state, and domain context retention across collaborative multi-agent execution turns."
license: Apache-2.0
---

# Agent Memory Lifecycle

## Overview
This skill manages short-term conversational context, shared blackboard state, and long-term agent memory across multi-agent workflows.

## Key Capabilities
- **Blackboard Coordination**: Provides a shared memory workspace where collaborating agents publish intermediate findings.
- **Session Checkpointing**: Saves full execution snapshots allowing interrupted workflows to resume without data loss.
- **Context Pruning**: Compacts long conversational histories while preserving essential domain parameters and task goals.
- **Multi-Turn Continuity**: Maintains user preferences and historical decisions across consecutive inquiries.

## Operational Workflow
1. **Context Initialization**: Load active session history and blackboard state using `memory_session_store`.
2. **State Updates**: Write agent planning decisions and execution outputs to the shared blackboard.
3. **Blackboard Synchronization**: Broadcast updated state to downstream collaborator agents.
4. **Session Persistence**: Commit finalized state snapshot to persistent storage at workflow completion.
