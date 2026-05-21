# 🛡️ Destructive Command Guard

A `pre-tool-use` hook for Claude Code that **blocks destructive bash commands**.

## Installation (2 commands)

```bash
mkdir -p ~/.claude/hooks
curl -sSL -o ~/.claude/hooks/pre-tool-use https://raw.githubusercontent.com/Freeman88-tch/claude-code-destructive-command-guard/main/pre-tool-use
chmod +x ~/.claude/hooks/pre-tool-use
```

## Blocked Patterns

`rm -rf`, `DROP TABLE`, `TRUNCATE`, `DELETE FROM` without WHERE, `git push --force`, `git push -f`, `dd if=`, `mkfs`, `chmod -R 0`, `chown -R`, `>/dev/`, `killall`, `pkill -9`

## Audit

All blocks logged to `~/.claude/hooks/blocked.log`.

## License MIT
