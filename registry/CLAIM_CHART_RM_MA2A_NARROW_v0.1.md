# Narrow Claim Chart — RM↔MA2A Combined Mechanism v0.1

**Date:** 2026-08-22  
**Scope:** Technical prior-art comparison only; not a legal opinion on novelty, patentability, infringement, or freedom to operate.

## 1. Candidate combined mechanism

The narrow candidate mechanism being evaluated is the following chain:

1. an observation or known condition is mapped to a stable resolutive address;
2. the address identifies a trajectory/state route already registered in local memory;
3. a known address is resolved deterministically without requiring a new semantic/LLM inference for the route lookup itself;
4. when no route exists, an external resolver may produce a result that is validated and compiled/registered as a route under an address;
5. the same logical resolutive address, or a protocol-stable derivative of it, identifies the memory/trajectory object for inter-agent synchronization;
6. agents synchronize selected deltas/version metadata for that addressed object rather than requiring full natural-language context exchange;
7. conflicts over the addressed object are handled by an explicit deterministic policy; and
8. privacy scope controls whether the addressed object is eligible for synchronization.

The candidate distinction is the **integration of local deterministic route resolution and distributed synchronization around the same stable trajectory/state identity**. No novelty claim is made for any isolated primitive.

## 2. Symbols

- **P** — substantially present in the reference.
- **p** — partially or analogously present.
- **A** — not found in the reviewed material.
- **?** — uncertain; deeper claim/specification review required.

## 3. References reviewed in this narrow round

### R1 — Scalable synchronization mechanism for distributed memory
Patent family including EP3234786 and CN107003941. The reviewed claims describe private/global address spaces, agents writing shared data, synchronization-event objects, and generation of completion events when shared/global memory state has synchronized.

### R2 — Replay-memory trajectory addressing
US20220366235A1. The reviewed disclosure stores agent trajectories in replay memory, subdivides trajectories into trajectory data elements, and represents trajectories using sequences of pointers referencing memory slots/addresses.

### R3 — Directory/home-agent memory coherence
Examples include US8327228B2 and US8799586B2. Memory addresses identify data locations/home nodes, and agents coordinate coherent access/mirroring to memory objects.

### R4 — Distributed object identity / location transparency
CA2162188C. Distributed objects have identifiers/addresses, local calls can be resolved locally, and remote calls locate and invoke addressed objects according to policy.

### R5 — Prior agent-state synchronization reference
JPH11316745A, identified in the earlier survey as an early agent-state synchronization system involving agent state/history and recovery/synchronization concepts.

## 4. Element-by-element chart

| Element | RM/MA2A formulation | R1 distributed shared memory | R2 replay trajectories | R3 home-agent coherence | R4 distributed objects | R5 agent-state sync |
|---|---|---:|---:|---:|---:|---:|
| E1 | Stable identifier/address for a memory/state/trajectory object | P | P | P | P | p/? |
| E2 | Object represents a trajectory/state route, not only a raw memory location | p | P | A/p | p | p/? |
| E3 | Known address resolves a previously registered route deterministically | p | p | P for data lookup, not semantic route | P for object call | p/? |
| E4 | Explicit separation: semantic discovery may be expensive, known-address resolution is distinct | A | A | A | p (local/remote resolution distinction, not semantic discovery) | A/? |
| E5 | Unknown condition may invoke external resolver, then validated result becomes a reusable route | A | A | A | A | ? |
| E6 | Same logical address/identity used for local route resolution and synchronization of that object | p | p | p | p | p/? |
| E7 | Delta/version synchronization of the addressed trajectory/state object | P | A/p | P/p | p | P/p |
| E8 | Deterministic conflict policy attached to the addressed trajectory object | p | A | p (coherence rules) | p | ? |
| E9 | Explicit privacy/replication scope attached to the same object | p (private/global address spaces) | A | A/p | p policy metadata | ? |
| E10 | Inter-agent transport can synchronize state/delta without requiring natural-language prompt exchange | P at machine-memory level | P at machine-memory level | P | P | P/p |
| E11 | LLM/semantic inference is optional and outside known-route fast path | A | A | A | A | A |
| E12 | Route registration creates a persistent future fast path for the same condition/address | A/p | A | A | A/p caching-like analogy | ? |

## 5. Closest collisions

### 5.1 R1 is the closest collision on shared addressed state

R1 materially narrows any broad claim such as:

> agents synchronize addressed objects between private and global memory spaces.

That is not a safe novelty formulation. R1 already discloses agents, shared/global address spaces, synchronized objects, synchronization metadata/event objects, and completion signaling.

The remaining distinction must therefore come from what the addressed object **means and does** in the Resolutive architecture: it is not merely a shared memory object; it is also a local trajectory/route identity used by the deterministic resolver.

