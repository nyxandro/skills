# nyxandro skills

A Claude Code plugin marketplace with my agent skills. Each skill lives and is updated in its
own repository; this repository only lists them, so that Claude Code can install any of them as
a plugin from one place.

## Install

Add the catalog once, then install the skills you need. In a Claude Code session:

```text
/plugin marketplace add nyxandro/skills
/plugin install telegram-bot-development@nyxandro
/plugin install prod-recon@nyxandro
```

On Claude Code 2.1.275 or later, one command adds the catalog and installs a skill:

```text
/plugin install telegram-bot-development --marketplace nyxandro/skills
```

Every installed skill adds its description to every session, so install the ones you use.

No version is pinned: every commit to a skill's repository is a new version. To take it, run
`claude plugin marketplace update nyxandro` and then `claude plugin update <skill>@nyxandro` in
your shell, or turn on auto-update for the catalog under `/plugin` → Marketplaces.

## Skills

| Skill | What it does | Repository |
| --- | --- | --- |
| `telegram-bot-development` | Build, review and debug Telegram bots and Mini Apps against the live Bot API: the agent checks the official docs and the installed library before any call | [telegram-bot-development-skill](https://github.com/nyxandro/telegram-bot-development-skill) |
| `t-invest` | Gives the agent access to your T-Invest brokerage account: portfolio data, analytics and operations on your command, answered from the real account | [t-invest-skill](https://github.com/nyxandro/t-invest-skill) |
| `property-testing` | Property-based tests with fast-check and Hypothesis: the strongest property, honest generators, failure triage | [property-testing-skill](https://github.com/nyxandro/property-testing-skill) |
| `issue-register` | Revise a project's register of open problems against the code: cut what is closed, keep one file, report | [issue-register-skill](https://github.com/nyxandro/issue-register-skill) |
| `goal-rules` | Finish a `/goal` task while the owner is away: no questions, recorded decisions, a hard stop-list, a written report | [goal-rules-skill](https://github.com/nyxandro/goal-rules-skill) |
| `prod-recon` | Read-only reconnaissance of prod or stage: find the way in, confirm the running commit, read logs and the database, report and stop | [prod-recon-skill](https://github.com/nyxandro/prod-recon-skill) |
| `session-handoff` | Carry unfinished work from one agent session to the next with one verified document | [session-handoff-skill](https://github.com/nyxandro/session-handoff-skill) |
| `sparring` | Model-vs-model sparring for plans, reviews and second opinions, with Claude, Codex and tmux-backed CLI agents | [sparring-skill](https://github.com/nyxandro/sparring-skill) |

Each skill's own README says what it needs and how to use it.

## Other agents

OpenCode and other agents that read skill folders: take the skill from its repository. Each
README there says how, and most offer a downloadable `.skill` archive.

## Repository layout

```text
.claude-plugin/marketplace.json   the catalog: one entry per skill, pointing to its repository
```

## License

MIT, for the files of this repository. It does not cover the skills: see each skill's repository.
