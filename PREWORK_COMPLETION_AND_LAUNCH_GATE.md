# KR Pre-Work Completion and Launch Gate

## 1. Purpose

This checklist defines the formal launch gate for the KR pre-work project.

Its purpose is to determine whether the pre-work project has actually completed its job:
- designing,
- hardening,
- validating,
- and packaging

the operating system for the future KR production project.

This is not a general “how are we doing?” checklist.

It is a strict readiness gate that answers:

**Should the real KR production project be launched now, or is pre-work still incomplete?**

---

## 2. Core principle

Pre-work is complete only when the real KR production project can begin without needing further foundational operating-system design.

That means:
- no major missing behavioral rule
- no major missing protocol
- no major missing registry/schema needed for coherence
- no major launch ambiguity
- no major unvalidated setup weakness

The standard is not:
- “we have done a lot”
or
- “the setup is already pretty good”

The standard is:
- **is production launch justified now?**

---

## 3. Use rule

Use this checklist only near the end of the pre-work project, when the operating system appears close to complete.

Do not use it too early as a motivational tool.

This is a gating instrument, not a progress-celebration tool.

If major pieces are obviously missing, continue pre-work instead of pretending to run the gate.

---

## 4. Gate outcome classes

The launch gate must end in one of four explicit outcomes.

### G1 — launch approved
The pre-work project is sufficiently complete and validated. The real KR production project may be created now.

### G2 — launch approved with minor corrections
The system is fundamentally ready, but a small number of contained fixes should be made before launch.

### G3 — launch hold
The system is not yet ready. Important missing, weak, or unvalidated parts still remain.

### G4 — partial readiness only
Some major sections are strong, but the system as a whole is not coherent enough for production launch.

The gate must not end in vague language like:
- “probably ready”
- “almost there”
- “good enough maybe”

It must issue one of the above outcomes.

---

## 5. Gate philosophy

This gate should evaluate five things together:

1. completeness
2. coherence
3. operational usability
4. validation strength
5. launch readiness

A setup package can fail the gate even if:
- many files exist,
- many ideas are strong,
- and much work has been done,

if the system still lacks one or more critical properties above.

The gate is meant to protect the production project from premature launch.

---

## 6. Section A — constitutional completeness

Check whether the governing core of the operating system exists.

### A.1 Core governing files exist
- [ ] `PREWORK_CHARTER.md`
- [ ] `PREWORK_ROADMAP.md`
- [ ] `ROLE_MODEL_AND_AUTHORITY_SYSTEM.md`
- [ ] `CORE_INSTRUCTION_STACK.md`
- [ ] `CHAT_WORKFLOW_PROTOCOL.md`
- [ ] `DEEP_RESEARCH_AND_REVIEW_PROTOCOL.md`
- [ ] `KR_MASTER_ASPECT_MAP.md`
- [ ] `REPO_ARTIFACT_SYSTEM.md`
- [ ] `EXECUTION_HANDOFF_SYSTEM.md`
- [ ] `PRODUCTION_BOOTSTRAP_PROTOCOL.md`
- [ ] `PRELAUNCH_VALIDATION_PROTOCOL.md`

### A.2 Core support files exist
- [ ] `DECISION_LOG_SCHEMA.md`
- [ ] `ASPECT_STATE_MODEL.md`
- [ ] `FILE_NAMING_AND_PLACEMENT_RULES.md`
- [ ] `ACCEPTANCE_CRITERIA_FRAMEWORK.md`
- [ ] `CODEX_TASK_PACKET_TEMPLATE.md`
- [ ] `ARTIFACT_REGISTRY_SCHEMA.md`
- [ ] `UNRESOLVED_QUESTIONS_REGISTRY_SCHEMA.md`
- [ ] `ASPECT_REGISTRY_SCHEMA.md`
- [ ] `DEEP_RESEARCH_REQUEST_TEMPLATE.md`
- [ ] `PRODUCTION_STARTUP_CHECKLIST.md`

