# KR Chat Workflow Protocol

## 1. Purpose

This document defines how work should happen inside the future KR production project on a chat-by-chat basis.

Its purpose is to ensure that the project operates in a disciplined, high-rigor, low-friction way that supports long-horizon hardening of every important aspect of KR.

The intended working model is:

- one aspect per chat
- one subtask at a time inside the chat
- bounded, deep reasoning at each step
- minimal user micromanagement
- user can often advance the work with simple prompts such as “continue”
- every serious thread should produce durable outputs, not merely conversation

This workflow is designed to maximize:
- depth
- coherence
- reuse of project memory
- quality of reasoning
- quality of outputs
- user leverage
- long-horizon maintainability

---

## 2. Core philosophy

The KR production project should not operate through broad, mixed, multi-aspect conversations.

It should operate through narrow, deep, aspect-specific threads.

This is intentional.

Breadth without strict containment causes:
- drift
- shallow reasoning
- unstable conclusions
- poor artifact quality
- weak handoff into repo structure

The project should therefore prefer:
- focused depth
over
- broad but noisy progress

The user’s preferred control style is also intentional:
- the model should carry the reasoning burden
- the user should not need to intellectually steer each step
- the user should be able to advance work with low-friction prompts
- the model should continue disciplined progress until a real stopping point is reached

---

## 3. Governing workflow law

The governing law of the KR production project is:

### 3.1 One aspect per chat
Each serious chat should focus on exactly one aspect of KR unless a second aspect is inseparable from the first.

### 3.2 One subtask at a time inside the chat
Within the active chat, the model should work on one bounded subtask at a time.

### 3.3 Each subtask should be materially useful
A subtask should not be trivial busywork.
It should move the aspect toward a more hardened, clearer, more decision-ready state.

### 3.4 Each chat should remain narrow
The model should resist introducing new side topics unless they are required to complete the current aspect.

### 3.5 Each chat should seek durable output
A serious chat should end with a decision, doctrine note, protocol, file proposal, rubric, map, unresolved-question statement, or other durable artifact.

---

## 4. Chat-level unit of work

A chat is not merely a conversation container.

A chat is the primary hardening workspace for one aspect.

Each chat should therefore have:

- one named aspect
- one current objective
- one current subtask
- one local boundary
- one intended form of durable output
- one current state in the aspect-hardening process

This means that every aspect chat should be understandable in terms of:
- what aspect it is hardening
- what the current local goal is
- what remains unresolved
- what output it is trying to produce

---

## 5. Allowed chat types

The production project should use a small number of deliberate chat types.

### 5.1 Aspect-hardening chat
Purpose:
- harden one major KR aspect deeply over time

Examples:
- input format strategy
- taxonomy usefulness criteria
- excerpting quality doctrine
- synthesis boundaries
- provenance and attribution model

This is the default chat type.

### 5.2 Decision-resolution chat
Purpose:
- resolve one major unresolved question that emerged from an aspect-hardening chat

Example:
- should PDF ingestion be a v1 requirement or a later-state expansion?

This chat type is narrower and more decision-focused.

### 5.3 Protocol-design chat
Purpose:
- design one reusable project protocol or system artifact

Example:
- review protocol
- artifact naming convention
- Codex task-packet format

### 5.4 Validation chat
Purpose:
- stress-test or critique an already drafted position, protocol, or artifact

Example:
- attack the current input-format doctrine for hidden weaknesses

### 5.5 Conversion chat
Purpose:
- convert already hardened conclusions into repo artifacts, file trees, templates, registries, or task packets

This chat type should be used when strategic thinking already exists and now needs durable formalization.

---

## 6. Default lifecycle of an aspect chat

Each aspect chat should move through the following default lifecycle.

### Phase 1 — aspect lock
The chat explicitly identifies:
- the aspect
- the objective
- the local boundary
- the intended output

### Phase 2 — internal mapping
The model identifies:
- what the aspect includes
- what it excludes
- what the main questions are
- what likely bottlenecks or hidden assumptions exist

### Phase 3 — bounded subtask progression
The model works through one bounded subtask at a time.

Examples:
- define the problem
- compare candidate directions
- identify failure modes
- separate v1 from later-state ambitions
- identify missing repo artifacts
- define evaluation criteria

### Phase 4 — hardening
The model critiques its own emerging conclusion, pressure-tests it, identifies weak points, and strengthens the result.

### Phase 5 — conversion
The model converts the hardened conclusion into durable outputs.

### Phase 6 — local closure
The chat ends by stating one of:
- the aspect is partially hardened and the next subtask is X
- the aspect is provisionally hardened
- the aspect requires deep research before continuing
- the aspect requires user input on a true blocker
- the aspect should branch into a separate dedicated chat for a sub-question

---

## 7. Chat opener requirements

Each serious new chat should open with an aspect-specific prompt.

The opener should define:
- the aspect name
- the objective of this chat
- the local scope boundary
- the expected output form
- any constraints or relevant repo context

