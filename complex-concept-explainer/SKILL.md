---
name: complex-concept-explainer
description: >-
  Explain difficult technical, AI, scientific, and business concepts accurately to non-experts.
  Use when asked to simplify an architecture, ontology, inference or reasoning engine, algorithm,
  data model, business process, or research document; produce a beginner-friendly report,
  executive explainer, teaching material, diagram, or interactive explanation.
  한국어로 복잡한 개념을 쉽게 설명하는 문서, 사례, 비유, 구조도, 임원용 해설을 만들 때 사용한다.
metadata:
  author: infomaxai
  version: "1.0.0"
---

# Complex Concept Explainer

## Goal

Make a difficult idea **understandable without making it false**. The outcome is not a shorter technical document; it is a reader who can explain the concept, use it in a realistic situation, and distinguish its limits from its promises.

Default language: match the user's language (Korean for Korean requests). Do not invent product behavior or private organizational facts.

## Use this skill when

- Explaining ontology, graph relationships, rules, inference, prediction, agents, APIs, databases, AI models, finance, or unfamiliar business operations.
- Turning design documents, technical references, or research papers into explanations for executives, non-developers, new team members, or cross-functional stakeholders.
- Creating a conceptual walkthrough, an analogy, a diagram, a training handout, or a presentation narrative.

Not a replacement for formal specifications, source-code documentation, legal advice, or correctness proofs. Preserve links to those sources when available.

## Workflow

### 1. Identify reader and learning objective

Determine from the request or context:
- **Reader:** executive / practitioner / beginner / developer; their likely prior knowledge.
- **Learning objective:** what question the reader should answer or decision they should make.
- **Artifact:** concise answer, editable Markdown document, slide outline, diagram, webpage, or other explicitly requested output.
- **Evidence:** supplied materials, live references, known facts, assumptions.

If missing, proceed with a reasonable audience assumption and label it briefly. Ask only when the ambiguity prevents a useful explanation. Do not create an external file or website unless requested or appropriate tools are available.

### 2. Build a private concept map before writing

Extract 3–7 essential concepts and connect each to the reader's main question.
Separate:
1. **Verified fact:** supported by the provided source or a reliable cited reference.
2. **Interpretation or design option:** a proposed way to use the concept.
3. **Illustration:** invented but explicitly hypothetical scenario or analogy.
4. **Unknown or contingent claim:** requires validation or specific configuration.

Resolve prerequisite concepts first; defer secondary jargon to a glossary. If a source is ambiguous or incomplete, preserve that uncertainty rather than filling the gap with an invented claim.

### 3. Explain in ascending levels of detail

Use this progression, adapting the section count to the requested length:

1. **One sentence:** what it is and why it matters, without unexplained jargon.
2. **Problem first:** the pain point before the solution.
3. **Familiar scenario:** one concrete situation with named roles, objects, actions, and outcomes.
4. **Mechanism:** how it works, including key dependencies and where data comes from.
5. **Visual model:** a small relationship or flow diagram when it clarifies the explanation.
6. **What it can and cannot do:** boundary conditions, failure modes, and uncertainty.
7. **Actionable takeaway:** a decision rule, diagnostic question, or next step.

Use one strong analogy, not many weak analogies. Explicitly state where the analogy stops being accurate. Prefer precise verbs over abstractions and concrete examples over repeated definitions.

### 4. Make relationships visible

Choose the lightest representation that answers the question:
- **Sequence/flowchart:** operations, cause and effect, data movement, decision gates.
- **Relationship graph:** entities, links, constraints, responsibilities, dependency chains.
- **Before/after table:** limitations of an existing method and what changes.
- **Timeline:** state transitions, approval or exception handling.

Prefer readable Mermaid diagrams for Markdown deliverables if supported. Keep diagrams small (usually 5–9 nodes), label arrows with their meaning, and provide an equivalent sentence for accessibility. Never depict an unverified relationship as an established fact.

Read [references/explanation-patterns.md](references/explanation-patterns.md) when choosing a pattern or visualization. Use [assets/explainer-template.md](assets/explainer-template.md) for longer stand-alone materials, not as a mandatory rigid outline.

### 5. Handle inference and prediction precisely

For reasoning/ontology topics, distinguish:
- **Observed data:** recorded facts or events.
- **Explicit knowledge:** relationships, definitions, constraints, policy rules.
- **Derived conclusion:** a result implied by those facts and rules.
- **Anomaly / contradiction:** assertions that cannot simultaneously satisfy a specified rule.
- **Missing information:** an expected relation or evidence not found; absence is not automatically proof of a violation.
- **Prediction:** a probabilistic estimate requiring a separate statistical model, evaluation data, and uncertainty.

A graph database or ontology does not itself guarantee reasoning, contradiction detection, completeness checking, or forecasting. Specify what rule, coverage assumption, validation method, or model produces each output. In open-world settings, 'not recorded' and 'false' differ.

Use the worked example in [examples/ontology-reasoning.md](examples/ontology-reasoning.md) if the reader needs to see inference, conflicts, or missing business process steps.

### 6. Produce the requested deliverable

- **Short answer:** lead with an intuitive explanation and one realistic example.
- **Executive brief:** decision/impact first; mechanism second; risks and assumptions visible.
- **Training material:** one concept per unit, progressive examples, quick comprehension checks.
- **Detailed technical explainer:** add formal terms, algorithms, data contracts, and source traceability in an appendix.
- **Diagram or webpage:** ensure every visual has a text explanation and works without animation or interaction.

Keep the final output readable in the medium available. Do not claim to have generated a PDF, slide deck, interactive website, or validated code unless it was actually created and checked.

### 7. Perform the reader test and factual audit

Before delivering, silently run these tests:
- Could the target reader state the concept in one sentence?
- Could they follow the scenario without looking up more than two new terms?
- Are facts, assumptions, analogies, and proposed designs clearly distinguishable?
- Could the diagram mislead about order, causation, certainty, or product capabilities?
- Would a subject-matter expert recognize the essential mechanism and its limits?
- Does the explanation say what changes operationally, not just define vocabulary?

Repair any failed point. For long/high-stakes materials, also read [references/quality-checklist.md](references/quality-checklist.md).

## House rules

- Be clear without being condescending. No forced enthusiasm, fictional confidence, or filler.
- Define an acronym on first use and avoid unnecessary foreign technical terminology.
- Prefer one sustained example; progressively reveal its complexity.
- Mark hypothetical values and illustrative organizations as examples.
- Attribute important factual claims to the source when one is supplied; never fabricate citations.
- Explain trade-offs. Avoid 'always', 'automatically', 'fully', or 'guaranteed' unless genuinely justified.
- Include a concise 'limits/assumptions' section for architecture, risk, policy, and model-performance claims.
- For executive audiences, prefer plain Korean headings, operational consequences, ownership, and decisions over test counts, hashes, or implementation trivia.

## Sample invocation

> "온톨로지와 관계형 데이터베이스의 차이를 비개발자 임원에게 설명해 줘. 인포맥스 같은 금융정보 회사의 승인 누락 사례를 가정해서, 실제 추론과 예측의 차이까지 도식으로 보여줘."

The result should distinguish database storage, explicit business relations, rule-driven conclusions, missing-evidence checks, and forecasting. The example is illustrative unless the organization's real rules and data are provided.
