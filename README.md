# Sira — a homeschool teaching skill for Claude Code

**Sira** helps a parent teach preschool and elementary children over time, grounded in **Kieran Egan's imaginative education** and the **Lost Tools of Learning**. It turns a folder into a stateful "family learning home" and produces low-prep, jargon-free, self-contained lessons — plus an "old friends" spaced-repetition system to keep what's learned alive.

Motto: *an academic unschooler's best friend.*

## Install

In Claude Code (you may need to `/login` first):

```
/plugin marketplace add visheshnagpal/sira-teach
/plugin install sira-teach@neha-teaching
```

*(Replace `visheshnagpal/sira-teach` with wherever this repo lives — a GitHub `owner/repo`, or a local folder path.)*

Then, in a folder you want to use as a learning home:

```
/sira-teach What should we help my child learn next?
```

Sira will interview you (one question at a time), set up the workspace, and build the first lesson.

## What's inside

- A six-branch operating model (onboard → make a lesson → record feedback → build guidance → audit progress → improve itself).
- Ten subject guides (geography, history, mathematics, sciences, languages, vocabulary/writing, literature, art/music, philosophy/world-religions, adulting).
- Craft references distilling Egan and the Lost Tools archive — kept *under the hood*; the parent and child only ever see practical, plain-language teaching moves.

## Credit & grounding

Built on Matt Pocock's `teach` skill structure; pedagogy grounded in Kieran Egan (*The Educated Mind*, *An Imaginative Approach to Teaching*) and Brandon Hendrickson's *The Lost Tools of Learning* (losttools.org). Subject guides are original distillations — they do not reproduce source archives.
