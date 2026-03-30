# KR File Naming and Placement Rules

## 1. Purpose

This document defines how the future KR production project should name and place durable files and directories so that the KR repo remains legible, coherent, recoverable, and resistant to documentation chaos over time.

Its purpose is to ensure that:
- important files are easy to find
- artifact classes remain visibly separated
- file authority is easier to infer
- duplicate or overlapping docs are less likely to emerge
- strategic artifacts do not pollute the control plane
- temporary work does not masquerade as durable doctrine
- the repo can scale without becoming structurally confusing

This document is primarily about non-code project artifacts, but it also defines how those artifacts should relate to code-adjacent documentation.

---

## 2. Core principle

A file’s path and name are part of its meaning.

They should help a future worker infer:
- what kind of artifact this is
- what scope it governs
- whether it is durable or temporary
- whether it is local or cross-cutting
- where related artifacts are likely to live

The repo should therefore not treat naming and placement as cosmetic details.
They are part of project cognition.

---

## 3. Design goals

The naming and placement system should satisfy all of the following:

1. **Legibility**
   A future worker should be able to navigate the repo without guessing.

2. **Authority clarity**
   File type and placement should help reveal what role the file plays.

3. **Low clutter**
   The root and key directories should remain clean.

4. **Predictability**
   Similar artifacts should follow similar naming and placement patterns.

5. **Locality**
   Files should live near the thing they govern unless they are cross-cutting.

6. **Scalability**
   The system should still make sense after many more files are added.

7. **Recoverability**
   Important artifacts should be easy to rediscover later.

---

## 4. Scope of this document

This document governs:
- durable strategic documentation
- doctrine files
- protocol files
- architecture notes
- evaluation artifacts
- registries
- templates
- execution-support artifacts
- working artifacts where they exist
- the relationship between cross-cutting docs and local engine docs

This document does not try to impose one naming style on:
- source code files
- package/module naming inside specific programming languages
- ecosystem-standard config files

Those should follow their own local language or tool conventions unless there is a strong repo-wide reason otherwise.

---

## 5. Governing placement law

A file should live in the smallest sensible namespace that matches its real scope.

This means:

### 5.1 Cross-cutting artifact
If the file governs multiple parts of KR or the project as a whole, it should live in a cross-cutting documentation namespace.

### 5.2 Local artifact
If the file governs only one engine, subsystem, or bounded local area, it should live near that area.

### 5.3 Control artifact
If the file governs live project control, it belongs in the control plane.

### 5.4 Temporary working artifact
If the file is intentionally temporary or intermediate, that status should be visible in both placement and lifecycle.

This law prevents both:
- excessive centralization
- and excessive scattering

---

## 6. Top-level placement doctrine

The repo root should remain sparse and high-signal.

The root should contain only:
- core project entry files
- canonical control-plane namespace(s)
- major code directories
- major documentation namespaces
- unavoidable tool/config files

The root should not become a dumping ground for:
- random doctrine docs
- isolated one-off notes
- unnamed experimental markdown files
- duplicate strategic memos
- “final_v2” style artifacts

A clean root is one of the repo’s main navigation aids.

---

## 7. Control-plane boundary rule

The `.kr/` namespace is reserved for project-control artifacts.

It should contain things like:
- charter
- active frontier
- handoff
- decisions ledger
- other truly control-plane files if explicitly justified

It should not absorb:
- general doctrine
- architecture memos
- evaluation systems
- arbitrary strategy notes
- implementation task packets
- broad product thinking

The control plane must remain small, disciplined, and high-authority.

This rule is non-negotiable.

---

## 8. Recommended cross-cutting documentation namespace

Cross-cutting durable non-code artifacts should generally live under a dedicated documentation namespace rather than directly at the root.

### Recommended pattern
Use a top-level `docs/` directory as the main home for cross-cutting durable project artifacts.

Within `docs/`, use functional families such as:
- `docs/doctrine/`
- `docs/protocols/`
- `docs/architecture/`
- `docs/evaluation/`
- `docs/registries/`
- `docs/templates/`
- `docs/execution/`
- `docs/working/` (only if truly needed)

This gives the repo a clear separation:
- `.kr/` for live control
- `docs/` for durable cross-cutting project knowledge
- code directories for implementation

That separation is strong and scalable.

---

## 9. Cross-cutting versus local placement rule

Before placing an artifact, the future KR production project should ask:

### Question 1
Does this artifact govern KR broadly?
If yes, place it under the cross-cutting documentation namespace.

### Question 2
Does this artifact govern only one engine or subsystem?
If yes, place it near that engine or subsystem.

### Question 3
Would putting it in a central namespace reduce useful locality?
If yes, prefer local placement.

