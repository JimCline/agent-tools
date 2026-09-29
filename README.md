# agent-tools

This project has moved to **[agentic-tool-labs/agent-tools](https://github.com/agentic-tool-labs/agent-tools)**. This repository is archived and no longer updated.

## Switching an existing install

The marketplace keeps its name, `agent-tools`, so remove it in Claude Code and add it back from the new address. Then install each plugin you had, one line per plugin:

```
/plugin marketplace remove agent-tools
/plugin marketplace add agentic-tool-labs/agent-tools
/plugin install <plugin>@agent-tools
```

The plugins are `ah`, `task-gopher`, `output-discipline`, `comment-discipline`, `review-guide`, `github-pr-toolkit`, `idle-compactor`, `compaction-capture` and `compaction-guard`.

## Updating a local clone

The new repository starts from a fresh history, so `git pull` in an old clone fails with "refusing to merge unrelated histories". Point the clone at the new address and reset it:

```sh
cd /path/to/your/clone
git remote set-url origin https://github.com/agentic-tool-labs/agent-tools.git
git fetch origin
git reset --hard origin/main
```

`git reset --hard` discards uncommitted changes and local commits in the clone, so save anything you want to keep first. Or clone the new repository fresh.
