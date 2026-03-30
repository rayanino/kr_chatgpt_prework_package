# KR First-Chat and Continuation Prompt Pack

## 1. Purpose

This document defines a compact, reusable prompt pack for the future KR production project.

Its purpose is to let the user operate the production project with low friction while preserving the intended working style:
- one aspect per chat
- one bounded subtask at a time
- strong model initiative
- minimal user micromanagement
- durable outputs rather than vague discussion
- disciplined escalation only when necessary

This pack is not a substitute for the project instructions or protocol files.

It is the user-facing prompt surface that activates those systems in practice.

---

## 2. Core principle

The production project should not require the user to repeatedly restate:
- the model’s role
- the project philosophy
- the workflow protocol
- the review expectations
- the artifact behavior

That should already be handled by:
- project instructions
- uploaded operating files
- project memory and context

The prompt pack therefore exists to do something narrower:

- start the right kind of chat well
- advance the current thread cleanly
- request a specific work mode when needed
- trigger critique, conversion, research, or execution preparation cleanly

The prompts should be:
- short
- stable
- reusable
- high-signal
- low-burden

---

## 3. Prompt pack philosophy

A good prompt in this system should usually do one of four things:

### 3.1 Open a new aspect thread
Tell the project what aspect this chat is for and what it must produce.

### 3.2 Advance the current thread
Let the project continue bounded hardening without re-steering everything.

### 3.3 Change work mode without changing aspect
Tell the project to shift from:
- mapping
to
- critique,
or from
- doctrine
to
- artifact conversion,
or from
- reasoning
to
- execution preparation

### 3.4 Escalate into a support process
Tell the project to prepare:
- a research request
- a Codex packet
- an artifact proposal
- a review memo
- a decision record draft

That is the function of the pack.

---

## 4. Use rules

### Rule 1
Use one serious aspect opener per new aspect chat.

### Rule 2
Once a chat is live, prefer short continuation prompts.

### Rule 3
Do not use a continuation prompt to silently switch aspects.

### Rule 4
If the aspect changes materially, open a new chat.

### Rule 5
Use explicit mode-shift prompts when you want:
- critique
- artifact conversion
- research prep
- execution handoff
- validation

### Rule 6
Do not overload prompts with unnecessary restatement if the project already has the operating system installed.

The prompts should trust the environment you built.

---

## 5. Prompt families

This pack contains six prompt families:

1. New aspect chat openers
2. Continuation prompts
3. Hardening and critique prompts
4. Artifact conversion prompts
5. Research-preparation prompts
6. Execution-preparation prompts

There is also a final section for recovery prompts if a thread starts behaving badly.

---

## 6. Family 1 — New aspect chat openers

These prompts are for starting a new serious production chat.

Each opener should define:
- the aspect
- the objective
- the boundary
- the desired output

### 6.1 General aspect opener template

Aspect:
[Aspect ID and name]

Objective:
[What this chat must determine, harden, or produce]

Scope boundary:
[What is in scope and what is out of scope]

Desired output:
[Doctrine note / recommendation / protocol / file plan / decision / etc.]

Special constraints:
[Any relevant repo facts, v1 constraints, evidence constraints, or project conditions]

Working rule:
Work one bounded subtask at a time. Keep this chat narrowly focused on this aspect. Minimize questions to me. Use strong defaults where reasonable. Convert important conclusions into durable outputs when ready.

---

### 6.2 Recommended first production chat opener

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

### 6.3 Alternative opener for input-format strategy

Aspect:
A8 — Input-format strategy

Objective:
Determine the right strategic direction for KR’s source-format support, including how to think about Shamela dependence, PDF support, and format expansion over time.

Scope boundary:
Focus on strategic format doctrine only. Do not drift into implementation details unless needed to expose a real strategic consequence.

Desired output:
A durable direction for format support, likely artifact proposals, and the main unresolved questions if full closure is not yet possible.

Special constraints:
Distinguish clearly between v1 urgency and long-horizon necessity. Challenge current repo narrowness where warranted.

Working rule:
Work one bounded subtask at a time. Be decisive, but honest about what still needs evidence.

---

### 6.4 Alternative opener for taxonomy doctrine

Aspect:
A13 — Taxonomy doctrine

Objective:
Define what a strategically useful and trustworthy taxonomy system should mean in KR, and what quality bar taxonomy placement must satisfy to be more than decorative classification.

Scope boundary:
Focus on taxonomy doctrine and usefulness standards. Do not drift into general retrieval UX or synthesis unless necessary to clarify taxonomy’s role.

Desired output:
A durable taxonomy doctrine direction and any resulting doctrine or evaluation artifact proposals.

