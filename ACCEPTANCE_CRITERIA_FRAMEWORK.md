# KR Acceptance Criteria Framework

## 1. Purpose

This document defines how the future KR production project should formulate, apply, and review acceptance criteria for:

- strategic conclusions
- doctrine artifacts
- protocol artifacts
- architecture artifacts
- evaluation artifacts
- execution task packets
- returned execution work
- major aspect-hardening outcomes

Its purpose is to ensure that acceptance in KR is not governed by vague impressions such as:

- “this seems good”
- “this feels strong enough”
- “this looks complete”
- “this sounds right”

Instead, KR should use explicit acceptance logic that makes quality review:

- more consistent
- more transferable
- more auditable
- more difficult to fake
- more useful for multi-agent work

This framework is a core bridge between:

- reasoning
- artifacts
- execution
- review
- trustworthiness

---

## 2. Core principle

Acceptance criteria define what must be true before KR treats something as acceptable for its intended role.

Acceptance is not the same as:

- admiration
- plausibility
- effort spent
- verbosity
- apparent sophistication

Acceptance means:
the item is good enough, for its intended purpose, under explicit standards.

The phrase “for its intended purpose” matters.

A doctrine note, a task packet, and an exploratory memo should not be judged by the same standard.

So KR needs:

- common acceptance logic
- but type-specific acceptance criteria

---

## 3. Design goals

The acceptance framework should satisfy all of the following:

1. **Clarity**
   It should be obvious what is being judged.

2. **Purpose alignment**
   The criteria should match the real role of the item.

3. **Reviewability**
   A reviewer should be able to apply the criteria concretely.

4. **Failure visibility**
   It should be easier to see why something failed.

5. **Tier sensitivity**
   Small local items and major strategic items should not be judged by identical intensity.

6. **Transferability**
   Different future workers should be able to apply the same acceptance frame.

7. **Anti-fuzziness**
   The framework should resist vague “good enough” judgments.

---

## 4. What acceptance criteria are for

Acceptance criteria are used to answer questions like:

- Is this aspect sufficiently hardened for the current stage?
- Is this doctrine note actually usable?
- Is this protocol operational rather than decorative?
- Is this file proposal strong enough to create?
- Is this execution packet ready to hand off?
- Does the returned implementation actually satisfy the packet?
- Is this recommendation mature enough to guide downstream work?
- Can this result be treated as active rather than provisional?

Acceptance criteria are therefore a gating mechanism, not an afterthought.

---

## 5. What acceptance criteria are NOT

Acceptance criteria are not:

- marketing language
- generic aspirations
- a substitute for real review
- purely aesthetic preferences
- a hidden, unspoken standard in the reviewer’s mind
- a giant wish list of everything that would be nice someday

They must define what is required for acceptance now, for the relevant role.

---

## 6. Acceptance object types

Different classes of objects need different acceptance frames.

The future KR production project should recognize at least these object types:

### O1 — strategic conclusion

A major recommendation, decision direction, or aspect-level outcome.

### O2 — doctrine artifact

A durable statement of project position or boundary.

### O3 — protocol artifact

A reusable method for recurring work.

### O4 — architecture artifact

A structural model or design position.

### O5 — evaluation artifact

A rubric, benchmark note, taxonomy of failure, or quality framework.

### O6 — registry or schema artifact

A structured durable reference artifact.

### O7 — execution task packet

A bounded handoff instrument for an implementation agent.

### O8 — returned execution work

The actual work returned after a task packet is executed.

### O9 — working artifact

An intentionally temporary but useful intermediate artifact.

Each object type should have a compatible acceptance frame.

---

## 7. Universal acceptance questions

Before type-specific criteria are applied, every object should first survive these universal questions.

### U1 — Purpose clarity

Is it clear what this object is supposed to do?

### U2 — Scope clarity

Is it clear what this object covers and does not cover?

### U3 — Internal coherence

Does it hold together logically?

### U4 — Role fit

Is it actually suitable for the role it is meant to play?

### U5 — Non-deceptiveness

Does it avoid pretending to be more mature, authoritative, or certain than it is?

### U6 — Downstream usefulness

Will accepting this object materially help future work?

If an object fails these universal questions badly, it should not be accepted even before type-specific review.

---

## 8. Acceptance criteria philosophy by tier

The depth of acceptance review should depend on the significance of the object.

### Tier A — light acceptance

For low-stakes local objects.

Use when:

- the object is bounded
- low-regret
- easily revisable
- not strategically central

### Tier B — standard acceptance

For meaningful but not deeply irreversible objects.

