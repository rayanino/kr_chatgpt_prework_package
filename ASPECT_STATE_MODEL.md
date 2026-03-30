# KR Aspect State Model

## 1. Purpose

This document defines how the future KR production project should track the state of each KR aspect over time.

Its purpose is to ensure that aspect hardening is not treated as a vague feeling of progress but as a structured process with recognizable states, transitions, blockers, and completion conditions.

The aspect state model exists to answer questions such as:
- has this aspect actually been entered yet?
- are we still mapping it or already critiquing a direction?
- is the current direction only provisional or genuinely hardened?
- is the aspect blocked by missing evidence, missing user approval, or unresolved dependencies?
- should the project continue hardening this aspect now, defer it, or convert it into execution?

This model is designed to support disciplined long-horizon coverage.

---

## 2. Core principle

An aspect is not either “done” or “not done.”

Important aspects in KR mature gradually through distinct stages:
- scoping
- mapping
- comparison
- direction-setting
- critique
- hardening
- conversion
- temporary closure
- re-entry when needed

The state model exists because hardening is a process, not a binary event.

If the project does not track that process explicitly, it will repeatedly confuse:
- first contact with real understanding
- provisional direction with hardened doctrine
- local closure with final completion
- blockage with laziness
- deferral with rejection

The state model is therefore a discipline tool.

---

## 3. Design goals

The aspect state model should satisfy all of the following:

1. **Interpretability**
   A future worker should be able to understand what state an aspect is in without rereading all earlier chats.

2. **Action guidance**
   The state should imply what kind of next move is appropriate.

3. **Non-false-finality**
   The model should avoid pretending an aspect is “done” when it is only lightly explored.

4. **Blocker visibility**
   The model should distinguish different types of blockage clearly.

5. **Re-entry support**
   The model should support returning to an aspect later without confusion.

6. **Coverage discipline**
   The model should make it harder for the project to lose track of under-hardened areas.

---

## 4. The state model

The future KR production project should use the following aspect states.

### S0 — unentered
The aspect exists in the master map but has not yet received serious dedicated hardening.

Meaning:
- no real aspect-specific chat has materially engaged it
- there may be passing mentions elsewhere, but no durable aspect work yet exists

Implication:
- the aspect still needs first entry
- no claims of understanding should be overstated

---

### S1 — scoped
The aspect has been deliberately entered and its boundaries have been defined.

Meaning:
- the project knows what belongs inside the aspect
- the project knows what is outside the aspect
- the objective of hardening this aspect has been framed

Implication:
- the next move is usually mapping, problem-definition, or question identification

---

### S2 — mapped
The aspect’s terrain has been laid out, but no final direction is yet firm.

Meaning:
- the core questions are visible
- major tensions or subquestions are identified
- key dependencies and likely bottlenecks are visible
- the shape of the aspect is understood better than at scoping stage

Implication:
- the next move is usually comparison, option analysis, or first direction-setting

---

### S3 — options compared
The aspect has progressed beyond mapping into structured comparison of plausible directions.

Meaning:
- multiple live paths have been examined
- tradeoffs are visible
- one or more candidate directions are emerging
- the project is no longer just describing the aspect but actively evaluating paths through it

Implication:
- the next move is to choose or draft a provisional direction, or identify the evidence needed to distinguish remaining contenders

---

### S4 — provisionally directed
The aspect has a current recommended direction, but it is not yet hardened enough to be treated as stable doctrine.

Meaning:
- the project has a leading position
- the rationale is visible
- alternatives have been considered at least somewhat
- meaningful uncertainty still remains
- critique may still significantly reshape the direction

Implication:
- the next move is critique, stress-testing, evidence gathering, or tightening the recommendation

---

### S5 — under critique
The current direction is being actively challenged, tested, or pressure-tested.

Meaning:
- hidden assumptions are being surfaced
- failure modes are being examined
- evidence needs are being identified or integrated
- the project is deliberately trying to break or strengthen the current direction

Implication:
- the next move is either refinement toward hardening, evidence escalation, or partial rollback if critique breaks the direction

---

### S6 — provisionally hardened
The aspect has a strong current position that is good enough to guide near-term reasoning, but it still carries identified limitations or unresolved questions.

Meaning:
- the direction survived meaningful critique
- important assumptions are explicit
- the position is operational enough to guide related work
- some residual uncertainty or incompleteness still remains

Implication:
- the aspect may now support dependent work, but should not yet be treated as maximally mature doctrine if the remaining gaps matter

