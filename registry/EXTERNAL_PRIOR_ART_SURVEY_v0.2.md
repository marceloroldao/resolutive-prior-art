# External Prior-Art Survey v0.2 — Resolutive Memory and MA2A

**Date:** 2026-08-22  
**Scope:** RF-0001, RM-0001, RM-0002, MA2A-0001, MA2A-0002  
**Status:** research survey; not a legal opinion and not a patentability determination.

## 1. Objective

This survey narrows the external prior-art search from product-level similarity to mechanism-level overlap. The principal question is not whether earlier systems used memory, state, trajectories, synchronization, event logs, content addressing, or multi-agent communication individually. Those are well-established classes. The relevant question is whether earlier work discloses the same technical organization used by the Resolutive family:

`observed state/relation -> resolutive address -> deterministic known-route resolution -> reusable route/trajectory -> selective state/trajectory synchronization between compatible agents`

with semantic or neural inference separated from the final known-address resolution step.

## 2. Strong historical prior art identified

### 2.1 Content-addressable and associative memory

Content-addressable memory and associative memory long predate the Resolutive work. Earlier systems retrieve data from content or similarity rather than only a conventional storage location. Kanerva's Sparse Distributed Memory (1980s) also defines a high-dimensional address space and associative recall, including sequence-memory extensions.

**Consequence for claims:** Resolutive Memory must not claim invention of associative addressing, content-addressable retrieval, high-dimensional address spaces, or sequence storage in general.

**Remaining distinction:** RM-0001 explicitly separates route discovery from route resolution and treats the resolved object as a reusable deterministic state/trajectory route rather than primarily a similarity-recalled content item.

### 2.2 Event Sourcing

Event Sourcing, documented publicly at least by 2005 and rooted in earlier event-log techniques, stores state changes as an ordered event sequence and permits reconstruction of current or historical application state by replay.

**Consequence for claims:** The Resolutive family must not claim invention of storing transitions, replaying transitions, reconstructing state from a sequence of events, snapshots, or temporal branching.

**Remaining distinction:** Resolutive trajectory addressing is framed as a lookup/resolution substrate in which a known address selects a previously established route/trajectory. Event Sourcing normally treats the event stream as the authoritative history from which aggregate state is rebuilt; it does not by itself disclose a semantic-discovery boundary followed by constant-average-time address resolution of a learned reusable route.

### 2.3 Agent state synchronization — NTT patent family

A highly relevant historical patent is **JPH11316745A**, priority **1998-04-30**, titled approximately *Agent state synchronization method and system*. It describes distributed agents, stored message communication histories, restoration after failure, synchronization of agent state with a database, and exchange/replay of past messages to recover the latest local state.

This is strong prior art against any broad statement that MA2A invented "agent state synchronization," "synchronizing agent state with a database," or "recovering an agent through communication-history replay."

**Important distinction:** the identified NTT mechanism is failure-recovery/message-history synchronization. MA2A-0002 instead specifies normal-operation versioned trajectory deltas attached to resolutive trajectory addresses, explicit privacy scopes, deterministic conflict policy, and selective replication of compatible resolutive state. This difference should remain explicit in all future claims.

### 2.4 General multi-agent synchronization

Multi-agent systems literature has long studied consensus, trajectory synchronization, state agreement, distributed control, and privacy-preserving synchronization. This body of work is extensive and predates modern LLM agents.

**Consequence for claims:** MA2A must not claim invention of consensus, trajectory synchronization in control systems, synchronization among autonomous agents, logical clocks, deterministic conflict resolution, or distributed state convergence in general.

### 2.5 FIPA ACL and earlier agent communication protocols

FIPA ACL and KQML established structured inter-agent communication decades before modern LLM-agent protocols.

**Consequence for claims:** MA2A must not claim invention of structured software-agent communication, agent identities, message envelopes, request/response semantics, capability negotiation, or agent discovery in general.

## 3. Recent nearby work

### 3.1 Trajectory-based agent memory

Recent work such as **TrajWiki (2026)** explicitly models memory as source-grounded evolution trajectories rather than static records. It maintains episodic snapshots and claim-level evolution, then routes queries through structured memory layers to linked trajectories.

This is materially closer to RM-0002 terminology than generic vector memory.

**Implication:** Future Resolutive disclosures should avoid claiming that "memory as trajectory" alone is novel. The distinction must be in the deterministic state-transition/addressing construction, exact retrieval contract, reversible or constrained trajectory machinery where demonstrated, and its integration with resolutive route reuse.

### 3.2 State-first / governed persistent memory

Recent systems explicitly treat memory as evolving governed state, including supersession, lifecycle state, conflict handling, and fail-closed retrieval/release.

**Implication:** State tracking, stale-state rejection, provenance, and deterministic memory governance are now active prior-art territory. Resolutive claims must focus on the address/route/trajectory substrate and the separation of discovery from resolution rather than on "stateful memory" broadly.

### 3.3 Shared state in agent protocols

AG-UI and other protocols define snapshots, deltas, and shared state synchronization between an agent and another software component. Recent multi-agent work also exchanges compressed state summaries to limit context drift.

**Implication:** State snapshots, state deltas, compressed summaries, and incremental synchronization cannot carry novelty alone.

