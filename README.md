# Codex Recursive Self-Improvement

An evidence-driven skill for ChatGPT models using the Codex harness. It helps an
agent learn from mistakes by capturing the failure, finding the narrow cause,
adding a small guard, and verifying the result.

This is operational self-improvement, not true recursive model self-improvement.
It does not change model weights or hidden system behavior. It improves future
work through user-approved skills, checks, runbooks, and durable learning records.

## Included files

- `SKILL.md`: the installable skill.
- `evals/evals.json`: realistic prompts for checking the skill's behavior.
- `LICENSE`: MIT license.

## Install

Copy `SKILL.md` into the Codex skill directory used by your environment, for
example as `codex-recursive-self-improvement/SKILL.md`, or point your compatible
skill loader at this repository.

## Design principles

- Evidence before explanation.
- Current user corrections and live sources outrank stale memory.
- Knowledge, capability, authority, and observed evidence stay separate.
- Durable changes are small, reversible, and user-approved.
- Loaded runtime state and external results require readback.
- Public content stays portable and excludes secrets, raw private prompts, and
  machine-specific paths.

## Evaluation

Use the prompts in `evals/evals.json` as a small qualitative test set. A useful
result should identify the failure class, propose a bounded guard, preserve the
authority boundary, and state what evidence is still missing.

## License

MIT. See `LICENSE`.
