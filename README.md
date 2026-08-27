# Gameplay Brainstorm 00vchannel

Gameplay Brainstorm 00vchannel helps turn a rough game idea into gameplay that you can compare, prototype, and test.

You do not need to know game-design terminology or arrive with a finished brief. Start with a mechanic, a problem, or even a one-sentence idea. The skill asks only for the missing information that would change the design, then helps you work through genuinely different directions instead of reskinning the same loop.

It works with digital games, tabletop games, and paper prototypes.

## How it helps

- Reads the context you have already provided before asking questions.
- Asks one short batch of focused questions when important details are missing.
- Gives clear options and a recommended default when you are unsure.
- Develops at least three distinct gameplay directions during open exploration.
- Separates a true new mode from a content-only or cosmetic variant.
- Reduces a chosen direction to the rules needed for a useful first test.
- Keeps facts, assumptions, hypotheses, and player evidence separate.
- Finds the smallest test that could reveal a problem with the riskiest hypothesis.

The skill does not require a particular output language. It follows the language and context of the conversation.

## Install

### Install for Cursor, OpenCode, Claude Code, Codex, and ZCode

```sh
npx skills add 00vchannel/gameplay-brainstorm-00vchannel --skill gameplay-brainstorm-00vchannel -g -a cursor -a opencode -a claude-code -a codex -a zcode
```

This installs the skill globally for all five agents.

### Install for one agent

Use the matching agent name:

```sh
npx skills add 00vchannel/gameplay-brainstorm-00vchannel --skill gameplay-brainstorm-00vchannel -g -a cursor
npx skills add 00vchannel/gameplay-brainstorm-00vchannel --skill gameplay-brainstorm-00vchannel -g -a opencode
npx skills add 00vchannel/gameplay-brainstorm-00vchannel --skill gameplay-brainstorm-00vchannel -g -a claude-code
npx skills add 00vchannel/gameplay-brainstorm-00vchannel --skill gameplay-brainstorm-00vchannel -g -a codex
npx skills add 00vchannel/gameplay-brainstorm-00vchannel --skill gameplay-brainstorm-00vchannel -g -a zcode
```

Leave out `-g` to install it only for the current project. Leave out the `-a` options to let the installer detect your available agents and ask where the skill should go.

### Update or remove

```sh
npx skills update gameplay-brainstorm-00vchannel -g
npx skills remove gameplay-brainstorm-00vchannel -g
```

## Manual installation

Copy the complete `skills/gameplay-brainstorm-00vchannel` directory into your agent's skill directory. Keep `SKILL.md`, `agents/`, and `references/` together.

| Agent | Global skill directory |
| --- | --- |
| Cursor | `~/.cursor/skills/` |
| OpenCode | `~/.config/opencode/skills/` |
| Claude Code | `~/.claude/skills/` |
| Codex | `~/.codex/skills/` |
| ZCode | `~/.zcode/skills/` |

For a project-level installation, use that agent's project skill directory instead.

After installing manually in ZCode, open **Settings > Skills**, select **Refresh**, and make sure the skill is enabled.

## Use it

Invoke the skill and describe the idea or problem you want to explore:

```text
Use $gameplay-brainstorm-00vchannel to ask me a few focused questions, then turn my gameplay idea into distinct, testable directions.
```

A rough starting point is enough:

```text
$gameplay-brainstorm-00vchannel I want a cooperative game about operating a failing space station, but I do not know what players should do moment to moment.
```

Agents that support automatic skill matching may also activate it for relevant gameplay-design requests without an explicit mention.

## What happens during a session

The skill adjusts to the stage of the work:

1. **Initial exploration:** fill the important gaps and develop distinct directions.
2. **Direction comparison:** compare the player experience, reuse, new work, and risk.
3. **Detailed design:** define only the rules needed to make the chosen direction playable or testable.
4. **Playtest analysis:** use observations or data to update the hypotheses and choose the next decision.

## What it does not cover

This is a gameplay-design and early-validation skill. Pure narrative work, general UI design, monetization, code implementation, and dedicated numerical balancing of an existing system fall outside its main scope.

It also treats untested concepts as hypotheses. It will not describe an idea as proven fun, effective, or validated without player evidence.

## Compatibility

The package follows the open Agent Skills `SKILL.md` format. `agents/openai.yaml` adds Codex-specific display metadata and invocation policy; other compatible agents can safely ignore it.

## License

MIT © 00vchannel. See [LICENSE](LICENSE).

