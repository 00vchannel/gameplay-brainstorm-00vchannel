# Gameplay Brainstorm 00vchannel

A beginner-friendly Agent Skill for turning incomplete game ideas into distinct, testable gameplay designs.

It helps people explore mechanics, modes, core loops, resources, progression, encounters, cooperative rules, paper prototypes, and playtests without requiring game-design terminology or technical implementation knowledge.

## What it does

- Reads the context you already provided before asking questions.
- Asks one focused batch of three to five design-changing questions when important information is missing.
- Offers clear options and a recommended default when you are unsure.
- Produces at least three materially distinct gameplay directions during open exploration.
- Distinguishes new modes from cosmetic or content-only variants.
- Turns a selected direction into the minimum rules needed for a useful prototype.
- Separates known facts, assumptions, hypotheses, and actual player evidence.
- Defines the smallest test capable of exposing evidence against the riskiest gameplay hypothesis.

It does not require a particular output language. The agent should follow the language and context of the conversation.

## Install

### Install for all five supported agents

```sh
npx skills add 00vchannel/gameplay-brainstorm-00vchannel --skill gameplay-brainstorm-00vchannel -g -a cursor -a opencode -a claude-code -a codex -a zcode
```

This installs the skill globally for Cursor, OpenCode, Claude Code, Codex, and ZCode.

### Install for one agent

Replace the final agent name as needed:

```sh
npx skills add 00vchannel/gameplay-brainstorm-00vchannel --skill gameplay-brainstorm-00vchannel -g -a cursor
npx skills add 00vchannel/gameplay-brainstorm-00vchannel --skill gameplay-brainstorm-00vchannel -g -a opencode
npx skills add 00vchannel/gameplay-brainstorm-00vchannel --skill gameplay-brainstorm-00vchannel -g -a claude-code
npx skills add 00vchannel/gameplay-brainstorm-00vchannel --skill gameplay-brainstorm-00vchannel -g -a codex
npx skills add 00vchannel/gameplay-brainstorm-00vchannel --skill gameplay-brainstorm-00vchannel -g -a zcode
```

Omit `-g` for a project-level installation. Omit all `-a` options to let the installer detect available agents and ask where to install the skill.

### Update or remove

```sh
npx skills update gameplay-brainstorm-00vchannel -g
npx skills remove gameplay-brainstorm-00vchannel -g
```

## Manual installation

Copy the complete `skills/gameplay-brainstorm-00vchannel` directory into the appropriate skill directory. Keep `SKILL.md`, `agents/`, and `references/` together.

| Agent | Global skill directory |
| --- | --- |
| Cursor | `~/.cursor/skills/` |
| OpenCode | `~/.config/opencode/skills/` |
| Claude Code | `~/.claude/skills/` |
| Codex | `~/.codex/skills/` |
| ZCode | `~/.zcode/skills/` |

For project-level installation, use the agent's project skill directory instead of its global directory.

After a manual ZCode installation, open **Settings > Skills**, select **Refresh**, confirm that the skill is enabled, and invoke it with `$gameplay-brainstorm-00vchannel`.

## Use

Explicitly invoke the skill and describe an idea or gameplay problem:

```text
Use $gameplay-brainstorm-00vchannel to ask me a few focused questions, then turn my gameplay idea into distinct, testable directions.
```

You can start with an incomplete idea. For example:

```text
$gameplay-brainstorm-00vchannel I want a cooperative game about operating a failing space station, but I do not know what players should do moment to moment.
```

When automatic skill matching is supported and enabled, relevant gameplay-design requests may also activate the skill without an explicit mention.

## Workflow

The skill adapts to the current design stage:

1. **Initial exploration** — fill important gaps and develop distinct directions.
2. **Direction comparison** — compare player experience, reuse, new work, and risk.
3. **Detailed design** — define only the rules required to make the chosen direction playable or testable.
4. **Playtest analysis** — update hypotheses and next decisions using actual observations or data.

## Boundaries

This skill is for gameplay design and early validation. Pure narrative, general UI work, monetization, code implementation, and dedicated numerical balancing of an existing system are outside its main scope.

Untested concepts are treated as hypotheses. The skill must not describe them as proven fun, effective, or validated.

## Compatibility note

The core package follows the open Agent Skills `SKILL.md` format. The optional `agents/openai.yaml` file provides Codex-specific display metadata and invocation policy; other compatible agents may safely ignore it.

## License

MIT © 00vchannel. See [LICENSE](LICENSE).