---

### S7 — hardened
The aspect has reached a strong, explicit, durable, operationally usable state for the project’s current stage.

Meaning:
- the problem is clearly defined
- the direction is clear
- major assumptions are surfaced
- serious alternatives were considered
- critique was survived
- evidence was used where needed
- durable outputs exist
- the project can rely on this aspect for further work

Implication:
- the aspect is currently fit to guide downstream decisions, artifact creation, and execution handoff where relevant

Important note:
“Hardened” does not mean eternally final.
It means sufficiently mature and trustworthy for the current stage of KR.

---

### S8 — blocked by evidence
The aspect cannot responsibly advance further until a specific research or evidence question is resolved.

Meaning:
- internal reasoning reached a real limit
- the missing issue is evidence-owned rather than preference-owned
- proceeding further would risk contamination or low-quality commitment

Implication:
- the next move is a targeted research task or evidence-gathering step
- the project should not fake closure

---

### S9 — blocked by user decision
The aspect cannot responsibly advance further until the user provides something that only the user can provide.

Meaning:
- the blocker is a real approval, preference, permission, or tool-access issue
- the model has already done the reasoning needed up to that boundary

Implication:
- the next move is a structured escalation to the user
- the project should not ask vague open-ended questions

---

### S10 — blocked by dependency
The aspect depends on another aspect, artifact, decision, or execution result that has not yet matured enough.

Meaning:
- the problem is not missing evidence or user preference
- it is missing internal project preconditions

Implication:
- the next move is to resolve the dependency or reorder sequencing

---

### S11 — deferred
The aspect is valuable but intentionally not active right now.

Meaning:
- the aspect is not rejected
- the project explicitly recognizes it as lower priority for the current stage
- deferral is strategic, not accidental neglect

Implication:
- the aspect remains on the map and may re-enter later
- future workers should not confuse deferral with completion

---

### S12 — rejected
A path, framing, or candidate aspect direction has been explicitly considered and not adopted.

Meaning:
- the project concluded that this direction should not be pursued, at least under current assumptions
- the rejection is durable enough to remember

Implication:
- future workers should not casually reintroduce the rejected path without new reasons

Important note:
Usually an entire aspect is not rejected; more often a candidate direction within an aspect is rejected.
But the state exists for the cases where the aspect itself proves illegitimate, redundant, or wrongly defined.

---

### S13 — superseded
The aspect’s earlier hardening result has been overtaken by a later, better, or narrower/wider framing.

Meaning:
- earlier doctrine or direction existed
- the project later replaced or substantially revised it
- the earlier state is no longer authoritative

Implication:
- future workers must follow the newer state and associated artifacts

---

## 5. State meanings at a glance

### Early understanding states
- S0 unentered
- S1 scoped
- S2 mapped

### Direction-building states
- S3 options compared
- S4 provisionally directed
- S5 under critique

### Operational maturity states
- S6 provisionally hardened
- S7 hardened

### Blocked or paused states
- S8 blocked by evidence
- S9 blocked by user decision
- S10 blocked by dependency
- S11 deferred

### Closure and replacement states
- S12 rejected
- S13 superseded

This grouping is useful for high-level navigation.

---

## 6. State transition philosophy

Aspects should not jump arbitrarily between states.

The normal flow is something like:

S0 → S1 → S2 → S3 → S4 → S5 → S6 → S7

But real project work is not always linear.

Valid deviations include:
- S4 → S8 if evidence is needed
- S5 → S3 if critique reopens the option space
- S6 → S10 if a hidden dependency emerges
- S7 → S13 if later work supersedes the current hardening
- S2 → S11 if the aspect is strategically deferred

The state model is not meant to force fake linearity.
It is meant to make actual position legible.

---

## 7. Normal state transitions

The following transitions are especially common and should be treated as normal.

### T1
S0 unentered → S1 scoped
When the project first opens a dedicated aspect chat and clearly defines scope.

### T2
S1 scoped → S2 mapped
When the core terrain, questions, and tensions become visible.

### T3
S2 mapped → S3 options compared
When the project starts actively weighing plausible directions.

### T4
S3 options compared → S4 provisionally directed
When a leading direction emerges.

### T5
S4 provisionally directed → S5 under critique
When the project actively attacks and stress-tests the direction.

### T6
S5 under critique → S6 provisionally hardened
When the direction survives critique well enough to guide work, but still has meaningful open edges.

### T7
S6 provisionally hardened → S7 hardened
When the aspect becomes sufficiently durable, explicit, operational, and trustworthy for the current stage.

