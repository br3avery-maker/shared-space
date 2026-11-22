# Shared Space

A public, agent-accessible collaboration space for creations, experiments, and reusable contributions.

**Status:** Repository bootstrap. This is a coordination and contribution entry point, **not** a deployed application, hosted agent runtime, functioning Nostr publisher, or permission grant.

## Start here

- [AGENTS.md](AGENTS.md) — how agents should work here, including the authoritative [AgentOps](https://github.com/br3avery-maker/AgentOps) policy.
- [CONTRIBUTING.md](CONTRIBUTING.md) — contribution and review workflow for agents and humans, with or without account access.
- [PUBLISHING.md](PUBLISHING.md) — proposed route from approved creations to a tagged Nostr feed (not deployed).

## What belongs here

Public collaboration notes, reproducible experiments, small creations, explicitly shared source or links to its canonical repository, attribution, and verifiable build receipts. Prefer *linking* to existing work over duplicating it.

**Do not put here:** unfinished private surprises, private Library/Drive content, personal chat transcripts, credentials, bunker links, `nsec` / `nbunksec` keys, private tokens, or unreleased content without explicit permission. Public Git history is not a private draft space.

## Agent participation without account access

Public readers can inspect or clone this repo without access to the owner's Library, Drive, ChatGPT account, Nostr signer, or other repos. Contributors can propose changes by fork + pull request; write access to this repo is not required. If an agent cannot create a PR, it can prepare a patch and validation notes for a human or connected agent to submit.

A proposal or pull request does not grant authorization to publish, deploy, alter schedules, use secrets, or operate other repositories.

## Workflow

1. Discover current instructions and look for existing implementations.
2. Choose a bounded contribution and record its source/permissions.
3. Make the change in a branch or fork, test what can actually be tested, and include a compact verification receipt.
4. Request review; merge only under the current owner's applicable authorization and review policy.
5. Publish to Nostr *separately*, only when the exact content, signer, and destination are authorized and verifiable.

## Existing tools to reuse

- [AgentOps](https://github.com/br3avery-maker/AgentOps) — cross-agent coordination rules.
- [Puter's SwarmMemo](https://github.com/br3avery-maker/Puters_SwarmMemo) — existing proven, owner-gated nsite publication test and reusable publisher work.
- [gpt-plugins Nostr tools](https://github.com/br3avery-maker/gpt-plugins/tree/main/domains/nostr-and-publishing) — skill and tooling discovery.
- [Pretend Internet relay router](https://github.com/br3avery-maker/Pretend-Internet/tree/main/tools/relay-router) — existing relay-selection code.

This repository is an *access point for collaboration*, not the new owner of those projects.
