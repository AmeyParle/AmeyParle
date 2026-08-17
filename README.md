# Amey Parle

**Backend Engineer — identity & auth for AI agents.** Node/TypeScript, Python.
MSCS, Indiana University.

I build backend systems and the identity layer underneath them — APIs, auth,
and cryptographic verification for AI agents acting on behalf of organizations.
First external contributor to the TRAIL Protocol, a W3C-track DID method for
agent identity.

## What I work on

- **Agent identity & authorization** — DIDs, verifiable credentials, reciprocal
  binding, scoped authority, delegation
- **Backend & APIs** — Node/TypeScript, Express, Prisma, PostgreSQL, Python
- **Cloud & infra** — Azure, Terraform, Docker, zero-trust networking

## Selected work

### TRAIL Protocol — collaborator
A W3C-track DID method for AI agents. I authored the §5.4.5 reciprocal
`BindingProof` credential (shipped in `@trailprotocol/core` on npm) and drove a
normative change to §14.5 — the trust score moved from a float to an integer on
0–100 after I flagged that the signed payload could carry fractional values by
spec requirement. Credited in the changelog.
🔗 github.com/trailprotocol/trail-did-method · npmjs.com/package/@trailprotocol/core

### Provable agent authority (TRAIL + Halo)
A working proof-of-concept making an agent's authority *provable* rather than
asserted: a real LLM agent's tool calls are gated by a reciprocal binding and an
org-signed scope grant, recorded into a tamper-evident hash chain, each record
signed by the agent. Keys resolved from DID documents; forged grants rejected;
adversarial test suite included.
🔗 github.com/AmeyParle/trail-halo-poc

### IncidentHub API
Incident-management backend — Node.js, Express, Prisma, PostgreSQL, JWT auth,
OpenAPI. Deployed on Render + Neon.
🔗 github.com/AmeyParle/incidenthub-api

### Azure Private Edge Gateway
Production-style secure cloud architecture — hub-spoke VNet, App Gateway WAF as
single entry point, VMSS with no public IP, Azure Firewall.
🔗 github.com/AmeyParle/private-edge-gateway

## Stack

**Languages:** TypeScript, JavaScript, Python
**Backend:** Node.js, Express, Prisma, PostgreSQL, REST, OpenAPI
**Identity:** DIDs, Verifiable Credentials, Ed25519 / JCS, JWT
**Cloud & infra:** Azure, Terraform, Docker, Linux

## Connect
LinkedIn: linkedin.com/in/amey-parle · GitHub: github.com/AmeyParle
