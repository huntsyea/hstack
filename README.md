# hstack

A collection of [agent skills](https://agentskills.io/specification). Install them with `npx skills add`.

## Install

```bash
npx skills add huntsyea/hstack
```

One skill:

```bash
npx skills add huntsyea/hstack@human-writing
```

Browse the collection on [skills.sh](https://skills.sh/huntsyea/hstack).

## Skills

### human-writing

Edit, audit, or draft prose without flattening the writer's voice. Stock AI patterns are things to inspect, not a list of banned words.

| File | Role |
| --- | --- |
| [`skills/human-writing/SKILL.md`](skills/human-writing/SKILL.md) | Instructions the agent loads |
| [`skills/human-writing/eval.md`](skills/human-writing/eval.md) | Internal pass/fail checklist after each run |

`eval.md` stays next to `SKILL.md` on purpose. The skill tells the agent to read it before responding.

## License

[MIT](LICENSE)
