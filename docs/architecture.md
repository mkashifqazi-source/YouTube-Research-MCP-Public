# Architecture and implementation boundaries

The current system is a deterministic evidence library with experimental native-caption adapters and offline validation. A production MCP endpoint and its intended prepare_video_for_research tool were not established as implemented.

Pure normalization accepts supported YouTube URL forms, validates video identity and derives a canonical reference plus stable `youtube:<video_id>` source identity without fetching the supplied URL. Live provider requests operate on that normalized identity, ordered language preferences and manual-caption preference.

Adapters for youtube-transcript-api and yt-dlp return the shared result/error/provenance contract. The service deduplicates provider identities and attempts configured providers sequentially under a conservative stop policy. Parsing and caption metadata assessment preserve what a provider actually returned, including scoped warnings and ambiguous absence.

An internal supplied-evidence validator and offline fixtures exist in the inspected current tree. Older H1/H2 documents still call this capability unimplemented. The case study therefore records implementation presence separately from accepted design, public ingestion integration and production approval. The validator is neither a pretend live provider nor a store/public tool.

The proposed evidence-first hybrid separates live retrieval, supplied evidence and durable persisted evidence. Persistence, cross-mode resolution, transcript cleaning/quality engines, search/range tools and chunk/timestamp-citation workflows remain future capabilities. Version constants and enums are not proof that those engines execute.

Cloud Run files implement one-shot feasibility probes/diagnostics, not a proven continuously available production transcript service. The accepted direction retains a useful evidence core while holding production retrieval until representative feasibility and acceptance are demonstrated. No storage/authentication vendor or production resolution order is selected by this public overview.
