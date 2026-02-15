# Avare

Avare is an awareness layer for production AI systems.

Modern AI systems operate without visibility into cost, latency, and behavior.
Avare introduces awareness as a first-class primitive.

---

## Why Avare?

AI systems in production often lack:

- Cost visibility
- Latency tracking
- Behavioral telemetry
- Structured logging
- Governance hooks

Avare provides a lightweight, framework-agnostic layer to make AI systems observable and accountable by design.

---

## What Avare Does (v0.1)

- Tracks request latency
- Captures model metadata
- Estimates token usage
- Estimates cost
- Emits structured telemetry logs

No dashboards.
No SaaS.
No lock-in.

Just awareness.

---

## Installation

```bash
pip install avare
```

## Quick Example
```
from avare import track

with track(model="gpt-4"):
    response = client.chat.completions.create(
        model="gpt-4",
        messages=[
            {"role": "user", "content": "Hello"}
        ]
    )
```

## Roadmap
v0.1 – Core awareness tracking
v0.2 – Budget enforcement hooks
v0.3 – Policy interface
v1.0 – Runtime integrations
