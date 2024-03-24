# 4. GitHub Repositories Organization: Git Repo per Domain

Date: 2024-03-24

## Status

- [ ] proposed
- [x] accepted
- [ ] deprecated
- [ ] superseded

## Context

In structuring our project's codebase, we considered several strategies:  Monorepo, a 'repository per microservice', and a 'git repository per domain' approaches. Each of them has distinct advantages and challenges, influencing our project's scalability, manageability, and development workflow.

### Monorepo

Pros:
- Centralized management of dependencies and tooling.
- Simplified code sharing across projects.

Cons:
- Scalability issues with large codebases.
- Complex CI/CD pipelines due to the broad impact of changes.
- Creates a single point of failure for the entire project.
- Challenges in access control and permission management.
- Potential for tight coupling between services.

### Repository per Microservice

Pros:
- High granularity in access control and dependency management.
- Simplified CI/CD pipelines for individual services.

Cons:
- Overhead in managing multiple repositories.
- Challenges in cross-service code reuse and coordinated changes.
- Potential for inconsistencies in tooling and dependencies across repositories.
- Difficulties in tracking changes that span multiple services.
- Complicated mental model for developers due to the fragmented codebase.

### Git Repo per Domain

Pros:
- Balanced approach between manageability and scalability.
- Encourages domain-driven design, enhancing clarity and focus.
- Streamlined CI/CD pipelines for domain-specific changes.
- Improved modularity and autonomy for domain teams.
- Encourages ownership and accountability for the dev teams.

Cons:
- Requires careful domain delineation upfront.
- Potential for inter-domain dependencies complicating deployment.

## Decision

After thorough consideration, we have decided to adopt the "git repo per domain" approach for our project's GitHub repositories structure.

## Rationale

The "git repo per domain" strategy was chosen for its ability to offer a balanced approach to managing our codebase. This strategy supports domain-driven design principles, encouraging teams to think in terms of business capabilities and bounded contexts. It strikes an optimal balance between the scalability challenges of a Monorepo and the manageability issues of a repository per microservice. Furthermore, it allows for more focused development within each domain, streamlined CI/CD processes, and better alignment with our project's architectural goals.

## Consequences

- Teams will be organized around business domains, each responsible for their domain's repository, promoting accountability and expertise.
- Initial effort is required to clearly define domain boundaries, which may evolve as the project progresses.
- Cross-domain coordination will be necessary for changes that span multiple domains, requiring effective communication and planning.
- The project will benefit from improved modularity, making it easier to scale, maintain, and extend our systems over time.
