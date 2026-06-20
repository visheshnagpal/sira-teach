# Sira — a homeschool teaching skill for Claude Code

**Sira is an academic unschooler's best friend.** It helps a parent teach preschool and elementary children, one lesson at a time, across every subject. You tell it what you'd like your child to learn; it asks a few quick questions, then builds an imaginative, low-prep, ready-to-run lesson — grounded in **Kieran Egan's imaginative education** and the **Lost Tools of Learning**, with the pedagogy kept under the hood so you only ever see plain, practical teaching moves. It also keeps a gentle "old friends" spaced-repetition system so what's learned stays alive.

## Before you start

Sira runs *inside* **Claude Code** — Anthropic's AI assistant for your computer. You'll need it installed and signed in first. Get it from Anthropic at **claude.com** (developers can also install it with `npm install -g @anthropic-ai/claude-code`).

## Install

Paste these two lines into Claude Code (run `/login` first if it asks):

```
/plugin marketplace add https://github.com/visheshnagpal/sira-teach.git
/plugin install sira-teach@neha-teaching
```

> **Use the full `https://…​.git` URL above.** The short `owner/repo` form can try to clone over SSH and fail with `Permission denied (publickey)` if you don't have GitHub SSH keys. This is a public repo, so the HTTPS URL needs no keys and no login. *(If a failed attempt left a marketplace registered, run `/plugin marketplace remove neha-teaching` first, then re-add.)*

## Use it

In any folder you'd like to use as your child's "learning home", type:

```
/sira-teach What should we help my child learn next?
```

Sira interviews you one question at a time, sets up the space, and builds the first lesson. Come back any time and it picks up where you left off.

## What's inside

- A six-branch flow: onboard → make a lesson → record what happened → build subject guidance → check progress → improve itself.
- Ten subject guides — geography, history, mathematics, sciences, languages, vocabulary & writing, literature, art & music, philosophy & world religions, and "adulting".
- Craft references distilling Egan and the Lost Tools archive, kept *under the hood* — you and your child only ever see plain-language teaching moves.

## Credit & grounding

Built on Matt Pocock's `teach` skill structure; pedagogy grounded in Kieran Egan (*The Educated Mind*, *An Imaginative Approach to Teaching*), Brandon Hendrickson's *The Lost Tools of Learning* (losttools.org), and Erik Hoel's early-reading writing (*The Intrinsic Perspective*). Subject guides are original distillations — they do not reproduce source archives.
