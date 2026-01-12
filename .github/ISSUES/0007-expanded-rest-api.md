# Expanded REST API

**Summary**
Add REST endpoints for users, tenants, volunteers, schedules, and events to provide full CRUD and administrative capabilities.

**Motivation**
Current API surface is small. Additional endpoints are required for admin workflows, volunteer coordination, and calendar integration.

**Acceptance criteria**
- Endpoints: `GET/POST/PUT/DELETE` for `users`, `tenants`, `volunteers`, `activities`, `events`, `schedules`.
- API documentation updated (OpenAPI) and examples in README.
- Tests for the new endpoints.

**Suggested tasks**
- Create routing modules (or FastAPI routers) for each resource.
- Wire routers into the app and secure appropriate endpoints.

**Notes**
`brio/routing/*.py` shows a similar organization.