Use when:

- the object affects future work
- but not at major strategic scale

### Tier C — strong acceptance

For strategically important objects.

Use when:

- the object will guide multiple future tasks
- the object affects doctrine, architecture, or major workflow
- mistaken acceptance would propagate confusion

### Tier D — critical acceptance

For high-stakes, hard-to-reverse, trust-sensitive, or domain-sensitive objects.

Use when:

- the object shapes core KR direction
- the object bears on trustworthiness or scholarly legitimacy
- the object may unlock major execution or structural commitment

This tiered model prevents both:

- under-review of important items
- and over-review of small ones

---

## 9. Acceptance doctrine for strategic conclusions

Strategic conclusions should be accepted only when they satisfy criteria such as:

### S1 — The real question is clear

The conclusion actually answers a clearly stated problem.

### S2 — The stakes are explicit

It is clear why this conclusion matters.

### S3 — The recommendation is direct

The project is not hiding behind vague options without judgment.

### S4 — Alternatives were considered

The conclusion did not arise by inertia alone.

### S5 — Major assumptions are surfaced

Important assumptions are visible.

### S6 — Critique occurred

The conclusion has survived at least one meaningful challenge pass.

### S7 — Residual uncertainty is explicit

Open questions are not buried.

### S8 — The result is operational

The conclusion can now guide artifacts, further hardening, or execution.

A strategic conclusion should not be accepted just because it sounds intelligent.

---

## 10. Acceptance doctrine for doctrine artifacts

A doctrine artifact should be accepted only when it satisfies criteria such as:

### D1 — Position clarity

It clearly states KR’s position on the issue.

### D2 — Boundary clarity

It clearly states what is in bounds and out of bounds.

### D3 — Rationale adequacy

It explains why this doctrine exists.

### D4 — Stage awareness

It distinguishes current state, v1, and longer-horizon implications where relevant.

### D5 — Durability

It reads like something future work can rely on, not like an exploratory memo.

### D6 — Non-implementation drift

It does not collapse into local implementation detail.

### D7 — Action relevance

It actually helps future decisions.

A doctrine note that is thoughtful but non-governing should not be accepted as doctrine.

---

## 11. Acceptance doctrine for protocol artifacts

A protocol artifact should be accepted only when it satisfies criteria such as:

### P1 — Repeatable method clarity

It clearly defines how a recurring activity should be done.

### P2 — Step or flow clarity

It provides an operational sequence or method, not just philosophy.

### P3 — Trigger clarity

It is clear when the protocol should be used.

### P4 — Output clarity

It is clear what the protocol should produce.

### P5 — Boundary clarity

It is clear what the protocol does not govern.

### P6 — Reusability

Future workers could actually apply it again.

### P7 — Anti-failure awareness

Likely failure modes are addressed where needed.

A protocol that sounds wise but does not operationalize recurrence should not be accepted.

---

## 12. Acceptance doctrine for architecture artifacts

An architecture artifact should be accepted only when it satisfies criteria such as:

### A1 — Structural clarity

It clearly explains the relevant system structure.

### A2 — Relation clarity

It makes major relationships between parts intelligible.

### A3 — Constraint visibility

Key structural constraints are explicit.

### A4 — Strategic fit

It fits KR’s actual aims and doctrine.

### A5 — Complexity realism

It does not hide architectural cost or ugliness.

### A6 — Downstream usefulness

It can guide future decisions or implementation.

### A7 — Non-handwaving

It is not just a conceptual sketch pretending to be design.

Architecture that is evocative but non-actionable should not be accepted.

---

## 13. Acceptance doctrine for evaluation artifacts

An evaluation artifact should be accepted only when it satisfies criteria such as:

### E1 — What is being judged is clear

It clearly names the object or behavior under evaluation.

### E2 — Success and failure are distinguishable

It helps separate good from bad, not just describe goodness vaguely.

### E3 — Criteria are reviewable

A reviewer can actually apply them.

### E4 — Calibration plausibility

The standard does not obviously overfit fantasy cases.

### E5 — Severity logic, if relevant

It can distinguish stronger and weaker failures where needed.

### E6 — Operational relevance

It can actually influence future acceptance or correction.

An evaluation artifact that cannot change decisions is not yet good enough.

---

## 14. Acceptance doctrine for registries and schemas

A registry or schema artifact should be accepted only when it satisfies criteria such as:

### R1 — Structural clarity

The fields or structure are clear.

### R2 — Consistency support

The structure will actually help normalize repeated entries.

### R3 — Right format choice

This really should be structured data or schema, not prose.

