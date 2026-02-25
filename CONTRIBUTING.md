# Contributing Workflow

## 1. Set up locally
1. Clone the repository: `git clone https://github.com/arminpressler/Ottos_test_web.git`
2. Add GitHub token auth for pushes if you plan to open PRs.
3. Check out the permanent staging branch: `git checkout preview`.

## 2. Feature branches
- Branch naming: `feature/<issue-number>-<short-slug>`
- Base branch: always `preview`.
- Keep branches focused on a single issue.

## 3. Pull request requirements
1. Open PRs targeting `preview`.
2. Reference the issue number in the PR body (`Fixes #<issue>` or `Relates to #<issue>`).
3. Include:
   - Summary of changes
   - Testing performed (manual steps or automated results)
4. Ensure lint/tests (if any) pass before requesting review.

## 4. Preview QA and promotion
1. Reviewers test changes after the PR merges into `preview`.
2. When `preview` is stable:
   - Create a PR from `preview` → `main`.
   - Run a final smoke test (load the site locally or via GitHub Pages preview).
   - Merge the PR to publish.

## 5. Housekeeping
- Delete feature branches after merge (GitHub auto-delete is enabled).
- Keep documentation updated if workflows or processes change.
