# Multi-tenant support

**Summary**
Add multi-tenant capabilities so multiple schools/clubs can use the same instance while keeping data isolated per tenant.

**Motivation**
The project currently manages activities in a single global scope. Multi-tenant support enables separate organizations (tenants) to manage their own activities, users, schedules, and volunteers without data leakage.

**Acceptance criteria**
- A `Tenant` model is introduced with required fields (name, slug, contact info).
- Routes and data access are scoped to a tenant (tenant header, subdomain, or path prefix).
- Admin role is tenant-scoped.
- Tests for tenant isolation and basic CRUD operations exist.

**Suggested tasks**
- Add `brio/models/tenants.py` (or equivalent) and persistence layer.
- Add routing middleware to resolve current tenant from request.
- Update endpoints to filter by tenant.
- Add simple fixtures in tests to verify isolation.

**Notes**
This maps to the `tenants.*` modules observed in the `brio` project.
