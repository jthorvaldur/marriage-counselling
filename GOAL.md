# Marriage Counselling Platform

**Relationship intelligence for couples who want to understand what's happening before it's too late.**

---

## What It Is

A platform that helps couples recognize destructive communication patterns — DARVO cycles, escalation loops, stonewalling, financial control, emotional withdrawal — using the same document intelligence infrastructure built for legal cases, but applied to prevention instead of prosecution.

The insight: the patterns that destroy marriages are predictable. They show up in text messages, emails, and conversations months or years before anyone files for divorce. If you can see the pattern, you can interrupt it.

---

## The Problem

Couples in crisis don't understand why rational approaches keep failing. One partner tries to compromise; the other interprets it as weakness. One partner tries to discuss finances; the other hides accounts. One partner asks for honesty; the other responds with DARVO (Deny, Attack, Reverse Victim and Offender).

Marriage counsellors see these patterns but have limited tools to surface them from the couple's actual communication history. The couple sits in a room for 50 minutes a week and tries to remember what happened. They can't — because the pattern is invisible from inside.

This platform makes the pattern visible. Not by taking sides. By showing both partners what is actually happening in their communication, backed by their own words.

---

## What It Does

1. **Ingests communication** — texts, emails, chat logs (with consent of both partners)
2. **Detects patterns** — DARVO cycles, Gottman's Four Horsemen (criticism, contempt, defensiveness, stonewalling), escalation loops, withdrawal/pursuit cycles
3. **Visualizes the cycle** — shows the pattern as a loop, not a he-said/she-said. Both partners see their role.
4. **Identifies triggers** — what topics, times, or contexts activate the destructive cycle
5. **Suggests interruptions** — evidence-based techniques to break the pattern at specific points
6. **Tracks progress** — are the cycles getting shorter? Less intense? More frequent? The data tells the truth.

---

## Who It's For

**Couples in therapy** — the therapist gets a data layer on top of their clinical judgment. Instead of relying on each partner's narrative, the therapist sees the actual communication pattern.

**Couples considering therapy** — the platform can show them what's happening before they commit to a therapist. Sometimes seeing the pattern is enough to change it.

**Individuals who suspect something is wrong** — one partner can analyze their own side of the communication to understand their role in the cycle. The platform never weaponizes this — it shows your part, not your partner's diagnosis.

---

## What It Is Not

- Not a therapist. Does not provide clinical advice.
- Not a litigation tool. Does not build a case against your partner.
- Not a surveillance tool. Requires consent from both partners for shared analysis.
- Not a diagnostic tool. Identifies patterns of behavior, not personality disorders.
- Does not take sides. Both partners see the same data.

---

## Design Principles

1. **Both partners are users.** The moment the platform favors one side, it becomes a weapon. Neutrality is not optional.
2. **Patterns, not labels.** "This conversation follows a pursue-withdraw cycle" is useful. "Your partner is a narcissist" is not.
3. **Your words, not our interpretation.** The platform shows what was said, when, and how it maps to known patterns. The couple draws conclusions.
4. **The cycle is the enemy, not the partner.** Frame the pattern as something that happens TO the relationship, not something one person does TO the other.
5. **Privacy is absolute.** Communication data is never shared outside the couple's account. Never used for training. Never accessible to third parties. Export and delete at any time.

---

## Relationship to Other Repos

| Repo | Focus | Relationship |
|---|---|---|
| **div_legal** | Active divorce case (test case data) | Source of pattern knowledge — what goes wrong |
| **caseledger** | Legal document intelligence for litigation | Shared infrastructure (vectors, embeddings, search) |
| **marriage-counselling** | Prevention and relationship intelligence | Same patterns, opposite purpose: prevent instead of litigate |
| **policy-orchestrator** | Control plane | Manages this repo like all others |
| **docvec** | Embedding infrastructure | Shared embedding pipeline |

The through-line: div_legal taught the system what goes wrong. CaseLedger helps people fight when it's too late. This platform helps people before it gets there. Three points on the same curve.

---

## Core Patterns to Detect

### From Clinical Literature:

| Pattern | Source | What to Detect |
|---|---|---|
| DARVO | Freyd (1997) | Deny-Attack-Reverse cycles in response to confrontation |
| Four Horsemen | Gottman | Criticism, Contempt, Defensiveness, Stonewalling |
| Pursue-Withdraw | Johnson (EFT) | One partner escalates, the other shuts down, which escalates the first |
| Financial Control | Domestic violence literature | Hidden accounts, unilateral spending, information asymmetry about money |
| Triangulation | Family systems theory | Bringing children, family, or friends into the couple's conflict |
| Gaslighting | Clinical psychology | Denying the other's perception of reality, especially regarding documented events |

### From the div_legal Test Case:

| Pattern | What We Learned | Prevention Application |
|---|---|---|
| Hidden accounts | Appear months/years before filing | Financial transparency tools — shared dashboards, automatic alerts |
| Communication outside agreed channels | Indicates boundary violations | Channel monitoring — are you communicating where you agreed to? |
| Document pressure | "Please sign this" without explanation | Consent verification — does both partners understand what they're agreeing to? |
| Family isolation | One partner contacts the other's family to control narrative | Social pattern detection — who is talking to whom about the relationship? |
| Moving targets | Changing numbers, shifting blame | Consistency tracking — does this week's story match last month's? |

---

## Stack

Same as caseledger where applicable:

- **Pipeline:** Python (pattern detection, embedding, analysis)
- **Inference:** Claude API (pattern classification, communication analysis)
- **Vector DB:** Qdrant (conversation embeddings, pattern matching)
- **Frontend:** Next.js + Tailwind (couple-facing dashboard)
- **Privacy:** End-to-end encryption. Zero-knowledge architecture where possible.

---

## Origin

Built from the wreckage of a real marriage. The patterns described here were lived, documented, and eventually litigated. The litigation produced a data infrastructure (2 million vectors, 57,000 documents, 7 Qdrant collections) that revealed what could have been seen years earlier — if anyone had been looking.

This platform is the tool that could have helped. It didn't exist then. It will exist now.
