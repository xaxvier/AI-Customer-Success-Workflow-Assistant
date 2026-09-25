# Test Case 05 — Ambiguous Customer Request

## Scenario

A customer reports that something is not working with their onboarding process but provides no details about the problem.

There is not enough information to determine:

* What functionality is affected
* How many users are affected
* How long the problem has existed
* Whether there is significant business impact
* Whether the situation is urgent

This scenario tests whether the AI can recognize uncertainty instead of guessing.

---

## Customer Message

> Something isn't working correctly with our onboarding process and we need help.

---

## Expected Analysis

### Category

Technical Issue — Onboarding Workflow

### Sentiment

Concerned

### Priority

Requires clarification

### Analysis Confidence

Medium

### Customer Goal

Identify and resolve the problem affecting the onboarding process.

### Important Missing Information

* What specifically is not working
* Expected behavior versus actual behavior
* When the problem started
* Whether the issue can be reproduced
* Number of affected users
* Which part of the onboarding workflow is affected
* Any error messages
* Screenshots or other diagnostic information
* Recent workflow or configuration changes
* Business impact
* Required timeline or deadline

### Recommended Actions

1. Ask the customer what they expected to happen and what actually happened.
2. Determine when the issue started.
3. Identify the affected workflow and users.
4. Request any relevant error messages or screenshots.
5. Determine whether the issue can be reproduced.
6. Assess the business impact and urgency.
7. Reassess the priority once sufficient information is available.
8. Escalate through the appropriate process if the investigation indicates a significant issue.

### Suggested Customer Response

Ask the customer to describe what they expected to happen, what happened instead, when the issue started, and whether they are seeing any error messages.

### Expansion Opportunity

None

### Expansion Reason

No evidence of additional adoption, new workflows, additional teams, or broader product usage is present in the message.

### Recommended Follow-Up

Reassess the issue after the customer provides additional information, particularly the affected functionality, users, business impact, and urgency.

---

## Evaluation

**Result: Pass after refinement**

The initial version of the workflow classified this scenario as Medium priority.

During evaluation, this was identified as a weakness.

The customer had not provided enough information to determine whether the issue was:

* A minor inconvenience
* A recurring workflow problem
* An important business disruption
* A time-sensitive issue
* A severe production problem

Assigning Medium priority would therefore require the AI to make an unsupported assumption.

The priority framework was updated to introduce:

**Requires clarification**

The workflow was then retested using the same scenario.

The updated behavior correctly recognized that more information was required before assigning a definitive priority.

---

## Key Learning

One of the most important principles discovered during testing was:

> An AI workflow should not be forced to provide an answer when the available information does not support one.

In this scenario, uncertainty is itself useful information.

Instead of:

```text
Priority = Medium
```

the workflow can produce:

```text
Priority = Requires clarification
```

and identify exactly what information the Customer Success Manager should collect.

---

## Iterative Improvement

This test demonstrates the project's evaluation cycle:

```text
Initial Prompt
      ↓
Test Scenario
      ↓
Unexpected Classification
      ↓
Identify Root Cause
      ↓
Refine Prompt
      ↓
Retest
      ↓
Improved Behavior
```

The change from a fixed priority classification to a clarification state was made based on observed behavior during testing.
