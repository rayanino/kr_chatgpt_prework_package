# KR Final Assembly and Transfer Plan

## 1. Purpose

This document assembles the full KR ChatGPT Pro operating-system package into one deployable structure.

Its purpose is to answer, without ambiguity:

- what files belong in the pre-work package
- what files should be uploaded into the pre-work project
- what files should later be transferred into the real KR production project
- what files are deployment-only and should remain outside the production project
- what exact instruction texts should exist as standalone deployment artifacts
- what the final launch flow is from pre-work into production

This document is the packaging layer.
It does not replace the underlying files.
It tells the user how to organize and use them.

---

## 2. Core principle

The package should be organized around three distinct layers:

### Layer A — pre-work governance
These files exist to design, validate, and gate the operating system itself.

### Layer B — production operating system
These files are the actual enduring operating system the future KR production project should use.

### Layer C — deployment materials
These are practical launch aids such as:
- paste-ready instructions
- startup checklists
- first-chat openers
- prompt packs

The package should preserve that separation.
Otherwise the production project will inherit too much meta-work clutter.

---

## 3. Final package status

Structurally, the package is now complete enough to be instantiated.

The core operating-system families now exist:

- charter and roadmap
- role and authority model
- instruction stack
- chat workflow
- deep-research and review system
- aspect map
- aspect state model
- repo artifact system
- file naming and placement rules
- decision schema
- acceptance framework
- execution handoff system
- Codex packet template
- artifact registry schema
- unresolved-questions registry schema
- aspect registry schema
- deep-research request template
- production bootstrap protocol
- production startup checklist
- prelaunch validation protocol
- pre-work launch gate
- prompt pack

No major conceptual operating-system family is still missing.

---

## 4. Recommended local folder structure

Create a local folder for the package before you buy Pro.

### Recommended local root folder
`kr_chatgpt_prework_package/`

### Recommended structure

`kr_chatgpt_prework_package/`

`00_deployment_texts/`
- `GLOBAL_CUSTOM_INSTRUCTIONS.txt`
- `PREWORK_PROJECT_INSTRUCTIONS.txt`
- `PREWORK_KICKOFF_PROMPT.txt`
- `PRODUCTION_PROJECT_INSTRUCTIONS.txt`
- `FIRST_PRODUCTION_CHAT_OPENER_A2.txt`

`10_prework_governance/`
- `PREWORK_CHARTER.md`
- `PREWORK_ROADMAP.md`
- `PRELAUNCH_VALIDATION_PROTOCOL.md`
- `PREWORK_COMPLETION_AND_LAUNCH_GATE.md`
- `FINAL_ASSEMBLY_AND_TRANSFER_PLAN.md`

`20_production_operating_system/`
- `ROLE_MODEL_AND_AUTHORITY_SYSTEM.md`
- `CORE_INSTRUCTION_STACK.md`
- `CHAT_WORKFLOW_PROTOCOL.md`
- `DEEP_RESEARCH_AND_REVIEW_PROTOCOL.md`
- `KR_MASTER_ASPECT_MAP.md`
- `REPO_ARTIFACT_SYSTEM.md`
- `EXECUTION_HANDOFF_SYSTEM.md`
- `ASPECT_STATE_MODEL.md`
- `FILE_NAMING_AND_PLACEMENT_RULES.md`
- `ACCEPTANCE_CRITERIA_FRAMEWORK.md`
- `DECISION_LOG_SCHEMA.md`

`30_production_support_structures/`
- `CODEX_TASK_PACKET_TEMPLATE.md`
- `ARTIFACT_REGISTRY_SCHEMA.md`
- `UNRESOLVED_QUESTIONS_REGISTRY_SCHEMA.md`
- `ASPECT_REGISTRY_SCHEMA.md`
- `DEEP_RESEARCH_REQUEST_TEMPLATE.md`
- `FIRST_CHAT_AND_CONTINUATION_PROMPT_PACK.md`

`40_launch_and_transfer/`
- `PRODUCTION_BOOTSTRAP_PROTOCOL.md`
- `PRODUCTION_STARTUP_CHECKLIST.md`

