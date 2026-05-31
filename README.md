# AIHelpers
Helpful Scripts and Tools for AI work

## codex-transcript

Bash script that renders Codex `rollout-*.jsonl` session files as a readable transcript, labeling
user prompts as `[TURN N]` and agent replies as `[AGENT]`. Preserves fenced code
blocks and wraps prose at a configurable width.

Usage: `scripts/codex-transcript [-w N] [rollout-file ...]` (defaults to
`./rollout-*.jsonl`).

Sample output:

```
[TURN 1]
  add a --json flag that emits each turn as a JSON object

[AGENT]
  I'll thread a --json option through the arg parser and switch the awk
  renderer to emit one object per turn instead of wrapped prose.

[TURN 2]
  also include the agent's token counts when available

[AGENT]
  Token counts live on the token_count event, not the message event, so
  I'll join them by turn index before emitting.
```

More scripts coming.
