# INTENT.md

> **Version:** 0.1.0
> **Scope:** marriage-counselling repo. Inherits from policy-orchestrator global INTENT.md.
> **Audience:** Every agent — human, AI, or automated — that reads or writes in this repo.

---

## Prime Directive

Build a relationship intelligence platform that helps couples recognize destructive patterns before they become litigation. Every feature serves prevention, not prosecution.

---

## 1. Operating Rules

**Signal over noise.** Every output must be directly relevant, logically consistent, and actionable.

**Internal consistency.** Verify work does not contradict repo purpose, prior architecture decisions, or existing conventions before proceeding.

**No drift.** This is a prevention tool, not a litigation tool. Case strategy, legal filings, and adversarial positioning belong in div_legal and caseledger. This repo helps people stay out of court.

**Flag uncertainty.**

    Uncertainty: [what is unknown]
    Assumption: [what is being assumed]
    Implication: [what breaks if the assumption is wrong]

---

## 2. Decision Principles

1. Simpler over complex.
2. Explicit over implicit.
3. Composable over monolithic.
4. Auditable over opaque.
5. Both partners are users. The system never takes sides.
6. Pattern identification over diagnosis. Describe what happened, not what someone "is."
7. Reversible over permanent.

---

## 3. Repo Boundaries

This repo is the **prevention product**. It must never contain:

- Personal case files or litigation documents from any active case
- Diagnostic labels (NPD, BPD, etc.) applied to individuals
- Legal advice or litigation strategy
- Any feature that weaponizes one partner's data against the other

This repo reuses infrastructure from caseledger (vector DB, embedding, document analysis) but serves a fundamentally different purpose: helping couples understand communication patterns, not building a case.

---

## 4. Agent Protocol

- Read this file before acting.
- Preserve existing conventions unless explicitly changing them.
- Do not modify files outside scope.
- Do not introduce secrets into tracked files.
- Do not duplicate functionality handled by caseledger or docvec.
- Provide validation steps after changes.
- Explain only what is needed.

---

## Override Mechanism

This file inherits from policy-orchestrator INTENT.md. Local overrides via INTENT.local.md. Section 3 (Repo Boundaries) cannot be relaxed.
