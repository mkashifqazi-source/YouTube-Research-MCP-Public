# Technical decisions

## Conservative provider fallback

**Context:** Providers can share unhealthy access/transport conditions.

**Decision:** Sequential once-per-provider execution, with fallback only for defined nonretryable availability categories.

**Why:** Blocking/retryable failure must not silently multiply requests or disguise ambiguity.

**Alternatives considered:** Unrestricted fallback/retry is rejected by the existing policy. No independent hosting remedy is established.

**Consequences:** Fewer chances to obtain a transcript in some cases, with clearer attempt accounting and bounded behavior.

**Current status:** Implemented service policy.

## Evidence-first hybrid direction

**Context:** A cloud endpoint can be reachable while live caption acquisition remains unreliable.

**Decision:** Preserve the deterministic core and propose explicit supplied/persisted/live evidence capabilities.

**Why:** Useful processing over accepted artifacts need not depend on fresh retrieval every time.

**Alternatives considered:** The ADR rejects treating host/provider reordering as an established solution and does not adopt a local dependency or bypass approach.

**Consequences:** Narrower honest promise, plus future validation/storage/retention complexity; first-time arbitrary-video acquisition remains unresolved.

**Current status:** Accepted research direction, not production release. Internal supplied-validation code exists; persistence/public orchestration remain future.

## Preserve supplied claims without upgrading their authority

**Context:** Callers may provide complete/manual/official/timing assertions alongside text.

**Decision:** Validate bounded data and preserve claims separately; initial kind is supplied and status uncertain.

**Why:** Structural validity is not independent speech/source verification.

**Alternatives considered:** The H2 contract rejects fabricated provider provenance or invented timing; no broader alternative study is claimed.

**Consequences:** Accepted evidence can remain useful with explicit warnings and timing restrictions.

**Current status:** Internal fixture validator present; old specification status needs reconciliation with current code.
