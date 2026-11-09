# Infomax AI Skills

Reusable Agent Skills for explaining, designing, and documenting complex work.

## Available skills

### [complex-concept-explainer](complex-concept-explainer/SKILL.md)

Turn difficult technical, AI, ontology, reasoning, and business concepts into accurate, accessible explanations for non-experts, practitioners, or executives.

Features:
- Plain-language explanation and progressively deeper detail
- Practical scenarios, analogies with clear limitations, and small diagrams
- Distinction between facts, constraints, inference, missing evidence, and prediction
- Audience-oriented document template and quality checklist

**Try asking:**

> 온톨로지와 관계형 데이터베이스의 차이를 비개발자 임원에게 설명해 줘. 승인 누락 사례를 가정해 추론과 예측의 차이까지 보여줘.

**Skill files**
- [Instructions](complex-concept-explainer/SKILL.md)
- [Explanation patterns](complex-concept-explainer/references/explanation-patterns.md)
- [Quality checklist](complex-concept-explainer/references/quality-checklist.md)
- [Example: ontology reasoning](complex-concept-explainer/examples/ontology-reasoning.md)
- [Document template](complex-concept-explainer/assets/explainer-template.md)

## Installation and use

Each skill is a directory containing a `SKILL.md` with YAML frontmatter, following the [Agent Skills format](https://agentskills.io/specification). Copy `complex-concept-explainer/` into your agent's supported skill directory, or configure the agent to load it from this repository. The exact location and activation procedure depend on the agent client.

The skill is instruction-only; no third-party packages, scripts, keys, or network access are required. Its use does not mean any claims or source materials have already been independently verified.
