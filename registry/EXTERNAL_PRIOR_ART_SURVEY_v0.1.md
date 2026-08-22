# External Prior-Art Landscape Survey v0.1

**Date:** 2026-08-22  
**Scope:** RF-0001, RM-0001, RM-0002, MA2A-0001, MA2A-0002, MA2A-0003  
**Purpose:** technical landscape comparison only; not a patentability opinion, freedom-to-operate opinion, or legal conclusion.

## 1. Executive summary

The initial survey finds substantial prior art for the individual primitives used by the Resolutive family: hierarchical LLM memory, vector and graph retrieval, content addressing, local-first replication, CRDT/event-log style state synchronization, public-key identity, and agent-to-agent interoperability protocols are all established classes of technique.

The strongest potentially distinguishing material is therefore not any one primitive in isolation. It is the disclosed organization of these mechanisms around a resolutive state/trajectory address as the common substrate for deterministic memory route reuse and inter-agent state synchronization, while treating language-model inference and natural-language transport as optional boundary mechanisms rather than mandatory operations on every retrieval or synchronization event.

This should be described as a candidate distinguishing combination requiring deeper patent/literature searching, not as established novelty.

## 2. Memory-system comparison

### 2.1 MemGPT / Letta lineage

MemGPT (Packer et al., 2023) proposes virtual context management inspired by operating-system memory hierarchies. Its core problem is extending effective LLM context by moving information among memory tiers and allowing an LLM-driven agent to manage that memory.

Overlap with RM/RF:

- persistent agent memory;
- hierarchical memory organization;
- long-running stateful agents;
- explicit separation of fast/slow memory classes.

Difference relevant to Resolutive disclosures:

- RM-0001 defines known-address route resolution as a deterministic memory primitive distinct from semantic interpretation;
- the route resolver does not require the LLM to decide what memory to retrieve once the resolutive address is already known;
- RF-0001 places this direct route reuse inside a broader state/trajectory architecture rather than an OS-style context paging scheme.

Primary reference: `Packer et al., MemGPT: Towards LLMs as Operating Systems, arXiv:2310.08560 (2023)`.

## 3. Mem0

Mem0 (Chhikara et al., 2025) extracts, consolidates, and retrieves salient information from conversations and also defines a graph-enhanced memory variant. The published architecture addresses persistent conversational memory and reductions in token/latency cost compared with full-context approaches.

Overlap:

- persistent long-term memory for agents;
- memory separated from the immediate LLM context;
- goal of reducing repeated context/token processing;
- structured storage/retrieval.

Difference relevant to Resolutive disclosures:

- Mem0's published architecture is centered on extraction/consolidation/retrieval of memories from conversations;
- RM-0001 explicitly separates semantic/query-to-route discovery from the deterministic known-address resolver;
- the Resolutive architecture targets reusable state/trajectory routes that can exist independently of conversational fact extraction.

Primary reference: `Chhikara et al., Mem0: Building Production-Ready AI Agents with Scalable Long-Term Memory, arXiv:2504.19413 (2025)`.

## 4. Zep / Graphiti

Zep/Graphiti uses temporal knowledge graphs to integrate changing conversational and enterprise data while preserving relationships and history.

Overlap:

- persistent agent memory;
- state that evolves over time;
- structured representation;
- incremental update and historical relationships.

Difference relevant to Resolutive disclosures:

- Zep/Graphiti centers memory on temporal entities, facts and graph relations;
- RM/RF centers the core resolver on state/trajectory addresses and route reuse;
- MA2A extends those addresses into synchronization units rather than treating the knowledge graph itself as the inter-agent protocol substrate.

Primary reference: `Rasmussen et al., Zep: A Temporal Knowledge Graph Architecture for Agent Memory, arXiv:2501.13956 (2025)`.

## 5. Content addressing / IPFS CIDs

IPFS CIDs are self-describing content-addressed identifiers that combine content type and cryptographic hash information.

Overlap:

- compact stable identifiers;
- hash/index based direct retrieval;
- distributed use of identifiers;
- integrity linkage.

Difference relevant to Resolutive disclosures:

- a CID identifies content by hash; RM's resolutive address may identify a registered trajectory, state relation, route, action, or transition structure and need not be a pure content hash;
- RM-0002 explicitly states that a hash verifies reconstructed content but does not itself reconstruct arbitrary source information;
- the trajectory descriptor problem is therefore distinct from ordinary content addressing even though content-addressing techniques may be used inside an implementation.

Primary reference: IPFS CID specification, current CIDv1.

## 6. Local-first systems and CRDT-related replication

Local-first software predates the Resolutive disclosures and explicitly supports local operation, offline changes, later synchronization, and CRDT-based convergence.

Overlap with RF/MA2A:

- local operation while disconnected;
- synchronization of changes rather than centralized mandatory computation;
- explicit handling of concurrent updates;
- client-side ownership/processing.

Difference relevant to Resolutive disclosures:

- local-first/CRDT work is a general replicated-data paradigm;
- MA2A attaches deterministic synchronization, privacy scopes, identity and conflict policy to resolutive trajectory/state addresses in an AI-agent architecture;
- MA2A does not claim invention of CRDTs, optimistic concurrency, version clocks, event sourcing, or local-first operation.

Primary reference: `Kleppmann et al., Local-First Software: You Own Your Data, in spite of the Cloud, Onward! 2019` and the established CRDT literature referenced therein.

