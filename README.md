# AI-SDLC Evidence

This repository contains evidence for the AI-driven Software Development
Lifecycle (AI-SDLC) workflow implemented using CodeMie and Atlassian Jira.

## Objective

Demonstrate how a single business request can be processed through an
end-to-end software development lifecycle using specialized AI assistants,
human approval gates, Jira integration, development automation, testing,
code review, quality validation, and final delivery tracking.

## AI-SDLC Workflow

The workflow is designed around the following stages:

1. Business Analysis
2. Requirements
3. Jira Management
4. Planning
5. Design
6. Human Approval
7. Development
8. JUnit / MockMvc Testing
9. Code Review
10. Quality Gate
11. Final Human Approval
12. Jira Finalization

## Demonstrated Feature

**Enhanced Owner Search – Spring PetClinic**

The feature demonstrates enhanced owner-search capabilities while
preserving existing last-name prefix search behavior.

The workflow covers:

- Last-name prefix search
- Telephone search
- Pet-name search
- Input validation
- Case-insensitive pet-name matching
- Whitespace trimming
- Pagination/search-context preservation
- Unique owner results
- Legacy `lastName` parameter compatibility

## Human-in-the-Loop

Human approval is enforced before code implementation and again before
final delivery.

The workflow must not bypass configured approval checkpoints.

## Testing

The current implementation uses:

- JUnit
- MockMvc

Browser/Web automation is not part of the current implementation.

## Traceability

The evidence is organized to provide traceability across:

Business Request
→ Business Analysis
→ Requirements
→ Jira
→ Planning
→ Design
→ Development
→ Testing
→ Code Review
→ Quality Gate
→ Human Approval
→ Jira Finalization

## Repository Structure

```text
ai-sdlc-evidence/
├── README.md
├── requirements/
├── design/
├── implementation/
├── tests/
├── quality-gate/
├── code-review/
└── evidence/

https://github.com/Kuldeepgupta72/sample-springboot-app
https://kuldeepgupta721990.atlassian.net/wiki/spaces/SD/pages/13598722/AI-SDLC+Orchestrator+End-to-End+Architecture+Demo+Guide