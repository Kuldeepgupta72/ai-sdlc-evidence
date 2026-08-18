# Jira Management Evidence

## Feature

Enhanced Owner Search – Spring PetClinic

## Purpose

Track the approved requirements as a Jira work item and maintain
traceability between the business requirement, implementation, testing,
and final delivery.

## Jira Details

| Field | Value |
|---|---|
| Jira Project | `<JIRA_PROJECT>` |
| Issue Type | `<ISSUE_TYPE>` |
| Issue Key | `<JIRA_ISSUE_KEY>` |
| Summary | Enhanced Owner Search |
| Status | `<JIRA_STATUS>` |
| Assignee | `<ASSIGNEE>` |

## Jira Story

### Summary

Enhanced Owner Search

### Description

Enhance the Spring PetClinic owner search capability to support
additional search criteria while maintaining compatibility with the
existing owner last-name search behavior.

### Requirements

- Support last-name prefix search.
- Support telephone search.
- Support pet-name search.
- Support case-insensitive pet-name matching.
- Handle leading and trailing whitespace.
- Return unique owner results.
- Preserve existing `lastName` parameter compatibility.
- Preserve pagination/search context where applicable.

## Acceptance Criteria

- Owner can be searched using last-name prefix.
- Owner can be searched using telephone number.
- Owner can be searched using pet name.
- Pet-name search is case-insensitive.
- Search input whitespace is handled.
- Duplicate owners are not returned.
- Existing `lastName` behavior remains compatible.
- JUnit tests validate the required behavior.
- MockMvc tests validate the relevant API/controller behavior.

## Traceability

| Source | Reference |
|---|---|
| Business Analysis | `evidence/01-ba-analysis.md` |
| Requirements | `evidence/02-requirements.md` |
| Jira Issue | `<JIRA_ISSUE_KEY>` |
| Implementation | `implementation/` |
| Tests | `tests/` |

## AI-SDLC Stage

Jira Management

## Previous Stage

Requirements

## Next Stage

Planning