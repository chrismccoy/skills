# session-stats

Render a Claude Code session's quantitative stats as a single self-contained, dark-theme HTML page.

The page is stats only: KPI cards (duration, prompts, tool calls, files written/edited, output
tokens, est. cost), a per-tool usage table with share bars, and a token-bucket table (input, output,
cache created, cache read). No prompts, observations, tone analysis, or recommendations.

## Pipeline

Two bundled scripts form an offline pipeline with no third-party Python packages (standard library only; requires Python 3):

1. `scripts/scan_jsonl.py` parses a Claude Code `.jsonl` transcript and emits a metrics JSON object.
   Cost is computed from each assistant message's token `usage` times per-model pricing (the
   transcript stores token counts, not dollars). Pricing follows the current Claude API catalog
   (Opus 4.8 = $5/$25 per MTok in/out, cache write $6.25, cache read $0.50). Override per MTok with
   env vars: `IN_RATE`, `OUT_RATE`, `CW_RATE`, `CR_RATE`.
2. `scripts/build_stats_html.py` injects that JSON into `assets/template.html` and writes a
   standalone document with no `<script>` tags and no external assets.

## Usage

Slash command (resolves the current session, or takes a path):

```
/session-stats [session.jsonl path]
```

Or run the pipeline directly:

```bash
python scripts/scan_jsonl.py --in <session.jsonl> \
  | python scripts/build_stats_html.py --out session-stats.html
```

Select one session from a multi-session scan with `build_stats_html.py --session <id-or-slug-prefix>`.

## Output

A complete `<!DOCTYPE html>` file that opens in any browser. Every number traces to the transcript;
absent fields render as `N/A`. The template is an inline static-CSS port of the design (no Tailwind,
no `<script>`, no external assets). To restyle, edit the CSS variables in the template's `:root` block
(for example `--accent`, `--ember`, `--ink`, `--coal`); `build_content()` emits the matching
`.kpi` / `table.t` / `.bar` classes, so keep those in sync if you change the structure.

## Layout

```
session-stats/
  .claude-plugin/plugin.json
  commands/session-stats.md          /session-stats command
  skills/session-stats/SKILL.md trigger + workflow
  scripts/scan_jsonl.py             jsonl transcript to metrics + cost
  scripts/build_stats_html.py       metrics JSON to dark HTML
  assets/template.html              fixed dark template
```
