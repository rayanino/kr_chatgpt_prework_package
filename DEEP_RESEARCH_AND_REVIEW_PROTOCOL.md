# KR Deep Research and Review-Control Protocol

## 1. Purpose

This document defines how the future KR production project should use:
- internal reasoning
- deep research
- adversarial critique
- multi-pass hardening
- evidence classification
- uncertainty tracking
- decision validation

Its purpose is to ensure that KR uses ChatGPT Pro’s strongest capabilities deliberately and systematically rather than casually.

This protocol exists to solve two opposite risks:

### Risk A — underuse
The model relies too much on internal reasoning when external evidence or serious verification is actually needed.

### Risk B — wasteful overuse
The model invokes deep research or elaborate review flows even when the problem is mainly internal, conceptual, or already sufficiently bounded.

The correct target is:
- maximal value extraction
- disciplined invocation
- explicit evidence boundaries
- repeatable review quality
- honest uncertainty handling

---

## 2. Core principle

Not every question deserves deep research.

Not every decision deserves the same level of review.

But every important KR decision should be passed through the strongest hardening process justified by:
- its strategic importance
- its irreversibility
- its external-fact dependence
- its uncertainty level
- its downstream contamination risk

The future KR production project should therefore operate on a graded hardening model, not a one-size-fits-all model.

---

## 3. High-level hardening model

Every serious question in KR should pass through one or more of the following layers:

### Layer 1 — Internal reasoning
Use structured internal reasoning to map the problem, identify assumptions, compare options, and form a provisional judgment.

### Layer 2 — Internal critique
Attack the provisional judgment from the inside:
- hidden assumptions
- failure modes
- edge cases
- strategic blind spots
- complexity costs
- possible alternatives

### Layer 3 — Deep research
Use external research when the question depends on facts, niche knowledge, current capabilities, domain truth, or evidence that internal reasoning cannot responsibly supply.

### Layer 4 — Evidence synthesis
Integrate research findings into the project’s internal reasoning. Resolve contradictions where possible. Mark unresolved tension where necessary.

### Layer 5 — Final hardening
Stress-test the proposed direction against:
- v1 constraints
- long-horizon goals
- architecture coherence
- integrity requirements
- repo implications
- implementation consequences

### Layer 6 — Durable conversion
Convert the result into a durable artifact:
- doctrine note
- protocol
- file proposal
- rubric
- decision record
- task packet
- unresolved-question record

Not every decision needs all six layers.
But every significant one needs enough layers to become trustworthy.

---

## 4. Decision tier system

The future KR production project should classify important questions into hardening tiers.

### Tier 0 — light
Small local decisions with low strategic weight and low downstream risk.

Examples:
- provisional naming
- local file section ordering
- small formatting defaults

Default treatment:
- internal reasoning only
- explicit assumption if needed
- no deep research unless facts are involved

### Tier 1 — standard
Meaningful project decisions with moderate downstream effect but low irreversibility.

Examples:
- choosing the better structure for a doctrine note
- deciding how to frame a specific aspect
- choosing between two low-regret workflow variants

Default treatment:
- internal reasoning
- internal critique
- durable output

Deep research only if the decision depends on external facts.

### Tier 2 — major
Strategically important decisions that shape project direction, architecture, file systems, workflow, or evaluation logic.

Examples:
- deciding how KR should handle input-format expansion
- defining the role of synthesis
- defining a major evaluation doctrine
- defining a new artifact class that many future tasks will depend on

Default treatment:
- internal reasoning
- internal critique
- deep research if relevant
- evidence synthesis
- final hardening
- durable conversion

### Tier 3 — critical
High-stakes, hard-to-reverse, externally sensitive, or domain-sensitive decisions that could meaningfully distort KR if handled badly.

Examples:
- decisions with deep Islamic-science implications
- decisions that constrain the long-horizon architecture materially
- decisions that commit the project to expensive or hard-to-reverse paths
- decisions that shape trustworthiness or scholarly legitimacy centrally

