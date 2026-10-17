# Zero-to-Independent-Developer Master Roadmap

**No fixed number of days.** Progress only after demonstrating mastery, while respecting official submission deadlines. Each phase blends concept education with student-authored practice. Provide Hindi/Hinglish explanations whenever useful, plus accurate English technical vocabulary.

## Milestone A — Laptop, files, tools, and confidence
- Operating system fundamentals: folders, extensions, paths, unzip/zip, processes, terminal/PowerShell, current directory.
- VS Code: create/open files, save, integrated terminal, extensions, debugger basics.
- CLI basics: `pwd`, `cd`, `ls/dir`, `mkdir`, create/read files, safe deletion, environment variables, exit codes.
- Install and verify Python, pip, venv, Git, browser developer tools; add other tools only when needed.
- Git vs GitHub: repository, local commit, branch, push/pull, diffs, restore. Never access any repository besides the approved one.
- Checkpoint: student independently opens a folder, creates code, runs a command, interprets output, and explains a Git commit.

## Milestone B — Python foundations
- Programming mental model; source code/interpreter, indentation, comments.
- Variables, strings, numbers, booleans, operators, I/O, type conversion.
- Lists, tuples, dictionaries, sets; indexing, iteration, mutation.
- if/elif/else, for/while, functions, parameters, return, scope.
- Modules, packages, exceptions, file I/O, virtual environments.
- Classes/objects, attributes, methods, constructors; necessary OOP patterns.
- Drills: find maximum, counts/frequencies, filtering, duplicate prevention, date checks, capacity-limits simulation, mini role checks.
- Checkpoint: student writes small algorithms from scratch and debugs without full solutions.

## Milestone C — Web foundations and frontend
- Browser/server/request/response, URL, HTTP GET/POST/PATCH/DELETE, headers, cookies, JSON, REST, status codes, API payload.
- HTML document, tags/forms/input, CSS selectors/box model, responsive grids and Bootstrap.
- JavaScript from zero: `let/const`, types, functions, arrays/objects, DOM, `fetch`, promises, async/await, errors.
- VueJS: app root, reactivity, interpolation, directives (`v-if`, `v-for`, `v-model`), events, computed state, components, props, lifecycle.
- Checkpoint: student independently creates an interactive trek list and explains browser-to-API data flow.

## Milestone D — Backend and data
- Flask app, routes, request/response, JSON API, input validation, errors.
- SQLite: tables, primary/foreign keys, UNIQUE/CHECK, SQL SELECT/INSERT/UPDATE/DELETE, joins, transactions.
- ER diagram and cardinalities; status/lifecycle transitions; consistent business rules.
- Authentication, password hashing, Flask sessions, role-based access, access-control negative tests.
- Checkpoint: student creates a small persistent API, demonstrates authorized/unauthorized requests, and explains SQL.

## Milestone E — Build official TMA features in student-owned incremental slices
- Structure and running setup; identity/admin creation.
- Admin dashboard and trek CRUD; staff registration/assignment; management/search.
- Staff assigned-trek dashboard and guarded updates.
- Trekker registration, profile, filtering and safe booking.
- Booking history and statuses; slot integrity; no duplicate booking.
- Integrated Vue↔Flask↔SQLite data flow.
- For each slice: sketch expected inputs/outputs, student implementation, testing, code narration, independent variation.

## Milestone F — Advanced MAD2 concepts
- Redis: cached values, TTL, hits/misses, freshness, invalidation on writes.
- Celery + Redis queue/broker: task states, workers, scheduled jobs, retries and local troubleshooting.
- Daily notifications; monthly HTML report; async CSV export completion.
- Performance, secure boundaries, responsive UI, failure testing and cleanup.
- Checkpoint: student traces a live request and asynchronous task end-to-end, tests stale cache and worker-down scenarios.

## Milestone G — Viva and project finalization
- L1 simulation: 10-minute local startup; feature demo; basic Python/Flask/JS/Vue/SQL questions; walk through owned code.
- L2 simulation: why architecture, schema queries, debugging, code modifications, authorization, async jobs, caching, explain alternatives.
- Rotating challenge bank: edit field, add filtering, enforce unique business rule, fix broken route, change role restriction, write SQL join, add computed Vue field, invalidate cache.
- Final project ZIP (one root folder), report <=5 pages, demo video, official validation form, Git tracker, originality + AI assistance declaration.
- Rehearse until student can independently complete unfamiliar, syllabus-scoped feature changes.

## Our learning protocol
Each micro-topic: (1) analogy/what/why (2) microscopic code walkthrough (3) predict output (4) student types (5) run/test (6) error investigation (7) student explains (8) variation (9) viva check. Do not claim understanding based on reading alone. Keep progress record and next-step handoff after meaningful sessions.

## Recommended architecture (provisional)
`VueJS + Bootstrap (browser UI)` -> `Flask JSON API` -> `SQLite data store`; `Redis` handles caching and Celery broker; a `Celery worker + scheduler` runs reminders/report/export; outbound email/webhook only for notifications. Prefer simplest compliant technology choices; never add unnecessary complexity that student cannot explain.

## First practical lesson, once official doc review is completed
How a computer executes a Python file; how files, folders and terminal relate. Student creates a tiny `hello.py` in a safe local learning folder, runs it, predicts/changes output and explains every token. Practice first; application features later.
