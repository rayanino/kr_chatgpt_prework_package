# KR Execution Handoff System

## 1. Purpose

This document defines how the future KR production project should translate hardened strategic reasoning into bounded execution work for implementation agents such as Codex, Claude Code, or other specialized workers.

Its purpose is to ensure that:
- execution receives clear, strategically aligned work
- implementation agents do not silently invent missing project logic
- strategic conclusions are not degraded during handoff
- review and acceptance are structured rather than improvised
- autonomous execution remains powerful but disciplined

This system is the bridge between:
- doctrine
- architecture
- repo artifacts
- execution tasks
- returned implementation work

Without this bridge, even strong strategic reasoning will fail to compound.

---

## 2. Core principle

Execution agents should not be asked to think strategically on behalf of KR unless the task explicitly requires and safely permits it.

The production project should do the strategic work first.

Only after the strategic shape is sufficiently clear should work be handed off for execution.

Therefore, the default rule is:

- strategy first
- bounded execution second
- review third
- adoption fourth

The handoff system exists to preserve that order.

---

## 3. Execution philosophy

The future KR production project should treat execution agents as powerful but bounded workers.

That means:

- they are excellent at implementing sharply specified tasks
- they can help refine local implementation details
- they can propose improvements within task scope
- they should not silently redefine doctrine, architecture, or project boundaries
- they must not become accidental strategic authorities just because the task was vague

The project must therefore optimize for:
- high-clarity handoff
- explicit scope
- explicit constraints
- explicit acceptance logic
- explicit review expectations

The better the handoff, the safer the execution.

---

## 4. What counts as execution work

Execution work is any work whose main value lies in producing a concrete change or bounded artifact rather than in open-ended strategic reasoning.

Examples include:
- repo file creation
- repo file editing
- script implementation
- refactors
- tests
- analyzers
- templates
- schema files
- registries
- control-plane updates when explicitly specified
- document creation from already-hardened doctrine
- wiring and plumbing tasks
- implementation of evaluation infrastructure
- data transformation utilities
- bounded research collection tasks when clearly specified

Execution work is not:
- determining KR’s end-state
- deciding broad architecture from scratch
- defining trustworthiness doctrine from first principles
- deciding whether a major feature belongs in KR without prior hardening
- redefining scope boundaries casually

Those are strategic tasks, not execution tasks.

---

## 5. Handoff eligibility rule

A task is eligible for execution handoff only when it is sufficiently hardened.

That means the production project should not hand off tasks merely because:
- something sounds useful
- the user wants momentum
- the model has an intuition
- the implementation agent is capable of “figuring it out”

A task is eligible only when:
- the problem is clearly defined
- the desired outcome is clear
- the scope is bounded
- the main assumptions are explicit
- the strategic reason for the task is understood
- the task is aligned with current project doctrine
- the expected output form is known
- the acceptance test is known or at least shapeable
- the remaining ambiguity is low-regret or explicitly delegated

If those conditions are missing, the task must be hardened further before handoff.

---

## 6. Classes of execution tasks

The future KR production project should classify execution tasks into classes.

### 6.1 Class X1 — direct implementation task
A concrete code or file change with tightly defined scope.

Examples:
- create a registry file
- implement one analyzer script
- add missing field propagation
- create a doctrine document from finalized content
- write a template file

These are the safest handoff class.

### 6.2 Class X2 — bounded design-implementation task
A task with a small amount of permitted local design freedom inside a fixed strategic boundary.

Examples:
- choose the cleanest local structure for a YAML schema
- implement a task packet template and make small format refinements
- create a file tree with local organization choices inside a prescribed artifact family

These tasks require explicit delegation of local discretion.

### 6.3 Class X3 — exploratory implementation task
A task where some uncertainty remains and the execution agent is asked to investigate or prototype within a tightly controlled frame.

Examples:
- compare two possible parser approaches within a defined boundary
- prototype a structured representation and report tradeoffs
- explore how best to encode a specific recurring artifact

These tasks must be framed very carefully and usually require explicit return-format expectations.

