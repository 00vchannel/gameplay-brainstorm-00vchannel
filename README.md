# Gameplay Brainstorm 00vchannel

Gameplay Brainstorm 00vchannel is an Agent Skill for structured gameplay brainstorming. It helps turn an incomplete idea into materially different playable directions, define the minimum rules needed to examine a chosen direction, and identify what should be tested first.

Its purpose is deliberately narrow. This skill supports brainstorming; using it does not, by itself, improve the quality of a game or its development process. It does not determine whether a concept is fun, feasible, commercially suitable, or worth producing. Those judgments still depend on execution, technical and production constraints, iteration, and evidence from relevant players.

The skill is designed to remain approachable without requiring game-design terminology. It can be used for digital games, tabletop games, and paper prototypes.

## What the skill does

- Reviews the existing conversation before asking for more information.
- Asks one focused batch of questions only when unanswered details would materially affect the design.
- Offers clear options and a recommended default when the user is unsure.
- Produces at least three materially distinct gameplay directions during open exploration.
- Compares directions by player experience, required work, reuse, and design risk.
- Distinguishes a new mode from a cosmetic or content-only variant.
- Defines only the rules needed to make the selected direction playable or testable.
- Separates known facts, working assumptions, testable hypotheses, and player evidence.
- Proposes the smallest test that could expose a problem with the highest-risk hypothesis.

The skill does not require a particular output language. It follows the language and context of the conversation.

## Install

### Cursor, OpenCode, Claude Code, Codex, and ZCode

Install the skill globally for all five agents:

```sh
npx skills add 00vchannel/gameplay-brainstorm-00vchannel --skill gameplay-brainstorm-00vchannel -g -a cursor -a opencode -a claude-code -a codex -a zcode
```

### One agent

Use the command for the agent you want to support:

```sh
npx skills add 00vchannel/gameplay-brainstorm-00vchannel --skill gameplay-brainstorm-00vchannel -g -a cursor
npx skills add 00vchannel/gameplay-brainstorm-00vchannel --skill gameplay-brainstorm-00vchannel -g -a opencode
npx skills add 00vchannel/gameplay-brainstorm-00vchannel --skill gameplay-brainstorm-00vchannel -g -a claude-code
npx skills add 00vchannel/gameplay-brainstorm-00vchannel --skill gameplay-brainstorm-00vchannel -g -a codex
npx skills add 00vchannel/gameplay-brainstorm-00vchannel --skill gameplay-brainstorm-00vchannel -g -a zcode
```

Omit `-g` for a project-level installation. Omit the `-a` options to let the installer detect available agents and ask where the skill should be installed.

### Update or remove

```sh
npx skills update gameplay-brainstorm-00vchannel -g
npx skills remove gameplay-brainstorm-00vchannel -g
```

## Manual installation

Copy the complete `skills/gameplay-brainstorm-00vchannel` directory into the relevant skill directory. Keep `SKILL.md`, `agents/`, and `references/` together.

| Agent | Global skill directory |
| --- | --- |
| Cursor | `~/.cursor/skills/` |
| OpenCode | `~/.config/opencode/skills/` |
| Claude Code | `~/.claude/skills/` |
| Codex | `~/.codex/skills/` |
| ZCode | `~/.zcode/skills/` |

For a project-level installation, use the corresponding project skill directory instead.

After a manual ZCode installation, open **Settings > Skills**, select **Refresh**, and confirm that the skill is enabled.

## Usage

Invoke the skill and describe the gameplay idea or problem you want to examine:

```text
Use $gameplay-brainstorm-00vchannel to ask me a few focused questions, then turn my gameplay idea into distinct, testable directions.
```

An incomplete starting point is sufficient:

```text
$gameplay-brainstorm-00vchannel I want a cooperative game about operating a failing space station, but I do not know what players should do moment to moment.
```

Agents that support automatic skill matching may also activate the skill for relevant gameplay-design requests without an explicit invocation.

## Workflow

The skill adjusts its response to the current stage of the work:

1. **Initial exploration:** identify the missing design constraints and develop distinct directions.
2. **Direction comparison:** compare the intended player experience, reusable elements, required new work, and major risks.
3. **Detailed design:** define the minimum rules needed to make the selected direction playable or testable.
4. **Playtest analysis:** interpret observations or data, update the relevant hypotheses, and decide what to change or test next.

A concept is treated as a new mode only when both its primary objective and its organizing recurring decision change. Changes limited to theme, enemies, maps, rewards, or presentation are treated as variants.

## Limits

This is a brainstorming and early gameplay-validation aid, not a complete game-design or production framework. It does not replace design judgment, prototyping, technical assessment, production planning, or playtesting.

Pure narrative development, general UI design, monetization, code implementation, and dedicated numerical balancing of an existing system are outside its main scope.

Untested concepts remain hypotheses. The skill should not describe an idea as proven fun, effective, or validated without relevant player evidence.

## Compatibility

The repository follows the open Agent Skills `SKILL.md` format. `agents/openai.yaml` provides Codex-specific display metadata and invocation policy; other compatible agents can safely ignore it.

## License

MIT © 00vchannel. See [LICENSE](LICENSE).