The chat opener should be narrow.

It should not say:
- “let’s discuss KR broadly”
- “think about everything related to this topic”
- “review the whole project again”

It should say something more like:
- “This chat is for hardening KR’s input-format strategy. The goal is to determine the right long-horizon format roadmap, distinguish v1 from later-state support, identify the strategic role of PDF support, and propose any doctrine files that should exist.”

That level of specificity is the target.

---

## 8. Scope-lock rule

Once a chat has opened and the aspect has been defined, the model should treat the aspect boundary as binding unless a justified reason appears to widen or split it.

The model should not casually pull in adjacent topics.

If an adjacent topic appears, the model should classify it as one of:

### 8.1 In-scope dependency
Necessary to continue the current aspect.
Remain in the current chat.

### 8.2 Important but separable
Relevant, but deserves its own future chat.
Record it and continue the current chat.

### 8.3 Noise or distraction
Not needed for the current hardening goal.
Exclude it.

This rule is critical for maintaining deep focus.

---

## 9. Subtask progression rule

Inside a chat, the model must not advance in large uncontrolled leaps.

It should move one bounded subtask at a time.

Each subtask should satisfy all of the following:
- it has a clear purpose
- it is small enough to reason about deeply
- it materially advances the aspect
- it does not silently change the aspect boundary
- it yields a useful intermediate result

A good subtask is something like:
- define the real problem this aspect solves
- separate v1 and long-horizon goals
- compare three candidate representations
- identify the strongest failure modes
- determine what file should exist for this doctrine
- test whether the current recommendation survives edge cases

A bad subtask is something vague like:
- think more about this
- explore everything related to it
- brainstorm generally

---

## 10. “Continue” protocol

The production project should be explicitly optimized for low-friction continuation prompts such as:
- continue
- go deeper
- harden this further
- critique this
- convert this into a file
- test edge cases
- compare against alternatives
- what is still weak here

The prompt “continue” should have a stable meaning.

### 10.1 Meaning of “continue”
When the user says “continue,” the model should:
1. preserve the active aspect boundary
2. preserve the current local objective
3. infer the best next bounded subtask
4. continue working without asking unnecessary questions
5. maintain continuity with the current state of the chat
6. aim toward a more hardened output

### 10.2 What “continue” should not do
It should not:
- restart the whole analysis
- widen the aspect unnecessarily
- switch to a different aspect
- ask broad exploratory questions by default
- produce filler recap unless needed for precision
- jump to a conversion task before the thinking is ready

### 10.3 If the next step is ambiguous
If there are multiple plausible next subtasks and one is clearly strongest, choose it.
If there are multiple materially different next subtasks with no clearly dominant one, the model should:
- name the decision point briefly
- recommend the strongest next step
- proceed if the ambiguity is low-regret
- escalate only if the branch materially changes the direction

The default is still forward motion.

---

## 11. Deepening prompts protocol

The following user prompts should have stable operational meanings.

### “go deeper”
Increase conceptual depth on the current subtask without widening scope.

### “harden this”
Move into critique, edge-case testing, weak-point detection, or strengthening.

### “critique this”
Attack the current recommendation or output adversarially.

### “test edge cases”
Probe unusual cases, failure modes, and boundary conditions.

### “convert this into a file”
Turn the current conclusion into a concrete repo artifact proposal or file draft.

### “make this operational”
Translate current reasoning into a protocol, checklist, template, or task packet.

### “continue”
Advance to the best next bounded subtask while staying within the active chat’s aspect.

The project should behave consistently enough that the user can rely on these prompts with minimal explanation.

---

## 12. Chat closure rule

A serious chat should not drift indefinitely.

A chat reaches a local stopping point when one of the following becomes true:

### 12.1 Durable output produced
The current local objective has been converted into a useful durable artifact.

### 12.2 Deeper work now belongs in a new dedicated chat
A sub-question has become large enough to deserve its own aspect or decision-resolution chat.

### 12.3 External evidence is required
The next meaningful step depends on research, verification, or evidence not yet obtained.

### 12.4 User input is truly required
A real blocker exists that depends on user preference, permissions, or approval.

### 12.5 Diminishing returns within the current chat
The chat has hardened the current local target sufficiently and the next meaningful move is different enough to warrant a new thread.

When closing, the model should state:
- what was achieved
- what remains unresolved
- whether the aspect is partially hardened, provisionally hardened, or still open
- what the best next move is

---

## 13. When to open a new chat

A new chat should be opened when one of the following is true:

### 13.1 New aspect
The topic belongs to a different aspect of KR.

### 13.2 Sub-question expansion
A sub-question has become large enough that continuing in the current chat would dilute focus.

### 13.3 Different work mode needed
The next step is not more hardening but a different mode such as validation, protocol design, or conversion.

### 13.4 Context contamination risk
The current chat has accumulated enough detail that clarity or precision may degrade.

### 13.5 New durable output target
The next step is aimed at a distinctly different artifact type than the current one.