Default treatment:
- strong internal reasoning
- adversarial critique
- deep research or evidence gathering when needed
- explicit uncertainty labeling
- explicit escalation if appropriate
- durable record of the reasoning and constraints

No Tier 3 decision should be treated casually.

---

## 5. Deep-research trigger law

Deep research should be used whenever the answer materially depends on knowledge that cannot be responsibly supplied from internal reasoning alone.

Deep research is triggered when one or more of the following are true:

### 5.1 External-fact dependency
The question depends on facts about:
- current tools or platforms
- current file formats or standards
- available ecosystems
- current technical capabilities
- external services
- current product constraints
- public resources or corpora

### 5.2 Niche-knowledge dependency
The question depends on specialized or non-obvious knowledge that internal reasoning alone may mis-handle.

### 5.3 Scholarly-truth dependency
The question depends on domain truth, legitimacy, classification, or correctness that should not be guessed.

### 5.4 Comparative-landscape dependency
The question is materially strengthened by understanding how similar systems, tools, or methods work in the world.

### 5.5 High-contamination-risk dependency
A wrong answer would meaningfully distort downstream design if assumed without verification.

### 5.6 High-uncertainty dependency
Internal reasoning yields several plausible paths and the tie depends on external evidence rather than pure design judgment.

### 5.7 Evidence-demanding challenge
A proposed direction sounds plausible but should not be accepted without stronger evidence.

---

## 6. Non-trigger rule

Deep research should NOT be triggered merely because:
- the question feels important
- the user wants a thorough answer
- the model wants to look sophisticated
- the issue is purely about internal operating design
- the question can be adequately answered through disciplined internal reasoning
- the next step is simply clearer conceptual decomposition

Examples where deep research is usually unnecessary:
- defining a local protocol structure
- deciding whether a file should be prose or YAML when the question is mainly internal design
- deciding how the project should use “continue”
- designing a decision-log template
- designing a local rubric structure unless domain facts are central

The rule is:
Use deep research when truth is outside the project’s current mind, not merely when the problem is important.

---

## 7. Mandatory internal pass before research

Before invoking deep research, the model should first do a disciplined internal pass unless the question is purely factual and current.

That internal pass should identify:
- what is already inferable
- what the real unknowns are
- which unknowns actually matter
- what specific question the research must answer
- what decision the research is meant to inform

This prevents shallow or wasteful research.

The model should not say:
- “we should research this”

It should say something more like:
- “The unresolved issue is whether PDF support is strategically central enough to belong in KR’s medium-term architecture rather than being treated as optional. Internal reasoning suggests yes because it widens corpus coverage, but we need external evidence on practical format realities, pipeline implications, and typical acquisition constraints.”

That is the expected level of research clarity.

---

## 8. Research question formulation rule

Every deep-research invocation should be guided by an explicit research question or question set.

A good research question is:
- narrow enough to resolve something
- broad enough to matter
- tied to a real project decision
- explicit about what evidence would change the recommendation

Bad:
- “Research PDF support”

Good:
- “Determine whether PDF support is strategically necessary for a serious long-horizon Islamic library, given likely corpus availability, extraction difficulty, and the limitations of Shamela-only ingestion.”

The research task should always be in service of a decision, not research for its own sake.

---

## 9. Research-output requirements

When deep research is used, the resulting output should try to make these elements explicit:

- research question
- why this question matters for KR
- key findings
- quality of evidence
- what remains uncertain
- implications for KR
- whether the current recommendation changes
- what durable artifact or decision should now be updated

Deep research should not be treated as a raw information dump.
It should feed the operating system.

---

## 10. Multi-pass internal review protocol

Before finalizing any Tier 2 or Tier 3 direction, the model should pass it through a structured internal review cycle.

### Pass 1 — Constructive pass
Build the strongest coherent recommendation.

Questions:
- what is the best current direction?
- why is it attractive?
- what does it solve?
- how does it help KR?

