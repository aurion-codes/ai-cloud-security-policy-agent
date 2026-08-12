# Example Security Requirement: Amazon S3

## Cloud Provider
AWS

## Service
Amazon S3

## Security Domain
Data Protection

## Security Requirement

All S3 buckets storing sensitive data must prevent public access and enforce
encryption at rest.

Infrastructure that does not meet these requirements should be prevented from
deployment unless an approved exception exists.

## Task

Perform a cloud security feasibility assessment and determine whether this
requirement can be enforced using Terraform Sentinel.

Identify:

- Relevant Terraform resources and attributes
- Security risks addressed
- Sentinel policy-as-code feasibility
- Recommended enforcement level
- Exception and override considerations
- Positive, negative, and edge-case test scenarios
- Technical limitations
- Final recommendation of Feasible, Partially Feasible, or Not Feasible