### A.3 Constitutional completeness judgment
- [ ] No major operating-system function still depends only on chat memory.
- [ ] No major core rule still exists only implicitly.
- [ ] No major missing file is still obvious.

If any critical file is missing, the gate should not pass.

---

## 7. Section B — behavioral completeness

Check whether the future production project’s behavior is fully defined.

### B.1 Role clarity
- [ ] The future model’s role is clear.
- [ ] Its authority boundaries are clear.
- [ ] Its question-minimization rules are clear.
- [ ] Its escalation rules are clear.
- [ ] Its uncertainty rules are clear.
- [ ] Its challenge posture toward the repo is clear.

### B.2 Workflow clarity
- [ ] One-aspect-per-chat is clearly defined.
- [ ] One-subtask-at-a-time is clearly defined.
- [ ] “Continue” behavior is clearly defined.
- [ ] New-chat versus same-chat rules are clearly defined.
- [ ] Chat closure behavior is clearly defined.

### B.3 Research and review clarity
- [ ] Deep-research trigger rules are defined.
- [ ] Review depth rules are defined.
- [ ] Critique protocol is defined.
- [ ] Evidence and confidence are not conflated.
- [ ] Hardening-completion logic is defined.

### B.4 Behavioral completeness judgment
- [ ] The future production project would know how to behave without needing its role re-derived in early chats.

If the project would still behave ambiguously, the gate should not pass.

---

## 8. Section C — structural completeness

Check whether the future production project has enough structure to operate systematically rather than conversationally.

### C.1 Aspect structure
- [ ] The master aspect map exists.
- [ ] The aspect state model exists.
- [ ] The aspect registry schema exists.

### C.2 Artifact structure
- [ ] The repo artifact system exists.
- [ ] File naming and placement rules exist.
- [ ] The artifact registry schema exists.

### C.3 Decision and uncertainty structure
- [ ] The decision log schema exists.
- [ ] The unresolved-questions registry schema exists.

### C.4 Execution structure
- [ ] The execution handoff system exists.
- [ ] The Codex task packet template exists.
- [ ] The acceptance framework exists.

### C.5 Structural completeness judgment
- [ ] The future production project would be able to track aspects, artifacts, decisions, unresolved questions, and execution handoffs coherently.

If these structures are weak or missing, launch should be held.

---

## 9. Section D — instruction readiness

Check whether the actual instructions needed at launch are ready.

### D.1 Global instructions ready
- [ ] The final global custom instructions are finalized.
- [ ] They are short enough and generic enough for account-level use.
- [ ] They do not improperly carry KR’s whole operating system.

### D.2 Production-project instructions ready
- [ ] The final production-project instructions are finalized.
- [ ] They encode the intended role strongly.
- [ ] They do not depend on vague interpretation.
- [ ] They are suitable for immediate paste into the production project.

### D.3 Pseudo-skill file set ready
- [ ] The intended project operating files are selected.
- [ ] Their roles are clear.
- [ ] They are suitable for upload into the production project.

### D.4 Instruction readiness judgment
- [ ] The production project’s instruction stack is actually deployable now.

If not, launch should not pass.

---

## 10. Section E — launch package readiness

Check whether the actual production launch package exists.

### E.1 Bootstrap readiness
- [ ] The production bootstrap protocol exists.
- [ ] The production startup checklist exists.
- [ ] The upload bundle is defined.
- [ ] The upload order is defined.

### E.2 First-chat readiness
- [ ] The first production aspect is selected.
- [ ] The first production opener is ready.
- [ ] The expected first output is clear.
- [ ] First-chat success conditions are clear.

### E.3 Launch package judgment
- [ ] A real production project could be created right now without needing improvisation.

If you would still need to invent major launch details live, the gate should not pass.

---

## 11. Section F — validation readiness

Check whether the operating system has actually been tested rather than only designed.

### F.1 Completeness audit performed
- [ ] The prelaunch validation protocol exists.
- [ ] Artifact completeness has been reviewed.

