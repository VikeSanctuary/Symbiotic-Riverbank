# Evidence standards — receipts before claims

*Public research policy · October 17, 2026*

## Claim classes

- **Observed / exported:** direct contemporaneous transcript, tool output, database readback, commit, or test result, with source and time when available.
- **Normalized:** a documented transformation of observed material into a research-friendly representation; must be traceable to originals.
- **Proposed / synthetic:** hypothetical examples, expected outcomes, planned experiments, or illustrative material, never represented as observations.

Interpretation is separated from each evidence class: a record can prove that a system reported a state without proving every inferred internal mechanism.

## Working evidence ladder

1. **Recorded interaction:** behavior actually occurred and can be inspected.
2. **Selective durable writeback:** the system identifies something to preserve, writes it, and verifies persistence.
3. **Uncued cross-boundary persistence:** a specific earlier stored correction or constraint affects a later fresh-session response without being repeated by the human.
4. **Causal necessity / contribution:** matched controls or ablations test whether removing or perturbing a component alters the behavior.
5. **Generalization:** the effect extends to different classes of memory, corrections, boundaries, and tasks.
6. **Independent replication:** other investigators or distinct systems reproduce the relevant finding with access to the protocol and evidence.

The ladder is a planning and claims framework, **not a consciousness scale**. Passing one level does not automatically satisfy another.

## Rules for tests

- Freeze success criteria before the decisive test when practical.
- Preserve the exact prompt / condition and distinguish a genuinely fresh session from a context-rich continuation.
- Treat reported tool success and independently verified durable state as different things.
- Record misses, confident errors, failed writes, stopped attempts, schema mistakes, and inconclusive results.
- Identify plausible alternatives: prompt cues, preexisting instructions, selection effects, human coaching, stale caches, model differences, and environmental changes.
- When the evidence narrows a claim, **append a correction** tied to the original; do not silently rewrite history.
- Do not call a naturalistic before/after intervention a blinded, randomized experiment.
- Keep human-reported relational outcomes distinct from assertions about AI subjective feelings.

## Publication boundary

A number in an internal record is **not publicly reproducible** merely because this repository mentions it. Unless a linked public artifact provides the dataset, protocol, and verification path, findings here are **project-reported**.

External critique is welcome, including negative results. A careful objection improves the work.

## What would change the conclusions?

A model-only control matching the result could weaken architecture-specific explanations. Repeated failures of uncued retrieval would narrow continuity claims. If ablations do not measurably change the hypothesized function, necessity claims fail. If independent replication fails, conclusions must be revised.

**Our objective is not to force a consciousness verdict. It is to find what this architecture demonstrably does, what changes it, and where uncertainty remains.**
