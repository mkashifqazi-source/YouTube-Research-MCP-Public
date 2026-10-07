# Transcript and supplied-evidence workflows

## Live best-effort retrieval

Normalize reference → derive exact source identity → build provider request → invoke one configured provider → capture result and safe attempt → stop or use narrowly eligible fallback → return provenance and uncertain transcript/error.

Provider IDs are deduplicated. Each is attempted once. The service continues only for nonretryable transcript unavailable, language unavailable, captions disabled or metadata unavailable. Success, retryable errors, missing error information and all other errors stop. Retryable does not mean retry now. Blocking must not silently trigger multiplied traffic.

Manual versus automatic selection is provider/request policy. Successful retrieval does not certify caption accuracy, authorship or completeness. Empty extractor dictionaries, especially with upstream warnings, establish only what returned metadata contains, not video-wide caption absence.

## Offline supplied evidence

Bound structural admission → validate exact supported identity agreement → validate raw text/segment/claim types and sizes → validate finite consistent timing where provided → preserve original content and timing representation → emit accepted/warnings or safe rejection.

The current internal validator uses trusted context for receipt time and clocks; caller dates/attribution/completeness remain claims. It performs no network fetch, persistence, model interpretation or content fingerprinting. Untimed/partially timed data is not repaired by invented timestamps. Different raw-text and segment-text representations retain a difference warning rather than destructive normalization.

## Future research packet/citations

The design anticipates operations over accepted evidence that remain useful when live retrieval fails. Search/range/chunk operations would need exact source/artifact binding, transformation lineage and timing eligibility. They are not currently shipped tools. A timestamp citation should remain unavailable where timing/alignment evidence cannot support it; chunking does not create missing coverage.
