# Ottos Test Web

Simple GitHub Pages site used for testing the OpenClaw agent.

## Live Site
https://arminpressler.github.io/Ottos_test_web/

## Preview Environment
Latest staging build from the `preview` branch:
https://htmlpreview.github.io/?https://github.com/arminpressler/Ottos_test_web/blob/preview/index.html

## Branch & Deployment Workflow

The repository now uses a permanent `preview` branch to stage changes before they reach `main` (the published GitHub Pages site).

1. **Create a feature branch**: use the format `feature/<issue-number>-<slug>` and branch off of `preview`.
2. **Open a PR into `preview`**: link the GitHub issue in the PR body. Automated checks and manual QA happen on the preview branch.
3. **Merge `preview` into `main`**: once the staged changes are approved, promote them by opening a PR from `preview` to `main`, running a final smoke test, and merging when everything looks good.

This flow keeps `main` stable while allowing continuous testing on `preview`. Update `CONTRIBUTING.md` for detailed contributor steps.
