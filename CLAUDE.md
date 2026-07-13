# CLAUDE.md — Marriage Counselling Platform

## Project Overview

Relationship intelligence platform. Detects destructive communication patterns (DARVO, Four Horsemen, pursue-withdraw cycles, financial control) from couples' actual communication history. Prevention-focused — helps couples see patterns before they become litigation.

See `GOAL.md` for full product vision. See `INTENT.md` for operating rules.

## Language & Stack

- Primary: Python (pattern detection, embedding, analysis)
- Secondary: TypeScript (Next.js frontend)
- Package manager: uv (Python), npm (web)

## Policies

Managed by policy-orchestrator. See `.control/repo.yaml`.

### Hard (enforced)

- Never commit `.env` or secret files
- No force push to main
- Both partners are users. The system never takes sides.
- No diagnostic labels applied to individuals (NPD, BPD, etc.)
- No litigation strategy or legal advice
- No weaponization of one partner's data against the other
- Privacy is absolute — communication data never leaves the couple's account

### Soft (advisory)

- Use conventional commits
- Keep README current
- Pattern identification over diagnosis

## Session Start Protocol

1. Read `INTENT.md`
2. Read `GOAL.md` for product context
3. Check related repos for shared infrastructure:
   - `caseledger/docs/` — pattern library, communication design, DARVO documentation
   - `docvec/` — shared embedding infrastructure
   - `policy-orchestrator/` — control plane

## Key Distinction from CaseLedger

| | CaseLedger | Marriage Counselling |
|---|---|---|
| Purpose | Litigation intelligence | Prevention intelligence |
| User | One party (adversarial) | Both partners (collaborative) |
| Output | Evidence for court | Patterns for understanding |
| Takes sides | Yes (built for one party's case) | Never |
| Labels | Documents contradictions | Describes communication patterns |
| Goal | Win the case | Save the relationship |

## Core Patterns to Detect

- DARVO (Freyd, 1997) — Deny, Attack, Reverse Victim and Offender
- Four Horsemen (Gottman) — Criticism, Contempt, Defensiveness, Stonewalling
- Pursue-Withdraw (Johnson/EFT) — escalation/shutdown cycles
- Financial Control — hidden accounts, information asymmetry about money
- Triangulation — bringing third parties into the couple's conflict

---

## Repo intent (folded from INTENT.md, 2026-07-12)

# INTENT.md


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
