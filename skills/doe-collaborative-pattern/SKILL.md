---
name: "doe-collaborative-pattern"
description: "Multi-agent pipeline coordinating Data-fining, Opinion-injection, and Express for precision calculation and domain expertise."
license: Apache-2.0
---

# DOE Collaborative Pattern

## Overview
This skill implements the DOE (Data-fining, Opinion-inject, Express) pattern, tailored for data-intensive, computationally rigorous tasks such as financial report generation and quantitative market analysis.

## Key Capabilities
- **Data-fining Agent**: Ingests, normalizes, and validates structured datasets, computing key financial metrics and ratios.
- **Opinion-inject Agent**: Infuses qualitative domain expert viewpoints, industry context, and strategic perspectives.
- **Expresser Agent**: Merges hard numerical findings with expert opinions to deliver executive-grade reports.

## Operational Workflow
1. **Data Ingestion**: Data-fining agent extracts and calculates numerical metrics via `tool_caller`.
2. **Perspective Injection**: Opinion-inject agent retrieves domain perspectives and regulatory stances via `knowledge_retriever`.
3. **Report Synthesis**: Expresser agent compiles quantitative tables and qualitative commentary into a unified document.
4. **Validation**: Verifies numerical consistency between generated commentary and source data tables.
