# Human writing

An [Agent Skill](https://agentskills.io/specification) for editing, auditing, or drafting prose without flattening the writer's voice. It treats stock AI patterns as things to inspect, not a list of banned words.

Works with Cursor, Claude Code, Codex, and any other agent that supports `npx skills add`.

## Install

```bash
npx skills add huntsyea/human-writing
```

Browse it on [skills.sh](https://skills.sh/huntsyea/human-writing) after the first install is indexed.

## What it does

The skill picks a mode from the request:

- **Edit** — default when a draft is supplied. Minimum effective edit, then the full draft plus a short **What changed** section.
- **Detect** — name patterns, quote the text, and suggest a fix. No rewrite, no AI score, no authorship claim.
- **Draft** — write new prose from a brief and any voice samples. Does not invent personal experience to sound human.

Technical documentation has its own rules in `SKILL.md`: verify against the code, keep a neutral instructional voice, and report review findings with `file:line` locations.

## Files

| File | Role |
| --- | --- |
| [`SKILL.md`](SKILL.md) | Instructions the agent loads |
| [`eval.md`](eval.md) | Internal pass/fail checklist after each run |

`eval.md` stays next to `SKILL.md` on purpose. The skill tells the agent to read it before responding.

## License

[MIT](LICENSE)
