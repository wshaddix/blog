---
title: Sagas
order: 70
---

# Sagas

A multi-step workflow that crosses service boundaries.

## Multi-step workflows across services

<!-- TODO: A sequence of steps, and what a later failure does to the earlier steps -->

## When compensation fails

<!-- TODO: The step that undoes earlier work fails, and the workflow records the step it could not finish -->

### What is already undone

<!-- TODO: Which earlier steps completed their compensation, and which are still open -->

## Needs a person

<!-- TODO: Park the saga until a person chooses the next action -->

### Who resolves it

<!-- TODO: The role that may close the state, and the decision stored with the workflow -->

## Step order

- TODO: List the steps in the order they must commit. Compensation walks back along that list.
- TODO: A step that cannot be undone has to sit where a later failure still has a way out.

## Unknown outcome after a timeout

- TODO: A timeout means the caller stopped waiting. It does not mean the step failed.
- TODO: Read the remote outcome before retrying or compensating. Guessing can charge twice or undo a success.

## Practical Examples

- See [Building a SaaS: Background Jobs](/building-a-saas/08-background-jobs/overview)
- See [Building a SaaS: Billing Integration](/building-a-saas/09-billing-integration/overview)

## Related Topics

- See [Outbox and the Idempotent Consumer](/patterns/integration-patterns/outbox-and-idempotent-consumer)
- See [Choreography and Orchestration](/patterns/integration-patterns/choreography-vs-orchestration)

---

**Next:** [Choreography and Orchestration](/patterns/integration-patterns/choreography-vs-orchestration)
