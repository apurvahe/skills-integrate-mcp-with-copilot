# Persisted domain models

**Summary**
Replace the in-memory `activities` dict with persistent domain models and storage for `users`, `kids`, `volunteers`, `activities`, `events`, and `schedules`.

**Motivation**
In-memory storage resets on restart and prevents realistic workflows. Persisted models enable history, queries, and integrations with frontends.

**Acceptance criteria**
- Add ORM models (SQLAlchemy or equivalent) for `User`, `Kid`, `Volunteer`, `Activity`, `Event`, `Schedule`.
- Migrations (or initial SQL schema) are provided.
- `GET /activities` reads from the DB; signup/unregister update DB.
- Basic tests exist to verify persistence.

**Suggested tasks**
- Choose a lightweight DB (SQLite for dev, Postgres for prod) and add `requirements.txt` entries.
- Implement models and simple repository functions.
- Replace in-memory operations with DB-backed operations.

**Notes**
This corresponds to the `brio/models` modules layout.
