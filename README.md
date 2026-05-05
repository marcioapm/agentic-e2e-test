# agentic-e2e-test

![CI](https://github.com/marcioapm/agentic-e2e-test/actions/workflows/ci.yml/badge.svg)

Throwaway repo for end-to-end smoke tests of the CDP (Chat-Driven Pipeline) agentic workflow. It exists to verify that the full story → task → PR loop works as expected — from a human writing a story in the project board to a merged PR in this repo.

## What is this?

This repo is a live test harness for the **Agentic E2E Demo** project. Each time a story is run, an AI agent picks up a task, does the work, and opens a PR here. If the PR lands, the pipeline is working.

Nothing production-critical lives here. Break things freely.

## Prerequisites

- **Node.js** ≥ 18 (or Python ≥ 3.11 — TBD based on test runner chosen)
- **Git**
- A GitHub account with read access to this repo (public, so that's everyone)

## Running the tests

> The test suite is scaffolded — real tests coming soon.

```bash
# Install dependencies (once a package.json exists)
npm install

# Run the test suite
npm test

# Or, if using Python/pytest:
# pip install -r requirements.txt
# pytest
```

## CI

Tests run automatically on every push and pull request via GitHub Actions. See `.github/workflows/ci.yml` (forthcoming).

## Contributing

This is a demo/throwaway repo, but PRs are welcome if you're testing the pipeline. Keep changes small and scoped to whatever task you were handed. Don't add real production logic here — it will be ignored or deleted.
