# External Prior-Art Survey v0.3

**Date:** 2026-09-05  
**Scope:** RM-0003, RF-0002, RT-0002  
**Purpose:** focused technical novelty screening before the proposed `v0.2.0` archival snapshot.  
**Status:** technical survey only; not a legal opinion, patentability determination, or freedom-to-operate analysis.

## Method

The search targeted mechanisms rather than project names. Each disclosure was decomposed into its functional chain, then compared against recent patent publications, technical systems, and established literature.

The survey distinguishes:

- **known primitive** — widely established component;
- **close combination** — materially overlaps several elements of the disclosure;
- **remaining differentiation** — narrower organization or execution path not found as a single clearly anticipatory source in this limited search;
- **high-risk broad claim** — wording that should not be used as an invention claim without further legal analysis.

---

# 1. RM-0003 — Persistent Concept Identity and Deterministic Concept-Relation Resolution

## RM-0003 functional chain under review

```text
surface expression
  -> deterministic normalization / alias mapping
  -> stable concept identity independent of wording
  -> explicit ambiguity / contextual-sense handling
  -> durable concept persistence
  -> typed concept relations
  -> bounded relation traversal
  -> native/local materialization
  -> deterministic HIT or explicit UNRESOLVED
  -> semantic fallback only after miss
```

## Strong prior-art overlap

### Stable identity independent of labels

Stable concept/entity identifiers separate from names are well established in knowledge graphs, ontologies, entity-resolution systems, and modern agent-memory tooling. Recent systems explicitly describe many surface forms or aliases resolving to one stable concept/entity identifier.

**Assessment:** known primitive / high overlap.

Do not broadly claim invention of:

- persistent concept IDs;
- aliases mapping to stable identities;
- renaming while preserving identity;
- homonym/sense separation by itself.

### Ontology dictionaries with concept IDs, relationships, alias tables and indexed lookup

Recent patent literature describes concept dictionaries in which each record has a concept identifier, attributes, typed relationships, alias/synonym/canonicalization tables, and indexed lookup structures. Some disclosures further connect these concepts to runtime caching, routing, or resource allocation.

**Assessment:** close combination.

This materially narrows any claim based only on:

```text
concept ID + aliases + typed relations + indexed lookup
```

### Durable semantic identity reused across systems

Recent semantic-registry systems explicitly describe reviewed concept codes/IDs written into durable memory and reused across sessions, languages, models, APIs, events, and audits.

**Assessment:** close overlap with the persistence/identity part of RM-0003.

## Remaining differentiation worth preserving

The narrower RM-0003 combination that remains technically interesting is not merely stable concept identity. It is the execution architecture in which:

1. the memory system persists concept state as authoritative durable records;
2. that state is materialized into a native execution index;
3. local/native deterministic resolution is attempted first;
4. ambiguity fails closed rather than inventing an identity;
5. exact concept or bounded relation-path resolution returns an auditable path;
6. semantic/model fallback occurs only after explicit local miss;
7. persisted state survives restart and rematerializes into the native resolver.

This sequence should be described as a concrete pipeline rather than as ownership of its individual primitives.

### Recommended claim discipline

Prefer wording such as:

> A memory execution architecture in which authoritative persisted concept identities and relation state are deterministically materialized into a native local resolver that returns HIT or UNRESOLVED under fail-closed ambiguity rules before optional semantic fallback.

Avoid wording such as:

> An invention of stable concept identity, aliases, ontology lookup, or concept graphs.

## RM-0003 preliminary rating

- Primitive novelty: **low**
- Combination distinctiveness: **moderate**
- Risk of broad-claim collision: **high**
- Value as defensive technical disclosure: **high**, if implementation commits and restart/E2E evidence are pinned

---

# 2. RF-0002 — Policy-First Resolutive Routing Across Knowledge and Compute

## RF-0002 functional chain under review