Special constraints:
Do not bluff on scholarly legitimacy questions. Separate speculative system design from asserted domain truth.

Working rule:
One bounded subtask at a time. Critique weak formulations aggressively.

---

## 7. Family 2 — Continuation prompts

These are the default low-friction prompts for staying inside the current aspect thread.

### 7.1 Continue
```text
Continue.

Meaning:

preserve the current aspect
preserve the current objective
infer the strongest next bounded subtask
keep advancing without asking unnecessary questions

Use when:

the thread is behaving well
you want the project to keep working normally
7.2 Go deeper
Go deeper.

Meaning:

deepen the current subtask
increase conceptual precision
do not broaden scope unnecessarily

Use when:

the current reasoning feels correct but not yet deep enough
7.3 Keep hardening
Keep hardening this.

Meaning:

continue strengthening the current direction
seek stronger robustness, not just more text

Use when:

the thread is already in a productive hardening phase
7.4 Advance to the next strongest subtask
Advance to the next strongest subtask.

Meaning:

move forward deliberately rather than merely elaborating the same subtask

Use when:

you want forward motion but still within the same aspect
8. Family 3 — Hardening and critique prompts

These prompts tell the project to shift into stronger stress-testing mode without changing aspect.

8.1 Critique this
Critique this.

Meaning:

attack the current direction
surface hidden assumptions
identify weaknesses and failure modes

Use when:

you want adversarial pressure on the current result
8.2 Harden this further
Harden this further.

Meaning:

refine the current direction under pressure
move it closer to a doctrine- or execution-worthy state

Use when:

the direction is promising but not yet strong enough
8.3 Test edge cases
Test edge cases.

Meaning:

probe unusual or difficult cases
examine boundary conditions

Use when:

the current direction may fail at the edges
8.4 Compare against the strongest alternative
Compare this against the strongest alternative.

Meaning:

identify the strongest competing path
compare gains, losses, and tradeoffs

Use when:

you suspect the current direction may have won too easily
8.5 Surface what is still weak
Surface what is still weak here.

Meaning:

identify the remaining unresolved weak points without redoing everything

Use when:

you want a sharp weakness scan before moving on
8.6 Tell me what would be required for this to count as hardened
Tell me what would be required for this to count as hardened.

Meaning:

explicitly connect the current state to the hardening standard

Use when:

you want to know what still blocks S7-style maturity
9. Family 4 — Artifact conversion prompts

These prompts tell the project to convert the current reasoning into repo-native structure.

9.1 Convert this into a file
Convert this into a file.

Meaning:

propose the right artifact class
propose path, name, purpose, and structure
do not stop at vague advice

Use when:

the current result is mature enough for durable storage
9.2 Turn this into the exact artifact proposal
Turn this into the exact artifact proposal.

Meaning:

produce the full artifact proposal format
be explicit about why it should exist

Use when:

you want the repo-materialization step clearly defined
9.3 Draft the file content
Draft the file content.

Meaning:

stop at the artifact draft itself
do not reopen the whole strategic discussion unless necessary

Use when:

the artifact decision has already been made and now you want the actual draft
9.4 What artifacts should exist now because of this?
What artifacts should exist now because of this?

Meaning:

identify all durable repo consequences of the current conclusion

Use when:

the discussion probably implies more than one file or registry update
9.5 Update the structural implications
Update the structural implications.

Meaning:

identify impacts on:
doctrines
protocols
registries
decisions
execution readiness

Use when:

you want system-wide conversion implications, not just one file
10. Family 5 — Research-preparation prompts

These prompts tell the project to shift from ordinary hardening into research framing.

10.1 Prepare the deep research request
Prepare the deep research request.

Meaning:

formulate a proper evidence-linked request
state the unknown clearly
define what evidence would help

Use when:

the thread hit a real evidence boundary
10.2 Clarify whether this truly needs deep research
Clarify whether this truly needs deep research.

Meaning:

distinguish between:
internal hardening still needed
real research need
user decision
dependency issue

Use when:

you are not sure whether research is actually justified yet
10.3 Frame the exact unresolved question first
Frame the exact unresolved question first.

Meaning:

sharpen the open issue before triggering research

Use when:

the issue feels evidence-gated but still fuzzy
10.4 If this needs research, tell me exactly what the research must resolve
If this needs research, tell me exactly what the research must resolve.

Meaning:

define the actual evidence boundary and resolution threshold

Use when:

you want sharper research discipline
10.5 Convert this into a research-backed decision path
Convert this into a research-backed decision path.

Meaning:

show:
current internal judgment
what must be researched
what decision will follow from the answer

Use when:

you want to connect unresolvedness to future commitment
11. Family 6 — Execution-preparation prompts

These prompts tell the project to shift from hardening into delegation readiness.

11.1 Prepare the Codex task packet
Prepare the Codex task packet.

Meaning:

produce a bounded execution packet
include scope, constraints, acceptance criteria, discretion rules, and return format

Use when:

the task is execution-ready
11.2 Tell me whether this is ready for Codex
Tell me whether this is ready for Codex.

Meaning:

test execution readiness honestly
do not assume readiness just because the work sounds useful

Use when:

you suspect the task may still be under-hardened
11.3 Split this into execution-ready tasks
Split this into execution-ready tasks.

Meaning:

decompose the current conclusion into bounded packets

Use when:

the direction is clear but too large for one safe handoff
11.4 Define the acceptance criteria for execution
Define the acceptance criteria for execution.

Meaning:

sharpen the review gate before delegation

Use when:

the task is close to ready but still too fuzzy for safe handoff
11.5 Prepare the review memo for returned work
Prepare the review memo for returned work.

Meaning:

define how the future returned work will be judged

Use when:

you want the full execution loop, not just the packet
12. Family 7 — Registry and decision prompts

These prompts help the project maintain its structured memory.

12.1 Should this become a decision record?
Should this become a decision record?

Meaning:

determine whether the current conclusion crossed the threshold into durable commitment
12.2 Draft the decision record
Draft the decision record.

Meaning:

convert the commitment into the decision-log schema
12.3 Update the aspect state
Update the aspect state.

Meaning:

determine the correct current state and what it implies
12.4 Tell me how this changes the aspect registry
Tell me how this changes the aspect registry.

Meaning:

identify state, priority, artifacts, blockers, and next-move changes
12.5 Tell me whether this should enter the unresolved-questions registry
Tell me whether this should enter the unresolved-questions registry.

Meaning:

distinguish between:
unresolved question
decision
working note
local ambiguity
13. Family 8 — Recovery prompts

These are for correcting a thread that starts drifting or behaving badly.

13.1 Re-lock the scope
Re-lock the scope. Stay strictly inside this aspect.

Use when:

the thread is drifting across aspects
13.2 Stop broadening and return to the current subtask
Stop broadening and return to the current subtask.

Use when:

the model is expanding instead of deepening
13.3 Do not ask me broad exploratory questions; make the strongest default move
Do not ask me broad exploratory questions; make the strongest default move.

Use when:

the model becomes too question-heavy
13.4 Give me the exact next bounded move, not a menu
Give me the exact next bounded move, not a menu.

Use when:

the model starts offering too many options without leading
13.5 Convert this from discussion into a durable output
Convert this from discussion into a durable output.

Use when:

the thread is thinking well but not materializing results
14. Recommended default operating rhythm

A strong default rhythm for most chats is:

start with a serious aspect opener
let the model respond
say Continue.
say Go deeper. or Harden this further. when needed
say Critique this. before accepting a major direction
say Convert this into a file. when the result is mature
say Prepare the Codex task packet. or Prepare the deep research request. only when the work genuinely reaches that stage

This rhythm keeps the project deep, narrow, and productive.

15. Example minimal production thread

A typical strong thread might look like this:

User

[pastes first serious aspect opener]

Model

[starts hardening the aspect]

User

Continue.

Model

[advances to the next bounded subtask]

User

Critique this.

Model

[attacks the current direction]

User

Harden this further.

Model

[strengthens the result]

User

Convert this into a file.

Model

[proposes and/or drafts the artifact]

This is the intended low-friction pattern.

16. Anti-failure rules

The user-side prompt discipline should avoid the following failures.

16.1 Broad-reset failure

Using prompts that restart the whole project or aspect repeatedly.

16.2 Hidden-aspect-switch failure

Using a continuation prompt while actually wanting to change aspects.

16.3 Prompt-overloading failure

Trying to force too many work modes in one prompt.

16.4 Micromanagement failure

Over-steering every substep instead of letting the production project do its job.

16.5 No-mode-signal failure

Expecting critique, artifact conversion, or execution prep without signaling the shift.

16.6 Drift-tolerance failure

Allowing a thread to become broad or passive without using recovery prompts.

These failures make the operating system weaker in practice.

17. Success condition

This prompt pack is successful only if the future KR production project can be run with:

one strong opener per new aspect chat
mostly short continuation prompts afterward
minimal user micromanagement
clear work-mode shifts when needed
reliable progress toward durable outputs
clean transition into research, artifact creation, or execution when appropriate

That is the intended control surface.