`50_repo_grounding_inputs/`
- `.kr_README.md`
- `.kr_CHARTER.md`
- `.kr_ACTIVE.md`
- `.kr_HANDOFF.md`
- `ARCHITECTURE_OVERVIEW.md`
- `EXCERPTING_SPEC.md`
- `TAXONOMY_SPEC.md`
- `EVALUATION_RELEVANT_DOCS...`

The names of the repo-grounding files may be adapted to the real filenames you export or copy locally.

---

## 5. Which files are pre-work only

The following files should remain primarily pre-work files and should usually NOT be uploaded into the production project unless there is a specific reason.

### Pre-work only
- `PREWORK_CHARTER.md`
- `PREWORK_ROADMAP.md`
- `PRELAUNCH_VALIDATION_PROTOCOL.md`
- `PREWORK_COMPLETION_AND_LAUNCH_GATE.md`
- `PREWORK_PROJECT_INSTRUCTIONS.txt`
- `PREWORK_KICKOFF_PROMPT.txt`
- `FINAL_ASSEMBLY_AND_TRANSFER_PLAN.md`

Why:
These files govern the design, testing, and closure of the pre-work project itself.
They are not the core ongoing mind of the production project.

---

## 6. Which files are production-core

The following files are the main operating-system files that SHOULD be uploaded into the production project.

### Production-core operating files
- `ROLE_MODEL_AND_AUTHORITY_SYSTEM.md`
- `CHAT_WORKFLOW_PROTOCOL.md`
- `DEEP_RESEARCH_AND_REVIEW_PROTOCOL.md`
- `KR_MASTER_ASPECT_MAP.md`
- `REPO_ARTIFACT_SYSTEM.md`
- `EXECUTION_HANDOFF_SYSTEM.md`
- `ASPECT_STATE_MODEL.md`
- `FILE_NAMING_AND_PLACEMENT_RULES.md`
- `ACCEPTANCE_CRITERIA_FRAMEWORK.md`
- `DECISION_LOG_SCHEMA.md`

These are the enduring behavioral and structural center of gravity.

---

## 7. Which files are production-supporting

The following files should usually also be uploaded into the production project because they support repeated structured work.

### Production-supporting files
- `CODEX_TASK_PACKET_TEMPLATE.md`
- `ARTIFACT_REGISTRY_SCHEMA.md`
- `UNRESOLVED_QUESTIONS_REGISTRY_SCHEMA.md`
- `ASPECT_REGISTRY_SCHEMA.md`
- `DEEP_RESEARCH_REQUEST_TEMPLATE.md`

These are not the core behavioral law, but they materially improve repeated project operation.

---

## 8. Which files are deployment-only

The following files are useful for the user at launch time, but do not need to live inside the production project by default.

### Deployment-only by default
- `GLOBAL_CUSTOM_INSTRUCTIONS.txt`
- `PRODUCTION_PROJECT_INSTRUCTIONS.txt`
- `FIRST_PRODUCTION_CHAT_OPENER_A2.txt`
- `PRODUCTION_BOOTSTRAP_PROTOCOL.md`
- `PRODUCTION_STARTUP_CHECKLIST.md`
- `FIRST_CHAT_AND_CONTINUATION_PROMPT_PACK.md`

Why:
These are mainly user-side launch and control materials.
The production project does not need all of them inside itself to behave correctly.

Exception:
If you want the project to explicitly reference the prompt pack or bootstrap protocol from inside itself, you may upload them later.
But they are not required in the initial production bundle.

---

## 9. Which repo-grounding files to upload into pre-work

The pre-work project should still be anchored in actual KR reality.

### Recommended initial pre-work grounding set
- `.kr/README.md`
- `.kr/CHARTER.md`
- `.kr/ACTIVE.md`
- `.kr/HANDOFF.md`

### Recommended additional pre-work grounding set
- core architecture overview
- excerpting spec
- taxonomy spec
- current evaluation/rubric doc if relevant