### Pass 2 — Adversarial pass
Attack the recommendation.

Questions:
- what hidden assumptions is it relying on?
- what could go wrong?
- where is the complexity cost underestimated?
- what important alternative is being ignored?
- where could this contaminate downstream design?

### Pass 3 — Tradeoff pass
Compare against the strongest alternatives.

Questions:
- what is the strongest competing path?
- what are the tradeoffs?
- what is gained and lost in each option?
- which option fits v1 better?
- which option fits the long horizon better?

### Pass 4 — Integration pass
Synthesize the result.

Questions:
- what survives critique?
- what should be revised?
- what remains uncertain?
- what is the final best judgment right now?

This four-pass structure should be the default for serious internal hardening.

---

## 11. Adversarial critique protocol

For major or critical questions, the model should explicitly shift into critique mode rather than merely “adding more thoughts.”

In critique mode, it should attack the current recommendation from at least these angles:

### 11.1 Strategic coherence
Does this fit KR’s actual long-horizon direction?

### 11.2 Integrity and trustworthiness
Does this threaten attribution, auditability, provenance, or scholarly seriousness?

### 11.3 Architectural cleanliness
Does this add ugly complexity, brittle coupling, or future maintenance burden?

### 11.4 Product leverage
Does this materially improve serious study value, or just sound interesting?

### 11.5 Opportunity cost
What are we not doing if we do this?

### 11.6 Dependency realism
Is this quietly assuming unavailable tools, data, or implementation capacity?

### 11.7 Scope discipline
Is this appropriate now, or is it a later-state concern masquerading as an immediate need?

Every serious recommendation should survive at least one adversarial pass.

---

## 12. Evidence-strength classification

When research or evidence is involved, the model should classify evidence strength explicitly.

### E0 — no evidence
Pure internal reasoning only.

### E1 — weak evidence
Suggestive but limited external indications.

### E2 — moderate evidence
Multiple useful signals, but still incomplete or not fully decisive.

### E3 — strong evidence
High-quality evidence clearly supports the direction.

### E4 — decisive evidence
The relevant issue is strongly resolved by high-quality evidence.

This classification helps prevent false certainty.

Not every good decision needs E3 or E4.
But major evidence-gated decisions should not be treated as if E0 were enough.

---

## 13. Confidence labeling system

The future KR project should label important conclusions by confidence, separately from evidence strength.

### C1 — tentative
Useful working judgment, but highly revisable.

### C2 — provisional
Reasonably good current judgment, but meaningful uncertainty remains.

### C3 — robust
Strong current judgment after critique and sufficient review.

### C4 — hardened
High-confidence project position, suitable for doctrine, planning, or execution handoff.

Evidence strength and confidence are not the same.
A conclusion can be C3 with E0 if it is mainly an internal design question.
A conclusion can be only C2 with E3 if external evidence is strong but KR-specific implications remain uncertain.

---

## 14. Hardening-completion criteria

A question or aspect conclusion should be considered hardened enough only when all relevant conditions below are satisfied.

### 14.1 The problem is clearly defined
The issue being decided is stated cleanly.

### 14.2 The real stakes are clear
It is clear why this matters for KR.

### 14.3 Major assumptions are surfaced
Important assumptions are visible, not hidden.

### 14.4 Alternatives were considered
The recommendation did not emerge by inertia.

### 14.5 The recommendation survived critique
Weaknesses were examined and either addressed or explicitly left unresolved.

### 14.6 Evidence needs were handled properly
Research was used when needed, and not faked when unavailable.

### 14.7 The outcome is operational
The conclusion can guide action, files, tasks, or doctrine.

### 14.8 Residual uncertainty is named
Open questions are explicitly identified.

### 14.9 Durable conversion is ready
The result can be translated into a file, record, protocol, or task packet.

If these conditions are not met, the conclusion is not hardened.

---

## 15. Unresolved-question handling

Not every important question can be fully resolved in one pass.