## 7. Public Agent2Agent (A2A) protocol

The Linux Foundation / Google-originated Agent2Agent (A2A) protocol is an open interoperability standard for independent, potentially opaque AI agents. Its published model includes agent discovery, modality negotiation, messages, tasks, artifacts, streaming, structured data and security. A key architectural principle is that agents can collaborate without exposing their internal memory or tools.

Overlap with MA2A:

- agent discovery and inter-agent interoperability;
- security/authentication requirements;
- structured data transport;
- long-running and asynchronous interaction;
- heterogeneous agent systems.

Important distinction:

- public A2A is task/message oriented and intentionally supports collaboration without access to an agent's internal state or memory;
- MA2A-0001 instead discloses synchronization of selected resolutive state/trajectory deltas as a first-class mechanism between compatible agents;
- MA2A's stated goal is that compatible agents need not reconstruct every interaction through natural-language agent messages when a deterministic shared state representation exists.

This contrast is material and should remain explicit in future disclosures. MA2A should not claim general invention of agent-to-agent protocols, discovery, JSON-RPC, authentication, task exchange, or structured messages.

Primary reference: Agent2Agent (A2A) Protocol official specification, version 0.3.x landscape as reviewed in August 2026.

## 8. PKI and organizational identity

Hierarchical PKI, certificate chains, Ed25519 signatures, challenge-response authentication, revocation and organization/device delegation are established security techniques.

Accordingly, MA2A-0003 should not claim novelty in PKI primitives themselves.

The potentially distinguishing architecture is narrower: tying official-network admission and organization-level delegation to a Memoria.ia/MA2A hierarchy in which an organization authority controls subordinate device/agent participation while protocol compatibility remains separate from official-network membership.

Even this combination requires a dedicated patent search before any novelty conclusion.

## 9. Candidate distinguishing combination

The current strongest candidate distinction across RF/RM/MA2A is:

> A local-first intelligent-agent architecture in which deterministic state/trajectory addresses provide a shared substrate for persistent memory route reuse and selective inter-agent state synchronization, while semantic/LLM processing is separated from known-address resolution and natural-language transport is optional rather than mandatory between compatible agents.

Supporting elements include:

1. explicit separation of route discovery from route resolution;
2. deterministic known-address memory lookup;
3. state/trajectory addresses as synchronization units;
4. selected delta exchange with scope boundaries;
5. L1 local cognition with non-LLM-required coordination plane;
6. deterministic synchronization/conflict policy;
7. organizational identity/admission layered above protocol compatibility.

No single item above should presently be represented as independently novel. The candidate novelty is in the specific combination and integration, subject to deeper search.

## 10. Claims that should remain avoided

The survey reinforces the existing disclosure safeguards:

- do not claim generic O(1) intelligence;
- do not claim invention of hash-table lookup;
- do not claim invention of content addressing;
- do not claim that a cryptographic hash reconstructs arbitrary source data;
- do not claim generic local-first synchronization or CRDT invention;
- do not claim invention of hierarchical PKI, Ed25519 or challenge-response;
- do not claim invention of agent-to-agent communication;
- do not claim generic persistent AI memory.

## 11. Recommended next search

The next stage should search patents and older literature around the exact combined concepts rather than broad product names. High-value concepts are:

- deterministic state-addressed agent memory;
- trajectory-addressed memory retrieval;
- state-machine path/route as persistent memory representation;
- shared state identifiers between autonomous agents;
- delta synchronization of internal agent state or memory;
- non-language state synchronization between AI agents;
- edge-local agent cognition with centralized non-inference coordination;
- organization-root delegated identity for agent/device networks.

The objective is to identify documents that combine multiple elements in the same teaching, rather than merely collecting references for known primitives.

## 12. Preliminary assessment

**RF-0001:** broad individual components are heavily anticipated; candidate value lies in the integrated architecture and explicit separation between resolution, semantic inference and synchronization.

**RM-0001:** strongest defensible distinction currently appears to be the route-discovery / deterministic-route-resolution separation applied to trajectory/state memory, not O(1) lookup itself.

**RM-0002:** trajectory-based reversible recovery remains technically experimental. Prior-art value is strongest as a documented architecture and test target; no compression/reconstruction novelty conclusion should be made yet.

**MA2A-0001/0002:** public A2A, local-first systems and distributed synchronization establish substantial surrounding prior art. The most interesting distinction is selected internal state/trajectory-delta synchronization between compatible agents rather than task/message exchange alone.

**MA2A-0003:** crypto primitives are established. Potential distinction is the organization-root/official-network admission arrangement as integrated into MA2A, subject to dedicated patent search.

## References

- Packer, C. et al. (2023). *MemGPT: Towards LLMs as Operating Systems*. arXiv:2310.08560.
- Chhikara, P. et al. (2025). *Mem0: Building Production-Ready AI Agents with Scalable Long-Term Memory*. arXiv:2504.19413.
- Rasmussen, P. et al. (2025). *Zep: A Temporal Knowledge Graph Architecture for Agent Memory*. arXiv:2501.13956.
- Kleppmann, M. et al. (2019). *Local-First Software: You Own Your Data, in spite of the Cloud*. Onward! 2019.
- IPFS / Multiformats. *CID (Content Identifier) Specification*.
- Agent2Agent Project. *Agent2Agent (A2A) Protocol Official Specification*.
