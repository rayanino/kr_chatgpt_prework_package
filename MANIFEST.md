# KR ChatGPT Pro Operating-System Package Manifest

## Purpose

This manifest explains:
- what files are in the package
- what class each file belongs to
- whether it is pre-work-only, production-core, production-support, or deployment-only
- whether it should usually be uploaded into the pre-work project
- whether it should later transfer into the production project

This manifest is the package navigation and transfer map.

It should be read before the package is instantiated inside ChatGPT Pro.

---

## File-class legend

### PREWORK_ONLY
Used to design, validate, and gate the operating system itself.
Usually should **not** transfer into the production project.

### PRODUCTION_CORE
Core operating-system files that define how the production project should think and behave.
These should usually transfer into production.

### PRODUCTION_SUPPORT
Support structures, schemas, registries, and templates that materially improve production work.
These often transfer into production.

### DEPLOYMENT_ONLY
User-side setup texts and launch aids.
Usually should **not** be uploaded into production by default.

### REPO_GROUNDING
Real KR repo files that anchor the package in actual project state.
These should be uploaded into both pre-work and production in carefully chosen subsets.

---

## Section A — Pre-work governance files

### PREWORK_CHARTER.md
Class: PREWORK_ONLY
Purpose: Defines what the pre-work project is, what it must produce, and what it must not become.
Upload to pre-work: Yes
Transfer to production: No

### PREWORK_ROADMAP.md
Class: PREWORK_ONLY
Purpose: Defines the staged completion path of the pre-work project.
Upload to pre-work: Yes
Transfer to production: No

### PRELAUNCH_VALIDATION_PROTOCOL.md
Class: PREWORK_ONLY
Purpose: Defines how the operating system should be tested before production launch.
Upload to pre-work: Yes
Transfer to production: Usually no

### PREWORK_COMPLETION_AND_LAUNCH_GATE.md
Class: PREWORK_ONLY
Purpose: Defines the formal stop/go gate for ending pre-work and launching production.
Upload to pre-work: Yes
Transfer to production: No

### FINAL_ASSEMBLY_AND_TRANSFER_PLAN.md
Class: PREWORK_ONLY
Purpose: Explains package structure, transfer rules, and deployment layers.
Upload to pre-work: Yes
Transfer to production: No

---

## Section B — Production core operating-system files

### ROLE_MODEL_AND_AUTHORITY_SYSTEM.md
Class: PRODUCTION_CORE
Purpose: Defines who ChatGPT Pro is inside KR and what authority it has.
Upload to pre-work: Yes
Transfer to production: Yes

### CORE_INSTRUCTION_STACK.md
Class: PRODUCTION_CORE
Purpose: Defines the layered instruction architecture for KR.
Upload to pre-work: Yes
Transfer to production: Usually no as a reference file, unless you want the project to explicitly retain the instruction-stack design; the actual instruction texts are deployed separately

### CHAT_WORKFLOW_PROTOCOL.md
Class: PRODUCTION_CORE
Purpose: Defines one-aspect-per-chat and one-subtask-at-a-time operation.
Upload to pre-work: Yes
Transfer to production: Yes

### DEEP_RESEARCH_AND_REVIEW_PROTOCOL.md
Class: PRODUCTION_CORE
Purpose: Defines when research is used, how review passes work, and how hardening works.
Upload to pre-work: Yes
Transfer to production: Yes

### KR_MASTER_ASPECT_MAP.md
Class: PRODUCTION_CORE
Purpose: Defines the full map of KR aspects that must eventually be hardened.
Upload to pre-work: Yes
Transfer to production: Yes

### REPO_ARTIFACT_SYSTEM.md
Class: PRODUCTION_CORE
Purpose: Defines how conclusions become durable repo-native artifacts.
Upload to pre-work: Yes
Transfer to production: Yes