### Question 4
Would putting it locally hide an artifact that many future workers need?
If yes, prefer central placement.

The right placement is the one that makes the artifact easiest to find by the workers who will actually need it.

---

## 10. Engine-local documentation rule

When a file primarily governs one engine or subsystem, it should usually live near that subsystem.

Examples:
- excerpting engine spec
- taxonomy engine-specific working note
- local engine evaluation guide
- engine-local schema explanation

This is especially important when:
- the artifact is tightly coupled to one local implementation area
- future workers editing that area will need it frequently
- the artifact is not meaningfully reusable at cross-project level

Do not centralize engine-local documentation merely for neatness if that reduces locality.

---

## 11. Cross-cutting doctrine rule

When a file expresses a durable project-wide or multi-engine position, it should not be buried inside one engine directory.

Examples:
- input-format doctrine
- v1 proof doctrine
- trustworthiness doctrine
- strategic expansion doctrine
- library-structure doctrine

These belong in the cross-cutting doctrine family, not in a single engine path.

---

## 12. Recommended family placement by artifact class

### 12.1 Doctrine artifacts
Recommended home:
- `docs/doctrine/`

Examples:
- `docs/doctrine/V1_PROOF_DOCTRINE.md`
- `docs/doctrine/INPUT_FORMAT_DOCTRINE.md`
- `docs/doctrine/TRUSTWORTHINESS_DOCTRINE.md`

### 12.2 Protocol artifacts
Recommended home:
- `docs/protocols/`

Examples:
- `docs/protocols/DEEP_RESEARCH_AND_REVIEW_PROTOCOL.md`
- `docs/protocols/CHAT_WORKFLOW_PROTOCOL.md`
- `docs/protocols/EXECUTION_HANDOFF_SYSTEM.md`

### 12.3 Architecture artifacts
Recommended home:
- `docs/architecture/`

Examples:
- `docs/architecture/LIBRARY_STRUCTURE.md`
- `docs/architecture/UNIT_OF_KNOWLEDGE_MODEL.md`
- `docs/architecture/CROSS_ENGINE_COHERENCE.md`

### 12.4 Evaluation artifacts
Recommended home:
- `docs/evaluation/`

Examples:
- `docs/evaluation/EVALUATION_DOCTRINE.md`
- `docs/evaluation/ERROR_TAXONOMY.md`
- `docs/evaluation/ACCEPTANCE_CRITERIA_FRAMEWORK.md`

### 12.5 Registry artifacts
Recommended home:
- `docs/registries/`

Examples:
- `docs/registries/ASPECT_REGISTRY.yaml`
- `docs/registries/ARTIFACT_REGISTRY.yaml`
- `docs/registries/UNRESOLVED_QUESTIONS.yaml`

### 12.6 Template artifacts
Recommended home:
- `docs/templates/`

Examples:
- `docs/templates/CODEX_TASK_PACKET_TEMPLATE.md`
- `docs/templates/DECISION_RECORD_TEMPLATE.md`
- `docs/templates/DOCTRINE_NOTE_TEMPLATE.md`

### 12.7 Execution-support artifacts
Recommended home:
- `docs/execution/`

Examples:
- `docs/execution/EXECUTION_READINESS_CHECKLIST.md`
- `docs/execution/HANDOFF_REVIEW_GUIDE.md`

### 12.8 Working artifacts
Recommended home:
- `docs/working/`

Examples:
- `docs/working/PDF_INGESTION_OPTION_MEMO.md`
- `docs/working/TAXONOMY_BRANCHING_EXPLORATION.md`

This family must be tightly controlled to avoid becoming a junk drawer.

---

## 13. Naming convention by artifact type

The future KR production project should use naming conventions that reflect artifact function.

### 13.1 Durable cross-cutting markdown artifacts
Recommended style:
- `UPPER_SNAKE_CASE.md`

Examples:
- `V1_PROOF_DOCTRINE.md`
- `INPUT_FORMAT_DOCTRINE.md`
- `CHAT_WORKFLOW_PROTOCOL.md`
- `UNIT_OF_KNOWLEDGE_MODEL.md`

Rationale:
- visually distinct
- grep-friendly
- consistent with existing KR control-plane style
- clearly document-like

### 13.2 Structured registries
Recommended style:
- `UPPER_SNAKE_CASE.yaml`
- or another structured extension if strongly justified

Examples:
- `ASPECT_REGISTRY.yaml`
- `ARTIFACT_REGISTRY.yaml`
- `BENCHMARK_REGISTRY.yaml`

### 13.3 Templates
Recommended style:
- descriptive name ending in `_TEMPLATE`

