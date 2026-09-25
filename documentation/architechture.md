# Project Architecture

## Overview

The AI Customer Success Workflow Assistant is designed as a human-in-the-loop workflow.

The Artificial Intelligence (AI) model performs an initial analysis of an unstructured customer message and converts it into structured Customer Success information.

A human Customer Success Manager (CSM) reviews the analysis before taking customer-facing or operational action.

---

## Workflow

```text
Customer Message
       │
       ▼
AI Analysis
       │
       ▼
Structured Customer Information
       │
       ├── Category
       ├── Sentiment
       ├── Priority
       ├── Analysis Confidence
       ├── Customer Goal
       ├── Missing Information
       ├── Recommended Actions
       ├── Suggested Customer Response
       ├── Expansion Opportunity
       └── Recommended Follow-up
       │
       ▼
Human CSM Review
       │
       ▼
Customer Follow-up / Internal Action
```

---

## Component 1 — Customer Message

The process begins with an unstructured customer message.

For example:

> Something isn't working correctly with our onboarding process and we need help.

The message may contain incomplete information, technical details, business requirements, or potential expansion signals.

---

## Component 2 — AI Analysis

The message is provided to an Artificial Intelligence model using the Customer Success triage prompt.

The prompt establishes rules for:

* Classification
* Sentiment analysis
* Priority determination
* Confidence
* Information gathering
* Recommended actions
* Customer response generation
* Expansion opportunity detection

The prompt also instructs the AI not to invent product capabilities or customer intent.

---

## Component 3 — Structured Output

The AI transforms the unstructured message into consistent fields.

For example:

```text
CATEGORY:
Technical Issue

SENTIMENT:
Concerned

PRIORITY:
Requires clarification

ANALYSIS CONFIDENCE:
Medium

CUSTOMER GOAL:
Identify and resolve the onboarding problem

MISSING INFORMATION:
- Affected functionality
- Affected users
- Error message
- Business impact

RECOMMENDED ACTIONS:
1. Gather diagnostic information
2. Determine scope
3. Assess business impact

EXPANSION OPPORTUNITY:
None
```

This structured format makes the analysis easier for a Customer Success Manager to review and potentially easier to connect to future workflow automation.

---

## Component 4 — Human Review

The AI output is not treated as a final decision.

A Customer Success Manager reviews the analysis before taking action.

This is a Human-in-the-Loop (HITL) approach.

Human review is particularly important when:

* Priority is high or critical
* Business impact is unclear
* The AI has low confidence
* Product capabilities need verification
* The customer is requesting something potentially unsupported
* An expansion opportunity has been identified

---

## Component 5 — Customer Follow-Up

After reviewing the AI output, the Customer Success Manager can:

* Request additional information
* Investigate an issue
* Verify product functionality
* Provide a response
* Escalate a problem
* Schedule a discovery session
* Follow up after an investigation

The AI provides decision support rather than automatically taking these actions.

---

## Design Principles

### 1. Structured classification

Controlled categories and priority definitions help reduce inconsistent outputs.

### 2. Evidence-based decisions

The AI should base classifications on information contained in the customer's message.

### 3. Explicit uncertainty

When there is insufficient information, the workflow should identify the missing information instead of guessing.

### 4. Human oversight

Customer-facing decisions remain subject to human review.

### 5. No unsupported claims

The AI should not invent product capabilities or promise outcomes that have not been verified.

### 6. Separation of concepts

Category, sentiment, priority, customer intent, and expansion opportunity are treated as separate dimensions.

---

## Future Architecture

A future version could introduce Retrieval-Augmented Generation (RAG).

The potential architecture would be:

```text
Customer Message
       │
       ▼
AI Analysis
       │
       ▼
Retrieve Relevant Product Documentation
       │
       ▼
Verified Product Information
       │
       ▼
Structured Customer Analysis
       │
       ▼
Human CSM Review
       │
       ▼
Customer Follow-up
```

This could reduce the risk of the AI making unsupported statements about product capabilities.

Other potential integrations could include:

* Customer Relationship Management (CRM) systems
* Workflow automation platforms
* Support ticketing systems
* Internal knowledge bases
* Customer health data

These integrations are future concepts and are not currently implemented in this project.
