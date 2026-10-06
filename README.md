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
