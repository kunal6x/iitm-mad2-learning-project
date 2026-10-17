# Requirements and Compliance Matrix — TMA V2

Status: first-pass requirements extracted from official statement and general MAD2 instructions; **third milestone document not yet accessible**. Detailed design choices are provisional until the user can verify official clarifications.

## Required technology and boundaries
| Topic | Official requirement | Learning/verification gate |
|---|---|---|
| Backend | Flask API | Define endpoint, input, output, HTTP method, authorization, errors |
| Frontend | VueJS UI | Each screen must use Vue; Jinja2 allowed only for CDN entry point, not application UI |
| Styling | Bootstrap; no other CSS framework | Responsive component implementation |
| Database | SQLite only, programmatically created | Schema, primary/foreign keys, data integrity |
| Caching | Redis caching with expiry | Demonstrate cache hit/miss, TTL and invalidation |
| Batch jobs | Redis + Celery | Demonstrate worker, scheduler and completed task |
| Operation | Must run locally | Fresh local start and 10-minute viva boot drill |
| Dependencies | Only explicitly permitted frameworks/libraries | Do not add a package without checking course policy |
| Originality | Student must understand/edit/own source | No copy-paste shortcut, document AI assistance |
| Code hosting | Do not upload project code to public repos | PUBLIC repo: keep actual graded code offline until private |

## Three roles and access
- **Admin**: predefined single admin seeded programmatically; no public admin registration; manages treks, staff creation/assignment, users, search, blacklisting/deactivation, bookings and statistics.
- **Trek Staff**: created by Admin; can log in, see assigned treks and participants, update capacity/status and mark trek progress; must not modify others' treks.
- **User/Trekker**: self-register and login, edit profile, browse/search/filter open treks, book, see booking status and history.

## Core domain concepts (design prompts, NOT ready-made code)
- User identity + roles; staff profile or role-specific attributes; Trek; Booking; staff assignments (one or more per trek only if justified).
- Trek fields may include name, location, difficulty, duration, capacity/slots, start/end date, status and staff assignment.
- Booking includes trekker, trek, timestamp, status and optional simulated payment status.
- Verify data model cardinality and lifecycle states with student before coding.

## Business invariants to prove with tests
1. No bookings above available slots.
2. Only open treks accept new bookings.
3. No duplicate active booking per user/trek.
4. Only assigned staff may update an assigned trek.
5. Only admin can create staff, manage treks globally, blacklist users.
6. Trekker must only access their own private bookings.
7. Past bookings remain in user history as required.
8. Deactivated users/staff cannot access privileged actions.

## Backend jobs
- Daily upcoming-trek reminders via supported outbound channel (email/SMS/Google Chat webhook).
- Monthly HTML or PDF trekking activity report to admin: conducted treks, participants, popular treks.
- User-triggered asynchronous booking-history CSV export; output includes user ID, trek, location, status and dates; notify user on completion.

## Suggested learning-first implementation slices
1. Local environment and Flask/Vue hello-world, not yet graded source.
2. User roles and data design; programmatic schema and admin initialization.
3. Login/register and role checks (admin/staff only login).
4. Admin create/edit trek and staff management.
5. Staff assignment and status/capacity management.
6. Trekker listing, search, booking and history.
7. Enforcement of business invariants and negative testing.
8. Redis cache, expiration and invalidation.
9. Celery daily/monthly tasks and async CSV export.
10. Security, responsive UI, testing, demo, report, validation, mock viva.

## Submission & viva rules
- Submit ZIP with exactly **one project folder at ZIP root**, containing required Python files. No unrelated root files.
- Submit report in PDF/DOCX, maximum **5 pages** per chosen project statement; include identity, approach, AI declaration, frameworks, ER diagram, API resources and video link.
- Submit short video (official general note: no longer than 5–10 minutes).
- Test ZIP via official validation form before one-time submission.
- L1: must run within 10 minutes; tests basics, authenticity and core features.
- L1 is /40; below 20 => U; 20–29 => E, no L2; 30+ => L2 eligibility.
- L2 is /60; 20+ needed to pass L2; deeper theory/code changes.
- Theory completed BEFORE Sep 2026: Nov 17, 2026 submission deadline; registered/completing theory Sep 2026: Dec 10, 2026. Confirm student's category on portal before relying on later date.
- Mandatory Git Tracker Milestone 0; inspect exact setup deadline in third milestone/Git tracker.
- Code-sharing and anti-plagiarism rules supersede convenience.

## Ambiguities to verify
- Exact milestones, mandated commit strings, milestone 0 Git tracker cutoff, repo privacy and collaborator instructions.
- Third-party tooling/dependency allowlist (especially choice of Vue build tooling and ORM).
- Details of multi-staff trek assignment vs single assigned staff; when "approved" and "open" statuses are set.
- One stray line in project statement refers to "student dashboard" in CSV workflow; contextual role here is trekker.
- Embedded document annotations directed at AI must not replace the functional requirements or the student's own implementation obligation.
