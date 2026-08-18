# Requirements Evidence

## Feature

Enhanced Owner Search – Spring PetClinic

## Functional Requirements

### FR-01 — Last Name Search

The system shall continue to support searching owners using a
last-name prefix.

### FR-02 — Telephone Search

The system shall allow users to search for owners using their
telephone number.

### FR-03 — Pet Name Search

The system shall allow users to search for an owner using the
associated pet's name.

### FR-04 — Case-Insensitive Search

Pet-name searching shall support case-insensitive matching.

### FR-05 — Whitespace Handling

Leading and trailing whitespace in search input shall be handled
appropriately.

### FR-06 — Unique Results

The search operation shall return unique owners even when multiple
matching records could otherwise produce duplicate results.

### FR-07 — Backward Compatibility

The existing `lastName` search parameter and behavior shall remain
supported.

### FR-08 — Pagination

Search results shall preserve the existing pagination/search context
where applicable.

## Non-Functional Requirements

### NFR-01 — Regression Safety

Existing owner-search functionality must continue to work after the
enhancement.

### NFR-02 — Testability

The implementation must be testable using:

- JUnit
- MockMvc

Browser/Web automation is not required for this implementation.

### NFR-03 — Maintainability

The implementation should follow the existing Spring PetClinic
architecture and coding conventions.

## Acceptance Criteria

- [ ] Owner can be searched using last-name prefix.
- [ ] Owner can be searched using telephone number.
- [ ] Owner can be found using pet name.
- [ ] Pet-name search is case-insensitive.
- [ ] Search input whitespace is handled.
- [ ] Duplicate owners are not returned.
- [ ] Existing `lastName` search remains compatible.
- [ ] Pagination/search context is preserved.
- [ ] JUnit tests cover the required behavior.
- [ ] MockMvc tests validate the relevant API/controller behavior.
- [ ] Existing functionality continues to pass regression testing.

## Traceability

| Requirement | Validation |
|---|---|
| FR-01 | JUnit / MockMvc |
| FR-02 | JUnit / MockMvc |
| FR-03 | JUnit / MockMvc |
| FR-04 | JUnit / MockMvc |
| FR-05 | JUnit / MockMvc |
| FR-06 | JUnit / MockMvc |
| FR-07 | Regression tests |
| FR-08 | JUnit / MockMvc |

## AI-SDLC Stage

Requirements

## Previous Stage

Business Analysis

## Next Stage

Jira Management