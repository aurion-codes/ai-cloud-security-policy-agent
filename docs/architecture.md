# Architecture

## Current Prototype

The current version focuses on converting a security requirement into a
structured feasibility assessment.

```mermaid
flowchart TD
    A[Security Requirement] --> B[Prompt / Agent Instructions]
    B --> C[LLM]
    C --> D[Security Risk Analysis]
    C --> E[Terraform Mapping]
    C --> F[Sentinel Feasibility]
    C --> G[Enforcement Recommendation]
    C --> H[Test Strategy]
    D --> I[Final Recommendation]
    E --> I
    F --> I
    G --> I
    H --> I
```

## Target Architecture

The next iteration should ground technical recommendations against trusted
documentation.

```mermaid
flowchart TD
    A[Security Requirement] --> B[Agent]
    B --> C[Retriever]
    C --> D[Terraform Provider Docs]
    C --> E[Sentinel Docs]
    C --> F[Cloud Provider Docs]
    D --> G[Grounded Technical Context]
    E --> G
    F --> G
    G --> B
    B --> H[Feasibility Decision]
    H --> I[Human Security Review]
```

## Design Goal

The agent should assist the engineer rather than replace security judgment.

The preferred workflow is:

1. Receive a security requirement.
2. Identify the security intent and risk.
3. Retrieve trusted technical documentation.
4. Map the requirement to Terraform resources and plan data.
5. Determine Sentinel feasibility.
6. Recommend enforcement level.
7. Generate test scenarios.
8. Flag assumptions and limitations.
9. Send the result for human review.
