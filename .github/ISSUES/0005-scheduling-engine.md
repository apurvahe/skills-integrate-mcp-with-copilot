# Scheduling engine (events, recurrence, junctures)

**Summary**
Implement structured event and schedule management: event instances, recurrence rules, time-slot/juncture handling, and capacity enforcement.

**Motivation**
Current schedule is a free-text string. Structured schedules enable conflict detection, recurring events, and better calendar integrations.

**Acceptance criteria**
- `Event` model representing date/time, duration, recurrence rule (RFC5545/rrule compatible or simplified), capacity, and assigned activity.
- `Schedule` or `Juncture` constructs for time-slot availability.
- Signup enforces capacity and checks schedule conflicts for participants and volunteers.
- Endpoints to create/update events and view calendar blocks.

**Suggested tasks**
- Add `brio/models/events.py` and `brio/models/schedules.py`.
- Implement validation in operations to detect conflicts and enforce limits.
- Add tests for recurrence and conflict detection.

**Notes**
See `events.py`, `schedules.py`, and `junctures.py` in the `brio` layout.
