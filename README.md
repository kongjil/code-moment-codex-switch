# code-moment-codex-switch

OpenClaw skill for automatically switching coding-heavy tasks to Codex (`newapi/gpt-5.3-codex`).

## What it does

This skill upgrades certain engineering tasks from the default chat model to a Codex workbench flow.

Strong trigger signals include:

- multi-file code changes
- tasks that require `build` / `test` / `lint` / pre-restart verification
- frontend/backend state-machine, routing, component, API, or config-linked changes
- iterative loops like: modify code → build/test → inspect result → patch again

## Main behavior

- keeps normal chat on the default model
- switches coding-heavy work to Codex when the task crosses the trigger line
- preserves confirmation gates for deploy/restart/delete/auth or routing changes

## Files

- `SKILL.md` — the skill definition

## Intended use

Use this in OpenClaw when you want coding work to default to a dedicated code model instead of staying on the general chat model.
