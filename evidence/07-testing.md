# Testing Evidence

## Feature

Enhanced Owner Search – Spring PetClinic

## Testing Objective

Validate the Enhanced Owner Search implementation against the approved
requirements using automated Java tests.

## Test Technology

The current implementation uses:

- JUnit
- MockMvc

Browser/Web automation is not part of the current testing scope.

## Test Coverage

The test suite covers the following areas:

### Last Name Search

- Existing `lastName` parameter behavior.
- Last-name prefix search.
- Leading/trailing whitespace handling.
- Not-found behavior.

### Telephone Search

- Empty input validation.
- Exact telephone matching.
- Whitespace trimming.
- Non-normalized telephone formatting.
- Telephone search precedence over the legacy last-name parameter.

### Pet Name Search

- Pet-name matching.
- Case-insensitive matching.
- Whitespace trimming.
- Multiple matching owners.
- Duplicate-owner prevention.
- Single-owner redirect behavior.
- Not-found behavior.

### Pagination

- Preservation of the last-name search parameter.
- Preservation of telephone search criterion and term.
- Preservation of pet-name search criterion and term.

## Test Classes

The implementation includes tests in:

```text
src/test/java/org/springframework/samples/petclinic/owner/OwnerControllerTests.java

src/test/java/org/springframework/samples/petclinic/owner/OwnerRepositoryPetNameSearchTests.java

src/test/java/org/springframework/samples/petclinic/owner/EnhancedOwnerSearchIntegrationTests.java