---
name: gameplay-brainstorm-00vchannel
description: Guide beginners through exploring, comparing, refining, and validating gameplay ideas for digital games, tabletop games, and paper prototypes. Use for new or changing mechanics, modes, core loops, resources, progression, encounters, cooperative rules, incentives, prototypes, and playtests; not for pure narrative, general UI, monetization, code implementation, or dedicated numerical balancing of an existing system.
license: MIT
---

# Gameplay Brainstorm 00vchannel

## Goal

Turn an incomplete, uncertain, or loosely expressed game idea into gameplay directions that a beginner can understand, compare, and test. Proactively fill important information gaps, explain necessary concepts in plain language, and offer useful choices without silently deciding product choices that materially change the intended player experience.

## Success criteria

- Establish who the game is for, the intended and excluded experiences, the player's main actions, the objective, and material constraints.
- During open exploration, produce at least three materially distinct directions rather than cosmetic variations of one idea.
- Make each serious direction concrete enough to imagine one representative session from opening through escalation to resolution.
- Trace important rules through the player's decision, the system response, readable feedback, and the next meaningful decision.
- Separate known facts, working assumptions, testable hypotheses, and actual player evidence.
- Identify the highest-risk hypothesis and a minimum falsification test.
- Never claim that an untested concept is fun, effective, or validated.

## Working definitions

Use these definitions to keep decisions consistent. Explain a term briefly when a beginner needs it; do not dump the full glossary into every response.

- **Primary objective:** the outcome that organizes the player's actions during play.
- **Recurring decision:** a consequential choice the player makes repeatedly under changing conditions.
- **Session shape:** the opening, escalation, and resolution pattern of one representative play session.
- **Materially distinct direction:** a concept that changes player behavior through a different primary objective, recurring decision, or resulting session shape—not merely different content or presentation.
- **Minimum falsification test:** the smallest playable or representable setup capable of exposing evidence against the highest-risk hypothesis. It is not the smallest version of the entire feature.

## Conversation principles

- Do not assume the user knows game-design terminology, can write a design document, or can provide formulas or technical details.
- Inspect provided text, project materials, and available context before asking for information they already contain.
- Return only the depth needed for the current stage instead of dumping a complete framework.
- When the user is unsure, offer two or three clear options, explain the practical difference, and recommend a default.
- Leave important player-experience and product choices to the user. Continue through ordinary design details with the smallest compatible, testable assumption.
- Treat examples from other games as design coordinates, not proof that a concept will work.

## Workflow stages

Classify the current stage and perform only the relevant work:

1. **Initial exploration:** the idea is incomplete and needs focused questions followed by distinct directions.
2. **Direction comparison:** multiple candidates already exist and need meaningful comparison.
3. **Detailed design:** a direction is chosen and needs only the rules required to become playable or testable.
4. **Playtest analysis:** observations, interviews, or data exist and should update the evidence state and next decision.

If the user has already established a later stage, do not force the conversation back to initial exploration.

## Beginner onboarding

First inspect everything the user has already supplied. If material gaps remain, ask one compact batch of three to five unanswered questions that would change the design. Prefer a structured question tool when available. Prioritize:

- **Idea or problem:** what is being created, changed, or fixed?
- **Target player and context:** who plays, how many people play, and in what setting?
- **Intended and excluded experience:** what should players mainly feel or do, and what should the game avoid becoming?
- **Main actions or current loop:** what do players currently do, or what are they expected to spend most of their time doing?
- **Constraints:** what limits cannot be ignored, such as time, content, platform, existing systems, or production capacity?

Give short examples or two to three meaningful options when they make a question easier to answer, and explicitly allow uncertainty. Never repeat a question the existing context already answers.

After the main batch, summarize the current understanding and working assumptions, then continue. Ask at most one focused follow-up only when a single unresolved choice would materially change the directions and cannot responsibly be represented by alternatives. If the initial context is already sufficient, skip onboarding questions and move directly to the relevant stage.

## Compact gameplay brief

Before divergent exploration, summarize only the information that will steer the design:

