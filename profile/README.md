<div align="center">

# provin

_Technology opens what **CAN** be. The market chooses what **SHOULD** be._
_Regulation carves what **MUST** be — then the market asks technology for the next **CAN**._

**Provenance has long only marked the points regulation demands.**
**But no matter how many points you stack, you never draw the line.**
**Continuous provenance — proving the line, not the points. That is the next CAN.**

The reference implementation of continuous provenance.

</div>

---

## What this is

**provin** makes _continuous provenance_ run. At every boundary where data is received or
transformed, it records — in a tamper-evident form — _who received what, what was done to it, and
what was passed on_ — and binds each record to the one before it into a single verifiable **line**.

Anyone can verify that line independently, across organizations — without a central trust authority.
A convincing point is cheap to forge; a connected line is not — it would take the keys of every
boundary it crossed and consistency with records already held downstream.

## What it does — and does not — promise

- ✅ **Authenticity and continuity** of the record: each link is signed, and the chain is unbroken and independently checkable.
- ❌ **Not** the truth of the contents. If a source records a wrong value, the value stays wrong even when the line is complete.
- It **complements** existing provenance standards rather than competing with them — it fills the layer of _continuity between boundaries_ that they leave out of scope.

## Protocol

provin is the reference implementation of **[dPLaaX](https://github.com/dplaax)** — the open protocol that defines continuous provenance.

## Status

Coming soon.
