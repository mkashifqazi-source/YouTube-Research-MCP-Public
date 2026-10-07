# Testing and validation

The source includes offline tests for URL normalization, contracts, provider behavior, orchestration, yt-dlp metadata/WebVTT evidence and supplied validation. Fake clients/fixture payloads test acquisition semantics without proving upstream availability.

Supplied-evidence tests actively deny network resolution/connections, external URL opening, subprocess invocation and file opening during validation. They check source agreement, fixed safe rejection tokens, caller-claim isolation, bounded hostile shapes, finite/corrected timing, content preservation, no caller-input mutation and absence of fabricated alignment/coverage verification. These tests assert the validator's actual offline boundary rather than only its return shape.

Provider/service regressions cover once-per-provider attempt accounting, conservative fallback, blocking/rate/timeout failure, caption selection and ambiguity. WebVTT parsing verifies segment representation; metadata tests distinguish returned-info scope from global no-caption claims.

Historical cloud probes established occasional retrieval but not representative reliability. The recorded matrix stopped on provider blocking. That is feasibility evidence, not a benchmark establishing production coverage. Offline correctness cannot establish sustained live access or a recurring-cost guarantee.

No live YouTube, provider, cloud or test execution was performed in this showcase task. Current supplied-validator acceptance and public integration need reconciliation with older specification-only status. Production gates remain distinct from successful offline fixtures.
