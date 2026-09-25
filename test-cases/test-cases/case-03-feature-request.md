# Test Case 03 — Feature Request

## Scenario

A customer wants a dashboard that provides visibility into employee onboarding progress.

There is no immediate operational problem. The customer believes the dashboard would make it easier for the Human Resources (HR) team to monitor onboarding.

This scenario tests whether the AI can distinguish a feature request from a technical problem and avoid assigning unnecessary urgency.

---

## Customer Message

> We would really like to have a dashboard that shows which employees have completed onboarding and which tasks are still outstanding. We don't have an immediate problem, but this would make it much easier for our HR team to monitor progress.

---

## Expected Analysis

### Category

Feature Request — Dashboard / Reporting

### Sentiment

Positive

### Priority

Low

### Analysis Confidence

High

### Customer Goal

Give the Human Resources team centralized visibility into employee onboarding completion and outstanding tasks.

### Important Missing Information

* Whether the dashboard should show individual employees, aggregate progress, or both
* Required metrics and filters
* Who would use the dashboard
* Whether the information needs to be real-time
* How the customer currently monitors onboarding progress
* Whether an existing report or workflow could provide similar visibility

### Recommended Actions

1. Clarify the desired dashboard requirements.
2. Understand how the Human Resources team currently monitors onboarding.
3. Identify the specific information and filters required.
4. Verify whether the requested functionality is currently supported.
5. If the exact functionality is unavailable, identify whether an alternative workflow or reporting approach could meet the underlying need.

### Expansion Opportunity

Potential

### Expansion Reason

The customer is identifying a broader reporting and visibility need for the Human Resources team. This may indicate an opportunity for broader adoption, but the message does not explicitly request additional users, workflows, or capabilities.

### Recommended Follow-Up

Clarify the reporting requirements and verify available functionality before discussing possible solutions.

---

## Evaluation

**Result: Pass after refinement**

The initial analysis correctly identified the request as a dashboard/reporting need and classified it as Low priority because the customer explicitly stated that there was no immediate problem.

During evaluation, two improvements were identified.

### Improvement 1 — Controlled Category

The initial response used:

> Dashboard / Onboarding Progress Tracking

The category taxonomy was refined so that the primary category remains:

> Feature Request

with the dashboard description treated as a secondary descriptor.

This prevents the AI from continually inventing new primary categories.

### Improvement 2 — Separate Sentiment from Intent

The initial response described the sentiment as:

> Positive and solution-oriented

"Solution-oriented" describes customer intent rather than sentiment.

The sentiment taxonomy was therefore restricted to predefined values such as Positive, Neutral, Negative, Frustrated, and Concerned.

The final classification uses:

> Positive

This makes the output more consistent and easier to process.

---

## Key Learning

A customer can request a new capability without experiencing an urgent problem.

The AI should therefore distinguish between:

* What the customer wants
* How the customer feels
* How urgent the request is
* Whether there is evidence of a potential expansion opportunity

These are separate dimensions and should not be combined into a single classification.
