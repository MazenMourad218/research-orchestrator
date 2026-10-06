# Research orchestrator for Claude

A meta skill for Claude that handles any market, policy, technology, competitor or customer research. It:

- sets the research context first (scope, languages, local data pitfalls)
- routes the work to the best research plugins you have installed, and falls back to web search when they aren't
- ranks sources (official and regulatory first, media last)
- enforces evidence rules: every fact sourced and dated, key numbers triangulated, confidence grades, honest gaps
- returns a standard research note: findings, evidence table, gaps, and "so what"

This repository is also a plugin marketplace, so you can install the skill and the research plugins it uses from one place.

## Option 1: install everything (recommended)

In the Claude desktop app:

1. Open **Customize > Plugins**, select **Add marketplace**, and enter `MazenMourad218/research-orchestrator`.
2. Install these three plugins from it:
   - **research-orchestrator**: the skill itself
   - **market-researcher** (by Anthropic): competitive analysis, sector overviews, comps
   - **exa** (by Exa): multi-step web research. After installing, open its **Connectors** tab and connect Exa.
3. Optionally, install two more from Anthropic's catalog (**Customize > Plugins > Discover**). They are not hosted on GitHub, so they can't be added here:
   - **Research Desk**: citation checks, decision matrix, second opinions
   - **Customer Research Kit**: feedback, interview and churn analysis

## Option 2: the skill only

1. Download **[research-orchestrator.zip](https://github.com/MazenMourad218/research-orchestrator/raw/main/research-orchestrator.zip)**. Don't unzip it.
2. In Claude, go to **Customize > Skills**, click **+**, then **Create skill > Upload a skill**, and select the zip.
3. Make sure **Code execution and file creation** is on (Settings > Capabilities on Free, Pro and Max; your admin controls it on Team and Enterprise).

Use one option, not both, or the skill will be installed twice.

## Claude Code

```
/plugin marketplace add MazenMourad218/research-orchestrator
/plugin install research-orchestrator@research-orchestrator-marketplace
/plugin install market-researcher@research-orchestrator-marketplace
/plugin install exa@research-orchestrator-marketplace
```

## Files

- `.claude-plugin/marketplace.json`: the marketplace listing
- `plugins/research-orchestrator/`: the plugin, with the skill in `skills/research-orchestrator/SKILL.md`
- `research-orchestrator.zip`: the skill on its own, ready to upload to Claude
# Research orchestrator: a Claude skill

A meta skill for Claude that handles any market, policy, technology, competitor or customer research. It:

- sets the research context first (scope, languages, local data pitfalls)
- routes the work to the best research skills you have installed, and falls back to web search when they aren't
- ranks sources (official and regulatory first, media last)
- enforces evidence rules: every fact sourced and dated, key numbers triangulated, confidence grades, honest gaps
- returns a standard research note: findings, evidence table, gaps, and "so what"

## Install in Claude (claude.ai, desktop or mobile app)

1. Download the skill: **[research-orchestrator.zip](https://github.com/MazenMourad218/research-orchestrator/raw/main/research-orchestrator.zip)**. Don't unzip it.
2. In Claude, go to **Customize > Skills**, click **+**, then **Create skill > Upload a skill**, and select the zip.
3. Make sure **Code execution and file creation** is on (Settings > Capabilities on Free, Pro and Max; your admin controls it on Team and Enterprise).

Then just ask Claude a research question. The skill switches on automatically.

## Recommended plugins (optional)

The skill works on its own, but routes to these when installed (all in Claude's plugin directory):

- **market-researcher** (Anthropic): competitive analysis, sector overviews, comps
- **Exa Deep Research**: multi-step web research
- **Research Desk**: citation checks, decision matrix, second opinions
- **Customer Research Kit**: feedback, interview and churn analysis

## Install in Claude Code

```
git clone https://github.com/MazenMourad218/research-orchestrator.git
cp -r research-orchestrator/research-orchestrator ~/.claude/skills/
```

## Files

- `research-orchestrator.zip`: ready to upload to Claude
- `research-orchestrator/SKILL.md`: the skill itself, readable on GitHub