### EXECUTION_HANDOFF_SYSTEM.md
Class: PRODUCTION_CORE
Purpose: Defines how hardened thought becomes bounded work for Codex or other workers.
Upload to pre-work: Yes
Transfer to production: Yes

### ASPECT_STATE_MODEL.md
Class: PRODUCTION_CORE
Purpose: Defines how aspect maturity is tracked over time.
Upload to pre-work: Yes
Transfer to production: Yes

### FILE_NAMING_AND_PLACEMENT_RULES.md
Class: PRODUCTION_CORE
Purpose: Defines where artifacts should live and how they should be named.
Upload to pre-work: Yes
Transfer to production: Yes

### ACCEPTANCE_CRITERIA_FRAMEWORK.md
Class: PRODUCTION_CORE
Purpose: Defines how doctrine, protocols, execution packets, and outputs are judged.
Upload to pre-work: Yes
Transfer to production: Yes

### DECISION_LOG_SCHEMA.md
Class: PRODUCTION_CORE
Purpose: Defines how durable decisions are recorded and tracked.
Upload to pre-work: Yes
Transfer to production: Yes

---

## Section C — Production support structures

### CODEX_TASK_PACKET_TEMPLATE.md
Class: PRODUCTION_SUPPORT
Purpose: Default reusable packet for bounded Codex work.
Upload to pre-work: Yes
Transfer to production: Yes

### ARTIFACT_REGISTRY_SCHEMA.md
Class: PRODUCTION_SUPPORT
Purpose: Defines the registry for tracking durable artifacts.
Upload to pre-work: Yes
Transfer to production: Yes

### UNRESOLVED_QUESTIONS_REGISTRY_SCHEMA.md
Class: PRODUCTION_SUPPORT
Purpose: Defines the registry for important open questions.
Upload to pre-work: Yes
Transfer to production: Yes

### ASPECT_REGISTRY_SCHEMA.md
Class: PRODUCTION_SUPPORT
Purpose: Defines the registry for current aspect state, priority, blockers, and next moves.
Upload to pre-work: Yes
Transfer to production: Yes

### DEEP_RESEARCH_REQUEST_TEMPLATE.md
Class: PRODUCTION_SUPPORT
Purpose: Standard template for high-quality research requests.
Upload to pre-work: Yes
Transfer to production: Yes

### FIRST_CHAT_AND_CONTINUATION_PROMPT_PACK.md
Class: DEPLOYMENT_ONLY by default, optionally PRODUCTION_SUPPORT
Purpose: User-side control surface for starting and steering production chats.
Upload to pre-work: Yes
Transfer to production: Optional

### PRODUCTION_BOOTSTRAP_PROTOCOL.md
Class: DEPLOYMENT_ONLY by default
Purpose: Defines how to create and launch the production project.
Upload to pre-work: Yes
Transfer to production: Usually no

### PRODUCTION_STARTUP_CHECKLIST.md
Class: DEPLOYMENT_ONLY by default
Purpose: Practical short-form launch checklist for production startup.
Upload to pre-work: Yes
Transfer to production: Usually no

---

## Section D — Deployment text files

These should be created as separate text files even though they were drafted inside the package design work.

### GLOBAL_CUSTOM_INSTRUCTIONS.txt
Class: DEPLOYMENT_ONLY
Purpose: Paste into account-level custom instructions.
Upload to pre-work: Optional
Transfer to production: No

### PREWORK_PROJECT_INSTRUCTIONS.txt
Class: DEPLOYMENT_ONLY
Purpose: Paste into the pre-work project instructions.
Upload to pre-work: No
Transfer to production: No

### PREWORK_KICKOFF_PROMPT.txt
Class: DEPLOYMENT_ONLY
Purpose: Start the first serious pre-work chat cleanly.
Upload to pre-work: No
Transfer to production: No