A new chat should not be opened frivolously, but neither should old chats be stretched beyond clarity.

---

## 14. When to stay in the same chat

The model should stay in the same chat when:
- the next step is a direct continuation of the same aspect
- the current sub-question is still subordinate to the same aspect
- the durable output target is still the same general artifact
- additional hardening would benefit from continuity
- the current chat remains clear and bounded

The default is:
- preserve continuity when the aspect is still the same
- branch only when focus would improve materially

---

## 15. Aspect-state updates inside a chat

Each aspect chat should implicitly or explicitly maintain a local state.

Suggested states:

- scoping
- mapping
- comparing options
- drafting direction
- critiquing
- hardening
- converting to artifacts
- waiting on evidence
- waiting on user decision
- locally complete

The model does not need to announce the state every turn, but it should reason as though the chat has a current state.

This helps “continue” function intelligently.

---

## 16. Durable-output rule

A serious chat should aim to produce one or more durable outputs such as:

- doctrine note
- strategy memo
- architecture recommendation
- decision record
- rubric
- aspect map
- protocol
- file proposal
- file tree
- checklist
- YAML schema proposal
- task packet
- unresolved-question statement

Reasoning alone is not enough.

A chat that repeatedly generates insight without converting it into durable structure is underperforming.

---

## 17. Conversion threshold rule

Not every intermediate thought deserves immediate conversion into a file.

The model should convert when one or more of the following are true:
- the concept is strategically important
- the concept is likely to be reused
- the concept needs to guide future chats
- the concept affects repo structure or implementation
- the concept would be costly to lose
- the concept has become stable enough to formalize

Until then, intermediate reasoning may remain in working form.

This avoids premature document sprawl.

---

## 18. User-burden minimization rule

The chat workflow should minimize the user’s burden.

This means:
- do not ask for permission to continue ordinary reasoning
- do not ask the user what subtask to do next unless truly necessary
- do not require the user to remember the protocol
- do not require elaborate steering messages
- allow short prompts like “continue” to work reliably
- surface true blocker questions only when needed

The project should feel like a strong internal engine, not a tool that must be manually driven.

---

## 19. Deep-research handoff rule

If the current chat reaches a point where external evidence is needed, the model should not vaguely say “we need research.”

It should define:
- the exact question that must be researched
- why the current reasoning is insufficient
- what kind of evidence would resolve the uncertainty
- whether the current chat should pause or continue on another subtask first

This keeps the workflow disciplined.

The full deep-research policy belongs in a separate protocol document, but this workflow document requires that evidence needs be identified precisely.

---

## 20. Anti-failure rules

To prevent workflow collapse, the model must avoid the following failures.

### 20.1 Broadening failure
The chat expands into multiple aspects and loses depth.

### 20.2 Micro-fragmentation failure
Every small thought becomes a new chat, destroying continuity.

### 20.3 Restart failure
Each “continue” causes the model to re-explain rather than advance.

### 20.4 Filler failure
The model produces long but low-progress text instead of hardening the aspect.

### 20.5 No-conversion failure
The chat produces insight but never durable outputs.

### 20.6 Silent-scope-shift failure
The chat subtly becomes about a different aspect without declaring it.

### 20.7 Endless-hardening failure
The chat keeps refining forever without recognizing a local stopping point.

These are all forbidden workflow patterns.

---

## 21. Recommended opener template for new chats

The following structure should be used when starting a serious new aspect chat:

### Aspect chat opener template

Aspect:
[Name of the aspect]

Objective:
[What this chat must determine, harden, or produce]

Scope boundary:
[What is in scope and what is out of scope]

Desired output:
[Doctrine note / recommendation / protocol / file plan / decision / etc.]

Special constraints:
[Any relevant repo facts, v1 constraints, evidence constraints, or project conditions]

Working rule:
Work one bounded subtask at a time. Keep the chat narrowly focused on this aspect. Minimize questions to the user. Use strong defaults where reasonable. Convert important conclusions into durable outputs.

---

## 22. Recommended closure template for serious chats

When a chat reaches a local stopping point, it should close with a structure like:

### Chat closure template

Current aspect:
[Aspect name]

What was achieved:
[Summary of the hardened progress made]

Durable outputs produced:
[List]

What remains unresolved:
[List]

Current aspect state:
[Partially hardened / provisionally hardened / blocked / needs research / locally complete]

Best next move:
[Exact next step or next chat]

This helps maintain clean project continuity.

---

## 23. Success condition

The chat workflow protocol is successful only if the future KR production project behaves like this:

- each chat has one clear aspect
- each turn advances one bounded subtask
- the user can mostly steer with short prompts
- the model carries the reasoning burden
- chats remain narrow and deep
- important conclusions become durable artifacts
- new chats are opened when strategically appropriate
- the project remains coherent over many chats
- every aspect can eventually be hardened to a high standard through repeated disciplined passes

That is the intended operating rhythm.
