# Volunteer management

**Summary**
Add volunteer profiles and assignment flows so volunteers can be registered and assigned to events or activities.

**Motivation**
Volunteer coordination is essential for safe, supervised extracurricular activities.

**Acceptance criteria**
- `Volunteer` model with contact info, availability, and skills.
- Endpoints to register volunteers and assign them to `Event` instances.
- Admin interface/API to view and manage volunteer assignments.

**Suggested tasks**
- Add `brio/models/volunteers.py` or equivalent.
- Add operations to match volunteers to events based on availability.
- Add UI placeholders in `static/` or API docs.

**Notes**
Matches `brio/models/volunteers.py` and operations for assignments.
