---
title: Risks and Limits
order: 20
---

# Risks and Limits

The failure modes that show up in a team that uses assistants every day.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Secrets

A prompt, a log, and a pasted config file are copies of the secret.

### Before it reaches the repo

- TODO: Scan the staged diff for a key, a connection string, or a token before the commit is stored.
- TODO: A match blocks the commit. A scan that does not finish blocks it too. A skipped check is not a pass.
- TODO: The hook that applies this rule is [Blocking a commit](/ai-assisted-development/tools#blocking-a-commit).

## Licenses and provenance

Generated code can resemble code the model was trained on. You still publish it under your license.

## Confident errors

APIs, flags, and version numbers are often invented. Check them against the current docs.

## Over-reliance

Accepting a suggestion you cannot explain. The review page is the countermeasure.

## Privacy

What leaves the machine, and which product setting controls it.

## Instructions hidden in data

- TODO: A document, a ticket, or a tool result can contain a sentence that is written as an instruction.
- TODO: That sentence does not widen the task, change the recipient, or add a tool.
- TODO: When you review a run, look for a tool argument that was taken from that untrusted text.

## Retrieval across tenants

A retrieval step can surface another tenant's rows after the database filter did its job.

- TODO: Data access takes a tenant argument. Leave it off and the method fails to compile, which closes a helper that would hand back every tenant's rows.
- TODO: Review the escapes a global filter leaves open: `IgnoreQueryFilters`, raw SQL, Dapper, reporting views, and jobs that run outside a request.
- TODO: Apply the same tenant check to cache keys, search and vector indexes, blob paths, exports, and log and trace attributes.
- TODO: Keep the tenant filter inside the index query. Ranking a mixed set and discarding other tenants in application code is the leak.
- TODO: Practice on staging that holds two look-alike tenants. Signed in as one, a request for the other's ids comes back 404. See [Two tenants in every fixture](/building-a-saas/10-testing-strategy/overview#two-tenants-in-every-fixture).
- TODO: When the query was written by an agent, the tenant predicate is the first thing the review reads. See [Paths that skip the filter](/building-a-saas/05-multi-tenancy/overview#paths-that-skip-the-filter).

## Example

A worked example will go here. When an example produces more than about 30 lines of C#, that code will live in a companion `.cs` file next to this page.

## Related

- [Secrets](/csharp/security/secrets)
- [Verification](/ai-assisted-development/verification)

---

**Next:** [AI-Assisted Development](/ai-assisted-development/overview)