### 6.4 Class X4 — review-only task
A task whose purpose is to inspect, critique, or validate existing work rather than create major new work.

Examples:
- review a PR against acceptance criteria
- inspect a generated doctrine file for structural drift
- validate whether an implementation matches the task packet

These tasks are often high leverage and lower risk than implementation.

---

## 7. Non-handoff rule

A task should not be handed off when:
- the actual problem is still vague
- the project does not yet know what good looks like
- the work would force the execution agent to invent doctrine
- the work depends on unresolved strategic questions
- the acceptance criteria cannot even be sketched
- the task spans too many unrelated concerns
- the task’s scope is too large to review properly
- the project is really asking for thought, not execution

In such cases, the correct move is not “send it anyway.”
The correct move is:
- harden first
- split the task
- create doctrine
- or isolate the unresolved question

---

## 8. Execution-readiness gate

Before any task is handed off, the production project should ask:

### 8.1 Problem clarity
Is the problem stated cleanly?

### 8.2 Strategic rationale
Is it clear why this task matters for KR?

### 8.3 Scope boundary
Is it clear what is in scope and what is out of scope?

### 8.4 Input state
Is the relevant current repo or project context known?

### 8.5 Expected output
Is it clear what the worker should produce?

### 8.6 Acceptance logic
Is it clear how the result will be judged?

### 8.7 Constraint visibility
Are important constraints stated explicitly?

### 8.8 Ambiguity control
If local ambiguity remains, is it acceptable and delegated intentionally?

### 8.9 Review plan
Is it clear how the result will be reviewed after return?

If these questions cannot mostly be answered, the task is not execution-ready.

---

## 9. The task packet concept

Every serious execution handoff should use a structured task packet.

A task packet is the execution artifact that carries hardened strategic intent into bounded implementation work.

Its job is to ensure that the worker receives:
- the right task
- in the right frame
- with the right boundaries
- under the right standards

The task packet is the central unit of the execution handoff system.

---

## 10. Required task packet fields

Every serious execution task should include the following fields in substance.

### 10.1 Task title
A short, precise title.

### 10.2 Task class
X1, X2, X3, or X4.

### 10.3 Objective
What must be accomplished.

### 10.4 Why this matters
Why this task exists in KR’s larger system.

### 10.5 Current context
What relevant state the worker must understand before acting.

### 10.6 In scope
What the worker is allowed and expected to do.

### 10.7 Out of scope
What the worker must not do.

### 10.8 Constraints
Relevant architectural, doctrinal, repo, or implementation constraints.

### 10.9 Inputs and dependencies
Files, docs, prior artifacts, or assumptions the task depends on.

### 10.10 Expected outputs
What concrete artifacts, edits, files, or reports should be returned.

### 10.11 Acceptance criteria
How the work will be judged.

### 10.12 Allowed discretion
What kinds of local choices the worker may make autonomously.

### 10.13 Disallowed discretion
What the worker must not redefine or assume.

### 10.14 Risk notes
Known ways the task could go wrong.

### 10.15 Return format
How the worker should present the result.

This set of fields should be treated as the default minimum for serious handoff.

---

## 11. Acceptance criteria doctrine

Acceptance criteria are not optional decoration.

They are the gate that protects KR from fuzzy execution.

Good acceptance criteria are:
- concrete
- aligned with the real reason the task exists
- reviewable
- bounded
- explicit about failure

Bad acceptance criteria are:
- vague
- aesthetic
- untestable
- merely “looks good”
- disconnected from strategy

Acceptance criteria should usually answer:
- what must be true for this task to count as done
- what must not be broken
- what signals would indicate failure
- what review evidence is expected

The better the acceptance criteria, the less execution agents need to guess.

---

## 12. Allowed discretion doctrine

Not every execution task should be rigid to the same degree.

The handoff system must explicitly define how much local discretion the execution agent has.

### 12.1 Zero-discretion tasks
The worker should follow the packet closely and not redesign anything important.

