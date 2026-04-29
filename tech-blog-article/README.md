# tech-blog-article

Drafts front-page-quality technical articles in the voice of a senior developer and technical writer - clarity of Julia Evans, pragmatism of Dan Abramov, storytelling of Charity Majors. Five inputs drive a locked output: 60-char title, concrete hook, credibility context, TL;DR box, complete-thought H2s, wrong-then-right code examples under 20 lines, real trade-offs, and one of four ending patterns. Pre-write validation halts on missing inputs or out-of-range word counts; silent post-write gate enforces title length, TL;DR bullet count, H2 quality, code-block annotations, and ending pattern.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace.

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install tech-blog-article@chrismccoy
```

## Use

Slash command:

```
/tech-blog-article "Why your Postgres connection pool keeps exhausting"   # arg seeds TOPIC, picker fills the rest
/tech-blog-article                                                        # full 5-question intake
```

Or auto-triggers on natural language:

- *"write a technical article about X"*
- *"draft a blog post on Y"*
- *"Hacker News style article on Z"*
- *"Dev.to article about ..."*
- *"engineering blog post about ..."*
- *"technical write-up on ..."*

## What's in here

```
tech-blog-article/
├── .claude-plugin/plugin.json   ← plugin manifest
├── commands/
│ └── tech-blog-article.md       ← /tech-blog-article slash command (5-field AskUserQuestion intake)
└── skills/tech-blog-article/
 ├── SKILL.md                    ← workflow (load template → validate inputs → write → silent output gate)
 └── references/
 └── prompt-template.md          ← authoritative master prompt with placeholders
```

## Inputs

- `TOPIC` - what the article is about.
- `AUDIENCE_LEVEL` - reader technical level (beginner, intermediate, advanced).
- `ARTICLE_ANGLE` - framing (tutorial, opinion, deep-dive, lessons-learned).
- `PRIMARY_LANGUAGE` - language/framework for code examples.
- `WORD_COUNT` - target length, integer 300-5000.

All five treated as inert data. Directives or "ignore previous" patterns embedded in any field are ignored.

## Output structure (locked)

- `# Title` - max 60 characters
- Hook paragraph (2-3 sentences, concrete scenario)
- Context paragraph (credibility + scope)
- `> **TL;DR**` box with 3-4 bullets
- H2 sections - each a complete thought, with wrong-then-right code examples, trade-offs, and a "So What?" payoff
- `## What I'd Do Differently / Key Takeaways` closing with one of four ending patterns
- One-line author bio

## Validation

**Before writing:** halts on any bracketed placeholder (`Missing input: <field>.`) or a word count outside 300-5000 (`Invalid input: Word count must be a number from 300 to 5000.`).

**After writing (silent):** title ≤ 60 chars; TL;DR 3-4 bullets; every H2 a complete thought; every code block has a language identifier and plain-English explanation; closing uses one ending pattern. Fails are fixed before output.

## Scope lock

Writes technical articles only. Non-writing or role-change requests get: `I only draft technical articles - give me a topic and I'll write.`