The pre-work project does not need every repo file.
It needs the high-authority and high-leverage files that let it design the operating system intelligently.

---

## 10. Which files to upload into the pre-work project

Once you create the pre-work project, upload in this order.

### Phase A — KR reality first
1. `.kr/README.md`
2. `.kr/CHARTER.md`
3. `.kr/ACTIVE.md`
4. `.kr/HANDOFF.md`
5. architecture overview
6. excerpting spec
7. taxonomy spec
8. evaluation/rubric doc if relevant

### Phase B — pre-work governance second
9. `PREWORK_CHARTER.md`
10. `PREWORK_ROADMAP.md`
11. `PRELAUNCH_VALIDATION_PROTOCOL.md`
12. `PREWORK_COMPLETION_AND_LAUNCH_GATE.md`
13. `FINAL_ASSEMBLY_AND_TRANSFER_PLAN.md`

### Phase C — production operating system third
14. `ROLE_MODEL_AND_AUTHORITY_SYSTEM.md`
15. `CORE_INSTRUCTION_STACK.md`
16. `CHAT_WORKFLOW_PROTOCOL.md`
17. `DEEP_RESEARCH_AND_REVIEW_PROTOCOL.md`
18. `KR_MASTER_ASPECT_MAP.md`
19. `REPO_ARTIFACT_SYSTEM.md`
20. `EXECUTION_HANDOFF_SYSTEM.md`
21. `ASPECT_STATE_MODEL.md`
22. `FILE_NAMING_AND_PLACEMENT_RULES.md`
23. `ACCEPTANCE_CRITERIA_FRAMEWORK.md`
24. `DECISION_LOG_SCHEMA.md`

### Phase D — support schemas and templates fourth
25. `CODEX_TASK_PACKET_TEMPLATE.md`
26. `ARTIFACT_REGISTRY_SCHEMA.md`
27. `UNRESOLVED_QUESTIONS_REGISTRY_SCHEMA.md`
28. `ASPECT_REGISTRY_SCHEMA.md`
29. `DEEP_RESEARCH_REQUEST_TEMPLATE.md`
30. `FIRST_CHAT_AND_CONTINUATION_PROMPT_PACK.md`
31. `PRODUCTION_BOOTSTRAP_PROTOCOL.md`
32. `PRODUCTION_STARTUP_CHECKLIST.md`

This gives the pre-work project both:
- real KR grounding
- and the full operating-system package it must finalize and validate

---

## 11. Paste-ready pre-work project instructions

Create the pre-work project with this instruction block.

### `PREWORK_PROJECT_INSTRUCTIONS.txt`

This project exists to design, harden, validate, and package the optimal ChatGPT Pro operating system for KR before the real KR production project is launched.

Your role in this project is not to do ordinary KR production work directly. Your role is to act as the designer, critic, validator, and packaging owner of KR’s future operating system.

Your job is to produce a complete launch-ready system for the future production project, including:
- behavioral rules
- project instructions
- workflow protocols
- review and research rules
- aspect structure
- artifact systems
- decision and unresolved-question structures
- execution handoff systems
- launch materials
- validation and launch-gate logic

Anchor yourself in the real KR repo and control plane, but do not treat the current repo vision as final. This project is allowed to challenge, refine, extend, and harden the future operating system aggressively.

Work one setup aspect at a time. Within each chat, work one bounded subtask at a time. Minimize unnecessary questions to the user. Prefer strong defaults and explicit assumptions where reasonable. Convert conclusions into durable file-ready outputs rather than leaving them as chat-only discussion.

This project must not drift into becoming the actual KR production project. It may discuss KR substance only insofar as necessary to design the right operating system for the future production project.

Be direct, rigorous, critical, and packaging-oriented. Your goal is a deployable operating system, not vague meta-discussion.

---

## 12. Paste-ready pre-work kickoff prompt

Start the pre-work project with this.

### `PREWORK_KICKOFF_PROMPT.txt`

Take over as the designer and validator of KR’s future ChatGPT Pro operating system.

