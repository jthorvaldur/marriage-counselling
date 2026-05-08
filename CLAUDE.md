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
