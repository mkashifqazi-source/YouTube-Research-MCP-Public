# Failure taxonomy and evidence quality

The shared taxonomy distinguishes invalid/unsupported reference and playlist forms; video access/state restrictions; caption/transcript/language availability; metadata ambiguity; source mismatch; rate limits/provider blocking; request/provider timeouts; size limits; and cache-related errors. Enum presence does not imply a cache implementation.

| Case | Evidentiary consequence |
|---|---|
| Valid normalized reference | Stable association; no existence/publicness assertion |
| Live success | Provider-bound segments and provenance; completeness remains uncertain |
| Provider blocking or retryable transport issue | Stop orchestration; no automatic second-provider bypass |
| Empty returned caption metadata | Preserve returned-info scope and warnings; no universal absence claim |
| Supplied valid text | Accepted bounded artifact; upstream kind/official/completeness claims remain unverified |
| Supplied identity mismatch | Reject; no cross-video substitution |
| Partial/untimed segments | Preserve timing limits; no fabricated full coverage |
| Future stored read | Preserve original acquisition time; a read is not refresh |

Provider diagnostics use bounded categories, and supplied-validation rejections use fixed safe tokens. This does not establish blanket redaction across all layers: original request references can remain in normalization results and require private handling. A failure category describes the observed failure domain, not a universal explanation of upstream access behavior.

Manual captions can be incomplete or erroneous; automatic captions introduce transcription errors. Acceptance of evidence does not establish truth of speech or factual correctness. Coverage quality, acquisition availability and content accuracy are independent axes.

Representative cloud retrieval, persistence integrity, timestamp citation quality and production cost/availability remain unresolved. The public promise is best-effort transcript evidence preparation, not guaranteed transcripts for arbitrary public videos.
