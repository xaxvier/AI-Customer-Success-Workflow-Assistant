# AI Customer Success Workflow Assistant

## Overview

This project explores how Artificial Intelligence (AI) can support Customer Success workflows by transforming unstructured customer messages into structured, actionable information.

The assistant analyzes a customer message and identifies:

* Category
* Sentiment
* Priority
* Analysis confidence
* Customer goal
* Missing information
* Recommended actions
* Suggested customer response
* Potential expansion opportunity
* Recommended follow-up

The project was created as a practical learning exercise to explore AI-assisted Customer Success workflows, prompt engineering, structured outputs, and AI evaluation.

---

## Problem

Customer Success Managers (CSMs) regularly receive customer requests in different formats and with different levels of detail.

A single message might contain:

* A technical problem
* A business impact
* A feature request
* An opportunity to expand product usage
* Missing information that must be collected before taking action

Manually interpreting every message can take time and can lead to inconsistent prioritization or follow-up.

This project explores whether an AI assistant can provide a consistent first-pass analysis while keeping a human Customer Success Manager in the decision-making loop.

---

## How It Works

The workflow follows this general process:

```text
Customer Message
       ↓
AI Analysis
       ↓
Category + Sentiment + Priority
       ↓
Customer Goal
       ↓
Missing Information
       ↓
Recommended Actions
       ↓
Suggested Customer Response
       ↓
Expansion Opportunity
       ↓
Recommended Follow-up
       ↓
Human Customer Success Review
```

The AI does not automatically take action on behalf of the Customer Success Manager.

Instead, it provides structured information that a human can review before responding to the customer or updating internal workflows.

---

## Classification Framework

### Categories

The assistant uses a controlled category taxonomy:

* Technical Issue
* Workflow Automation
* Feature Request
* Integration
* Training / How-To
* Billing
* Account / Access
* General Question

A short secondary descriptor can be added when useful.

### Sentiment

The assistant uses five sentiment categories:

* Positive
* Neutral
* Negative
* Frustrated
* Concerned

Customer intent and sentiment are treated separately. For example, a customer can be positive and exploratory while discussing additional use cases.

### Priority

Priority is determined using the available business impact and urgency information.

| Priority               | Examples                                                                                                       |
| ---------------------- | -------------------------------------------------------------------------------------------------------------- |
| Critical               | Production/service outage, severe business disruption, large numbers of users unable to perform essential work |
| High                   | Important functionality unavailable, significant business impact, time-sensitive issue                         |
| Medium                 | Recurring problem, significant manual work, important workflow issue, upcoming business activity affected      |
| Low                    | General question, training request, feature exploration, minor inconvenience                                   |
| Requires clarification | Not enough information to determine impact, urgency, affected users, or functionality                          |

The **Requires clarification** state is important because the AI should not guess when critical information is missing.

---

## Expansion Opportunity

The assistant does not automatically treat every customer problem as an expansion opportunity.

It uses three levels:

### None

There is no evidence of additional adoption or broader use.

### Potential

The customer mentions needs that could potentially involve:

* Additional workflows
* Additional teams
* More users
* Reporting
* Increased usage
* Additional use cases

### Strong Signal

The customer explicitly expresses interest in:

* Using the platform for another department
* Adding additional workflows
* Expanding the number of users
* Evaluating additional capabilities
* Automating additional business processes

Expansion classification is based on evidence in the customer's message rather than assumptions.

---

## Prompt Design

The core of the project is a structured prompt that instructs the Artificial Intelligence model to:

1. Analyze the customer's message.
2. Classify it using predefined categories.
3. Separ