```text
request
  -> privacy / authorization / locality admissibility filter
  -> knowledge-availability candidates
  -> capability / model / hardware candidates
  -> load / latency / distance / cost / energy / reputation factors
  -> deterministic or explainable ranking
  -> select admissible route without global broadcast
  -> execute locally or remotely
  -> record measurable contribution / resource ledger
  -> explicit fallback if no admissible route exists
```

## Strong prior-art overlap

### Agent routing by capability, latency, cost and policy

Contemporary agent-routing patents and products already rank agents or compute nodes using capability metadata, latency, cost, historical performance, resource usage, security clearance, data classification, locality, and regulatory constraints.

**Assessment:** very close combination.

Do not broadly claim invention of:

- capability-aware agent routing;
- latency-aware or cost-aware routing;
- privacy-aware compute placement;
- routing across heterogeneous agents/nodes;
- routing rules that filter ineligible agents before ranking.

### "Policy-first routing"

The phrase itself is now used publicly in modern model-routing systems to describe authorization, locality, data-handling and capability constraints applied before latency/cost/quality optimization.

**Assessment:** terminology collision is strong.

The repository may continue using the phrase descriptively, but it should not be treated as proprietary novelty.

### Context-preserving agent routing

Recent patent literature also covers shared context objects, capability profiles, access scopes, privacy/redaction rules, heterogeneous execution environments, and failure rerouting.

**Assessment:** close overlap with the orchestration portion of RF-0002.

## Remaining differentiation worth preserving

The strongest narrower RF-0002 distinction is the **joint routing of knowledge and compute under the same admissibility model**, combined with the Resolutive/M2A2 architecture:

1. first ask whether a known memory/knowledge route already resolves the request;
2. if not, select an admissible resolver/compute node;
3. enforce privacy scope before optimization;
4. avoid global broadcast when learned knowledge-density/capability information identifies promising nodes;
5. treat memory retrieval, public knowledge, local LLM, remote LLM and general compute as alternative route classes;
6. retain separate auditable compute/storage/knowledge contribution ledgers rather than equating value to model token count;
7. keep identity/transport in MA2A and memory semantics in Memoria.ia, leaving routing as a separate decision layer.

This architecture is more specific than generic model routing.

### Recommended claim discipline

Prefer wording such as:

> A routing layer that selects among memory, knowledge and compute resolution routes after enforcing scope admissibility, while preserving separate memory, identity/transport and routing responsibilities and avoiding broadcast when sufficient learned route information exists.

Avoid wording such as:

> An invention of policy-first routing, agent selection, cost-aware routing, privacy-aware routing or heterogeneous compute scheduling.

## RF-0002 preliminary rating

- Primitive novelty: **low**
- Combination distinctiveness: **low-to-moderate**
- Risk of broad-claim collision: **very high**
- Defensive-disclosure value: **moderate-to-high**, if scoped specifically to the Resolutive/M2A2 division of responsibilities and knowledge+compute route unification

---

# 3. RT-0002 — Information-Event Time and Recurrent Macrograph Structure

## RT-0002 functional chain under review

```text
finite deterministic/stochastic trajectory system
  -> identify recurrent causal core
  -> distinguish deterministic flights from branch points
  -> collapse deterministic flights into variable-length macro edges
  -> define event index k distinct from physical step index t
  -> associate entropy primarily with branch events
  -> compute mean physical duration per event
  -> recover physical-time entropy rate from event entropy / mean duration
  -> use the macrograph as a candidate operational rank/unrank codec
```

## Strong theoretical antecedents

### Semi-Markov processes and entropy rate

Semi-Markov theory has long separated state transitions from variable sojourn durations and has established entropy-rate formulae for processes with nonuniform transition times.

**Assessment:** strong mathematical antecedent.

Therefore the following are not novel by themselves:

- variable-duration transitions;
- entropy rates for processes with nonuniform event durations;
- distinguishing transition/event count from physical time.

### Computational mechanics / epsilon-machines

Computational mechanics establishes causal states, recurrent predictive structure, minimal unifilar presentations, and entropy rate derived from transition structure. Hidden semi-Markov and renewal-process work also develops informational and causal architecture in continuous or variable-duration settings.

**Assessment:** strong conceptual antecedent.

