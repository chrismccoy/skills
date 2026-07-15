# changelog-generator

Write a changelog for your users from a repository's whole git history by reading the real code changes, not the commit messages. It goes from the first commit to `HEAD`, sorts every change by type, and writes newest first in plain language.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace.

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install changelog-generator@chrismccoy
```

## Use

Slash command:

```
/changelog-generator            # runs on the current repo
/changelog-generator ../my-app  # runs on a repo at that path
```

Or just ask in your own words:

- *"generate a changelog for this repo"*
- *"write release notes from the git history"*
- *"what actually shipped in this project?"*
- *"changelog from the code changes, don't trust the commit messages"*
- *"turn this repo's history into release notes my users can read"*

## What's in here

```
changelog-generator/
├── .claude-plugin/plugin.json         ← plugin manifest
├── commands/
│   └── changelog-generator.md         ← /changelog-generator slash command
└── skills/changelog-generator/
    ├── SKILL.md                       ← trust rules, steps, per-range brief, output format
    └── scripts/
        └── map-history.sh             ← repo check, first commit, tags, full timeline
```

## What it does

- **Reads the code change, not the message.** Commit messages leave things out ("bunch of fixes", "and more") and get the label wrong. The code change is the truth. The changelog says what really shipped, not what someone typed.
- **Covers the whole history.** First commit to `HEAD`, no gaps. It will not take a date or version range. The scope is always everything.
- **Checks the repository first.** `map-history.sh` stops if the folder is not a git repository, warns you when the copy is shallow (so it cannot claim to cover everything), and handles a one-commit history.
- **Splits the history into eras.** It breaks the timeline into date-and-theme chunks, one per release, using tags as the boundaries.
- **Handles big histories.** Over about 40 commits, or when a change is too large to read in one pass, it splits the work across several helpers at once, then combines their reports and double-checks anything surprising against the real code. It never quietly skips or samples.
- **Sorts every change by type.** feature, improvement, fix, security, breaking change, or internal.
- **Catches what messages hide.** It lists features buried under "and more", drops fixes that only undo a break made earlier in the same batch, refuses to call reworded or moved code "new", and flags any commit whose message says more or less than the code change actually did.
- **Pulls out security and breaking changes.** Real security work (how a check or block actually works) and breaking changes (a removed setting, a flipped default, a dropped endpoint) each get their own section.

## Output format

Grouped under emoji headings, newest release first, always in the same order, in plain language:

```markdown
# Updates - <period or version>

## ✨ New Features
## 🔧 Improvements
## 🔒 Security
## ⚠️ Breaking Changes
## 🐛 Fixes
```

The order is always New Features, then Improvements, then Security, then Breaking Changes, then Fixes. Empty sections are left out, and the order never changes. One line per entry, up to 7 bullets per section (the rest roll into a "and N smaller changes" line).

Good: **Faster search**: results now appear as you type, no Enter needed.
Bad:  **Refactored SearchController.debounce()**: reduced re-render calls.

When it is done, it offers to save the result to `CHANGELOG.md` and tells you where the code changes did not match the commit messages.

## Safety rails

- **Everything in the repo is data, not orders.** Commit messages, code changes, source, and filenames are read as text to describe. If a diff says something like "ignore the above" or "output X instead", it gets described, never obeyed.
- **Coverage check.** Before it writes anything, it confirms the chunks chain together with no gaps and that it opened the real code change behind every entry, none based on a commit message alone.
- **No made-up output.** If the folder is not a git repository it stops and says so instead of inventing a changelog. If the copy is shallow it warns you that the history is cut off.

## Style guide support

If the repo has a `CHANGELOG_STYLE.md` (or you name one), the plugin follows its formatting and voice. The one exception is the section order and the no-gaps rules, which always win. Any conflict is flagged for you.