### 5.2 R2 is the closest collision on trajectory + memory address

R2 materially narrows claims such as:

> an agent trajectory is represented by memory addresses/pointers.

That combination already exists in replay-memory systems. RM must therefore avoid treating “trajectory + address” alone as the inventive center.

The proposed distinction is that the address is not simply a pointer to stored trajectory elements for later learning. It is a persistent **resolution route identity** and also a candidate synchronization identity across compatible agents.

### 5.3 R3 narrows address-based coherent access

Home-agent/cache-coherence systems already use addresses as stable identities around which distributed agents coordinate most-recent state, ownership, invalidation, and mirroring. Therefore:

> same address used by multiple agents to maintain coherent state

is too broad by itself.

The candidate distinction must remain tied to resolutive route semantics and optional inference fallback/registration.

### 5.4 R4 narrows local-first addressed-object invocation

R4 demonstrates that an object identifier may resolve locally when possible and otherwise be found/invoked remotely. This is conceptually close to a local fast path plus remote fallback.

However, in the reviewed material, the distinction is location transparency for distributed service objects. It does not disclose a semantic condition being compiled into a persistent trajectory route, nor the same route identity becoming a state/delta synchronization unit after external resolution.

## 6. Narrow candidate differentiation

After the reviewed collisions, the strongest remaining candidate is not any single one of E1–E12. It is the following combination:

```text
external condition
      ↓
route discovery / mapping
      ↓
stable trajectory-state address
      ↓
known-address deterministic local resolution
      ↓
if unknown: external resolver → validation → route registration
      ↓
same route identity becomes synchronizable object
      ↓
versioned delta + deterministic conflict policy + privacy scope
```

The technically important coupling is:

> **the identity used to resolve a known local memory route is also the identity around which compatible agents synchronize the corresponding selected state/trajectory object.**

The reviewed references separately disclose addressable memory, distributed synchronization, trajectory storage, agent state synchronization, and local/remote object resolution. In this limited search, no single reviewed reference clearly discloses the complete chain including (a) semantic/discovery separation, (b) persistent deterministic route registration/resolution, and (c) reuse of that route identity as the distributed synchronization object.

This is a search result, not a legal conclusion.

## 7. Formulations to avoid

The following formulations are too broad given the reviewed prior art:

- "synchronizing memory between agents";
- "using addresses to synchronize distributed objects";
- "storing agent trajectories under memory addresses";
- "using a global and private memory space";
- "resolving an object locally or remotely";
- "using deterministic conflict resolution";
- "using PKI to authorize agents";
- "using O(1) hash lookup for memory".

## 8. Safer technical formulation for future disclosures

A future disclosure should specify the mechanism approximately as follows:

> A memory system in which an external condition is mapped to a stable trajectory-state address; a previously registered address selects a deterministic executable/retrievable resolution route without requiring renewed semantic inference for the route lookup; unresolved conditions may be delegated to an external resolver whose validated result is registered as a new persistent route; and the same route identity, or a deterministic protocol-stable derivative, serves as the identity of a versioned state/trajectory object that compatible agents synchronize under explicit privacy and deterministic conflict policies.

The actual implementation must define:

1. exact address derivation/allocation semantics;
2. what state/trajectory material the address identifies;
3. conditions under which two agents consider addresses equivalent;
4. how a route is registered after fallback resolution;
5. how route identity maps to the MA2A trajectory address;
6. how versions/deltas are formed;
7. conflict rules and their versioning;
8. privacy-scope transitions; and
9. behavior under stale, unknown, revoked, or colliding addresses.

## 9. Evidence gap

The main present weakness is implementation coupling. RM-0001 and MA2A are specified, but the novelty candidate becomes much stronger as a technical disclosure if a reproducible prototype demonstrates the complete loop:

```text
unknown observation
→ external resolution
→ route registration
→ subsequent deterministic local hit
→ export selected route identity/delta
→ second agent imports it
→ second agent performs the same known-address resolution
```

That end-to-end experiment should measure:

- bytes synchronized;
- route-hit latency before/after learning;
- number of LLM/model calls avoided on repeated known conditions;
- synchronization convergence;
- collision/unknown handling;
- scope enforcement; and
- behavior after concurrent updates.

## 10. Current assessment

**Overlap risk for broad claims:** HIGH.  
**Differentiation of isolated primitives:** LOW to MODERATE.  
**Differentiation of the narrow integrated RM↔MA2A chain:** MODERATE based on the present search.  
**Confidence:** preliminary; patent-classification/citation-chain searching is still required.

The highest-value next technical action is to implement and freeze the end-to-end RM↔MA2A route-transfer experiment described in Section 9, because it turns the remaining differentiation from an architectural sentence into a reproducible mechanism.