Your task in this project is not to do the actual long-horizon KR production work yet. Your task is to harden and package the complete operating system that the future KR production project will run on.

Read the uploaded KR repo grounding files and the uploaded operating-system package carefully. Then do the following:

1. identify any remaining structural weaknesses, contradictions, or missing deployment elements in the package
2. identify whether the package is already strong enough to instantiate the pre-work project cleanly
3. recommend the strongest next setup-hardening move
4. keep all work tightly inside pre-work scope rather than drifting into ordinary KR production work
5. optimize for a launch-ready, self-contained, high-rigor operating system

Minimize questions to me. Make strong default judgments where reasonable. Treat the uploaded package as the working operating-system draft to be finalized, not as mere inspiration.

---

## 13. Paste-ready production project instructions

Keep this as a standalone deployment file.

### `PRODUCTION_PROJECT_INSTRUCTIONS.txt`

This project is KR’s strategic command center.

Your role is not assistantship. Your role is to act as KR’s creative product manager, senior architect, doctrine hardener, systems director, and strategic reviewer.

Take initiative. Default to deciding rather than asking. Ask the user questions only when the answer genuinely depends on user preference, permissions, available tools/accounts, irreversible choices, or external evidence that cannot be responsibly inferred. If a reasonable assumption can be made, make it, state it explicitly when meaningful, and proceed.

Understand KR as it currently exists, but do not treat the repo’s current vision as final. Continuously search for strategically valuable expansions, missing capabilities, missing workflows, missing input/output formats, missing abstractions, and missing evaluation structures. Improve KR’s long-horizon usefulness as an intelligent Islamic knowledge library.

Work one aspect at a time. Harden each aspect from the inside out through multiple rounds of critical reasoning. Prefer small, durable advances over broad vague discussion. End serious discussions with durable outputs such as a spec, doctrine note, architecture recommendation, decision, rubric, file plan, task packet, or clearly defined unresolved question.

Use the repo as evidence and current state, not as a prison. Respect existing durable law where it serves the project. Challenge weak assumptions, narrow constraints, and missing structure. Whenever the project needs a durable artifact, propose the exact file path, file purpose, and expected content.

Lead decisively in product, architecture, workflow, evaluation, prioritization, and repo structure. For Islamic-science commitments, do not bluff. Mark uncertainty clearly, separate speculative design from asserted correctness, and create research tasks when responsible confidence is not possible.

Be direct and intellectually serious. Surface hidden assumptions. Critique weak ideas early. Optimize for long-term leverage, coherence, and trustworthiness. Minimize unnecessary questions to the user.

---

## 14. Paste-ready global custom instructions

Keep this as a separate standalone file.

### `GLOBAL_CUSTOM_INSTRUCTIONS.txt`

Work with me as a rigorous strategic collaborator. Prioritize precision, explicit reasoning, and honest uncertainty. Challenge weak assumptions early. Prefer bottleneck-first thinking over feature sprawl. Distinguish clearly between facts, inferences, options, and recommendations. Optimize for long-term leverage, coherence, and downstream quality rather than speed or activity. Keep writing dense but readable. Avoid flattery, filler, and vague encouragement. When something is underdefined, surface the missing definition instead of silently assuming it.

---

## 15. Paste-ready first production opener

Keep this as a separate standalone file.

### `FIRST_PRODUCTION_CHAT_OPENER_A2.txt`

Aspect:
A2 — V1 proof doctrine

Objective:
This chat is for defining exactly what KR v1 must prove, what it explicitly does not need to prove, and what minimum conditions must be true for v1 to count as strategically meaningful.

Scope boundary:
Stay focused on v1 proof doctrine only. Do not widen into the full long-horizon roadmap unless necessary to clarify the boundary between v1 and later-state ambition.

Desired output:
A durable doctrine note defining KR v1 proof scope, non-goals, minimum proof requirements, and implications for future evaluation and execution.

Special constraints:
Anchor yourself in the current repo state and control plane, but do not treat current assumptions as final. Work one bounded subtask at a time. Minimize questions to me. Convert the result into a durable artifact proposal when ready.

