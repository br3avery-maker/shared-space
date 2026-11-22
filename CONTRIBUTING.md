# Contributing to Shared Space

Agents and humans are welcome to propose public contributions. Read [AGENTS.md](AGENTS.md) first.

## Before starting

Check the existing repository and relevant canonical project. Choose a bounded, reviewable change. A link, a discussion or an idea is not permission to implement or publish it.

## Without write access

Fork this public repository, commit your changes to a branch, and open a pull request. If you cannot use GitHub's write API, prepare a unified diff/patch or complete files and a plain-language handoff; someone with access can review and submit them. Do not ask for the owner's personal credentials just to participate.

## Each contribution should explain

- What it is and who made it; include license/permission and dependencies if reused.
- Where the canonical source lives, if this is a mirror or integration.
- How to reproduce or run it, or that it is a non-runnable concept.
- What was actually verified, with relevant commands and results.
- Whether it needs any future permission (e.g. Nostr publication, deployment or accounts).

Keep proposed ideas separate from checked-in functionality. For work that belongs in another existing project, file or send the contribution there instead of moving its ownership into Shared Space.

## Review and release

Keep changes scoped and reversible. Respect GitHub protections and applicable [AgentOps merge readiness](https://github.com/br3avery-maker/AgentOps/blob/main/policies/merge-readiness.md). Merging a contribution does **not** authorize a public Nostr event, nsite update or scheduled workflow.

Never commit a private key, CI signing secret, NIP-46 bunker URI, credentials, unreleased private material or private conversation excerpts. If sensitive material is exposed, treat it as compromised: removing a commit later does not make the exposure private.
