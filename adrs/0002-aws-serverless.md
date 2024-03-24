# 2. AWS Serverless Platform

Date: 2024-03-24

## Status

- [x] proposed
- [ ] accepted
- [ ] deprecated
- [ ] superseded

## Context

The team is embarking on a new project that requires a highly scalable, reliable, and cost-effective infrastructure. After evaluating various options, the team narrowed down the choices to AWS Serverless and Containers Orchestrators. Each option has its pros and cons, outlined below.

### Option 1: Use AWS Serverless

Pros:
- **Scalability**: Automatically scales with the application's needs without requiring manual intervention.
- **Cost-effectiveness**: Payment is based on the actual usage, reducing the cost during low traffic periods.
- **Reduced operational overhead**: AWS manages the infrastructure, allowing the team to focus more on development rather than maintenance.
- **Fast deployment**: Simplifies and accelerates the deployment process for new applications and features.

Cons:
- **Vendor lock-in**: Using AWS-specific services might limit migration options in the future.
- **Cold start issues**: Initial request latency may be higher, especially for infrequently used services.

### Option 2: Use Containers Orchestrators

Pros:
- **Portability**: Containers can run anywhere, reducing vendor lock-in risks.
- **Flexibility**: Offers more control over the environment and configurations.

Cons:
- **Operational complexity**: Requires more effort to manage and scale effectively.
- **Higher costs**: Potentially higher operational costs due to the need for continuous running of services.
- **Setup and maintenance**: Requires additional setup and maintenance efforts compared to serverless options.

## Decision

The team has decided to use AWS Serverless for the new project.

## Rationale

AWS Serverless was chosen for several key reasons:
- It offers significant scalability and cost-efficiency benefits, crucial for a project with variable and unpredictable workloads.
- The reduction in operational overhead allows the development team to focus more on delivering features and less on infrastructure management.
- Despite the potential for vendor lock-in, the advantages of rapid development, deployment, and reduced costs outweigh this concern for the project's current stage and foreseeable future.

## Consequences

- The team will need to become familiar with AWS Serverless technologies and best practices.
- Monitoring and optimizing for cold start times will be necessary for some components of the application.
- Architectural designs will need to consider AWS-specific features and limitations, potentially impacting portability.
- All team members must be involved in continuous learning to stay updated with AWS Serverless advancements and updates.