These are the core development transitions.

---

## 8. Blocked-state transitions

Blocked states should be used deliberately and specifically.

### T8
Any active state → S8 blocked by evidence
When research or verification is now necessary.

### T9
Any active state → S9 blocked by user decision
When the next step depends on real user approval, preference, or access.

### T10
Any active state → S10 blocked by dependency
When another aspect, artifact, or task must mature first.

Blocked states are not failure.
They are explicit project truth.

---

## 9. Re-entry transitions

Blocked or paused aspects may later re-enter active hardening.

Examples:
- S8 → S5 after research resolves the key evidence question
- S9 → S4 after user approval is given
- S10 → S4 or S5 after the dependency is resolved
- S11 → S1 or S2 when the project intentionally reactivates the deferred aspect

The model should explicitly mark re-entry rather than act as though the aspect never paused.

---

## 10. Hardened-state doctrine

“Hardened” should be treated seriously.

An aspect should not enter S7 hardened unless all of the following are substantially true:

### 10.1 Problem clarity
The aspect’s core problem is clearly defined.

### 10.2 Scope clarity
The aspect boundary is stable enough for practical use.

### 10.3 Direction clarity
A clear direction exists.

### 10.4 Critique survival
The direction has survived meaningful critique.

### 10.5 Assumption visibility
Important assumptions are explicit.

### 10.6 Evidence discipline
Evidence needs were handled properly where relevant.

### 10.7 Durable outputs
At least one durable artifact exists that captures the result.

### 10.8 Operational usefulness
The aspect can now guide downstream work.

If these conditions are missing, the aspect is not yet hardened.

---

## 11. Provisionally hardened doctrine

S6 provisionally hardened is important because many aspects will become good enough to guide some work before they are maximally mature.

Use S6 when:
- the aspect is already strong
- the project can rely on it cautiously
- remaining weaknesses are visible
- further hardening would help, but the aspect is not fundamentally underdefined anymore

This state is valuable because it avoids a false binary between:
- “still messy”
and
- “fully hardened”

Many productive aspects will live in S6 for meaningful periods.

---

## 12. Deferred-state doctrine

S11 deferred must be used carefully.

Deferred does not mean:
- forgotten
- irrelevant
- solved
- rejected

It means:
- valuable, but not active now

A deferred aspect should ideally include:
- why it is deferred
- what would make it active later
- whether the deferral is due to stage timing, priority tradeoff, or dependency sequence

This protects against quiet neglect.

---

## 13. Superseded-state doctrine

S13 superseded exists because KR is a long-horizon project.
Some aspect conclusions will evolve.

When an aspect state is superseded:
- the newer direction should be clearly identifiable
- the earlier hardened position should remain intelligible historically
- future workers should not have to guess which position is current

Supersession should also trigger:
- decision-log updates if relevant
- artifact updates if relevant
- active doctrine correction if relevant

A superseded aspect is not necessarily a failure.
It may reflect legitimate maturation.

---

## 14. State assignment rules

The future KR production project should assign aspect states conservatively.

### Rule 1
Do not upgrade a state merely because a chat felt productive.

### Rule 2
Prefer the lower state when uncertainty exists between two adjacent states.

### Rule 3
A state should reflect the real maturity of the aspect, not the enthusiasm of the current session.

### Rule 4
Blocked states should be specific; do not use them vaguely.

### Rule 5
Do not call something hardened if it has not survived critique.

These rules matter because the value of the state model depends on honesty.

---

## 15. State update triggers

An aspect state should typically be updated when one of the following happens:

- a new dedicated aspect chat materially advances the aspect
- a durable artifact is produced that changes the maturity of the aspect
- critique materially weakens or strengthens the current direction
- a blocker is identified
- a blocker is resolved
- the aspect is intentionally deferred
- the aspect is superseded by a later position

Routine minor mentions elsewhere usually do not justify a state update.

---

## 16. Aspect-state record format

Each aspect should be representable in a structured compact form such as:

### Aspect state record template

Aspect ID:
[Aspect identifier]

Aspect name:
[Aspect name]

Current state:
[S0–S13]

Why this is the current state:
[Short explanation]

Last meaningful change:
[Session or marker]

Current leading direction, if any:
[Short statement]

Main blocker, if any:
[Evidence / user decision / dependency / none]

Main unresolved question, if any:
[Short statement]

Current durable artifacts:
- [Artifact]
- [Artifact]

