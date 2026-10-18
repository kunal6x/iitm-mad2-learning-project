# MAD-2 FINAL ZERO-TO-INDEPENDENT-DEVELOPER PLAN

**Date:** 2026-10-18  
**Project:** IIT Madras Modern Application Development II — Trekking Management Application V2  
**Learner baseline:** Absolute beginner, including computer/terminal and programming fundamentals  
**Primary goal:** The learner handwrites, tests, debugs, modifies, explains and submits an original, requirements-compliant project and succeeds in Level 1 and Level 2 vivas even when questions differ from seniors' reports.

## Authority and constraints

- Primary authority: [official instructions, chosen project statement, and milestones](SOURCE_INDEX.md), plus official course announcements and portal updates.
- Senior survey: 676 nonempty experience responses from 2023–Aug 2026; an **anecdotal pattern library**, never a finite question syllabus or exam guarantee.
- Tech requirements captured from official statement: Flask API; VueJS UI; Bootstrap; programmatically created SQLite; Redis cache; Redis + Celery background jobs; Admin, Trek Staff, Trekker roles.
- Official milestone instructions and some embedded diagrams still need verification, particularly mandatory Git tracker Milestone 0 and commit expectations.
- Project code and secrets must never be committed to this currently **public** learning repository. Use it only for original study notes, exercises that are unrelated to assessed deliverables, checklists and progress. The user's original graded code is kept locally until an authorized private submission-compliant destination exists.
- The only GitHub repository for this learning effort is `kunal6x/iitm-mad2-learning-project`. Do not modify any unrelated projects.
- No shortcut via fully AI-authored project code. Small teaching examples are allowed; genuine assessed project implementation is student-authored. Record AI use honestly if required.
- Known course documentation mentions different submission deadlines depending on theory cohort: 2026-11-17 or 2026-12-10; **do not assume the later date without confirming registration category and course portal**.

## The learning promise: two tracks at once

**Track A — Learn fundamentals:** What/why/how, microscopic worked example, mental simulation, student-produced example, deliberate bug, teach-back.

**Track B — Build a compliant project:** As soon as a relevant skill is understood, apply it to the real Trekking Management V2 requirements. Start with a tiny vertical slice (browser → Vue → API → ORM → SQLite) as soon as minimal prerequisites are met; grow role by role. Never delay all project implementation until every course topic is exhausted.

**Track C — Examiner training:** Every session includes targeted viva questions, source-file explanations and one unfamiliar requirement variation. Senior-reported tasks seed ideas; the examiner may ask harder or different things.

## Teaching loop for EVERY micro-topic

1. **Purpose:** connect the concept to a real action in Trekking, using simple Hindi/Hinglish and correct English technical terms.
2. **Mental model:** explain inputs/outputs, diagrams, running process and what could go wrong.
3. **Trace:** predict the output of a 3–12-line example before running it.
4. **Type:** learner writes from a blank file; no blind copy/paste.
5. **Run:** observe actual output, inspect traceback/browser/network logs if needed.
6. **Break/fix:** learner identifies and repairs one intentional bug.
7. **Transfer:** learner changes data, constraints or a feature without a step-by-step script.
8. **Explain:** 2–4 'why/how/what-if' questions and one code walkthrough.
9. **Record:** log mastery evidence, mistakes, commands, files, revision date and next task in `SESSION_HANDOFF.md` (no unverified completion).

**Assistance ladder:** (1) learner attempts alone → (2) guiding question → (3) conceptual hint → (4) pseudocode → (5) minimal worked example unrelated to graded project → (6) line-by-line rescue for a stuck prerequisite. Withdraw hints as mastery grows.

**Mastery levels:**
- 0: Not seen.
- 1: Can follow an explanation.
- 2: Completes an exercise with help.
- 3: Writes and debugs independently, referring to documentation if necessary.
- 4: Handles a new unseen variant under time pressure and explains trade-offs.