## 4. Patent-near trajectory prior art

A recent example, **US20260003328A1**, discloses memory-based learning controllers that store sets of trajectories connecting initial states to target states and derive a control policy based on a current state.

This is strong neighboring art for trajectory-memory/control, but it is not the same as RM-0001's known-address deterministic memory resolver or MA2A's selective trajectory-state synchronization.

**Consequence:** Avoid broad claims such as "storing trajectories in memory and selecting a trajectory from a current state."

## 5. Claim decomposition

The following components are individually well established and should be treated as prior-art primitives:

| Primitive | Prior-art strength | Safe conclusion |
|---|---:|---|
| Hash/indexed O(1)-average lookup | Very strong | Not novel alone |
| Content-addressed memory | Very strong | Not novel alone |
| Associative memory | Very strong | Not novel alone |
| State machines / deterministic transitions | Very strong | Not novel alone |
| Sequence / trajectory memory | Strong | Not novel alone |
| Event replay / event sourcing | Very strong | Not novel alone |
| Agent communication protocols | Very strong | Not novel alone |
| Agent state synchronization | Very strong | Not novel alone |
| Snapshots and deltas | Very strong | Not novel alone |
| CRDT / deterministic convergence concepts | Very strong | Not novel alone |
| PKI / Ed25519 identity | Very strong | Not novel alone |
| Privacy scopes / ACLs | Very strong | Not novel alone |

## 6. Candidate distinctive combination

The most defensible technical distinction currently appears to be the **specific composition**:

1. an external observation/query is mapped to a finite state/relation representation;
2. a discovery/router stage maps that representation to a resolutive address;
3. the address resolves a previously registered deterministic route/trajectory directly;
4. the route may encode payload, next state, action, or delegated resolver;
5. unresolved observations may use a separate expensive/neural/external resolver;
6. validated results can become new registered routes;
7. compatible agents can synchronize selected versioned trajectory/address state rather than requiring natural-language reconstruction;
8. privacy scope is attached to the synchronized state/trajectory object;
9. synchronization and conflict handling are deterministic and separate from LLM judgment.

No single source identified in this survey has yet been found to disclose this exact full chain as one architecture.

That is **not** a legal conclusion of novelty. It is a technical search finding that justifies more focused claim-chart work.

## 7. Distinctions to preserve in future documents

### RM-0001

Use:

`semantic/observation discovery -> resolutive address -> deterministic route resolution`

Do not reduce RM-0001 to "associative memory," "content addressing," or "state lookup."

### RM-0002

Use:

`information-bearing deterministic state relations + explicitly defined sufficient trajectory descriptor + independently verified recovery`

Only strengthen this claim after reproducible recovery evidence exists. "Memory as trajectory" alone is no longer a strong novelty position.

### MA2A-0001/0002

Use:

`selective synchronization of versioned resolutive trajectory/address state between compatible agents, with deterministic conflict policy and explicit privacy scope`

Do not claim generic "agent state synchronization." The 1998 NTT patent is clear prior art for that broad formulation.

## 8. Risk assessment

### High collision risk

- generic state synchronization;
- event replay;
- content/associative addressing;
- trajectory memory in the abstract;
- delta synchronization;
- PKI hierarchy;
- deterministic conflict resolution in distributed systems.

### Moderate collision risk

- state-first agent memory;
- trajectory-based LLM-agent memory;
- persistent governed memory;
- deterministic agent-memory updates;
- shared agent state with snapshots/deltas.

### Lower apparent collision risk in this search

- the complete discovery/resolution separation coupled to resolutive route registration and reuse;
- using the same trajectory/address abstraction as both the local deterministic memory-resolution substrate and the selectively synchronized inter-agent state unit;
- edge-local semantic/LLM interpretation with a non-LLM synchronization plane that exchanges resolutive state objects rather than requiring natural-language agent context reconstruction.

"Lower apparent collision risk" means only that this search did not find a direct anticipatory source. It does not establish patentability or freedom to operate.

## 9. Next search targets

A later survey should create element-by-element claim charts against:

1. JPH11316745A — agent state synchronization/failure recovery;
2. Event Sourcing and event-log state reconstruction;
3. Kanerva Sparse Distributed Memory and associative sequence retrieval;
4. trajectory-memory systems including TrajWiki;
5. modern state-first/governed agent memory;
6. AG-UI and related shared-state delta protocols;
7. current A2A/MCP-style agent interoperability specifications;
8. CRDT/MVCC/event-sourced convergence systems;
9. patents combining persistent AI-agent memory with distributed synchronization.

## 10. Current technical conclusion

The external search weakens any broad novelty claim around individual primitives, which is expected and healthy. At the same time, it sharpens the candidate contribution of the Resolutive architecture.

The strongest current formulation is not:

> agents have memory and synchronize state.

It is closer to:

> a system in which discovered conditions are compiled into persistent resolutive addresses that directly select reusable deterministic state/trajectory routes, and in which those addressed trajectory objects can themselves become the versioned, policy-scoped synchronization unit among compatible agents, while semantic/neural inference remains outside the known-route resolution and synchronization fast path.

That formulation should guide future RF/RM/MA2A disclosures and any professional patentability review.