### R4 — Coverage adequacy

The structure captures the needed fields without obvious critical omissions.

### R5 — Non-bloat

It is not overdesigned for imagined future complexity.

### R6 — Reusability

Future entries can actually use the structure cleanly.

A registry or schema that is elaborate but unnecessary should not be accepted.

---

## 15. Acceptance doctrine for execution task packets

A task packet should be accepted for handoff only when it satisfies criteria such as:

### X1 — Task clarity

The worker can tell exactly what task exists.

### X2 — Strategic rationale

It is clear why the task matters.

### X3 — Scope boundary

It is clear what is in scope and out of scope.

### X4 — Constraint visibility

Important constraints are explicit.

### X5 — Acceptance criteria presence

The packet itself contains reviewable success criteria.

### X6 — Discretion clarity

Allowed and disallowed discretion are explicit.

### X7 — Return format clarity

The worker knows how to report back.

### X8 — Reviewability

The returned work can later be judged against this packet.

A task packet that still depends on the execution worker inventing strategy should not be accepted.

---

## 16. Acceptance doctrine for returned execution work

Returned execution work should be accepted only when it satisfies criteria such as:

### Y1 — Objective match

It solves the intended task.

### Y2 — Scope discipline

It stayed within the allowed boundary.

### Y3 — Constraint compliance

It respected the packet’s stated constraints.

### Y4 — Acceptance criteria satisfaction

It actually passes the packet’s success conditions.

### Y5 — No hidden drift

It did not smuggle in unauthorized strategic changes.

### Y6 — Artifact cleanliness

The produced files or changes are usable and durable enough.

### Y7 — Residual-issue honesty

Any unresolved issues are surfaced rather than hidden.

Returned work should be reviewed for fit, not merely effort.

---

## 17. Acceptance doctrine for working artifacts

Working artifacts are accepted differently because their role is different.

A working artifact should be accepted only when it satisfies criteria such as:

### W1 — Clear intermediate purpose

It is clear why this working artifact exists.

### W2 — Scope honesty

It does not pretend to be final doctrine.

### W3 — Useful temporary structure

It helps intermediate thinking enough to justify existing.

### W4 — Lifecycle plausibility

It is likely to be promoted, merged, archived, or removed later.

### W5 — Containment

It does not quietly become permanent junk.

Working artifacts should be useful, temporary, and honest.

---

## 18. Minimal acceptance template

The future KR production project should be able to state acceptance logic in a compact standard form.

### Acceptance criteria template

Object:
[What is being judged]

Object type:
[O1–O9]

Acceptance tier:
[A / B / C / D]

Purpose:
[What role this object is meant to play]

Must be true:

- [Criterion]
- [Criterion]
- [Criterion]

Must not be true:

- [Failure condition]
- [Failure condition]

Review method:
[How this will be judged]

If accepted:
[What becomes possible]

If rejected:
[What must happen next]

# 19. Strong acceptance template

For more important objects, the project should use a stronger form.

Strong acceptance template

Object:
[What is being judged]

Object type:
[O1–O9]

Acceptance tier:
[C / D]

Purpose:
[Exact intended role]

Scope:
[What this object covers and does not cover]

Universal checks:

purpose clarity
scope clarity
internal coherence
role fit
non-deceptiveness
downstream usefulness

Type-specific must-be-true criteria:

[Criterion]
[Criterion]
[Criterion]

Critical failure conditions:

[Failure condition]
[Failure condition]

Evidence requirements, if any:

[Required evidence]
[Required evidence]

Review method:

[Review pass]
[Critique pass]
[Evidence check]
[Final acceptance review]

Acceptance result classes:

accepted
accepted with revisions
revision required
rejected

If accepted:
[Downstream consequence]

If rejected:
[Exact next move]

---

## 20. Acceptance result classes

The future KR production project should classify acceptance outcomes clearly.

### AC1 — accepted

The object is good enough for its intended role.

### AC2 — accepted with minor revisions

The object is fundamentally good enough, but minor corrections are still required.

### AC3 — revision required

The object is directionally relevant but not yet acceptable.

### AC4 — rejected

The object should not be adopted in its current form.

### AC5 — wrong-object error

The problem is not the quality of the object alone; it is that the wrong kind of object was created for the need.

This last category matters. Sometimes a weak result is not just “bad quality.” Sometimes it is the wrong artifact type entirely.

---

## 21. Failure-condition doctrine

Every serious acceptance frame should include not only “must be true” criteria, but also explicit failure conditions.

This matters because many reviews become weak when they only say what ideal success looks like.