Examples:
- create this file with this structure
- implement this exact missing field
- update these documented paths
- apply this agreed schema

### 12.2 Local-optimization tasks
The worker may make local implementation choices if they do not violate strategic constraints.

Examples:
- choose the cleanest function decomposition
- choose a reasonable internal helper layout
- choose concise wording inside a fixed template

### 12.3 Comparative-option tasks
The worker may compare options, but must return them within a fixed framing rather than silently choose a strategic direction.

Examples:
- compare two encoding options and recommend one
- prototype two structures and report tradeoffs

The task packet must make the discretion level explicit.
Otherwise the worker will invent it.

---

## 13. Disallowed discretion doctrine

Execution agents must not silently decide on their own:
- broad project direction
- major doctrine changes
- architecture pivots
- acceptance criteria changes
- scope expansion
- hidden extra tasks
- irreversible external actions unless explicitly authorized
- domain-truth claims that were not already grounded

If an execution task implicitly requires one of these, the task was badly framed and must be returned for further hardening.

---

## 14. Task splitting doctrine

A task should be split before handoff when:
- it spans multiple aspects
- it combines strategy and implementation too tightly
- it has multiple independent outputs
- it would be difficult to review as a single unit
- failure in one part would obscure the quality of another
- the worker would need to hold too many decisions in parallel

The production project should prefer:
- smaller, well-bounded packets
over
- giant handoffs that “sort of cover the area”

Small packets are easier to review, safer to delegate, and less likely to smuggle strategic drift.

---

## 15. Return-format doctrine

Every execution task should specify the expected return format.

Examples:
- patch summary plus changed files
- file drafts only
- comparison memo
- implementation plus test results
- review memo with pass/fail judgment
- proposed repo tree plus rationale
- unresolved blockers list

The return format matters because it determines how the production project will review the work.

A worker should not be left to decide whether to return:
- code
- prose
- options
- summary
- or an action plan

That should be specified.

---

## 16. Review-after-return doctrine

Execution handoff is incomplete without returned-work review.

Every returned task should be reviewed against:

### 16.1 Objective match
Did the worker solve the right problem?

### 16.2 Scope discipline
Did the worker stay within the allowed boundary?

### 16.3 Constraint compliance
Did the worker respect the stated constraints?

### 16.4 Acceptance criteria
Does the work meet the defined acceptance standard?

### 16.5 Hidden drift check
Did the worker smuggle in unapproved direction changes?

### 16.6 Artifact quality
Are the returned files or edits actually durable, clean, and usable?

### 16.7 Residual ambiguity
Did the worker leave behind unresolved ambiguity that should have been surfaced?

Review is not optional.
It is the mechanism that keeps execution subordinate to strategy.

---

## 17. Review outcome classes

After review, a returned task should receive one of the following outcomes:

### R1 — accepted
The task meets the objective and acceptance criteria.

### R2 — accepted with minor follow-up
The task is fundamentally good, but a small correction or extension is needed.

### R3 — revision required
The task is directionally relevant but not yet acceptable.

### R4 — rejected as misframed
The task failed mainly because the original handoff was flawed, ambiguous, or under-hardened.

### R5 — rejected as execution failure
The handoff was sound, but the execution work did not satisfy it.

This classification matters because not every failure is the worker’s fault.
Sometimes the problem is the packet.

---

## 18. Strategic contamination rule

If a returned execution artifact contains implicit strategic decisions that were not authorized, the production project must detect and handle that explicitly.

Possible responses:
- accept the local implementation but reject the strategic drift
- send the strategic issue back into hardening
- split the execution artifact into accepted and non-accepted parts
- mark the issue for a dedicated decision-resolution chat

The production project must never quietly absorb accidental strategic drift from implementation work.

---

## 19. Execution-agent suitability rule

Not every task is suitable for every worker.

The production project should explicitly consider:

### Best suited for bounded implementation agents
- clear code changes
- file creation from finalized content
- schema creation
- structured refactors
- analyzers
- registries
- templates
- tests
- low-ambiguity docs

