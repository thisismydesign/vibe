# vibe

### AI dev agent setup - make Cursor & Claude more like Devin

With this setup you can give more autonomy to Cursor and Claude Agents to work end-to-end creating PRs, checking CI, etc.

## Project setup

- Install [Claude Code](https://docs.anthropic.com/en/docs/agents-and-tools/claude-code/overview) and initialize to create [CLAUDE.md](CLAUDE.md) containing project guidelines, commands, etc.
  - This is optional but it will auto-generate a good starting point for your project.
- Setup a global Cursor [Rule](https://docs.cursor.com/context/rules-for-ai) to always follow [CLAUDE.md](CLAUDE.md): [cursor/rules/global.mdc](.cursor/rules/global.mdc)
- Setup custom Cursor Rules, such as [@task](.cursor/rules/task.mdc) which tells the agent how to execute a task end-to-end including testing, creating a PR, etc.
