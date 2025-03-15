# vibe

### AI dev agent setup - make Cursor & Claude more autonomous like Devin

With this setup you can give more autonomy to Cursor and Claude Agents to work end-to-end creating PRs, checking CI, etc.

## Usage

- Give a task to Cursor Agent: `@task Add i18n to the project`

## Project setup

- Install [Claude Code](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview) and initialize to create [CLAUDE.md](CLAUDE.md) containing project guidelines, commands, etc.
  - This is optional but it will auto-generate a good starting point for your project. Alternatively you can use README, docs, or anything else.
- Setup a global Cursor [Rule](https://docs.cursor.com/context/rules-for-ai) to always follow CLAUDE.md: [cursor/rules/global.mdc](.cursor/rules/global.mdc)
- Setup custom Cursor Rules, such as [@task](.cursor/rules/task.mdc) which tells the agent how to execute a task end-to-end including testing, creating a PR, etc.
  - Note that @task won't be recognized as a [symbol](https://docs.cursor.com/context/@-symbols/overview) like @Web, @Codebase, etc. It's just a name, you can use whatever you want.
  - In the beginning you might need to remind the Agent to follow the rules, but it gets better with time.