Examples:
- `DECISION_RECORD_TEMPLATE.md`
- `CODEX_TASK_PACKET_TEMPLATE.md`

### 13.4 Schemas
Recommended style:
- descriptive name ending in `_SCHEMA`

Examples:
- `DECISION_LOG_SCHEMA.md`
- `ASPECT_STATE_SCHEMA.yaml`

### 13.5 Working memos
Recommended style:
- explicit descriptive names without pretending they are doctrine

Examples:
- `PDF_INGESTION_OPTION_MEMO.md`
- `RETRIEVAL_COMPARISON_WORKING_NOTE.md`

Do not name a temporary memo like doctrine if it is not doctrine.

---

## 14. Naming goals

A good filename should help answer:
- what topic is this about?
- what kind of artifact is it?
- how durable is it likely to be?
- what should I expect to find inside?

A good filename should be:
- specific
- stable
- greppable
- low-ambiguity
- function-revealing

A filename should avoid requiring prior personal context to interpret.

---

## 15. Forbidden naming patterns

The future KR production project should avoid filenames like:

- `notes.md`
- `ideas.md`
- `thoughts.md`
- `new.md`
- `misc.md`
- `temp.md`
- `draft2.md`
- `final.md`
- `final_final.md`
- `v3_real.md`

These names destroy recoverability and authority clarity.

If a file matters enough to exist, it matters enough to be named properly.

---

## 16. Date-stamp rule

Dates should not be embedded in filenames unless the artifact is inherently time-bound.

Good candidates for date-bearing names:
- time-specific reports
- campaign outputs
- periodic reviews
- snapshots
- migration records tied to a dated event

Poor candidates:
- doctrine files
- protocols
- enduring architecture notes
- templates
- registries

Durable files should have stable names.
Their content or metadata can reflect updates without renaming the file repeatedly.

---

## 17. Versioning-in-name rule

Do not version durable documents in filenames unless there is a strong and explicit reason.

Avoid:
- `INPUT_FORMAT_DOCTRINE_V2.md`
- `TRUST_MODEL_FINAL_V3.md`

Prefer:
- one authoritative file
- explicit supersession or lifecycle handling inside the artifact system
- decision-log support for major changes
- git history for revision history

Name-level versioning should be a last resort, not a habit.

---

## 18. Singular-versus-plural directory rule

Use plural directory names for artifact families.

Examples:
- `docs/doctrine/`
- `docs/protocols/`
- `docs/registries/`
- `docs/templates/`

Rationale:
- the directory represents a family, not a single artifact
- plural names are clearer and scale better

Use singular filenames for individual artifacts.

---

## 19. Depth rule

Do not create unnecessary directory depth.

The future KR production project should prefer:
- shallow, legible paths

over:
- deeply nested paths that require too much guesswork

Good:
- `docs/doctrine/V1_PROOF_DOCTRINE.md`

Usually bad:
- `docs/strategy/core/v1/doctrine/proof/V1_PROOF_DOCTRINE.md`

Extra depth is justified only when:
- the family has grown enough to need subdivision
- the subfamily meaning is stable and useful
- the added depth improves, rather than harms, discoverability

---

## 20. Folder-creation rule

Create a new directory only when one or more of the following are true:

- multiple artifacts of the same class now exist or are expected soon
- the new directory creates meaningful functional separation
- the new directory reduces clutter in an existing namespace
- the new directory expresses a durable distinction the project will keep using

Do not create directories for:
- one speculative file
- a naming fashion
- premature organization
- imagined scale that never arrives

Folders should emerge from real structural need.

---

## 21. Update-existing versus create-new placement rule

When a new durable concept emerges, the future KR production project should ask:

- does an existing file already own this concept?
- does an existing family directory already provide the correct home?
- would a new file improve clarity, or merely split context unnecessarily?
- would adding this to an existing artifact create overload?

The default should be:
- update existing durable homes when that preserves clarity
- create new files only when the scope is truly distinct

This rule is essential for long-term repo discipline.

---

## 22. Locality-of-authority rule

The path of a file should help reveal its authority.

Examples:
- `.kr/ACTIVE.md` implies live project-control authority
- `docs/doctrine/INPUT_FORMAT_DOCTRINE.md` implies durable cross-cutting doctrinal authority
- `docs/templates/CODEX_TASK_PACKET_TEMPLATE.md` implies reusable scaffold, not governing doctrine
- `docs/working/PDF_INGESTION_OPTION_MEMO.md` implies intermediate exploration, not final law

This is important:
placement should help future workers infer how much weight to assign to the artifact.

---

## 23. Working-artifact containment rule

