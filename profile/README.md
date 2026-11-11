<div align="center">

# provin

**prove your data into line.**

_Continuous provenance for data that crosses organizational boundaries —
every handoff signed, every claim attributable, no central operator._

</div>

---

## Why

You cannot prove that content is true. Not because the technology is
immature — because it is impossible in principle. AI turned this limit from
an exception into the default: unverifiable stages — model inference, human
judgment — are now standard pipeline components, and forging a plausible
artifact costs nearly nothing. _"It looks right"_ stopped being evidence.

If content cannot be guaranteed, one lever remains: **raising the
after-the-fact cost of a lie**. That cost only lands with attribution — a lie
no one can be pinned to cannot be punished, sued, or priced into a
reputation. And between organizations that refuse a central operator,
attribution must be carried by the records themselves: **signed at every
boundary they cross, each record bound to the one before it**.

This deterrence has preconditions — it only reaches parties with an identity
worth protecting. Between companies, those preconditions already hold. A
company _is_ accumulated credibility it cannot afford to lose, and
inter-company economy has always run on promises staked on a name.
Contracts, audits, double-entry books: none of them prove content true.
**They make lies attributable.** provin extends that machinery to data
pipelines.

> **Trust is not a guarantee of truth. It is the attributability of lies.**

## What runs here

| Repository | What it is |
| --- | --- |
| [**oss**](https://github.com/provin-line/oss) | The engine. Control plane (`cmd/network`) + data plane (`cmd/pipeline`) — Go, Ed25519, W3C Verifiable Credentials, `did:dplaax`. |
| [**profile.spec**](https://github.com/provin-line/profile.spec) | The normative wire profile — the claim registry the dPLaaX protocol delegates to this profile. |
| [**e2e**](https://github.com/provin-line/e2e) | Three-organization end-to-end tests: forge a payload mid-chain, watch delivery stop. |
| [**bench**](https://github.com/provin-line/bench) | The gate-scaling measurement harness — where the µs/credential numbers come from. |
| [**auth**](https://github.com/provin-line/auth) | DID-grant auth provider + reference policy verifier for the fail-closed node. |
| [**site**](https://github.com/provin-line/site) | [www.provin.dev](https://www.provin.dev) — the public-facing site. |

Self-hosting? [`oss/deploy/quickstart`](https://github.com/provin-line/oss/tree/main/deploy/quickstart)
stands up the full authenticated stack — provider, policy verifier, node, NATS —
and drives a record to a `VERIFIED` verdict.

## What it promises — and what it doesn't

- ✅ **Authenticity, continuity, attribution.** Every link signed; the chain
  unbroken and independently checkable — across organizations, with no
  central trust authority.
- ❌ **Not the truth of the contents.** A wrong value, correctly signed,
  stays wrong — and stays _attributed_. That asymmetry is not a gap in the
  design; it is the design.
- It **complements** existing provenance standards — it fills the layer they
  leave out of scope: continuity between boundaries.

## Protocol

provin is the reference implementation of
[**dPLaaX**](https://github.com/dplaax) — the open protocol that defines
continuous provenance. Wire semantics start in the spec, not in this
implementation.

## Status

**Working proof-of-concept — versioned, measured, and evaluated in public.**

- [provin oss v0.4.0](https://github.com/provin-line/oss/releases/tag/v0.4.0) — the current release
- [provin oss v0.3.0](https://github.com/provin-line/oss) — the revision line evaluated in the systems paper
- [dPLaaX spec v0.2.0-alpha.1](https://github.com/dplaax/spec) (pre-release) — public review welcome
- [Systems paper](https://doi.org/10.5281/zenodo.21853326) — acceptance decisions at delivery time, evaluated on
  public snapshots _(preprint)_
