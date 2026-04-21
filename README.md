# 0→1 Human-Machine UX Conductor

Portable skill package for zero-to-one human-machine UX framing.

This repository publishes a single skill:

- `zero-to-one-human-machine-ux-conductor`

The skill is designed for early-stage product, agent, and human-machine collaboration work where discussion tends to drift into slogans, premature UX detail, or downstream structure before the upstream direction is stable.

## Included Files

- [SKILL.md](./SKILL.md)
  - Entry point with trigger conditions, read order, stage gates, and output contract.
- [architecture_conductor_agent_spec.md](./architecture_conductor_agent_spec.md)
  - Agent role, gatekeeping authority, rollback behavior, and tone.
- [framework_0to1_human_machine_collab.md](./framework_0to1_human_machine_collab.md)
  - The zero-to-one human-machine collaboration framework and chapter ordering source of truth.
- [references/zero-to-one-human-machine-ux-conductor-map-reference.md](./references/zero-to-one-human-machine-ux-conductor-map-reference.md)
  - Optional reference companion with example output shapes and map structures.

## Install

Clone the repository once:

```bash
git clone git@github.com:Vickysh221/zero-to-one-human-machine-ux-conductor.git ~/zero-to-one-human-machine-ux-conductor
```

### Claude Code

```bash
mkdir -p ~/.claude/skills
ln -sfn ~/zero-to-one-human-machine-ux-conductor ~/.claude/skills/zero-to-one-human-machine-ux-conductor
```

### Codex

```bash
mkdir -p ~/.agents/skills
ln -sfn ~/zero-to-one-human-machine-ux-conductor ~/.agents/skills/zero-to-one-human-machine-ux-conductor
```

### OpenClaw

OpenClaw loads skills from the directories listed in `skills.load.extraDirs`.
If your OpenClaw config already points at a local skills folder, use that existing path.
If not, this setup matches a common local path:

```bash
mkdir -p ~/.openclaw/workspace/local-skills
ln -sfn ~/zero-to-one-human-machine-ux-conductor ~/.openclaw/workspace/local-skills/zero-to-one-human-machine-ux-conductor
```

Example config fragment:

```json
{
  "skills": {
    "load": {
      "extraDirs": [
        "/Users/your-name/.openclaw/workspace/local-skills"
      ]
    }
  }
}
```

## Verify

```bash
test -f ~/.claude/skills/zero-to-one-human-machine-ux-conductor/SKILL.md
test -f ~/.agents/skills/zero-to-one-human-machine-ux-conductor/SKILL.md
test -f ~/.openclaw/workspace/local-skills/zero-to-one-human-machine-ux-conductor/SKILL.md
```

## Usage

Ask the agent to use `zero-to-one-human-machine-ux-conductor` when you need to:

- frame a zero-to-one product or agent direction before UX structure expands too early
- separate `Target A / Direction Framing` from `Target B / Structure Convergence`
- preserve gate judgments, risks, assumptions, and unresolved contradictions
- drive discussion through structured intermediate artifacts instead of polished but premature solution prose

## Packaging Notes

- The skill depends on the sibling files in this repository. Do not copy `SKILL.md` alone.
- `name:` in [SKILL.md](./SKILL.md) is `zero-to-one-human-machine-ux-conductor`, so the install directory should use the same slug.
- Symlink-based install is best if you plan to update the repository over time. If you prefer a static copy, replace `ln -sfn` with `cp -R`.
