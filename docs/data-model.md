# Identity, transcript and provenance model

| Concept | Contract / interpretation |
|---|---|
| Video/source identity | Exact video ID and `youtube:<video_id>`; reference normalization does not prove current video existence |
| Caption kind | manual, auto or supplied; kind differs from acquisition origin |
| Transcript status | complete, partial, unavailable or uncertain; current successful live adapters remain uncertain |
| Segment | Text plus start, duration and end; parsed timings do not establish full-video coverage |
| Provider provenance | Provider identity/version, retrieval time, paid-unit accounting and safe warnings |
| Result envelope | Success data or structured error plus warnings and separate version concepts |
| Error | Category, retryability, provider and bounded safe details |
| Attempt history | Ordered provider attempts scoped to one operation |
| Supplied evidence | Preserved raw text and/or segments, claims, normalized identity, trusted-context receipt time and validation profile |

Supplied evidence is conservatively kind supplied and status uncertain even if a caller claims manual, official or complete. Validating an ID/content association proves consistent references, not that the text is what the video says. Timing syntax/range eligibility does not prove alignment with the video or verified time coverage.

Raw and clean text are distinct concepts. The current enum exposes none/clean/raw, but an end-to-end primary-tool text projection and cleaning engine were not established. Provider-parsed segment text should not be described as untouched upstream raw bytes.

The proposed H1 record separates immutable acquisition origin from current access mode. Loading stored live-origin evidence would retain its original provider/acquisition time and add separate storage/read observations. No current-source freshness follows from a later read.

Content fingerprints, source matching and external workflow history have different authority. No implemented persistence/history engine is inferred from schema vocabulary. A future fingerprint would identify a specified representation, not prove source authenticity or prior research completion.
