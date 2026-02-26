# Contributing Workflow

## Workflow Principles
- All changes flow through feature branches and pull requests targeting `preview`.
- Before requesting review, rebase (or merge) the latest `preview` into your feature branch so conflicts are handled on the branch, not on the protected branch.
- Protected branches (`preview`, `main`) are updated via PR merges only. Direct pushes are reserved for documented emergency fixes and must include a follow-up note in the PR or commit message explaining the rationale.
- Conflict resolutions are documented: if you need to resolve conflicts manually, leave a short note in the PR describing what you did.

## 1. Set up locally
1. Clone the repository: `git clone https://github.com/arminpressler/Ottos_test_web.git`
2. Add GitHub token auth for pushes if you plan to open PRs.
3. Check out the permanent staging branch: `git checkout preview`.

## 2. Feature branches
- Branch naming: `feature/<issue-number>-<short-slug>`
- Base branch: always `preview`.
- Keep branches focused on a single issue.
- Rebase against `preview` regularly (and always before requesting review).

## 3. Pull request requirements
1. Open PRs targeting `preview`.
2. Reference the issue number in the PR body (`Fixes #<issue>` or `Relates to #<issue>`).
3. Include:
   - Summary of changes
   - Testing performed (manual steps or automated results)
4. Ensure lint/tests (if any) pass before requesting review.
5. Resolve any conflicts with `preview` in your branch before marking the PR ready for review. The CI sync-check workflow will fail if conflicts remain.

## 4. Preview QA and promotion
1. Reviewers test changes after the PR merges into `preview`.
2. When `preview` is stable:
   - Create a PR from `preview` → `main`.
   - Run a final smoke test (load the site locally or via GitHub Pages preview).
   - Merge the PR to publish.
   - Document any manual conflict resolution taken during promotion in the PR description or follow-up comment.

## 5. Housekeeping
- Delete feature branches after merge (GitHub auto-delete is enabled).
- Keep documentation updated if workflows or processes change.
- If an emergency hotfix requires bypassing the PR flow, record the reason and follow up with a PR that re-aligns the branches.
