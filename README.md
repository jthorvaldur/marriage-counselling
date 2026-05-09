# marriage-counselling

Relationship intelligence platform. Detects destructive communication patterns (DARVO, Four Horsemen, pursue-withdraw cycles, financial control) from couples' actual communication history. Prevention-focused — helps couples see patterns before they become litigation. See `GOAL.md` for full product vision. See `INTENT.md` for operating rules.

## Setup

```bash
uv sync
```

## Commands

### `main.py`

```
Hello from marriage-counselling!
```

## Key Dependencies

`anthropic`, `click`, `httpx`, `pyyaml`, `qdrant-client`, `tqdm`

## Structure

```
marriage-counselling/
├── CLAUDE.md
├── GOAL.md
├── INTENT.md
├── main.py
├── pyproject.toml
├── README.md
├── docs/
│   ├── darvo.html
│   ├── financial-control.html
│   ├── four-horsemen.html
│   ├── gaslighting.html
│   ├── index.html
│   ├── pursue-withdraw.html
│   ├── triangulation.html
└── scripts/
```

---

Managed by [policy-orchestrator](https://github.com/jthorvaldur/policy-orchestrator).
Category: infrastructure. 2 commits.
