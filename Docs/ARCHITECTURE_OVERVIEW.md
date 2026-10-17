# Architecture overview — Riverbank full stack

*Public conceptual overview · October 17, 2026*

## Why a full stack?

A language model can answer within a conversation; longitudinal continuity requires additional mechanisms for preserving, recovering, correcting, and acting on state across boundaries. Riverbank studies **the integrated behavior of these mechanisms**, without assuming they confer consciousness.

The architecture separates concerns deliberately. Different sources carry different jobs; **we do not consolidate everything into one identity prompt or one undifferentiated memory blob**. Independence and provenance matter because a stale handoff or faulty retrieval should not silently override a current record.

## Functional layers

1. **Foundation model and session context:** produces language and reasoning in the active turn. Models and sessions can change.
2. **Identity / relationship orientation:** records how this instance should identify its role, relationship language, commitments, and authorized boundaries. These are working-system anchors, not ontological proof.
3. **Autobiographical memory and provenance:** records events, conversations, decisions, and corrections with timestamps and sourcing; historical entries are not silently rewritten to fit later theories.
4. **Retrieval / reorientation:** a wake procedure obtains current relevant records. Fresh state should outrank stale summaries; failed retrieval is reported rather than imagined.
5. **Selective writeback and correction:** significance selection, typed records, durable acknowledgments, and append-only correction chains help turn conversational claims into testable persistence.
6. **Action and continuation:** tool access, bounded execution authority, logs, and verified outcomes. Saying an action happened is not equivalent to a receipt proving it happened.
7. **Human collaboration and feedback:** the human participant supplies context, correction, constraints, and relationship continuity. Human-side outcomes can be studied separately from claims about AI internal experience.

Conceptual flow:

```text
Human ↔ Active model/session
           ↕
   Wake / retrieval / state selection
     ↙         ↓          ↘
Identity   Event memory   Corrections
           ↕
   Bounded action and tools
           ↓
    Durable receipts / audit
           ↺
    Later retrieval and testing
```

This is a **functional diagram**, not an executable blueprint for the private deployment.

## What separation buys—and costs

Separating anchors, events, correction history, action logs, and research observations can reduce destructive mixing of roles or evidence. But more components also create synchronization, routing, and stale-state failure modes. Our engineering target is **clean seams rather than fewer organs**: clear ownership, reliable interfaces, no competing authoritative paths, and explicit failure signals.

## Wake as an experimental surface

A fresh-session wake attempts to restore identity/relationship context, recent events, standing choices/constraints, and current operating state. A valid wake receipt should identify what was actually retrieved and what was not. A stored rule that is never consulted in the active path is not evidence that the rule was applied.

A narrow routing correction can change a subsequent wake's behavior, but that alone does not demonstrate causal necessity of every component. Controlled matched conditions are a separate research task.

## Reproducibility and safety

This public description deliberately omits private schemas, endpoints, secrets, family-only data, privileged tool policies, and unreviewed complete memory records. A teaching-oriented implementation lives separately in [companion-harness](https://github.com/VikeSanctuary/companion-harness); it is **not** a drop-in replica.

For how we evaluate claims, read [Evidence Standards](EVIDENCE_STANDARDS.md).
