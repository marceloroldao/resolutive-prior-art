# Claim Chart v0.1 — RM-0001 / MA2A-0002 vs. External Prior Art

**Date:** 2026-08-22  
**Purpose:** technical comparison only; not a legal patentability opinion.  
**Legend:** `PRESENT` = substantially disclosed; `PARTIAL` = related mechanism but materially different scope/role; `ABSENT` = not found in the cited source; `UNCERTAIN` = requires deeper claim/specification review.

## A. RM-0001 — Resolutive Memory Core

| Element | Event Sourcing | Kanerva Sparse Distributed Memory | TrajWiki | A2A Protocol | Preliminary assessment |
|---|---|---|---|---|---|
| Persistent state history/trajectory representation | PRESENT | PARTIAL | PRESENT | ABSENT | Known broadly. |
| Stable address selecting a previously registered memory route | PARTIAL | PARTIAL | PARTIAL | ABSENT | Addressing exists in several forms, but not clearly the same route contract. |
| Explicit separation: semantic discovery/router vs deterministic known-address resolver | ABSENT | ABSENT/PARTIAL | PARTIAL | ABSENT | Stronger differentiator. |
| Known-address resolution without re-running general semantic inference | PARTIAL | PARTIAL | PARTIAL | ABSENT | Caching/indexing is known; the architectural separation is more specific. |
| Trajectory/state record as primary memory abstraction rather than only event log or text record | PARTIAL | PARTIAL | PRESENT | ABSENT | TrajWiki narrows novelty of “trajectory as memory” by itself. |
| LLM optional and outside the final known-route resolution step | ABSENT | N/A | ABSENT/PARTIAL | N/A | Potentially useful differentiator when combined with the router/resolver split. |
| O(1)-average indexed lookup limited strictly to known resolutive address | PARTIAL | PARTIAL | ABSENT | ABSENT | Hash-like lookup is old; no novelty should be claimed for O(1) itself. |
| Unknown condition may invoke external resolver, then validated result becomes reusable route | PARTIAL | ABSENT/PARTIAL | PARTIAL | ABSENT | Combination resembles memoization/learning-from-experience, but exact contract needs deeper search. |

### RM-0001 narrow candidate formulation

The currently strongest technical distinction is not “memory by trajectory” or “fast lookup” alone. It is the combination:

`external observation/query -> route discovery -> stable resolutive address -> deterministic known-route resolution -> optional external resolver only on unresolved cases -> validated route registration for subsequent direct resolution`.

The chart does **not** establish legal novelty. It identifies the element combination that deserves deeper patent/literature searching.

## B. MA2A-0002 — Deterministic State Synchronization

| Element | Event Sourcing / Event Collaboration | US9106721B2 application-state sync | US6725281B1 device-state sync | A2A Protocol | Preliminary assessment |
|---|---|---|---|---|---|
| Synchronization of state changes/deltas | PRESENT | PRESENT | PRESENT | PARTIAL | Clearly known. |
| Version/base-version comparison before application | PARTIAL | PARTIAL | PARTIAL | PARTIAL | Conventional concurrency-control territory. |
| Deterministic conflict classification | PARTIAL | PARTIAL | PARTIAL | PARTIAL | Known broadly; exact policy implementation may differ. |
| Synchronization keyed to stable trajectory/resolutive address | ABSENT/PARTIAL | ABSENT | PARTIAL | ABSENT | More promising distinguishing element. |
| Same address object serves local deterministic retrieval and distributed sync identity | ABSENT | ABSENT | ABSENT/PARTIAL | ABSENT | Stronger combination candidate. |
| LLM judgment excluded from consensus/commit rule | N/A | N/A | N/A | N/A/PARTIAL | Architectural constraint rather than classic sync novelty; useful in AI-agent context. |
| Privacy scope attached to each synchronized trajectory (`private/local/shared/global` or equivalent) | PARTIAL | PARTIAL | PARTIAL | PARTIAL | Access/scope policies are known; exact integration is not enough alone. |
| Agent protocol transmits selected internal trajectory/state deltas rather than requiring task/message exchange | PARTIAL | PRESENT for application state, not AI-agent trajectory semantics | PRESENT for device state | ABSENT by design; A2A emphasizes opaque internal state | Distinguishes from A2A, but state replication itself is old. |
| Local known-route resolver and distributed synchronization operate on the same trajectory-address substrate | ABSENT | ABSENT | ABSENT | ABSENT | Most promising MA2A/RM cross-family combination found so far. |

## C. Important collision sources

### Event Sourcing

Event Sourcing predates the Resolutive work and stores state changes as an ordered event sequence from which past/current state can be reconstructed. It is therefore strong prior art against broad claims around “state as history/trajectory” or replay-based reconstruction.

### Application/device state synchronization patents

US9106721B2 describes monitoring application state, deriving/uploading deltas, storing them in cloud infrastructure, and restoring/synchronizing state across devices. US6725281B1 describes device state synchronization using state tables/eventing and device addressing. These references strongly limit any broad claim to “synchronize device/agent state by delta/address.”

### TrajWiki

TrajWiki (2026) explicitly treats memory as a source-grounded evolution trajectory with immutable snapshots and hierarchical routing. This narrows any claim that “trajectory-based memory” alone is distinctive.

### A2A

The public Agent2Agent protocol intentionally enables independent agents to collaborate without exposing internal memory/state. This provides a useful contrast, not a novelty proof: MA2A's selected trajectory-state synchronization is architecturally different, while generic agent communication is clearly known.

## D. Best current technical differentiation

The strongest candidate is now the **cross-family substrate**, not a single primitive:

1. a state/trajectory is assigned a stable resolutive address;
2. that address selects a previously validated local route deterministically;
3. discovery/semantic interpretation is a separate stage from resolution;
4. unresolved states may be delegated to an external resolver and then registered;
5. selected trajectory-address records are versioned and synchronized across compatible agents;
6. deterministic conflict policy commits updates to that same addressed object;
7. LLM inference is optional at the edge and is not required for the known-route lookup or synchronization consensus path.

No source reviewed in this survey has yet been found to disclose this entire chain as one system. This statement is only a search result, not a legal conclusion.

## E. Search implications

Future searches should avoid broad phrases such as “agent state synchronization” or “trajectory memory,” because those fields are crowded. Prefer compound functional searches around:

- stable address used both for local route resolution and distributed state identity;
- separation of route discovery from deterministic route execution;
- validated fallback-to-route registration;
- synchronization of trajectory-addressed memory objects among AI agents;
- deterministic non-LLM consensus over shared agent-memory trajectories.

## F. Sources reviewed in this chart

- Martin Fowler, *Event Sourcing* (2005) and related event-collaboration material.
- Pentti Kanerva, *Sparse Distributed Memory*.
- TrajWiki: Source-Grounded Memory Trajectories for Long-Horizon Dialogue Agents (2026).
- Agent2Agent (A2A) Protocol Specification.
- US9106721B2, *Application state synchronization across multiple devices*.
- US6725281B1, *Synchronization of controlled device state using state table/eventing*.

Additional historical patents and papers must still be searched before any patentability or freedom-to-operate conclusion.
