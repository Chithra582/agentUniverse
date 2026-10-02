---
name: "domain-knowledge-rag"
description: "Integrates domain-specific knowledge bases, vector stores (Chroma, Milvus), and dense retrieval for financial and enterprise domains."
license: Apache-2.0
---

# Domain Knowledge RAG

## Overview
This skill provides domain-specific Retrieval-Augmented Generation capabilities, allowing agents to access enterprise knowledge bases, financial disclosures, and regulatory documents.

## Key Capabilities
- **Multi-Vector Store Support**: Interfaces with ChromaDB, Milvus, and custom vector databases.
- **Hybrid Retrieval**: Combines dense vector semantic similarity with sparse BM25 keyword matching.
- **Domain Document Chunking**: Employs domain-aware text splitters preserving tabular structures and financial footnotes.
- **Citation Tracking**: Traces generated agent conclusions directly back to source reference documents.

## Operational Workflow
1. **Query Processing**: Formulate domain query from current agent reasoning turn.
2. **Vector Retrieval**: Execute hybrid retrieval against knowledge collections using `knowledge_retriever`.
3. **Re-Ranking**: Filter and rank retrieved passages based on domain relevance.
4. **Context Injection**: Prepend validated knowledge context into agent prompt windows.
