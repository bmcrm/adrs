# 1. Record architecture decisions

Date: 2024-04-01

## Status

- [x] proposed
- [ ] accepted
- [ ] deprecated
- [ ] superseded

## Context

- We need single place for all our architectural decisions made along the project development

### Option 1: Use ADRs

Pros:
- ADRs are a well-known standard for documenting architectural decisions
- ADRs can be easily integrated into the project repository

Cons:
- ADRs require additional time to write and maintain

### Option 2: Use Wiki

Pros:
- Wiki is a well-known standard for documentation

Cons:
- Wiki is not a standard for documenting architectural decisions
- Wiki requires additional setup and maintenance

## Decision

Use GitHub repo with ADRs as Markdown files to document all architectural decisions.

## Rationale

It's a best practice and a common standard to use ADR as a centralized place for Architecture Decisions. Using git also provides additional visibility and a developer-friendly interface.

## Consequences

Team members must submit ADRs proposals to start discussions when significant changes introduced to code, data, or infrastructure.
Other team members must review and give feedback as soon as possible.
All team members must keep the ADRs up to date and well-explained so new team members can use ADRs as the high-level overview of the system.
