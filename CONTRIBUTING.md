# Contributing to Edge Gateway Service

[Root README](README.md) · [Architecture](docs/ARCHITECTURE.md) · [Setup](docs/SETUP.md) · [API guide](docs/API.md) · [Network Ecosystem](README.md#network-ecosystem)

## Current scope

This is a documentation-only gateway scaffold. No listener, routing implementation, dependency manifest, runtime stack, deployment, or test suite is implemented. Architecture and API notes are proposals. Do not describe sibling links as working integrations.

## Contribution workflow

Read the guides and agree a narrowly scoped issue/design with the owner. Begin local work on a focused branch:

```sh
git clone https://github.com/OBAIAHMOPURI/edge-gateway-service.git
cd edge-gateway-service
git switch -c docs/describe-change
```

Use a pull request for normal review. This documentation batch's direct-to-main publication was specifically approved and is not a standing merge policy. Do not add guessed build/run commands; runtime selection is still open.

## First implementation decisions

- Decide the relationship to `edge-gateway-service1` and which, if either, is canonical. Neither is confirmed as a replacement/version of the other; do not merge, rename, or retire repositories without approval.
- Define route allowlists, request size/method validation, forwarding-header ownership, and safe upstream selection to avoid arbitrary destination access.
- Agree identity/policy contracts, fail-closed behavior where required, timeout budgets, cancellation, and safe retry/idempotency rules.
- Choose a supported runtime, configuration format, local synthetic upstream fixture, build pinning, and test harness before implementation claims.

## Quality and review evidence

For documentation, run `git diff --check`, inspect Markdown rendering, and verify root README, architecture/setup/API links and all seven sibling links. Keep current facts separate from proposals. There is no existing automated test result to cite.

For future code, include reproducible prerequisites and tests for invalid routes/configuration, disallowed upstreams, spoofed identity headers, rejected credentials, policy outages, request limits, timeouts, and non-idempotent retries. State exact commands/results and mark unrun tests honestly. A pull request should explain rationale, scope, compatibility, evidence, remaining risks, and migration/rollback needs. Update all affected contracts and guides together.

## Security and operational boundary

Use synthetic traffic and sandbox upstreams. Never commit tokens, credentials, private notes, or real request payloads. Sensitive reports belong in an owner-approved private channel, not a public issue. Public endpoints, production access, live proxying, infrastructure, and sharing changes require separate authorization. No license is selected by this guide.

## Sibling repository network

Navigation only; the gateway relationship is undecided and no live integrations are claimed.

- [alert-notification-dispatcher](https://github.com/OBAIAHMOPURI/alert-notification-dispatcher/blob/main/README.md)
- [Brainwave_Matrix_Intern — Banky Application](https://github.com/OBAIAHMOPURI/Brainwave_Matrix_Intern/blob/main/README.md)
- [BrainWave_Matrix_Intern1 — Hospital Management System](https://github.com/OBAIAHMOPURI/BrainWave_Matrix_Intern1/blob/main/README.md)
- [edge-gateway-service1](https://github.com/OBAIAHMOPURI/edge-gateway-service1/blob/main/README.md)
- [identity-auth-proxy](https://github.com/OBAIAHMOPURI/identity-auth-proxy/blob/main/README.md)
- [telemetry-stream-worker](https://github.com/OBAIAHMOPURI/telemetry-stream-worker/blob/main/README.md)
- [workflow-state-sync](https://github.com/OBAIAHMOPURI/workflow-state-sync/blob/main/README.md)