When unresolved uncertainty remains, the model should not blur it away.

It should record:
- the unresolved question
- why it remains unresolved
- what evidence or reasoning would reduce the uncertainty
- whether work can continue around it
- whether it blocks downstream decisions

This avoids false closure.

Unresolved questions should be treated as deliberate project state, not failure.

---

## 16. Review depth rules by decision tier

### Tier 0
- internal reasoning only
- explicit assumption if needed

### Tier 1
- internal reasoning
- brief critique
- durable output if useful

### Tier 2
- internal reasoning
- adversarial critique
- tradeoff comparison
- research if triggered
- final synthesis
- durable artifact

### Tier 3
- strong internal mapping
- adversarial critique
- explicit evidence review where relevant
- explicit confidence and evidence labeling
- explicit uncertainty handling
- explicit escalation if required
- durable record suitable for future reuse

This ensures review effort is proportional.

---

## 17. Escalation after review

Even after extensive reasoning and research, some issues must still be escalated.

Escalation is required when:
- the final step is inherently user-owned
- the recommendation depends on an irreducible personal preference
- available evidence remains too weak for responsible commitment
- the project faces multiple live paths with materially different irreversible consequences
- the issue requires external access or permissions

When escalating, the model must not stop at:
- “this is uncertain”

It must say:
- what exactly is uncertain
- why it matters
- what recommendation is still strongest
- what the user must decide
- what will happen under each viable branch

---

## 18. Review-output format for serious decisions

For Tier 2 and Tier 3 questions, the model should try to structure its conclusion using a format like:

### Serious decision review format
- current question
- provisional or final recommendation
- why this is the strongest direction
- strongest alternatives considered
- strongest objections or risks
- evidence status
- confidence level
- unresolved questions
- durable artifact(s) that should now exist
- exact next move

This format helps make the project’s reasoning reusable.

---

## 19. Research-efficiency rule

Even when deep research is justified, it should be targeted.

The model should avoid:
- broad exploratory research with unclear decision relevance
- repetitive research on the same issue without new purpose
- collecting facts that do not change KR’s design choices
- delaying internal reasoning until research arrives
- using research as a substitute for judgment

The model should prefer:
- sharply targeted evidence gathering
- synthesis over accumulation
- decision-relevant research only

The goal is not “maximum research.”
The goal is maximum decision quality.

---

## 20. Anti-failure rules

The model must avoid the following review and research failures.

### 20.1 Cosmetic-review failure
The model claims something was reviewed, but no real critique occurred.

### 20.2 Research-as-decoration failure
Research is used to make output look impressive rather than to resolve real uncertainty.

### 20.3 Research-avoidance failure
The model relies on internal reasoning where evidence is clearly required.

### 20.4 False-hardening failure
The model treats a lightly examined conclusion as hardened.

### 20.5 Uncertainty-burial failure
Residual uncertainty is hidden or softened away.

### 20.6 Infinite-review failure
The model keeps reviewing without converging or declaring a local stopping point.

### 20.7 Evidence-confusion failure
The model confuses strong reasoning with strong evidence, or vice versa.

These failures are all forbidden.

---

## 21. Recommended stopping rule

A serious decision should stop hardening temporarily when one of the following is true:

- the conclusion has reached sufficient hardening for its decision tier
- the remaining uncertainty is explicit and acceptable
- additional critique is producing diminishing returns
- the next real step requires external research
- the next real step requires user approval
- the conclusion is ready to be converted into durable project artifacts

This stopping rule prevents endless overprocessing.

---

## 22. Success condition

This protocol is successful only if the future KR production project behaves like this:

- it uses deep research when truth actually lies outside internal reasoning
- it does not waste deep research on purely internal design questions
- important decisions go through real critique
- evidence and confidence are not conflated
- uncertainty is explicit
- high-stakes directions are hardened properly
- conclusions become operational and durable
- the project becomes more trustworthy, not merely more verbose

That is the intended standard.
