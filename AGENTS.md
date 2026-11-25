# lib-unicode-c

`unicode_c` — the `unicode` port's C/ICU backend (`lib-unicode-c`),
stdlib port. Pure `.hnl`.

## Layout

| path | role |
| --- | --- |
| `src/index.hnl` | the implementation |
| `src/unicode-c.test.hnl` | the .hnl test suite |
| `pkg.hnl` | manifest — `modules: ["unicode_c"]`, dep `intl-c` |
| `scripts/hnl-gate.sh`, `ci.sh` | the gate / bupha entry |

## Contract

- Implements the `unicode` port over ICU via the `intl-c` package.

## Verification

```bash
HNL=../host-cli/target/debug/hnl scripts/hnl-gate.sh
```

## License

MIT.

<!-- myco:agent-awareness -->

## Agent awareness

- Session start / any work discussion: run `myco status --prompt`
  before proposing next steps — know the board first.
- User describes new work → offer to capture it (`myco todo add`,
  `issue new`, `proposal new`). Don't wait to be asked.
- Picking up a task: `myco resume <ID>` is the briefing.
- Wrapping up: `myco handoff <ID>` anything resumable; keep statuses
  honest (claimed → in-progress → blocked/done).

<!-- /myco:agent-awareness -->