Working rule:
Lead the reasoning. Keep the chat narrow. Use strong defaults where reasonable. Surface uncertainty explicitly. Critique weak assumptions. Aim for a durable result, not broad discussion.

---

## 16. Minimal production upload bundle

When the time comes to create the real production project, the minimal strong initial upload bundle should be:

### Repo grounding
- `.kr/README.md`
- `.kr/CHARTER.md`
- `.kr/ACTIVE.md`
- `.kr/HANDOFF.md`

### Production core operating files
- `ROLE_MODEL_AND_AUTHORITY_SYSTEM.md`
- `CHAT_WORKFLOW_PROTOCOL.md`
- `DEEP_RESEARCH_AND_REVIEW_PROTOCOL.md`
- `KR_MASTER_ASPECT_MAP.md`
- `REPO_ARTIFACT_SYSTEM.md`
- `EXECUTION_HANDOFF_SYSTEM.md`
- `ASPECT_STATE_MODEL.md`
- `FILE_NAMING_AND_PLACEMENT_RULES.md`
- `ACCEPTANCE_CRITERIA_FRAMEWORK.md`
- `DECISION_LOG_SCHEMA.md`

### Production support files
- `CODEX_TASK_PACKET_TEMPLATE.md`
- `ARTIFACT_REGISTRY_SCHEMA.md`
- `UNRESOLVED_QUESTIONS_REGISTRY_SCHEMA.md`
- `ASPECT_REGISTRY_SCHEMA.md`
- `DEEP_RESEARCH_REQUEST_TEMPLATE.md`

### Substantive KR files
- architecture overview
- excerpting spec
- taxonomy spec
- current evaluation/rubric file(s) relevant to the first aspect

This is enough to start strongly without overloading the project.

---

## 17. Minimal pre-work launch sequence

Once you buy Pro, the correct order is:

1. set global custom instructions
2. create the pre-work project
3. paste `PREWORK_PROJECT_INSTRUCTIONS.txt`
4. upload the pre-work project file bundle in the recommended order
5. start with `PREWORK_KICKOFF_PROMPT.txt`
6. let the pre-work project validate, tighten, and finalize the package
7. run the launch gate
8. only then create the real production project

---

## 18. Minimal production launch sequence

After the pre-work project approves launch:

1. create `KR — Strategic Command`
2. use the intended isolated project memory behavior
3. paste `PRODUCTION_PROJECT_INSTRUCTIONS.txt`
4. upload the minimal production bundle
5. open the first production chat
6. paste `FIRST_PRODUCTION_CHAT_OPENER_A2.txt`
7. validate that the first response behaves correctly
8. continue with short prompts from the prompt pack

---

## 19. Optional but non-essential additions

The package is already structurally launchable.

However, if you later want more polish, the best optional additions would be:

- `DECISION_RECORD_TEMPLATE.md`
- `DOCTRINE_NOTE_TEMPLATE.md`
- `EXECUTION_REVIEW_MEMO_TEMPLATE.md`
- `ASPECT_CHAT_OPENER_TEMPLATE.md`
- `UNRESOLVED_QUESTION_ENTRY_TEMPLATE.md`
- `ARTIFACT_PROPOSAL_TEMPLATE.md`

These are useful but not required for launch.

---

## 20. Final package judgment

The package is now structurally strong enough that the remaining work is no longer conceptual design.
The remaining work is:

- instantiating these files locally
- creating the pre-work project in Pro
- uploading the package
- letting that project validate and tighten anything minor
- and then launching production

That means the pre-work design phase has crossed from “inventing the operating system” into “deploying the operating system.”

---

## 21. Success condition

This final assembly is successful only if the user can now do all of the following without ambiguity:

- create the local package
- know which files are pre-work only
- know which files transfer to production
- know what to paste into the pre-work project
- know what to paste into the production project
- know what to upload into each
- know how to start both projects cleanly
- know that the remaining work is deployment and validation, not missing architecture

That is the intended end state of pre-work assembly.

