# Operations / business layer

**Summary**
Refactor business logic into an `operations/` layer separate from routing to centralize validation, transactions, and permission checks.

**Motivation**
Separating concerns improves maintainability and testability and mirrors `brio/operations/*`.

**Acceptance criteria**
- Move signup/unregister and activity CRUD logic into `operations/*` modules.
- Routing files call operations functions and only handle request/response mapping.
- Unit tests exist for operations functions independent of web framework.

**Suggested tasks**
- Create `operations/activities.py`, `operations/users.py`, etc. and refactor `app.py` handlers to use them.

**Notes**
This mirrors the modular layout found in `brio/operations`.
