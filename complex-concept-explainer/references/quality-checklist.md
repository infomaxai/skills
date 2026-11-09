# Quality checks for concept explainers

Use these checks to revise a substantial explainer. They are a reasoning aid, not a substitute for external verification or real reader testing.

## Comprehension

- [ ] The opening answers what it is, why it matters, and for whom.
- [ ] Each new technical term is defined when first used.
- [ ] Essential dependencies appear before their consequences.
- [ ] At least one realistic example shows an input, operation, and output.
- [ ] At least one counterexample or limitation prevents overgeneralization.
- [ ] The diagram is legible and has equivalent explanatory text.
- [ ] Every subsection contributes to the reader's learning goal.

## Accuracy and provenance

- [ ] Facts with a supplied source can be traced back to it.
- [ ] Hypothetical characters, inputs, metrics, and organizations are marked as illustrative.
- [ ] The explanation distinguishes what the source says from what is being proposed.
- [ ] Relative dates, product capabilities, and performance figures are verified when material.
- [ ] Important configuration assumptions and exceptions are visible.
- [ ] No invented quotations, citations, benchmarks, tests, or demonstrations.

## Reasoning-specific checks

- [ ] The ontology/schema is not confused with the reasoning implementation.
- [ ] Rules, constraints, and evaluation semantics are explicit.
- [ ] Contradiction means incompatible claims under the named rule, not merely different values.
- [ ] Missing evidence is not automatically interpreted as a false claim or completed violation.
- [ ] Closed-world assumptions, authoritative sources, and freshness checks are stated if used.
- [ ] Confidence or probability appears only when a real predictive or scoring method supports it.
- [ ] Output categories distinguish fact, inference, warning, and recommendation.
- [ ] False-positive risks and human review or escalation paths are described for consequential cases.

## Audience calibration

### Executive reader
- [ ] Operational impact, decision options, responsible roles, cost/risk assumptions are visible.
- [ ] The main message survives without reading a technical appendix.

### Practitioner
- [ ] Prerequisites, data fields, exceptions, validation steps, and integration points are clear.

### Engineer
- [ ] Precise semantics, failure cases, constraints, and unresolved implementation choices are identified.

## Reality check: five sample reader questions

Ask whether the finished document answers the following without additional research:
1. What specific problem does this solve?
2. What does the system need as input?
3. What exactly happens between input and output?
4. When might this fail or give a misleading answer?
5. What should our team decide, implement, or validate next?

If a question cannot be answered, revise the document before publishing.

## Quality rubric (optional)

Score each dimension 0/1/2: **clarity**, **technical correctness**, **traceability**, **example quality**, **limitations**, **decision usefulness**.

- 0 = absent or misleading
- 1 = partially fulfilled
- 2 = clear and substantiated

A low score identifies a revision target. Do not report an unperformed user study or test as passed.