**Gate for a key topic:** level 3 or 4; correctly explain reasoning; code from blank; test success + failure; repair a bug; adapt to one unpracticed variation. Never mark 'mastered' just for having read the lesson.

## Dependency-driven learning modules

| Stage | Foundations | Project application and pass gate |
|---|---|---|
| M0 | Laptop, files, extensions, paths, terminal, VS Code, Python interpreter, pip/venv, Git, processes/ports, browser ↔ server mental model | Learner creates/saves/runs a Python file and narrates request-response from click to data store |
| M1 | Python syntax, values/types, Boolean logic, conditions, loops, collections, functions, imports, scope, errors, files, classes/objects, tests | Independently implement trek capacity, duplicate-check and role-permission pure Python drills |
| M2 | Internet basics, client/server, URLs, HTTP methods, status, JSON, cookies, HTML forms, CSS layout, Bootstrap, DevTools | Hand-build a trek search/booking mock page and inspect a network request |
| M3 | Flask app, decorators, routes, path/query params, request/JSON body, validation, response/errors, Blueprints and configuration | Write several treks GET/filter and validated POST API endpoints from blank |
| M4 | SQLite, SQL CRUD/joins, PK/FK/UNIQUE/CHECK, ER cardinalities, indexing/transactions; SQLAlchemy models, relationships/session/filters/joins | Build and query real role/trek/booking models, reject invalid/duplicate/overcapacity bookings |
| M5 | JavaScript language, functions, arrays/objects, events, DOM, fetch, promises and async/await | Fetch and display API results, handle loading/errors without copying |
| M6 | Vue root/app, SFCs, reactivity, directives, v-model, router, props/emits, computed/watch, lifecycle, state and API integration | Build a routed trek list and a new page on an unfamiliar request |
| M7 | Incrementally integrate Admin, Staff and Trekker roles; auth/session/authorization, responsive UI, booking lifecycle | Demo core workflows end-to-end with role/invalid-data checks, explain every file |
| M8 | Redis key/TTL, cache hit/miss, invalidation; Celery broker/worker/beat, tasks, periodic notifications, monthly reports, async CSV exports | Show real cache invalidation and a background task, diagnose worker-down/retry case |
| M9 | Tests, debugging tools, boundary cases, security, setup, dependencies, clean ZIP/report/demo, Git history, compliance | Reinstall from clean copy, reproduce/fix an injected issue, complete submission checklist |
| M10 | Level 1/2 mocks, code narration, live modification, random unseen integrations, architectural Q&A | Independently implement/debug/explain unfamiliar modifications and execute reliable timed demos |

These modules are **interleaved**, not silos. Learn the minimum dependency before implementing a matching slice. Later revisit internals to deeper proficiency.

## Project development sequence (student authored)

1. Local setup and a disposable learning-only Flask/Vue hello-world.
2. Define official role/workflow requirements and draw ER diagram, explain keys and relationships.
3. Database created programmatically, seed single predefined Admin, identity/role model.
4. Registration/login/logout, safe password storage, role authorization, deactivated access.
5. Admin trek management and staff creation/assignment.
6. Trek Staff assigned-trek/participants dashboard and permitted updates.
7. Trekker profile, browse/search/filter, safe booking and personal booking history.
8. Booking invariants: capacity, status, duplicates, authorized access, concurrency edge cases.
9. Redis cache with TTL and invalidation where data is mutated.
10. Redis/Celery: worker, scheduler, daily reminders, monthly report, async CSV export.
11. Validation/testing/debugging, clean launch, originality/report/demo/ZIP/viva readiness.

## Unknown/harder-examiner engine (five tiers)

- **Tier 1 — Recall and trace:** Explain syntax, predict exact output, trace request, identify code ownership.
- **Tier 2 — Typical viva live tasks:** Add filter, route, SQL join, UI button, change CSS, adjust scheduler, show cache use.
- **Tier 3 — Twist:** Add a field across DB/API/UI; rename a state; combine two filters; handle empty/invalid results; change per-role visibility.
- **Tier 4 — Failure and edge cases:** Prevent race/overbooking, duplicate concurrent requests, stale Redis cache, expired auth, broken worker, failed external notifications, client/server inconsistency.
- **Tier 5 — Open-ended unfamiliar scenario:** Examiner describes new workflow not on seniors' sheet; learner designs data flow, decides files to touch, implements tests, defends security/data integrity and alternatives.

