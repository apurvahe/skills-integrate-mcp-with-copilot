# Authentication & RBAC

**Summary**
Add user accounts, password hashing (bcrypt), login endpoints, and role-based access control (admin/parent/volunteer).

**Motivation**
Current API allows unauthenticated signups; secure authentication and role checks are required for admin actions and privacy.

**Acceptance criteria**
- `POST /auth/register` and `POST /auth/login` endpoints exist.
- Passwords are hashed using bcrypt before storage.
- JWT or session-based authentication is implemented.
- Role checks prevent unauthorized endpoint use (admin-only routes for creating activities, assigning volunteers).

**Suggested tasks**
- Add `users` model fields for hashed password and role.
- Add authentication middleware/dependencies for FastAPI.
- Add tests for login, protected endpoints, and RBAC enforcement.

**Notes**
See `notes/bcrypt` and `brio/models/users.py` for reference.
