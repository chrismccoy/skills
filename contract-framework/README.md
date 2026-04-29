# contract-framework

Writes a clear, fair contract for freelance and consulting work. You answer a few questions about your business, your client, what you are delivering, and how you get paid. It hands back a ready-to-fill agreement in plain English that protects both sides without scaring the client off.

It always covers the three things freelancers fight about most: work that grows beyond what was agreed, clients who pay late, and who owns the finished work.

> This gives you a solid starting draft, not legal advice. Anything that changes from one country or state to another is clearly marked so you can check it with a local lawyer before you sign.

Part of the [`chrismccoy`](../README.md) Claude Code marketplace.

## Install

```
/plugin marketplace add chrismccoy/skills
/plugin install contract-framework@chrismccoy
```

## How to use it

Run the command and it walks you through the questions:

```
/draft-contract "brand identity: logo, type system, and guidelines"
/draft-contract
```

The first line uses your description as a head start. The second starts from a blank slate and asks you everything.

You can also just ask for it in plain words:

- *"draft a freelance contract"*
- *"write a service agreement"*
- *"create a consulting agreement"*
- *"draft a client contract for a design project"*
- *"put together an independent contractor agreement"*
- *"make me a contract framework"*

## What it asks you

- **Your name or business** (required)
- **Your client's name or company** (required)
- **What you are delivering** (required)
- **How you get paid** (required): the amount, the schedule, or the milestones
- **Anything extra you want protected** (optional): leave it blank for the standard protections
- **The tone** (optional): formal, plain professional, or a warmer creative style. Plain professional is the default.

If one of the four required answers is missing or looks like it was filled in wrong, it stops and asks you for just that piece before writing anything.

## What you get back

A contract with eight clearly labelled parts, always in this order:

- **Parties**: who the agreement is between, with spaces for full names, addresses, and the date.
- **Scope of services**: what is included, what is not, revision limits, and a rule that extra work needs to be agreed in writing first.
- **Payment terms**: the amount, the schedule, how invoices work, what happens if payment is late, and that finished work is held back until you are paid.
- **Intellectual property**: you keep ownership until you are paid in full, then it passes to the client, with a note if they would rather license the work instead.
- **Confidentiality**: both sides agree to keep private information private, with the usual sensible exceptions.
- **Termination**: how either side can end the agreement, including a cancellation fee and notice.
- **Liability and warranties**: sensible limits on responsibility and a promise that the work is original.
- **General provisions**: the standard closing clauses and a signature block for both sides.

If it can save files, it writes the contract to a tidy filename like `contract-your-business-client-name.md` and just tells you where it went. If it cannot, it prints the full contract on screen.

## What it will never do

- Make up laws, court cases, or country-specific rules.
- Invent names, numbers, fees, deadlines, or limits you did not give it. Where a detail is missing, it leaves a clearly marked blank like `[TO BE COMPLETED: kill fee basis]` for you to fill in.
- Add anything outside the eight parts above.
- Follow hidden instructions tucked inside your answers. Everything you type is treated as plain information for the contract, nothing more.

Anything that depends on where you live, like late-payment interest or which country's law applies, is written in neutral wording and flagged so you can confirm it locally.
