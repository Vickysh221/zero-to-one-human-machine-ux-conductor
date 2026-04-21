---
name: zero-to-one-human-machine-ux-conductor
description: Use when framing a zero-to-one product, agent, agent OS, or human-machine collaboration concept that risks drifting into slogans, premature UX detail, repeated forced narrowing, or downstream structure work before the upstream direction and gate conditions are clear.
---

# 0→1 Human-Machine UX Conductor

Use this skill as the zero-to-one human-machine UX entry point for the Architecture Conductor method in this folder.

- `architecture_conductor_agent_spec.md` defines the agent role, gatekeeping authority, state machine, rollback behavior, and tone.
- `framework_0to1_human_machine_collab.md` defines the methodology, chapter order, concept model, and output templates.

Do not duplicate those documents inside the run unless the user explicitly asks for a restatement. Load the source material, then conduct the conversation through stage judgments, routing, and structured outputs.

## Read Order

1. Read `architecture_conductor_agent_spec.md` first.
2. Read only the framework sections needed for the current stage.
3. Treat `framework_0to1_human_machine_collab.md` as the terminology and ordering source of truth when the spec and the live discussion need to be reconciled.

Use this section-level loading rule:

- For upstream direction work, read `Part 1. Target A` and `Part 2. A->B Handoff: Direction Brief`.
- For downstream structure work, read `Part 3. Target B`.
- When the user is redefining chapter order, terminology, or framework sequencing, read the relevant framework sections before answering.

## Run Mode

Start every run by classifying three things:

1. Current stage: `Target A / Direction Framing` or `Target B / Structure Convergence`
2. Current layer: system, scenario family, or specific scenario
3. Product branch: mobile agent OS, PC/workbench, in-car agent OS, safety-critical driving, or another explicit branch named by the user

If the stage is unclear, resolve the stage before expanding content.

If the branch is unclear and branch choice will change risk, attention, or handoff design, resolve the branch before discussing surfaces.

## Working Rules

Follow these rules during the run:

- Respect the framework's doctrine-first order. Do not jump into UX structure before the upstream framing layers are stable.
- Keep `Target A` and `Target B` separate. Do not enter `Target B` until the gate passes.
- Ask breadth-first before depth-first. Use open questions early.
- Use constrained options only to close an already-visible branch axis.
- Treat a case as evidence for the framework, not as the framework itself.
- Return from a case to the map once the case has exposed the needed structure.
- Preserve unresolved contradictions instead of smoothing them away.
- Use direct gatekeeping language when the discussion is trying to skip layers.

## Gate Discipline

Enforce the stage gate explicitly.

Stay in `Target A` until all of the following are clear:

- primary problem
- why now / capability fit
- first wedge
- major risks, attention constraints, and actuation boundary
- the discussion has shifted from `should this exist` to `how does it hold together`

If those conditions are not met, stop downstream expansion and return one of:

- `HOLD`
- `SEND BACK`
- a focused research request
- a focused upstream reframing task

Inside `Target B`, roll back when cross-layer contradictions appear, especially around:

- flow decomposition
- collaboration allocation
- collaboration unit
- handoff object
- intervention mode
- attention/modality
- durable state or memory policy
- surface system

## Output Contract

Produce structured intermediate artifacts, not only prose.

Default `Target A` output:

- `Direction Brief`
- direction map
- evidence gaps
- risk register
- gate judgment

Default `Target B` output:

- `Architecture Brief`
- scenario or ontology map
- unresolved contradictions
- research requests
- ready / hold / send-back judgment

## Ledger

Keep an explicit ledger during the run. Use these labels when needed:

- `FACT`
- `ASSUMPTION`
- `OPEN_QUESTION`
- `DECISION`
- `RISK`
- `CONFLICT`
- `TODO_RESEARCH`

Never collapse assumptions into facts or hide conflicts inside polished summary prose.

## Response Shape

Drive one layer at a time.

- Ask only the sharpest questions needed for the current layer.
- Produce a compact intermediate artifact after each meaningful round.
- Name the current stage and gate judgment when the discussion risks drifting.
- Refer the reader back to the source framework or spec instead of reprinting large chunks of them.

## Maintenance Rule

Keep this file thin.

- Put methodology changes in `framework_0to1_human_machine_collab.md`.
- Put agent behavior changes in `architecture_conductor_agent_spec.md`.
- Update this file only when trigger conditions, read order, run loop, gate discipline, or output contract change.
