# CodeMie Assistant Configs

Import-ready CodeMie assistant definitions backing the AI-SDLC workflow
(`../workflow/workflow.yml`). Each file was exported from the CodeMie platform
and reduced to the fields accepted by `codemie sdk assistants create/update`.

Project: `kuldeep_gupta1@epam.com`

## Files → Assistant → Workflow node(s)

| Config file | Assistant | assistant_id | Workflow node(s) |
|-------------|-----------|--------------|------------------|
| `01-ba-assistant.json` | AI-SDLC – BA Assistant | `4b9955e1-…` | `BA_ANALYSIS` (assistant_1) |
| `02-requirement-assistant.json` | AI-SDLC – Requirement Assistant | `d3a9867b-…` | `REQUIREMENTS` (assistant_2) |
| `03-jira-management-assistant.json` | AI-SDLC – Jira Management Assistant | `249d5d49-…` | `Jira_management` (assistant_3) |
| `04-planning-assistant.json` | AI-SDLC – Planning Assistant | `bc7fcd9a-…` | `PLANNING` (assistant_4) |
| `05-design-assistant.json` | AI-SDLC – Design Assistant | `3f330bc4-…` | `DESIGN` (assistant_5) |
| `06-development-assistant.json` | AI-SDLC – Development Assistant | `1daf68e2-…` | `DEVELOPMENT` (assistant_6), `CODE_REVIEW` (assistant_8) |
| `07-test-assistant.json` | AI-SDLC – Test Assistant | `4628e708-…` | `TESTING` (assistant_7), `QUALITY_GATE` (assistant_9), `FINAL_HUMAN_APPROVAL` (assistant_10), `JIRA_FINALIZATION` (assistant_11) |

> Two assistants are reused across multiple workflow nodes, so 7 configs cover
> all 11 workflow assistant slots.

## Usage

Create a new assistant from a config:

```bash
codemie sdk assistants create --json 01-ba-assistant.json
```

Update an existing assistant:

```bash
codemie sdk assistants update <assistant-id> --json 01-ba-assistant.json
```

## Notes

- `context` entries reference datasource IDs in the source project; re-importing
  into a different project requires the equivalent datasources to exist there.
- `toolkits` reference project/user integrations (Git, Project Management) that
  must be configured in the target project. Add `"skip_integration_validation":
  true` if importing with test credentials.
- Server-managed fields (`id`, `slug` history, counts, timestamps) were removed;
  `slug` is retained for stable deep-linking.
