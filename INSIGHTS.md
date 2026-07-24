# Marketplace Insights - Plugin Analysis

A quick guide to what's in this marketplace and how the plugins compare. Each plugin is sorted into one of three groups by **how much it does** - not by how good it is. A "quick win" plugin can be just as useful as a "full toolkit" one; it just does a smaller, more focused job.

**At a glance:** 1 quick win · 15 guided helpers · 14 full toolkits.

## Quick wins

Small, focused, one-and-done. You give it something, it hands one clear answer straight back.

| Plugin | How you start it | What it does for you |
|--------|------------------|----------------------|
| `excel-formula-troubleshooter` | `/fix-formula` | Paste a broken Excel or Google Sheets formula and get the fixed version, with an explanation of what went wrong |

## Guided helpers

These ask you a few questions (or take a short description), then produce a complete, well-organized result in one go. Great when you know roughly what you want and want an expert to shape it.

| Plugin | How you start it | What it does for you |
|--------|------------------|----------------------|
| `jq` | `/jq` | Builds a ready-to-paste command for pulling data out of JSON, and explains each step |
| `html-design-styles` | `/html-design-styles` | Restyles a web page in one of 53 named looks (bento, brutalist, glassmorphism, and more) |
| `vgademo` | `/vgademo` | Walks you through a few choices, then writes a tiny retro 1990s-style graphics demo |
| `tech-blog-article` | `/tech-blog-article` | Writes a polished technical blog post with a strong opening, clear examples, and honest trade-offs |
| `language-tutor` | `/language-tutor` | Translates and explains a phrase, or corrects your writing with grammar and pronunciation tips |
| `contract-framework` | `/draft-contract` | Writes a clear, fair freelance or consulting contract covering the work, the payment, and who owns the finished result, with anything legal flagged to check locally |
| `readme-builder` | `/readme-builder` | Reads a whole project and writes one beginner friendly README in a fixed order, plain English, with hype words and long dashes kept out |
| `tutorial-builder` | `/tutorial-builder` | Turns code or a topic into a step-by-step, hands-on tutorial that teaches, every code block runnable with its output shown, gated by a checklist and a 1-5 score |
| `naming-strategist` | `/name-domains` | Brainstorms 10 brandable domain names, picks the best 3, and gives you a checklist to verify them |
| `refactoring-analyst` | `/refactor` | Reviews your code and returns a prioritized clean-up plan, every issue tied to a real file and line |
| `kubernetes-architect` | `/kubernetes-architect` | Turns your app details into ready-to-use Kubernetes setup files |
| `docker-compose-architect` | `/docker-compose-architect` | Builds a secure Docker setup for your app - networks, storage, health checks, secrets kept safe |
| `app-blueprint` | `/blueprint` | Turns a one-line app idea into a full plan: folders, data, APIs, libraries, tests, and deployment |
| `wordpress-consultant` | `/wordpress-consultant` | A senior WordPress audit across architecture, performance, security, and scaling, with a 0-100 scorecard |
| `accessibility-audit` | `/accessibility-audit` or `/a11y-audit` | Checks a page, folder, or pasted component for accessibility problems, explains why each one matters, fixes them if you ask, and tells you which keys to test |

## Full toolkits

The heavy hitters. They run multi-step workflows, generate whole sets of files, or include built-in scripts and checklists. Best for bigger jobs where you want production-ready results, not just a draft.

| Plugin | How you start it | What it does for you |
|--------|------------------|----------------------|
| `wp-builder-pro` | `/wp-builder-pro` | Builds and fixes custom WordPress code - themes, plugins, blocks, WooCommerce, and more |
| `wordpress-plugin` | `/wordpress-plugin` | Generates a complete, ready-to-submit WordPress plugin from scratch, security and cleanup included |
| `wordpress-architect-review` | `/wordpress-architect-review` | Reviews a WordPress plugin or theme file by file, with a scorecard and the top fixes to make |
| `wordpress-formatter` | `/wordpress-formatter` | Formats a theme's template files to the WordPress standard - tabs, spacing, arrays - without changing how any page renders, and checks its own work |
| `powershell-script-engine` | `/powershell-script-engine` | Writes clean, production-ready PowerShell scripts with logging, error handling, and safe credential use |
| `html-to-wordpress-theme` | `/html-to-wordpress-theme` | Converts your static HTML into an installable WordPress theme, checking its own work as it goes |
| `unslop` | `/unslop` | Strips the AI-sounding voice out of your comments and names without changing how the code runs |
| `strip-unicode` | `/strip-unicode` | Flattens messy Unicode - curly quotes, long dashes, invisible characters - down to plain ASCII, cleaning a file in place or handing back tidied text, with a table of what changed |
| `docblock-rewrite` | `/docblock-rewrite` | Rewrites bulky code comments into short one-liners anyone can read, backing up the originals first |
| `codebase-to-mermaid` | `/codebase-to-mermaid` | Reads a codebase you don't know and draws accurate diagrams, every box tied to a real file and line |
| `mermaid-to-ascii` | `/mermaid-to-ascii` | Redraws a Mermaid diagram file as plain text-art and saves it next to the original, ready to paste into a comment, README, or terminal |
| `explain-my-code` | `/explain-my-code` | Reads a whole codebase and writes one onboarding document - architecture, flow, patterns, and risks, with diagrams |
| `changelog-generator` | `/changelog-generator` | Writes a changelog from a repo's whole history by reading the real code changes, not the commit messages, then sorts each change and saves the file |
| `session-stats` | `/session-stats` | Turns a Claude Code session into a single shareable stats page - prompts, edits, cost, and files changed |

## Good to know

**Three plugins have a shortcut name that's different from the plugin name:**

- `excel-formula-troubleshooter` → type `/fix-formula`
- `naming-strategist` → type `/name-domains`
- `contract-framework` → type `/draft-contract`

The other 27 use their own name as the command. `accessibility-audit` also answers to the shorter `/a11y-audit`.

**How each one gets what it needs from you:**

- **Asks multiple-choice questions** (just pick from a menu): 24 plugins - the easiest way to start
- **Asks a few questions directly:** 1 - `html-to-wordpress-theme`
- **Just works from what you point it at** (a file path or your current session, no questions): 5 - `changelog-generator`, `docblock-rewrite`, `mermaid-to-ascii`, `session-stats`, `wordpress-architect-review`

**One plugin runs only when you type its command:**

`accessibility-audit` is the exception to the rule below. It has no background trigger at all, on purpose. Accessibility tools are common, and if you have another one installed, two of them answering "make this accessible" is a coin flip. Typing `/accessibility-audit` or `/a11y-audit` removes the guesswork.

Every other plugin can be started with a simple `/command`, or just by describing what you want.