Do not claim invention of:

- causal states;
- recurrent-state models;
- entropy rate from finite-state transition structure;
- event-time descriptions in stochastic processes.

## Remaining differentiation worth preserving

RT-0002 remains the least crowded of the three disclosures when stated concretely as the discovered structure of the specific trajectory universe:

1. a tested recurrent basin is reduced to a small causal core;
2. most physical transitions are deterministic consequences of public dynamics;
3. only a small subset of recurrent states introduce branch entropy;
4. deterministic flights between branch states are collapsed into a variable-length macrograph;
5. the macrograph reproduces the same asymptotic physical-time growth/entropy rate as the underlying recurrent dynamics;
6. event entropy divided by measured mean physical flight length returns the physical-time information rate;
7. the proposed next step is not merely analysis but an exact rank/unrank codec over admissible recurrent trajectories using public physical length plus a final address.

The defensible contribution is thus the **specific constructive reduction and codec architecture**, not the general notion of event time or semi-Markov entropy.

### Recommended claim discipline

Prefer wording such as:

> A constructive trajectory encoding method that identifies entropy-bearing branch states in a public reversible/causal trajectory law, collapses intervening deterministic flights into variable-duration macro edges, and uses the resulting recurrent macrograph for exact rank/unrank of the admissible trajectory family while preserving the original physical-time entropy rate.

Avoid wording such as:

> An invention of information time, variable-length state transitions, causal states, or entropy per event.

## RT-0002 preliminary rating

- Primitive novelty: **low**
- Specific constructive distinctiveness: **moderate-to-high**
- Risk of broad-claim collision: **moderate**
- Defensive-disclosure value: **high**, especially once the operational rank/unrank codec is implemented and verified

---

# 4. Comparative summary

| Disclosure | Broad overlap | Narrow combination distinctiveness | Priority for further work |
|---|---:|---:|---:|
| RM-0003 | High | Moderate | High |
| RF-0002 | Very high | Low-to-moderate | Medium |
| RT-0002 | High theoretical overlap | Moderate-to-high | Very high |

## Interpretation

### RM-0003

The concept-identity layer should remain in v0.2.0, but claims must focus on **persistent authoritative state -> native materialization -> fail-closed deterministic resolution -> fallback on miss**, not on stable IDs or aliases alone.

### RF-0002

Keep as a family-level disclosure, but treat it primarily as a **specific systems architecture and separation of responsibilities**, not as a broad novelty claim over routing. External collision density is high.

### RT-0002

This currently offers the strongest research differentiation among the three if the macrograph is converted into an exact operational codec. The mathematical background is established, but the particular constructive use inside the trajectory-addressing program remains worth documenting.

---

# 5. Release recommendation for v0.2.0

Before archival publication:

1. Pin exact implementation commits for RM-0003 and RT-0002.
2. Add a source/evidence appendix to RF-0002 showing the executable routing prototype and benchmark scope.
3. Revise any wording that implies invention of stable concept identity, policy-first routing, causal states, semi-Markov timing or generic agent routing.
4. Preserve the external-survey references as evidence that the registry intentionally narrows its claims around known art.
5. For RT-0002, preferably implement the proposed macro-event rank/unrank codec before assigning a stronger maturity status.

## External references screened

- Recent concept-identity systems describing stable entity/concept IDs with aliases, homonyms or senses.
- Recent ontology/concept-processing patent literature describing concept IDs, typed relationships, alias tables and indexed lookup.
- Modern semantic-registry systems using durable concept codes across memory, APIs and models.
- Recent distributed AI-agent routing patents using capability, cost, latency, policy, security and locality constraints.
- Contemporary model-routing systems explicitly using the term `policy-first routing`.
- Semi-Markov entropy-rate literature.
- Computational-mechanics / epsilon-machine literature on causal states and entropy rate.
- Hidden semi-Markov / renewal-process work on informational and causal architecture.

This survey records a limited search, not an exhaustive patent-office search. Absence of a single anticipatory reference in this survey must not be interpreted as proof of novelty or patentability.