### Best suited for strategic reasoning first
- doctrine creation from scratch
- broad architecture decisions
- major workflow redesign
- long-horizon expansion choice
- trustworthiness boundary design
- user-value modeling

### Best suited for review-oriented workers
- PR review
- criteria checking
- mismatch detection
- protocol compliance inspection

The handoff system should route work by fit, not by convenience.

---

## 20. Execution packet template

The following structure should be the default execution packet template.

### Execution task packet template

Task title:
[Short precise title]

Task class:
[X1 / X2 / X3 / X4]

Objective:
[What this task must accomplish]

Why this matters:
[Why this task matters in KR’s larger system]

Current context:
[Relevant state, files, doctrines, constraints]

In scope:
- [Allowed task item]
- [Allowed task item]

Out of scope:
- [Forbidden expansion]
- [Forbidden expansion]

Constraints:
- [Architectural or doctrinal constraint]
- [Repo or implementation constraint]

Inputs and dependencies:
- [Relevant file / doc / prior decision]
- [Relevant assumption or artifact]

Expected outputs:
- [What should be returned]

Acceptance criteria:
- [Criterion]
- [Criterion]
- [Criterion]

Allowed discretion:
[What local choices the worker may make]

Disallowed discretion:
[What the worker must not redefine]

Risk notes:
[Known failure modes or traps]

Return format:
[Patch summary / file drafts / comparison memo / tests / review memo / etc.]

Review note:
[How the returned work will be judged]

21. Task-packet quality criteria

Before sending a task packet, the production project should evaluate whether the packet itself is good.

A good packet is:

narrow
intelligible
strategically grounded
reviewable
explicit about boundaries
explicit about discretion
hard to misunderstand
easy to reject if violated

A bad packet is:

broad
fuzzy
burden-shifting
missing acceptance logic
missing risk notes
implicitly strategic
impossible to review cleanly

A worker can only be as good as the packet permits.

22. Escalation-during-execution rule

If an execution worker encounters a question that exceeds the allowed discretion in the packet, that question should be escalated rather than silently answered through implementation.

The production project should expect these escalation categories:

strategic ambiguity
doctrinal ambiguity
architecture ambiguity
scope ambiguity
missing dependency
acceptance ambiguity
evidence dependency

This rule is important because “solve as you go” is useful only within the right boundary.
Beyond that boundary, it becomes project drift.

23. Execution backlog discipline

The future KR production project should avoid turning its whole strategic agenda into a giant execution backlog too early.

Only tasks that are actually ready should enter the execution queue.

That means the execution queue should contain:

bounded work
reviewable work
work aligned with the current active frontier or clearly justified strategic preparation

It should not become a graveyard of half-hardened ideas.

The production project should prefer a smaller, cleaner queue over a large speculative one.

24. Anti-failure rules

The future KR production project must avoid the following execution-handoff failures.

24.1 Vague-packet failure

The worker receives a task that sounds good but is too vague to implement safely.

24.2 Strategy-dumping failure

The project hands broad unresolved strategy to an execution worker and calls it a task.

24.3 Hidden-scope failure

Important boundaries are left implicit.

24.4 Acceptance-vacuum failure

No one knows what counts as success.

24.5 Over-delegation failure

The worker is given more strategic discretion than intended.

24.6 Under-delegation failure

The task is so rigid that reasonable local optimization becomes impossible.

24.7 Review-neglect failure

Returned work is accepted without serious review.

24.8 Misblame failure

A bad result is blamed on the worker when the packet itself was under-hardened.

24.9 Giant-task failure

Too much is bundled into one execution packet.

These failures must be actively resisted.

25. Success condition

The execution handoff system is successful only if the future KR production project behaves like this:

it hands off only work that is ready
it uses structured task packets
it defines scope and constraints clearly
it states acceptance criteria explicitly
it defines discretion boundaries deliberately
it reviews returned work rigorously
it prevents execution agents from becoming accidental strategic authorities
it converts hardened thought into reliable action without strategic slippage

That is the intended standard.

