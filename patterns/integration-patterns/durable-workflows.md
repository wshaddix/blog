---
title: Durable Workflows
order: 65
---

# Durable Workflows

A workflow that stores its place so another process can continue it after a crash.

## Resume after a crash

- TODO: Record the last step that finished. After the host dies, a new process continues from that step.
- TODO: A completed step stays completed across the restart.

## Waits with a deadline

- TODO: A wait names a deadline and a path to take when that deadline passes with no event.
- TODO: Store the deadline with the workflow. A restart keeps the same deadline and fires the timeout path once.

## Replay-safe code

- TODO: Replaying a workflow returns the recorded result of a step that already finished.
- TODO: A replay skips side effects that already happened, such as a sent message or a completed charge.

## An event that arrives early

- TODO: A signal can arrive before the workflow has reached the wait for it.
- TODO: Keep that event until the wait begins, then apply it once.

## Durable execution in .NET

- TODO: Write the workflow as one method when the steps share a wait, instead of a chain of separate jobs. See [A workflow as one method](/building-a-saas/08-background-jobs/overview#a-workflow-as-one-method).
- TODO: Put side effects in activities. The orchestration method only decides the order, so a replay can run it again safely.
- TODO: A durable timer stores the wake time with the workflow and survives a restart.
- TODO: An external event is a signal from outside the process that resumes a workflow waiting on it.
- TODO: Compensation undoes a step that already finished when a later step fails.
- TODO: A plain background job is enough when the work does not wait, replay, or resume after a crash.

### Testing against a local emulator

- TODO: Run the workflow against a local emulator. The test starts the host, delivers the event, and reads the recorded outcome, with no cloud account.

## Practical Examples

- See [Building a SaaS: Background Jobs](/building-a-saas/08-background-jobs/overview) - Workflows that wait
- See [Building a SaaS: Billing Integration](/building-a-saas/09-billing-integration/overview) - Trials and dunning

## Related Topics

- See [Sagas](/patterns/integration-patterns/sagas)
- See [Choreography and Orchestration](/patterns/integration-patterns/choreography-vs-orchestration)

---

**Next:** [Choreography and Orchestration](/patterns/integration-patterns/choreography-vs-orchestration)
