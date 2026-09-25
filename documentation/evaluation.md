# AI Workflow Evaluation

## Evaluation Objective

The objective of the evaluation was to determine whether the Customer Success AI workflow could consistently transform unstructured customer messages into useful, structured information.

The evaluation focused on:

* Classification consistency
* Priority determination
* Sentiment classification
* Identification of customer goals
* Identification of missing information
* Recommended actions
* Expansion opportunity detection
* Handling of ambiguous requests
* Avoidance of unsupported assumptions

---

## Test Method

Five manually created customer scenarios were used.

The scenarios represented different Customer Success situations:

1. Workflow automation
2. Technical issue
3. Feature request
4. Expansion signal
5. Ambiguous customer request

Each scenario was analyzed using the same core prompt.

The output was then reviewed against expected behavior.

When inconsistent behavior was identified, the prompt or classification rules were refined and the scenario was evaluated again.

---

## Evaluation Summary

| Test Case | Scenario            | Result                |
| --------- | ------------------- | --------------------- |
| Case 1    | Workflow Automation | Pass                  |
| Case 2    | Technical Issue     | Pass                  |
| Case 3    | Feature Request     | Pass after refinement |
| Case 4    | Expansion Signal    | Pass                  |
| Case 5    | Ambiguous Request   | Pass after refinement |

---

## Finding 1 — Controlled Categories

### Observation

During the feature request test, the AI initially produced a category such as:

> Dashboard / Onboarding Progress Tracking

Although this described the customer's request, it did not follow the intended controlled taxonomy.

### Improvement

The category system was refined to use a controlled list of primary categories:

* Technical Issue
* Workflow Automation
* Feature Request
* Integration
* Training / How-To
* Billing
* Account / Access
* General Question

A secondary descriptor can provide additional context.

### Result

The primary category became:

> Feature Request

with:

> Dashboard / Reporting

as the secondary description.

### Lesson

Controlled taxonomies can improve consistency and make AI output easier to process downstream.

---

## Finding 2 — Separate Sentiment from Intent

### Observation

The feature request test initially produced:

> Positive and solution-oriented

The term "solution-oriented" describes the customer's intent rather than their emotional sentiment.

### Improvement

Sentiment was restricted to:

* Positive
* Neutral
* Negative
* Frustrated
* Concerned

Customer goals and intent are now handled separately.

### Result

The final sentiment was:

> Positive

### Lesson

AI outputs become more useful when different concepts are represented as separate fields instead of combining them.

---

## Finding 3 — Expansion Signals Should Be Evidence-Based

### Observation

A customer problem or feature request does not automatically represent an expansion opportunity.

### Improvement

Expansion opportunities were divided into:

* None
* Potential
* Strong Signal

The AI must identify evidence in the customer's message before assigning an expansion classification.

### Result

The expansion test correctly identified a Strong Signal because the customer explicitly mentioned two additional use cases.

### Lesson

Customer Success expansion signals should be based on observable customer needs rather than assumptions.

---

## Finding 4 — Introduce "Requires Clarification"

### Observation

The ambiguous customer request initially received:

> Medium priority

However, the customer only said:

> "Something isn't working correctly with our onboarding process and we need help."

There was not enough information to determine the business impact or urgency.

### Improvement

A new priority state was introduced:

> Requires clarification

This is used when information is insufficient to determine priority reliably.

### Result

The ambiguous scenario was classified as:

> Requires clarification

### Lesson

A well-designed AI workflow should be able to recognize uncertainty rather than being forced to make an unsupported classification.

---

## Finding 5 — Avoid Unsupported Commitments

### Observation

When analyzing time-sensitive technical issues, an AI-generated customer response could potentially imply that a problem will be resolved by a particular deadline.

### Improvement

The prompt was updated to prevent unsupported promises and guaranteed resolution deadlines.

The AI can recommend prioritizing an investigation or providing a status update, but it should not guarantee an outcome it cannot control.

### Lesson

Customer-facing AI should distinguish between:

* Recommended action
* Expected outcome
* Guaranteed commitment

These are not equivalent.

---

## Overall Findings

The evaluation demonstrated that prompt design has a significant effect on the consistency and usefulness of AI-generated Customer Success analysis.

The most important improvements were:

1. Controlled classification categories
2. Separate sentiment and customer intent
3. Evidence-based expansion detection
4. Explicit handling of uncertainty
5. Avoidance of unsupported promises

The project also demonstrated that testing multiple scenarios can reveal weaknesses that are not obvious when evaluating a single example.

---

## Limitations

This evaluation has several limitations.

### Small Test Set

Only five manually created scenarios were evaluated.

A larger test set would provide stronger evidence of consistency.

### Human Evaluation

The results were manually reviewed rather than evaluated using an automated scoring system.

### No Production Data

The scenarios are synthetic examples created for learning and demonstration purposes.

They do not represent real customer data.

### No Automated Integration

The current project does not automatically send results to Customer Relationship Management (CRM), support, or workflow systems.

### Model Dependence

AI output can vary depending on the underlying model and its behavior.

---

## Future Evaluation

A future version could evaluate a larger dataset containing dozens or hundreds of anonymized customer scenarios.

Potential evaluation metrics could include:

* Category accuracy
* Priority classification accuracy
* Sentiment accuracy
* Expansion detection accuracy
* Missing-information relevance
* Response quality
* Unsupported-claim rate
* Human reviewer agreement

A future evaluation could also compare different prompt versions to measure whether changes improve consistency.

---

## Conclusion

The evaluation showed that the workflow can provide a useful first-pass analysis of customer messages when clear classification rules and safeguards are provided.

More importantly, the testing process demonstrated that AI workflow design should be iterative.

The workflow was not treated as successful simply because it produced reasonable answers.

Instead:

```text id="v7t1k4"
Design
  ↓
Test
  ↓
Identify weakness
  ↓
Refine
  ↓
Retest
  ↓
Document
```

This iterative process became an important part of the project itself.
