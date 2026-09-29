# Sterium AI

**A one-person studio that ships software by directing AI coding agents.**
I write the objectives and playtest the results; the code is written by AI agents. For the larger projects,
planning, implementation, review and repair run through my own pipeline, with agents from different AI providers
checking each other under contracts a machine can verify.

🌐 [steriumai.dev](https://steriumai.dev) · ▶ [Play DEEPER free](https://play.steriumai.dev) · ✉️ hello@steriumai.dev

## Projects

### [agent-orchestrator](https://github.com/sterium-ai/agent-orchestrator) — the pipeline
An unattended delivery pipeline: GitHub issues in, reviewed and merged pull requests out. It runs **Claude Code, Codex
and GitHub Copilot** as interchangeable workers across five roles, and adds the parts that make unattended runs safe:
- the reviewer is always a **different AI provider** from the author
- the supervisor **re-runs the acceptance checks itself** and merges **only the exact commit that was reviewed**
- a bounded repair ladder, crash recovery and quota failover between providers
- 582 automated checks. In its case study it merged **124 pull requests in 13 days** on a Godot game.

### [deepholm](https://github.com/sterium-ai/deepholm) — built by the pipeline
A deterministic colony simulation in Godot 4, written and reviewed almost entirely by the agents above. Seeded,
replayable simulation kept apart from the viewer, **90 headless test scripts with 808 checks**, a save format that went
through **25 schema versions with 24 tested migrations**, and **43 architecture decision records**.

### [DEEPER](https://github.com/sterium-ai/deeper-site) — the game
A pixel-art colony survival game where the only way is down: eight layers, twelve creatures and a dragon, fluid lava,
light that decides where monsters spawn, and a soundtrack generated live. TypeScript and Canvas with no engine: the
whole browser demo is **one 280 KB file**. [Play the demo](https://play.steriumai.dev) · full game coming to Steam,
itch.io and Google Play.

### [stack-and-wrap](https://github.com/sterium-ai/stack-and-wrap) — a 3D prototype
A mobile-first gift-shop tycoon in Three.js: stack boxes, wrap presents, automate the shop, unlock new zones. Exact
economy numbers with animated transfers, pooled visuals, quality tiers for phones, and 280 logic checks that run in
plain Node. [Play it in the browser](https://sterium-ai.github.io/stack-and-wrap/).

## How the work is done
- **Contracts over trust:** tasks carry acceptance commands; nothing merges until the host has run them.
- **No self-review:** an agent never approves its own code; a different provider reviews every change.
- **Decisions are written down:** architecture decision records, size budgets and schemas keep many agents consistent.