Randomize old and newly invented cases. Do not leak answer first. Use deliberate time pressure only after competence is built. Require why/what-if/alternative questions, not just code output.

## Session rhythm (adjust duration to available time)

For a 90-minute session:
- 10 min retrieval quiz on earlier material and target selection.
- 20 min concept + trace and output prediction.
- 25 min student types a tiny task and runs/debugs it.
- 25 min apply the concept to the actual project or a safe precursor.
- 10 min examiner changes the requirement; oral viva check; progress log.

For a 30-minute session: 5 min recall, 8 min concept, 12 min hands-on, 5 min explain/review. Scale session length without changing the learning method.

Each learner attempt follows: *write → send code/error/screenshot → targeted feedback → learner fixes → test → teacher checks and updates mastery*. User does not need to keep restating this protocol.

**Spaced recall:** revisit new material next session, then roughly 3 and 7 days later, rotating previously weak topics. Use targeted practice rather than re-explaining topics already independently mastered.

**Adaptive pacing:** If prerequisite weak, reduce task size and teach it immediately; if mastered, increase unexpected change difficulty. Record bottlenecks; allocate extra drills to integration and live coding.

## Concrete viva rehearsal gates

- **Level 1:** clean run within 10 minutes (per previously reviewed instructions), demo all required roles/workflows, justify requirements and code architecture; test setup repeatedly; zero dependence on an assistant during demo.
- **Level 2:** from blank write a backend endpoint, ORM query, Vue page/API call, bug fix, CSS alteration, and Celery/Redis demonstrations; explain security, state, data consistency, alternatives.
- **Hard/unseen:** complete an unfamiliar cross-layer change with clear assumptions, realistic safety checks and observable tests.
- Confidence is evidence-based: 80%+ independent success on mixed drills *plus* all mandatory project feature gates; use mock failures to select revision topics, not to inflate progress.

## Continuity and GitHub workflow

- `README.md`: navigation.
- `docs/FINAL_ZERO_TO_VIVA_PLAN.md`: this contract and final plan.
- `docs/REQUIREMENTS_MATRIX.md`: mapping official requirement → implementation → verification.
- `docs/SOURCE_INDEX.md`: exact official links and unresolved document/image checks.
- `docs/SESSION_HANDOFF.md`: single canonical source of next lesson, mastered levels, actual student proof, mistakes, blockers.
- `docs/LEARNING_PROTOCOL.md`: detailed learning and privacy safeguards.
- Practice questions and old response summaries must be written in our own words and must exclude student names, email, and other identifying data.
- At meaningful checkpoints during active chats, update original notes in this allowed repo; cannot promise unattended background pushes.
- Before official submission, re-check course portal announcements and milestone/ZIP/viva instructions.

## Immediate launch sequence

**Session 0:** Baseline diagnostic without judgment: Does learner know creating folders, file extensions, terminal, typing a command, seeing output? Begin at the lowest unknown step. Connect a trek booking click to browser → Vue → HTTP → Flask → SQLAlchemy → SQLite → response.

**Session 1:** VS Code + terminal + `hello.py`, `print()`, why interpreter runs the file, variables. Learner independently changes code and reports observed output.

**Session 2:** Conditions/comparisons; pure Python capacity decision and 3 negative test cases.

**Session 3:** Lists/dicts/loops/functions; simulate a tiny trek/booking system in memory.

**Session 4:** Web request/response and forms + tiny Flask request; progressively expand through the modules. Do not skip an unmastered dependency.

**Status as of 2026-10-18:** Plan finalized; **no learner coding mastery has yet been demonstrated**. Next action is **Session 0**.
