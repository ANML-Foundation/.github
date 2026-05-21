# ANML Foundation

**ANML** (Agentic Notation Markup Language) is an open, machine-first document format for agent-to-agent and agent-to-service communication on the web.

Pronounced "animal" — `/ˈæn.ɪ.məl/`

---

### The agentic web needs its own native format

The graphical web was built for humans with browsers. The agentic web — where autonomous agents act on behalf of users — needs something different. Agents don't need hero images, cookie banners, or responsive layouts. They need structured meaning: what is this service, what can I do here, what are the rules, and how do I act on behalf of my user.

ANML is that format. A single duckument tells any agent — from any vendor — everything it needs to understand a service without inference over unstructured markup.

### What an ANML duckument provides

- **Content** — structured, semantic information for machine interpretation
- **Interactions** — operations bound to HTTP methods and endpoints
- **Knowledge** — bidirectional information exchange with TTLs and confidentiality
- **Constraints** — disclosure and consent rules agents must evaluate before sharing data
- **State** — workflow context showing where the user is in a multi-step process
- **Persona** — behavioral and tonal guidance for how agents represent the service

### Links

- 🌐 [anmlfoundation.org](https://anmlfoundation.org)
- 📄 [IETF Internet-Draft](https://datatracker.ietf.org/doc/draft-jeskey-anml/)
- 📖 [Why ANML?](https://anmlfoundation.org/why-anml)
- 📬 [sponsors@anmlfoundation.org](mailto:sponsors@anmlfoundation.org)

### Official SDKs

| Package | Language | Install |
|---|---|---|
| [anml-client-python](https://github.com/ANML-Foundation/anml-client-python) | Python | `pip install anml-client` |
| [anml-server-python](https://github.com/ANML-Foundation/anml-server-python) | Python | `pip install anml-server` |
| [anml-client-node](https://github.com/ANML-Foundation/anml-client-node) | TypeScript | `npm install @anml-foundation/client` |
| [anml-server-node](https://github.com/ANML-Foundation/anml-server-node) | TypeScript | `npm install @anml-foundation/server` |
| [anml-client-rust](https://github.com/ANML-Foundation/anml-client-rust) | Rust | `cargo add anml-client` |
| [anml-server-rust](https://github.com/ANML-Foundation/anml-server-rust) | Rust | `cargo add anml-server` |

### Status

ANML is an active Internet-Draft (`draft-jeskey-anml-00`) submitted to the IETF. We're looking for early adopters, contributors, and sponsors to help shape the standard.

