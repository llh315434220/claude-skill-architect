# Technical Design Document Template

*Author: [User Name]*
*Status: Draft*

## 1. Context & Scope
*   **Problem Statement:** What are we solving?
*   **Goals:** What is the definition of success?
*   **Non-Goals:** What are we explicitly NOT doing?

## 2. Proposed Design
*   **High-Level Architecture:** (Describe the system diagram here)
*   **API Design:**
    *   `GET /resource`: Description
*   **Data Model:**
    *   Table: `Users` (Schema details)

## 3. Detailed Design
*   **Algorithm/Logic:** How does the core logic work?
*   **State Management:** How is state handled?
*   **Error Handling:** How do we handle failures?

## 4. Cross-Cutting Concerns
*   **Security:** AuthZ, AuthN, PII handling.
*   **Scalability:** How does this handle 10x growth?
*   **Observability:** Metrics, Logs, Traces.
*   **Cost:** Estimated infrastructure cost.

## 5. Alternatives Considered
*   **Option A:** Why was it rejected?
*   **Option B:** Why was it rejected?

## 6. Rollout Plan
*   **Phases:** Alpha -> Beta -> GA
*   **Rollback:** What if it breaks?