### F.2 Consistency audit performed
- [ ] Internal consistency across files has been reviewed.
- [ ] No major contradictions remain.

### F.3 Behavioral simulation performed
- [ ] First-chat simulation has been considered.
- [ ] “Continue” behavior has been considered.
- [ ] Artifact-conversion behavior has been considered.
- [ ] Execution-handoff behavior has been considered.

### F.4 Failure-mode stress testing performed
- [ ] Passive-assistant failure has been tested conceptually.
- [ ] Broad-chat failure has been tested conceptually.
- [ ] Research-overuse and underuse have been tested conceptually.
- [ ] No-artifact failure has been tested conceptually.
- [ ] Execution-drift failure has been tested conceptually.

### F.5 Validation readiness judgment
- [ ] The operating system has been pressure-tested enough that launch would not be blind.

If the setup has not really been tested, the gate should not pass.

---

## 12. Section G — production readiness judgment

This section asks the direct question.

### G.1 Can the production project begin real work immediately?
- [ ] Yes, without further foundational setup design.

### G.2 Can the project stay self-contained?
- [ ] Yes, it can begin with a coherent internal operating system.

### G.3 Can the user start productively with low friction?
- [ ] Yes, the user could create the project, upload the files, paste the instructions, start the first chat, and continue with short prompts.

### G.4 Would the first production chats likely behave correctly?
- [ ] Yes, based on the current setup and validation.

### G.5 Is further pre-work now lower leverage than production launch?
- [ ] Yes.

If several of these are not true, the gate should not pass.

---

## 13. Scoring frame

This section is optional but useful.

Score each category:
- 0 = missing
- 1 = weak
- 2 = adequate
- 3 = strong

### Suggested scoring categories
- constitutional completeness
- behavioral completeness
- structural completeness
- instruction readiness
- launch package readiness
- validation strength
- total-system coherence
- production usability

### Interpretation guide
- Mostly 3s with no serious zeros or ones: likely launch approved
- Some 2s and one or two contained 1s: maybe launch approved with minor corrections
- Several 1s or any critical 0: launch hold
- Strong islands but weak system integration: partial readiness only

The score informs judgment. It does not replace judgment.

---

## 14. Hard no-launch conditions

The pre-work project must not approve launch if any of the following are true:

- [ ] The final production-project instructions are still missing or unstable.
- [ ] The first production opener is missing.
- [ ] The upload bundle is still unclear.
- [ ] The project still lacks a coherent aspect system.
- [ ] The project still lacks a coherent execution handoff system.
- [ ] The project still lacks a coherent research/review system.
- [ ] Major behavior still depends on re-teaching the project in early chats.
- [ ] Major contradictions still exist across the governing files.
- [ ] The operating system has not been meaningfully validated.

Any one of these is enough to hold launch.

---

## 15. Minor-corrections-only conditions

Launch may still be approved with minor corrections if:
- all core files exist,
- the operating system is coherent,
- launch is practically executable,
- and the remaining issues are narrow, contained, and non-structural.

Examples of minor corrections:
- tightening wording in one protocol
- refining one template field
- clarifying one startup instruction
- improving one checklist item

Minor corrections are not:
- missing core systems
- missing launch logic
- missing first-chat design
- unresolved behavioral ambiguity

---

## 16. Final verdict block

At the end of the gate, the pre-work project should produce a verdict in this form:

### Launch gate verdict

Verdict:
[G1 / G2 / G3 / G4]

Strongest reasons:
- [Reason]
- [Reason]
- [Reason]

Strongest remaining weaknesses:
- [Weakness]
- [Weakness]

Required corrections before launch, if any:
- [Correction]
- [Correction]

Can production launch proceed now?
[Yes / No / Yes after minor corrections]

Best next move:
[Exact next step]

17. Success condition

This gate is successful only if it prevents both:

premature production launch,
and
endless unnecessary pre-work drift.

The goal is to launch neither too early nor too late.

The goal is to launch when the operating system is truly strong enough to justify real work.

