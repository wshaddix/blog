# Sagas

A multi-step workflow that crosses service boundaries.

## Multi-step workflows across services

## When compensation fails

### What is already undone

## Needs a person

### Who resolves it

## Step order

- TODO: List the steps in the order they must commit. Compensation walks back along that list.
- TODO: A step that cannot be undone has to sit where a later failure still has a way out.

### Hold, then capture

- TODO: Place a hold on the scarce thing first: a seat, a balance, or a card authorization.
- TODO: Run the later steps while that hold stays open.
- TODO: Capture after those steps have committed. Release the hold when a later step fails.

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
