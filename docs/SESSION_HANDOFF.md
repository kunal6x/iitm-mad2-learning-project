# Session Handoff — 18 October 2026

## Stable objective
IIT Madras BS Modern Application Development II, selected **Trekking Management Application V2**. Student self-identifies as absolute zero in programming, language syntax, framework and even laptop-tool fundamentals. Primary objective is **independent implementation and deep viva readiness**, not AI-generated turnkey submission.

**Final agreed-style learning plan:** [FINAL_ZERO_TO_VIVA_PLAN.md](FINAL_ZERO_TO_VIVA_PLAN.md). This overrides older roadmap if pedagogical guidance conflicts. Mix fundamentals + student-authored implementation + examiner drills in every session. Senior viva survey is evidence, never a fixed question syllabus; ask harder and different questions as mastery grows.

## Confirmed access
- GitHub account: `kunal6x`.
- **Only authorized repository**: `kunal6x/iitm-mad2-learning-project`.
- All OTHER repositories are off limits; unrelated work belongs to senior engineers.
- Approved repo is currently **public**. Official rules prohibit public project code; use it only for original notes/checklists until private.
- On 2026-10-18 the assistant committed the original final learning plan as a Markdown document. This is not a student project source submission.

## Official documents
- General project/viva instructions — previously reviewed text.
- TMA V2 problem statement — previously reviewed text.
- TMA V2 milestone document — **text retrieval failed**; URL saved in SOURCE_INDEX.
- Official inline images and wireframe — **not visually inspected**.
- Recheck official source/portal for recent changes, and keep all unretrieved requirements clearly marked unverified.

## Known requirements and constraints
Flask API; VueJS UI; Bootstrap; SQLite created in code; Redis cache; Redis + Celery jobs; three roles (Admin/Staff/Trekker); local demonstration; report max 5 pages; ZIP with single root project directory and Python files; validation form; originality and viva live modification. L1 30/40 qualifies for L2, L2 pass threshold noted as 20/60 in previously reviewed instructions; check official latest.
Git tracker registration compulsory.

## Senior survey / viva adversarial preparation
- Excel 2023–2026: 676 response entries with questions or tips; 37 responses explicitly mention Trekking; 35 paraphrased examiner-inspired live tasks assembled in a local ZIP.
- Expected variability: setup/demo, Python/Flask, Vue/JS, ORM/SQL, role security, Redis caching, Celery scheduling, live changes. More challenging unseen requirements must be introduced in tiers.
- Survey has anecdotal reports; not authoritative rules or official question exhaustiveness.
- Local pack exists as a downloadable ZIP from the source chat; **do not upload the raw seniors' responses to the public repo**.

## Deadlines
Course documents previously parsed as: **2026-11-17** for theory passed before September 2026, **2026-12-10** for registered/completing September theory. Actual cohort must be verified on course portal; **never assume later date**. Verify mandatory Milestone 0 tracker timeline from inaccessible official source.

## Current learning status
- New final master plan committed to `docs/FINAL_ZERO_TO_VIVA_PLAN.md`.
- Senior-question analysis complete (not equivalent to learning).
- No beginner diagnostic completed.
- No project source code authored in this learning track yet.
- Python and VS Code skill mastery level still unassessed.
- No student-written demo or viva task passed yet.

## NEXT ACTION (do not ask user to repeat goals)
**Begin Session 0.** Assess absolute baseline in tiny steps by explaining folders/files vs processes and VS Code/terminal, then have student create/save/run `hello.py` and explain each token. Alongside, narrate one browser/Vue → HTTP → Flask → ORM → SQLite → response Trek booking flow. Request only the next observable student action/output and provide targeted feedback; do NOT dump all code. Update this handoff after demonstrated milestones.

## Progress evidence format
Date, module, subtopic, learner's original code/artifact, executed output, mistake fixed, viva answer, independent level 0–4, next smallest task. No invented completion.

## Continuity
For every fresh session, inspect this handoff and the final plan, then continue from the first uncompleted verified checkpoint. GitHub updates only during active interaction; no background auto sync.

## Live lesson update — 18 October 2026 (after Session 0)
- Student reports Python installed and functioning, VS Code file created. The actual command output has not been inspected.
- Student explained `print("5 + 5")` is literal string; correctly distinguished `int` for 10 and `str` for "10".
- Student authored a Python booking capacity conditional with correct broad decision logic; `&&` was used incorrectly and corrected to Python `and`.
- Mini-viva `and/or/not` was initially incorrect, then student explained all three accurately. Keep a brief delayed retrieval check.
- Student accurately predicted `for i in range(2,5): print(i*2)` gives 4, 6, 8; initially unsure of newline behavior, now taught print default newline. The student described while termination accurately although used loose wording that it has no condition; clarified that while explicitly tests a condition.
- Learner says basic variables, conditions and loops are familiar and requests a faster pace. Do not keep administering trivial repeated recall, but **do not mark these mastered at level 3 until independent running code and negative tests are demonstrated**.
- Lesson now underway: lists, dictionaries, lists of dictionaries, functions, `return` vs `print`, using trekking examples. Next: student-written menu-less trek availability/search mini challenge, test cases and a small new variant; then modularize into functions and advance to OOP/Flask as appropriate.
- No graded project source created or pushed.

## Learner evidence — 18 October 2026: list/dictionary/function exercise
- User independently wrote a Python function `findt(trek, seats)` returning available trek names from a list of dictionaries, using loop, comparison, `append`, `return`; tested `findt(treks, 33)` and obtained empty list.
- Relevant error: code used global `treks` rather than the passed parameter `trek`, and reused `trek` as a loop variable, shadowing the parameter. Teach parameter-local scope and a contrasting dataset test.
- Missing edge guard: `seats <= 0` should return `[]`; negative seat request in student code incorrectly matches all treks.
- Dict missing-key viva: clarified `d["missing"]` raises `KeyError` vs `d.get("missing")` returns `None` or chosen default. Do not record as independently passed until student retests.
- Next: brief parameter-scope / mutation exercise and then OOP classes `Trek`, `Booking`, `User`; keep user code student-authored. Faster pacing justified by demonstrated competence but verify scopes and error handling before transition to Flask.
