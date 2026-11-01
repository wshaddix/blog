# Recipes

Short Git sequences for everyday work.

## Rebase on shared branches

- TODO: Rebase a branch only while you are the only person using it.
- TODO: After someone else has pulled it, merge to take new commits from the base.
- TODO: A force-push after that rebase rewrites commits other people already have.

## Finding commits that seem lost

A commit missing from the branch you are looking at is often still in the local repository.

- TODO: Start with how it went missing: committed on a different branch, made on a detached HEAD, or stored under a name you did not expect.
- TODO: Use `git worktree list` and `git branch -a --contains` to see which branch or worktree still has the commits.
- TODO: After a reset or a removed worktree, read `git reflog`, including the reflog for that branch.
- TODO: Run `git fsck --lost-found` when no branch and no reflog still points at the commit.
- TODO: Before `git worktree remove`, confirm the branch is pushed and that `git log origin/branch..branch` shows no unpushed commits.
- TODO: The reflog's expiry is the window you have to recover the commit, before garbage collection drops it.
- TODO: Keep a short checklist an agent runs before it deletes a worktree. See [Before removing a worktree](/ai-assisted-development/techniques#before-removing-a-worktree).

## Related Topics

- See [Branching and pull requests](/devops/version-control/branching-and-pull-requests)
- See [Building a SaaS: Project Setup](/building-a-saas/01-project-setup/overview)

---

**Next:** [Branching and Pull Requests](/devops/version-control/branching-and-pull-requests)