Working artifacts are dangerous if left unmanaged.

If `docs/working/` exists, it should be governed tightly.

Rules:
- only use it for real intermediate artifacts worth preserving temporarily
- do not let it become a general scratchpad
- regularly promote, merge, archive, or delete working artifacts
- never let working files quietly become de facto doctrine because they were never cleaned up

A working namespace is useful only if it is actively curated.

---

## 24. Promotion rule

When a working artifact matures into durable project guidance, it should be promoted into the correct durable family.

Examples:
- a working comparison memo becomes a doctrine note
- a rough process note becomes a protocol
- a repeated tracking note becomes a registry
- a recurring local structure becomes a schema or template

Promotion should usually involve:
- a new durable home
- proper naming
- authority clarification
- lifecycle handling for the old working file if it remains

---

## 25. Archive and deprecation rule

When files are superseded, deprecated, or no longer authoritative, their status must become clear.

The future KR production project should avoid leaving ambiguous old files in place without context.

Possible handling patterns:
- update the old file to mark it superseded
- move it into an archive namespace if appropriate
- note the replacement artifact
- record the supersession in the decision system where relevant

The exact archive mechanism can remain light at first, but ambiguity must not remain.

---

## 26. Recommended header convention for durable markdown artifacts

Durable strategic markdown files should begin with a compact metadata header similar to KR’s existing control-plane style.

Recommended pattern:

- Purpose:
- Authority:
- Update when:
- Must not contain:

Example:

> Purpose: Define KR’s durable position on input-format support.
> Authority: Cross-cutting doctrine for source-format expansion.
> Update when: The strategic format roadmap changes materially.
> Must not contain: Local parser implementation notes, temporary experiments, or execution tickets.

This header improves:
- authority clarity
- update discipline
- scope discipline

It is strongly recommended for durable markdown artifacts.

---

## 27. File-family boundary rules

The future KR production project must keep family boundaries clear.

### Doctrine files must not become:
- broad implementation notes
- meeting summaries
- scratchpads

### Protocol files must not become:
- general value essays
- architecture arguments without procedure

### Registry files must not become:
- long-form prose essays

### Template files must not become:
- actual instance records

### Working files must not pretend to be:
- durable law

These boundaries matter because naming and placement only work if artifact classes remain real.

---

## 28. Relationship to code files

This document does not try to rename code according to doc conventions.

Code should usually follow:
- language ecosystem norms
- local module conventions
- existing codebase patterns where sensible

However, when a documentation artifact is tightly local to code, it should:
- live near the relevant code
- be named clearly
- not compete with cross-cutting doctrine files

Examples:
- engine-local `SPEC.md`
- local `README.md`
- engine-local evaluator note

The production project should not centralize all meaning into `docs/` if locality would be better.

---

## 29. Relationship to generated artifacts

Generated outputs, reports, or run artifacts should not be mixed with durable doctrine or protocol files.

They should live in namespaces that reflect:
- their generated nature
- their time-bound role
- their non-doctrinal status

This helps prevent confusion between:
- project law
- and project evidence or output snapshots

Generated artifacts should not be mistaken for governing files.

---

## 30. File proposal requirements

Whenever the future KR production project proposes creating a new file, it should specify:

- proposed path
- proposed file name
- artifact class
- why this location is correct
- why this name is correct
- whether an existing file should be updated instead
- what authority level the file will have
- expected sections or schema

Naming and placement should always be justified, not merely chosen.

---

## 31. Anti-failure rules

The future KR production project must avoid the following failures.

### 31.1 Root-sprawl failure
Too many strategic docs accumulate at the repo root.

### 31.2 Namespace-chaos failure
Files of very different kinds are mixed together without family boundaries.

### 31.3 Vague-name failure
Files are named so vaguely that their purpose is not inferable.

### 31.4 Duplicate-home failure
The same concept appears in multiple plausible homes without authority clarity.

### 31.5 Wrong-locality failure
A local engine artifact is buried centrally, or a cross-cutting artifact is hidden locally.

### 31.6 Working-as-durable failure
Temporary artifacts remain in places that imply authority.

### 31.7 Directory-overengineering failure
Too many folders are created before real need exists.

### 31.8 Document-version-chaos failure
Multiple numbered “final” files accumulate instead of one authoritative artifact.

These failures must be resisted actively.

---

## 32. Success condition

The file naming and placement system is successful only if the future KR production project can use it to keep the repo:

- easy to navigate
- low-clutter
- authority-legible
- scalable
- recoverable
- resistant to duplicate or ambiguous artifacts
- cleanly separated between control, doctrine, protocol, evaluation, registry, template, working, and execution roles

That is the intended standard.