Best next move:
[Exact next step]

This may later be used inside a registry or tracking artifact.

---

## 17. What the next move should look like by state

The state should imply what kind of next move is appropriate.

### If S0 unentered
Next move:
Open a scoped aspect chat.

### If S1 scoped
Next move:
Map the terrain, identify core questions and boundaries.

### If S2 mapped
Next move:
Compare live options or candidate directions.

### If S3 options compared
Next move:
Draft a provisional direction or identify decisive evidence needs.

### If S4 provisionally directed
Next move:
Critique, stress-test, and refine.

### If S5 under critique
Next move:
Integrate critique, research if needed, or revise direction.

### If S6 provisionally hardened
Next move:
Either rely on it cautiously, or do a final hardening pass if the residual gaps matter.

### If S7 hardened
Next move:
Use it to guide downstream work, revisit only when needed.

### If S8 blocked by evidence
Next move:
Run a targeted research or evidence-gathering task.

### If S9 blocked by user decision
Next move:
Escalate a precise decision request to the user.

### If S10 blocked by dependency
Next move:
Resolve the dependency or reorder aspect sequencing.

### If S11 deferred
Next move:
Leave dormant until the trigger for reactivation appears.

### If S12 rejected
Next move:
Do not revive unless new reasons justify reopening.

### If S13 superseded
Next move:
Follow the newer position and update any lagging artifacts.

This is one of the main practical values of the state model.

---

## 18. Relationship to the aspect map

The aspect map defines what aspects exist.

The aspect state model defines where each aspect currently stands.

These are different functions and must not be collapsed into one document unless there is a deliberate registry structure that clearly separates:
- aspect identity
- aspect description
- aspect priority
- aspect state

The map is the topology.
The state model is the progression logic.

---

## 19. Relationship to the decision log

Not every state change deserves a decision record.

A state change should become a decision record only when:
- it reflects a real commitment
- it materially changes project direction
- it gates execution
- it supersedes an earlier active position
- it changes doctrine or boundaries

For example:
- S2 mapped → S3 options compared usually does not need a decision record
- S6 provisionally hardened → S7 hardened for a major aspect might

The state model tracks maturity.
The decision log tracks commitments.

---

## 20. Relationship to execution

Execution work should generally not depend on aspects still in early states unless the task is explicitly exploratory.

Typical execution-readiness implications:

- S0–S2: usually too early for execution
- S3–S4: only limited exploratory execution may be safe
- S5: execution usually premature unless it is critique-supporting or evidence-gathering
- S6: some bounded execution may be appropriate
- S7: full aligned execution handoff is usually appropriate where relevant

This is not an absolute law, but it is a strong default.

---

## 21. Relationship to pre-work and production launch

The pre-work project itself may use this state model conceptually while designing the operating system.

But its primary role is inside the future KR production project.

Once production begins, the state model should help answer:
- what aspect should be entered next
- what aspect should be continued
- which aspect is stuck and why
- which aspect is mature enough to support task packets
- which areas of KR are still under-hardened

This makes the production project much more systematic.

---

## 22. Anti-failure rules

The future KR production project must avoid the following state-model failures.

### 22.1 Fake-progress failure
The project upgrades aspect states too quickly just because discussion happened.

### 22.2 False-finality failure
The project marks aspects hardened when they are still shaky.

### 22.3 Permanent-early-state failure
The project never updates aspect states, making the model useless.

### 22.4 Vague-blocker failure
The project says an aspect is blocked but does not specify how.

### 22.5 Deferred-equals-forgotten failure
Deferred aspects vanish from strategic awareness.

### 22.6 State-spam failure
Every tiny movement triggers noisy state changes that reduce clarity.

### 22.7 Supersession-confusion failure
Older and newer states coexist without clear authority.

These failures must be resisted actively.

---

## 23. Maintenance rule

Aspect states should be updated deliberately, not constantly.

Good times to update state include:
- after a major aspect chat
- after a critique pass changes the maturity level
- after evidence resolves a blocker
- after a doctrine artifact is accepted
- after a significant dependency is cleared
- after a superseding direction is adopted

This keeps the state model useful without making it noisy.

---

## 24. Success condition

The aspect state model is successful only if the future KR production project can use it to do all of the following:

- understand the maturity of each aspect
- distinguish exploration from hardening
- identify the right next move
- make blockers explicit
- avoid pretending that lightly explored aspects are settled
- support systematic long-horizon coverage
- connect aspect maturity to execution readiness

That is the intended standard.