### PRODUCTION_PROJECT_INSTRUCTIONS.txt
Class: DEPLOYMENT_ONLY
Purpose: Paste into the production project instructions.
Upload to pre-work: Optional reference only
Transfer to production: No as a file; it is pasted as the instruction block

### FIRST_PRODUCTION_CHAT_OPENER_A2.txt
Class: DEPLOYMENT_ONLY
Purpose: Start the first production aspect chat.
Upload to pre-work: No
Transfer to production: No as a file; it is pasted into the first chat

---

## Section E — Repo grounding inputs

These are real KR files and should not be confused with the operating-system package itself.

### .kr/README.md
Class: REPO_GROUNDING
Purpose: Defines how to enter the KR control plane.
Upload to pre-work: Yes
Transfer to production: Yes

### .kr/CHARTER.md
Class: REPO_GROUNDING
Purpose: Defines durable KR mission, principles, and worker roles.
Upload to pre-work: Yes
Transfer to production: Yes

### .kr/ACTIVE.md
Class: REPO_GROUNDING
Purpose: Defines the current active frontier.
Upload to pre-work: Yes
Transfer to production: Yes

### .kr/HANDOFF.md
Class: REPO_GROUNDING
Purpose: Provides recent project state and resume context.
Upload to pre-work: Yes
Transfer to production: Yes

### Architecture overview
Class: REPO_GROUNDING
Purpose: Gives broader system structure beyond the control plane.
Upload to pre-work: Yes
Transfer to production: Yes if relevant to early aspect work

### Excerpting spec
Class: REPO_GROUNDING
Purpose: Grounds work in the current excerpting system.
Upload to pre-work: Yes
Transfer to production: Yes if early aspect work touches excerpting, v1 proof, or evaluation

### Taxonomy spec
Class: REPO_GROUNDING
Purpose: Grounds work in the current taxonomy system or intended taxonomy design.
Upload to pre-work: Yes
Transfer to production: Yes if early aspect work touches taxonomy or system structure

### Evaluation / rubric docs
Class: REPO_GROUNDING
Purpose: Grounds work in current evaluation realities.
Upload to pre-work: Yes if relevant
Transfer to production: Yes if relevant to early aspects

---

## Pre-work upload recommendation

The pre-work project should receive:
1. repo grounding files first
2. pre-work governance files second
3. production operating-system files third
4. production support and deployment-reference files last

The pre-work project should function as the primary auditing environment for the package.

---

## Production upload recommendation

The production project should receive:
1. repo grounding files
2. production-core operating files
3. selected production-support files
4. only the most relevant substantive KR files for early work

It should **not** receive the full pre-work governance layer by default.

---

## Minimal files required before starting pre-work

Before starting the pre-work project, the following should definitely exist locally:

- README.md
- MANIFEST.md
- the 24 markdown package files
- GLOBAL_CUSTOM_INSTRUCTIONS.txt
- PREWORK_PROJECT_INSTRUCTIONS.txt
- PREWORK_KICKOFF_PROMPT.txt
- PRODUCTION_PROJECT_INSTRUCTIONS.txt
- FIRST_PRODUCTION_CHAT_OPENER_A2.txt

Without these, the package is still under-prepared for clean instantiation.

---

## Minimal files required before starting production

Before creating the real production project, the following should definitely be ready:

- final production project instructions
- final global custom instructions
- final first production opener
- final production-core operating files
- selected production-support files
- selected repo-grounding files
- a passed pre-work launch gate

Without these, production launch is premature.

---

## Package status rule

Until the pre-work project audits and approves the package, the package should be treated as:

- strong draft
- under audit
- not yet canonized
- not yet merged wholesale into the repo’s durable structure

This rule is important.
The package should be validated before being treated as settled project law.

---

## Practical next move

The practical next move after creating this README and MANIFEST is:

1. create the five deployment text files
2. place all files into the local package structure
3. buy Pro
4. create the pre-work project
5. upload the package and start the pre-work audit

That is the correct next sequence.
