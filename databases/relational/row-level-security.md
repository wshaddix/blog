# Row-Level Security

The database can refuse a row that an application filter forgot to hide.

## The filter is not enough

- TODO: A global query filter does not run for raw SQL, for a query that ignores filters, or for a connection that never went through the model.
- TODO: Put the same tenant rule in the database so those paths still return nothing. The product side is [Row-level security as a second guard](/building-a-saas/05-multi-tenancy/overview#row-level-security-as-a-second-guard).

## The tenant on the session

- TODO: Set the current tenant on the connection or the transaction before the first statement.
- TODO: A pooled connection remembers that setting. Clear it when the connection goes back, or the next borrower inherits the previous tenant.

## SQL Server

- TODO: A security policy binds a predicate function to the table. The function reads the tenant from session context.
- TODO: Ship the function and the policy in the same migration as the table they protect.

## Postgres

- TODO: Enable row security on the table and add a policy that compares the tenant column to a setting on the session.
- TODO: Name that setting in one place so the application and the policy cannot drift apart.

## Roles that bypass

- TODO: The table owner and a superuser skip the policy unless you force it to apply to them.
- TODO: The login the application uses is not the owner. Force the policy on every role that must not see another tenant, including an admin role the app uses.

## Reads and writes

- TODO: A read policy hides rows. A write check rejects an insert or update that would place a row in another tenant.
- TODO: Apply both. A read policy on its own still allows a write into the wrong tenant.

## The index

- TODO: Index the column the predicate uses, or every query scans the table to enforce the policy.
- TODO: Lead the indexes the application already depends on with the tenant, so the policy and the query share a plan.

## Proving it

- TODO: Connect as the application login, set the session to tenant A, and read tenant B. Expect no rows.
- TODO: Repeat the check for an insert. The write is rejected. The fixture shape is [Two tenants in every fixture](/building-a-saas/10-testing-strategy/overview#two-tenants-in-every-fixture).

## Related Topics

- See [Transactions and isolation](/databases/relational/transactions-and-isolation)
- See [Indexes and query plans](/databases/relational/indexes-and-query-plans)
- See [Building a SaaS: Multi-Tenancy](/building-a-saas/05-multi-tenancy/overview)

---

**Next:** [Indexes and Query Plans](/databases/relational/indexes-and-query-plans)
