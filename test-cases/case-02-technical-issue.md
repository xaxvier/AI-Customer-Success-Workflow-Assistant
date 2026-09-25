# Test Case 02 — Technical Issue

## Scenario

A customer's onboarding workflow has stopped sending completion notifications to managers.

Approximately 30 managers are affected, and another group of employees is scheduled to start onboarding the following day.

This scenario tests whether the AI can recognize business impact and urgency without incorrectly classifying the situation as a Critical incident.

---

## Customer Message

> Our onboarding workflow stopped sending the notification to managers when an employee completes their tasks. This started this morning and approximately 30 managers are affected. We have another group of employees starting tomorrow.

---

## Expected Analysis

### Category

Technical Issue — Notification Failure

### Sentiment

Concerned

### Priority

High

### Analysis Confidence

High

### Customer Goal

Restore or troubleshoot the notification process so managers can receive onboarding completion notifications before the next group of employees begins onboarding.

### Important Missing Information

* When the last successful notification was received
* Whether all workflows or only one workflow are affected
* Whether employee task completion is still being recorded
* Any recent workflow or configuration changes
* Error messages or logs
* Notification method being used
* Whether permissions or integrations were recently changed

### Recommended Actions

1. Determine when the notification failure began.
2. Determine whether the issue affects one workflow or multiple workflows.
3. Confirm whether employee task completion is still being recorded.
4. Review relevant configuration, permissions, integrations, or available logs.
5. Determine whether a workaround is available.
6. Escalate through the appropriate support process if required.
7. Prioritize follow-up because another employee group is scheduled to begin onboarding tomorrow.

### Expansion Opportunity

None

### Expansion Reason

The customer message describes an existing functionality problem and does not provide evidence of interest in additional users, workflows, teams, or capabilities.

### Recommended Follow-Up

Provide a status update after the initial investigation and reassess the priority if additional business impact is discovered.

---

## Evaluation

**Result: Pass**

The AI correctly identified the issue as a technical notification problem and classified it as High priority because approximately 30 managers are affected and another onboarding group is starting the following day.

The scenario was not classified as Critical because the available information does not indicate a complete production outage, severe business-wide disruption, or inability for a large number of users to perform essential work.

The AI also correctly identified that there was no evidence of an expansion opportunity.

---

## Evaluation Note

One important consideration is avoiding unsupported promises.

The customer has a time-sensitive situation, but the Customer Success Manager should not promise that the issue will definitely be resolved before the next onboarding group begins.

The appropriate approach is to prioritize the investigation, communicate status, and provide a workaround if one is available.
