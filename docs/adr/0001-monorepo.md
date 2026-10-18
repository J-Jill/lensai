# ADR 0001: Use a monorepo

- **Status:** Accepted
- **Date:** 2026-10-18

## Context
LensAI has four parts: a backend, a frontend, a demo AI app and the infrastructure.
We needed to decide where to keep the code for each part.

## Decision
We will keep all parts in single repository, each one in its own folder.

## Alternatives considered
A polyrepo: one repository for each part. We did not choose it because a
change that affects the backend and the frontend would need two pull requests
and careful coordination.

## Consequences
- Good: one change across backend and frontend goes in a single commit.
- Good: anyone visiting the GitHub repo can see the whole system in one place.
- Trade-off: if the project grew to many teams and services, one repository
  could become slow and harder to manage.