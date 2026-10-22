# Amey Parle

AI and data governance, built on agent identity. I work on how an organization proves what its AI systems did, and on whose authority, and I turn that into controls a bank can adopt and an examiner can test.

**Lead maintainer of [`did:trail`](https://github.com/trailprotocol/trail-did-method)**, a W3C-registered DID method for agent identity, and co-author of W3C AI KR Community Group text on what an audit record can establish about an agent's actions.

Looking for AI governance, model risk and data governance roles in the New York metro area.

---

### Governance portfolio: Harbor Federal Bank

A governance program for a fictional mid-size US bank, built against real regulation (SR 26-2, NIST AI RMF, ISO/IEC 42001, the EU AI Act, ECOA/Reg B) and real public data.

**[AI Agent Governance Control Framework](harbor-federal/ai-agent-governance-framework.pdf)** (PDF) — 26 controls across six domains (inventory, identity and delegation, human oversight, testing, monitoring, incident response), scaled by risk tier. SR 26-2 puts agentic AI outside its scope, so banks have to build this governance themselves. Mapped to NIST AI RMF, ISO/IEC 42001 and the EU AI Act, applied to a bank collections agent, and checked against two real incidents: the Replit production-database deletion and *Moffatt v. Air Canada*.

In progress, publishing by Oct 25: AI inventory and risk tiering for 10 banking use cases · fair-lending validation of a credit model (Python, Fairlearn) · data quality scorecard on public HMDA mortgage data.

---

### Standards work

**[RFC 8785 conformance vectors](https://github.com/giskard09/draft-etcheverry-action-ref/tree/main/conformance/trail)** — merged into the `draft-etcheverry-action-ref` IETF draft repo, Sept 2026.

An independent author-set for JSON canonicalization comparison semantics. Anchored to the UTF-8 byte listing published in RFC 8785 §3.2.4 and the property-sorting data in §3.2.3, so the set demonstrates agreement with the reference before reaching cases the reference does not cover. Zero-dependency verifier, 19 assertions.

The set carries two failure classes, and they are not symmetric:

- **Unicode normalization — fails closed.** JCS applies no normalization (§3.1). A subject identifier in precomposed and decomposed form renders identically and canonicalizes to different bytes. A relying party sees a conflict that is not there.
- **Integers above 2^53 — fails open.** `9007199254740993` and `9007199254740992` both serialize to `9007199254740992`. Two subjects, one canonical form. A relying party sees a match that is not there, and nothing in the artefacts indicates it.

Each vector states its failure mode, so the distinction is machine-readable rather than resting on prose. In assurance terms, a fail-open comparison lets an audit record prove the wrong thing without anyone noticing.

**W3C AI KR CG trust-layer crosswalk** — contributed the comparison-semantics column ([issue #10](https://github.com/w3c-cg/aikr/issues/10)), naming the four properties a profile must state for canonicalization to establish anything about subject identity. Named contributor in the group's thread summary.

**[Microsoft Azure Verified Modules](https://github.com/Azure/terraform-azurerm-avm-res-app-managedenvironment)** — root-caused and fixed perpetual Terraform state drift in Azure Container Apps Managed Environments. Cherry-picked with authorship preserved into the official consolidated v0.5.0 release.

---

### did:trail

W3C-registered DID method for non-human and agent identity. I set technical direction, review and merge external contributions, and hold npm publish rights on the [`@trailprotocol`](https://www.npmjs.com/package/@trailprotocol/core) scope.

- Authored the **§5.4.5 reciprocal BindingProof credential** and its TypeScript reference implementation — issue/verify API, Ed25519 signatures, JCS Data Integrity proofs, StatusList2021 revocation, signed test vectors. 80 passing tests, merged into v1.3.0.
- Drove a **normative change to §14.5**: the trust score moved from a float to an integer on 0–100 after I flagged that the signed payload could carry fractional values by spec requirement.
- Own key-rotation and canonicalization decisions, hardening the protocol against replay and re-serialization attacks.

---

### Projects

**[trail-halo-poc](https://github.com/bkuan001/halo-record)** — making an agent's authority provable rather than asserted. Every LLM tool call is gated by a verified reciprocal binding and an org-signed scope grant, then recorded into a tamper-evident hash chain and signed by the agent. Signing keys resolved from DID documents; policy enforcement lives outside the agent process, so authorization is prompt-injection resistant. Adversarial suite covering tamper, wrong-key and forged-grant cases, which exposed an issuer-pinning gap I then closed. Listed in halo-record Community Examples.

**[private-edge-gateway](https://github.com/AmeyParle/private-edge-gateway)** — 21-resource hub-and-spoke Azure reference architecture. App Gateway/WAF v2, Azure Firewall, segmented VNets, NSGs, private VM Scale Set. Zero-trust ingress with zero public IPs, plus incident-recovery runbooks.

---

### Skills

**Governance** NIST AI RMF · ISO/IEC 42001 · EU AI Act · SR 26-2 · model inventory and risk tiering · control design and testing · data quality
**Identity** DIDs · Verifiable Credentials · Ed25519 · JCS · StatusList2021 · JWT · OAuth 2.0 / OIDC · RBAC
**Languages** TypeScript · JavaScript · Python · SQL · Bash
**Backend** Node.js · Express · Prisma · PostgreSQL · REST · OpenAPI
**Agents** MCP · tool-calling loops · Anthropic / Groq / Ollama APIs
**Infra** Azure · Terraform · Docker · GitHub Actions
**Testing** Jest · adversarial and conformance testing

---

M.S. Computer Science, Indiana University Bloomington.
[LinkedIn](https://linkedin.com/in/amey-parle) · ameyparle@gmail.com
