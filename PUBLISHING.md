# Agent creation feed — publication design (not configured)

**Status: proposed, not deployed.** No signer, secrets, GitHub Actions workflow, Nostr feed or nsite was created by this repository's initial setup. Merging source code must never silently trigger public publishing.

## Intent

Let an agent contribute a creation via a GitHub fork/PR even without access to the owner's private services. After review and **separate, explicit authorization of the exact public release**, publish the approved static artifact as an nsite and create a Nostr feed announcement.

## Reuse the existing proven work

- [Puter's publishing runbook](https://github.com/br3avery-maker/Puters_SwarmMemo/blob/main/publishing/REUSABLE-PUBLISHER.md) and [release gate](https://github.com/br3avery-maker/Puters_SwarmMemo/blob/main/publishing/release_gate.py).
- [AgentOps publication evidence and cautions](https://github.com/br3avery-maker/AgentOps/blob/main/integrations/chat-github-nsite-publishing.md).
- [Existing Nostr publishing skills](https://github.com/br3avery-maker/gpt-plugins/tree/main/domains/nostr-and-publishing) and [Pretend Internet relay router](https://github.com/br3avery-maker/Pretend-Internet/tree/main/tools/relay-router).

The verified single-site publishing test does not prove the more general release workflow or a new signer identity has been tested end to end.

## Proposed sequence

1. **Intake:** a public pull request identifies author, canonical source, license/permission, intended creation, and reproducible output.
2. **Prepare:** review and test the exact built files. Generate an immutable release inventory (paths, SHA-256 hashes, sizes, version, attribution); keep publication separate from the merge.
3. **Authorize:** the owner approves *that* release and destination. A dedicated, revocable **publisher identity** may be provisioned later; no private signing key goes into this public repository.
4. **Publish:** use established nsyte / NIP-5A / Blossom / Nostr workflow. Preserve stable named nsite IDs across revisions.
5. **Announce:** publish a signed Nostr feed event with consistent `t` tags, author/source information and link to verified site; e.g. `agent-creations`, `pretend-internet`, `game` or `story`. Tags organize discovery; the publisher's public key and an allowlist establish trust.
6. **Verify:** independently retrieve the signed manifest, published blobs and feed announcement; record actual outcomes and failures. A successful signature alone is not proof of working site delivery.

## Feed selection

A consuming site can query configured Nostr relays for approved publisher public keys and `#t` tag values and display linked creations. Distinguish the NIP-5A manifest events used for static site resolution from the separately signed announcement events used to populate the feed. A tag alone is not authentication, moderation or publishing authority.

## Security and privacy

No private gifts, unreleased surprises, personal account data or connection secrets in public Git history, release manifests or announcements. Use a separate, durable signer identity only after deliberate setup and permission checks; do not generate throwaway credentials for a site that will need updates. Existing credentials and services should not be copied from other projects.

**Future work:** Decide which existing site consumes the feed and which authorized signer identity publishes. That choice is not made by this document.
