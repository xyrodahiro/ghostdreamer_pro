# 0002 Stateless relay

Decided 2026-11-22.

- Content is prepared (not live capture); scheduled playout with normal live-stream delay. HLS for viewers; no WebRTC.
- The relay domain stores pointers, owner public keys (flat file) and aggregate feature counters only. No content, no per-visitor data, no database.
- Security in the URL: each owner's app holds a keypair and signs share links (stream, location, expiry). The relay verifies the signature per request. Revoke by expiry or key-version bump.
- Content stays with owners: external (their host, CDN or YouTube) or singular (their own Ghostdreamer instance).
- Access is by unlisted link only; no public directory. Optional passcode later.
- Visitor feedback adds +1 to daily feature counters (one JSON file); /stats renders a server-side bar chart.
- Owners relay only content they own or have rights to. As host: terms of use, DMCA agent and takedown process, report link, admin disable.
- Staging: v0.4 single user, v0.5 multi-owner opt-in, v0.6 Pro RC.