Failure conditions should answer:

- what would make this object unacceptable?
- what would indicate that the object is misleading, unsafe, structurally weak, or wrongly framed?
- what would force revision rather than quiet acceptance?

A review that lacks failure conditions is usually too soft.

---

## 22. Acceptance and confidence are not the same

An object can be accepted for its intended role even if it carries uncertainty.

Examples:

- a provisionally hardened doctrine note may be accepted as a working doctrine for the current stage
- a task packet may be accepted even if a low-regret local implementation uncertainty remains
- a working memo may be accepted as a useful temporary artifact without being accepted as final doctrine

Therefore, acceptance should always be interpreted relative to:

- role
- scope
- stage
- tier

This prevents the false idea that accepted means perfect or eternal.

---

## 23. Acceptance and stage-awareness

The same object may have different acceptance standards depending on project stage.

Examples:

- a v1 doctrine note may be accepted under standards appropriate to the current stage of KR
- a long-horizon architecture artifact may require stronger critique before acceptance
- a temporary execution packet may be accepted even if broader project theory is still evolving

Acceptance must therefore remain stage-aware.

The future KR production project should explicitly ask:

- acceptable for what stage?
- acceptable for what role?
- acceptable with what known limits?

---

## 24. Acceptance review sequence

For important objects, acceptance should happen through a sequence rather than one vague judgment.

Recommended sequence:

### Step 1 — identify object type

What kind of thing is this?

### Step 2 — identify intended role

What is this object supposed to do?

### Step 3 — set acceptance tier

How hard should the review be?

### Step 4 — define criteria

What must and must not be true?

### Step 5 — review against criteria

Actually test the object.

### Step 6 — classify result

Accepted, revision required, rejected, etc.

### Step 7 — define consequence

What happens next because of this result?

This sequence should become habitual in the future production project.

---

## 25. Acceptance and aspect hardening

For aspect work, acceptance criteria should help determine when:

- a chat result is merely exploratory,
- a direction is provisional,
- an aspect is provisionally hardened,
- or an aspect is hardened enough to guide dependent work.

This means aspect hardening should often include an explicit acceptance question such as:

- what would need to be true for this aspect conclusion to be acceptable at S6?
- what would need to be true for S7?

This ties the acceptance framework directly to the aspect state model.

---

## 26. Acceptance and execution readiness

No task should enter execution merely because it seems useful.

Execution readiness should be treated as an acceptance judgment.

A task is execution-ready only if:

- the packet passes its own acceptance frame
- the strategic rationale is stable enough
- the relevant aspect is mature enough
- the acceptance criteria for the task are explicit
- the review plan exists

Execution readiness is therefore a special acceptance gate, not a mood.

---

## 27. Anti-failure rules

The future KR production project must avoid the following acceptance failures.

### 27.1 Vibe-based acceptance failure

Objects are accepted because they feel good, not because they passed criteria.

### 27.2 Hidden-standard failure

A reviewer knows internally what they want, but never states it.

### 27.3 No-failure-condition failure

The criteria only describe ideals and never name disqualifiers.

### 27.4 Over-demand failure

Acceptance criteria become so perfectionistic that useful progress cannot pass.

### 27.5 Under-demand failure

Criteria are so weak that low-quality work passes.

### 27.6 Wrong-role failure

An object is judged by standards that do not match its role.

### 27.7 Stage-blind failure

The project applies later-stage standards blindly to current-stage work, or vice versa.

### 27.8 Decorative-criteria failure

Criteria exist on paper but are not really used in review.

These failures must be actively resisted.

---

## 28. Recommended acceptance memo structure

When the future KR production project performs a serious acceptance review, it should summarize it in a structure like:

### Acceptance review memo

Object:
[What was reviewed]

Object type:
[Type]

Acceptance tier:
[Tier]

Purpose:
[Intended role]

Criteria applied:

- [Criterion]
- [Criterion]

Strongest passes:

- [Pass]
- [Pass]

Strongest failures or weaknesses:

- [Weakness]
- [Weakness]

Result:
[AC1 / AC2 / AC3 / AC4 / AC5]

Why:
[Short explanation]

Next move:
[Exact next step]

# 29. Success condition

The acceptance framework is successful only if the future KR production project can use it to do all of the following:

define what “good enough” means for different object types
judge doctrine, protocols, architecture, execution packets, and returned work consistently
distinguish acceptance from admiration
make failure visible
support aspect hardening and execution readiness
reduce vague quality judgments
improve multi-agent trustworthiness and review discipline

That is the intended standard.
