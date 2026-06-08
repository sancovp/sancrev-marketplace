# SANCREV Marketplace

The Claude Code **plugin catalog** for the SANCREV / GNOSYS ecosystem.

This is a **thin reference catalog** (tier 3 of the [scalable-publishing](https://sancovp.github.io/aisaac/) topology): it holds **one** `.claude-plugin/marketplace.json` that **points at each plugin's own public repo** (tier 2). It does **not** house any plugin's code — plugins are projected into their own repos from the private dev monorepo by the publishing pipeline, and this catalog just references them.

## Install

```bash
claude plugin marketplace add sancovp/sancrev-marketplace
claude plugin install doc-mirror@sancrev-marketplace
claude plugin install promptworld@sancrev-marketplace
```

> Plugins activate on the next Claude Code **restart**.

## Plugins

| Plugin | What it is | Repo |
|---|---|---|
| **doc-mirror** | A 1:1 documentation mirror of any codebase, maintained by an invariant state machine (per-module impl `doc(m)` grounded in real code structure + a `vision(m)` backlog, CLI-only managed files, no random documents). | [sancovp/doc-mirror](https://github.com/sancovp/doc-mirror) |
| **promptworld** | The meta-compiler *World: an Engineer-CEO + PromptGym specialist agents that compile / compose / publish prompt systems through the nomicon, with a one-command docker deploy wizard. | [sancovp/promptworld](https://github.com/sancovp/promptworld) |

## Docs

Full documentation, blogs, and the ecosystem map: **https://sancovp.github.io/aisaac/**

---

*Adding a plugin = one entry in `.claude-plugin/marketplace.json` pointing at the plugin's own public repo. Never a code monorepo; never a one-off marketplace per plugin.*
