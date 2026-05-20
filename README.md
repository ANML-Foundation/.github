<p align="center">
  <a href="https://anmlfoundation.org">
    <img src="https://anmlfoundation.org/images/anml-foundation-logo.png" alt="ANML Foundation" width="500">
  </a>
</p>

<p align="center">
  <strong>The comprehension layer for the agentic web.</strong>
</p>

<p align="center">
  <a href="https://datatracker.ietf.org/doc/draft-jeskey-anml/">Internet-Draft</a> ·
  <a href="https://anmlfoundation.org/docs">Documentation</a> ·
  <a href="https://anmlfoundation.org/why-anml">Why ANML?</a> ·
  <a href="https://anmlfoundation.org/integrations">Integrations</a>
</p>

---

## What is ANML?

**ANML** — pronounced "animal" — is a machine-first markup language designed for the agentic web. Where HTML serves humans, ANML serves the autonomous agents that are becoming the primary consumers of web content.

ANML is a structured, machine-readable document format that conveys meaning, context, behavioral guidance, privacy rules, and workflow state — all in one place, without inference. We call ANML files **"duckuments."**

> A duck moves along the water with effortless grace — straightforward, easily understood, calm on the surface. But beneath the waterline there is a lot going on: structured interactions, disclosure constraints, workflow state, knowledge exchange, and behavioral guidance all working together.

## The Gap ANML Fills

When an autonomous agent encounters a service today, it typically gets:

- **An API contract** (OpenAPI, GraphQL) — tells the agent what endpoints exist, but nothing about what the service *means*, how to behave, what's sensitive, or where the user is in a workflow.
- **An HTML page** — rich with visual information for humans, but requires expensive inference to extract intent and actions that were never explicitly encoded.

Neither gives an agent what it actually needs. ANML provides a **comprehension layer** — a universal document format that any conforming agent can read to understand a service without bespoke integration.

## Key Capabilities

| Capability | Description |
|---|---|
| **Machine-First** | Structured for direct interpretation by autonomous agents, minimizing inference cost and maximizing determinism |
| **Dual Serialization** | XML for human authoring and review. JSON for programmatic generation and agent-pipeline consumption. Both normative |
| **Privacy by Design** | Agents control disclosure. Services may request information but constraints govern what can be shared |
| **No Prior Integration** | Like HTML for browsers, any conforming agent can read any ANML duckument without service-specific code |
| **Workflow State** | Explicit multi-step flow tracking so agents know where users are in a process |
| **Knowledge Exchange** | Bidirectional information sharing between services and agents with TTLs and confidentiality levels |
| **Usage Rights** | Machine-readable hierarchy (none < display < cache < store < train) governing what agents may do with content |
| **Trust Delegation** | DNS-bootstrapped verification that a serving domain is authorized to assert another site's identity |

## Where ANML Fits

ANML doesn't replace existing protocols — it gives agents the semantic context they need to use them intelligently.

| Layer | Answers | Examples |
|---|---|---|
| **Transport** | How do I call this? | REST, MCP, A2A, gRPC |
| **Capability** | What data do I send? | OpenAPI, JSON Schema, UCP |
| **Comprehension (ANML)** | What does this mean? How should I behave? | ANML duckuments |

## What an ANML Duckument Defines

- **Content** — Structured, semantic information for machine interpretation
- **Interactions** — Operations bound to HTTP methods, endpoints, and parameters
- **Knowledge** — Bidirectional information exchange between services and agents
- **Constraints** — Disclosure, consent, and authorization rules agents must evaluate
- **State** — Metadata identifying the current phase of a multi-step interaction
- **Persona** — Advisory behavioral and tonal guidance for agent responses

## Repositories

| Repo | Description |
|---|---|
| [anml-server-rust](https://github.com/ANML-Foundation/anml-server-rust) | Reference ANML server implementation in Rust |
| [anml-client-rust](https://github.com/ANML-Foundation/anml-client-rust) | Reference ANML client implementation in Rust |

## Quick Example

**JSON**

```json
{
  "anml": "1.0",
  "ttl": 300,
  "head": { "title": "Checkout — Acme Electronics" },
  "constraints": {
    "disclosure": [
      { "field": "payment-credential", "requires": "explicit-consent" },
      { "field": "shipping-address", "requires": "explicit-consent" }
    ]
  },
  "state": {
    "flow": {
      "step": [
        { "id": "cart", "label": "Cart", "status": "completed" },
        { "id": "checkout", "label": "Checkout", "status": "current" },
        { "id": "payment", "label": "Payment", "status": "pending" }
      ]
    }
  },
  "interact": {
    "action": [
      { "id": "create-session", "method": "POST", "endpoint": "/checkout-sessions", "auth": "required" }
    ]
  },
  "knowledge": {
    "inform": [
      { "confidentiality": "public", "ttl": 3600, "content": "Free shipping over $75. 30-day returns." }
    ]
  },
  "persona": {
    "tone": { "value": "helpful" },
    "instructions": "Confirm the final amount before requesting payment."
  }
}
```

**XML**

```xml
<?xml version="1.0" encoding="UTF-8"?>
<anml xmlns="urn:ietf:params:xml:ns:anml:1.0" ttl="300">
  <head>
    <title>Checkout — Acme Electronics</title>
  </head>
  <constraints>
    <disclosure field="payment-credential" requires="explicit-consent"/>
    <disclosure field="shipping-address" requires="explicit-consent"/>
  </constraints>
  <state>
    <flow>
      <step id="cart" label="Cart" status="completed"/>
      <step id="checkout" label="Checkout" status="current"/>
      <step id="payment" label="Payment" status="pending"/>
    </flow>
  </state>
  <interact>
    <action id="create-session" method="POST"
            endpoint="/checkout-sessions" auth="required"/>
  </interact>
  <knowledge>
    <inform confidentiality="public" ttl="3600">
      Free shipping over $75. 30-day returns.
    </inform>
  </knowledge>
  <persona>
    <tone value="helpful"/>
    <instructions>Confirm the final amount before requesting payment.</instructions>
  </persona>
</anml>
```

## Links

- 🌐 [anmlfoundation.org](https://anmlfoundation.org)
- 📄 [IETF Internet-Draft: draft-jeskey-anml-00](https://datatracker.ietf.org/doc/draft-jeskey-anml/)
- 📖 [Documentation](https://anmlfoundation.org/docs)
- 🤝 [Integrations](https://anmlfoundation.org/integrations)
- 📧 [sponsors@anmlfoundation.org](mailto:sponsors@anmlfoundation.org)

---

<p align="center">
  © 2026 ANML Foundation · Internet-Draft: draft-jeskey-anml-00
</p>