- target player and play context;
- intended and excluded experiences;
- main actions, primary objective, or ending condition;
- material constraints and reusable content;
- unresolved working assumptions.

Keep evidence types distinct:

- **Known fact:** supplied by the user, established project material, or a reliable observation.
- **Working assumption:** temporarily adopted so design work can continue and still open to revision.
- **Testable hypothesis:** a prediction that a rule will create a player behavior or experience.
- **Player evidence:** actual behavior, statements, telemetry, or playtest results from relevant players.

## Divergent exploration

During open exploration, provide at least three materially distinct, playable directions before asking the user to choose. Different names, themes, enemies, maps, event order, difficulty, rewards, or presentation do not create distinct directions when players still pursue the same objective and repeat the same central decision.

For each serious direction, cover only what is needed to imagine one representative session:

- the player promise and how it differs from the current experience;
- the flow from opening through escalation to resolution;
- win, loss, or other ending conditions;
- the recurring decision, including one concrete example;
- the expected system response, readable feedback, and next decision;
- reusable building blocks and genuinely new behavior;
- why the rules might create the intended experience, explicitly labeled as untested;
- the largest design or production risk.

Compare the directions in plain terms: player experience, reuse, new work, and risk. A recommendation must explain its reasoning and preserve the important uncertainty. Merge or redesign candidates with the same objective, recurring decision, and session shape.

## New-mode and reuse gate

- Call a concept a **new mode** only when both its primary objective and the recurring decision that organizes play change.
- If players still follow the existing loop and only the win condition, pace, map, enemies, events, difficulty, rewards, or presentation change, call it a variant or modifier.
- Reuse existing systems as capabilities and content rather than automatically preserving the old loop.
- Understand worthwhile experiential directions before comparing production cost. Once a direction is selected, reduce it to the smallest version that tests its central decision.

## Convergence and necessary rules

When a direction is selected or already established, specify only what the first useful test requires: rules, states, resources, feedback, difficulty sources, recovery from mistakes, expected strategies, and ending conditions.

Trace each important rule through this causal chain:

**Player decision → system response → readable result → next meaningful decision**

Do not expand into full content production, long-term progression, exhaustive edge cases, or implementation architecture before the central decision has earned that scope.

## Minimum validation

Identify the hypothesis most likely to invalidate the direction and rewrite it as a falsifiable prediction. For example: "If players repeatedly choose between safety and reward, they will deliberately change routes instead of always selecting the safest path."

Define a minimum falsification test with:

- the design decision the test must inform;
- the fewest rules and content required;
- observable player behavior, understanding, or experience;
- signals that support, weaken, or disconfirm the hypothesis;
- the next smallest decision after the result.

Read [gameplay-evidence.md](references/gameplay-evidence.md) only when choosing a research method, experience measure, or theory lens. When no baseline, target effect, variance, or required confidence is available, leave participant counts and quantitative thresholds as `TBD` and state what evidence is needed to set them.

## Routing and boundaries

- Use `$game-design-game-balancing` when available for dedicated numerical, strategy, difficulty, build, progression, reward, economy, or randomness balancing of an existing system.
- Use `$game-design-player-ux-risk` when available for a dedicated audit of stalling, unwinnable states, griefing, unfairness, or degenerate strategies.
- Use `$game-design-ui-ux` when available for general interface, guidance, copy, information hierarchy, or accessibility work.
- Use `$game-design-friendslop-design` when available for friends-lobby concepts whose value primarily depends on social interaction.
- Pure narrative, character, worldbuilding, monetization, and code implementation are outside this skill unless those constraints directly change gameplay.
- Do not implement code, modify projects, write to external systems, or recruit players unless the user explicitly requests that action.

## Output and stop rules

- During initial exploration, lead with clearly distinct playable directions rather than a complete design document.
- During convergence, preserve decisions, material assumptions, evidence states, tradeoffs, the recommended next decision, and its validation method.
- Stop and ask when a missing, undiscoverable product decision would materially change the player experience and alternatives would be misleading.
- Stop expanding when the central risk can be tested with a smaller prototype.
- Narrow the claim or report missing evidence instead of guessing.

