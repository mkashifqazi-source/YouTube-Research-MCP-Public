# YouTube Research MCP

A deterministic transcript-evidence foundation with exact video identity, conservative provider acquisition and offline supplied-evidence validation.

Public Technical Overview · Private Development Repository

## Overview

The project prepares YouTube transcript evidence for downstream research while preserving source identity, acquisition provenance and uncertainty. Its name describes the intended MCP product; the current code is a library and feasibility foundation, not an established production MCP server.

## Problem

Caption providers can be blocked, incomplete or ambiguous. A returned transcript can be useful without proving complete coverage or truthful speech. Supplied text introduces additional source-association and timing claims that must be validated without upgrading them into observed facts.

## System Architecture

~~~mermaid
flowchart LR
  U[YouTube reference] --> N[Offline identity normalizer]
  N --> S[Bounded provider service]
  S --> A[youtube-transcript-api / yt-dlp]
  A --> E[Segments, provenance, warnings or errors]
  I[Supplied fixture evidence] --> V[Offline internal validator]
  V --> P[Preserved supplied evidence and claims]
  E -. future .-> R[Research evidence operations]
  P -. future .-> R
~~~

## Core Components

URL/video normalization; typed result/status/error/provenance contracts; native-caption adapters; conservative fallback; metadata/WebVTT evidence parsing; internal supplied validator; and offline test fixtures/cloud diagnostics.

## Key Technical Workflows

Normalize → request → attempt provider once → stop or narrowly eligible fallback → return source-bound evidence. Supplied input follows offline bounded validation, retaining raw representations and claims without fetching or persisting anything.

## Engineering Decisions

Acquisition success remains uncertain. Manual/auto/supplied kind differs from origin/status. Retryable/provider-blocked errors stop fallback. Proposed persisted reads retain original acquisition time. Cleaning, quality engines and timestamp citations remain future work.

## Reliability / Safety / Validation

Empty provider metadata is not proof of video-wide caption absence. Valid source binding does not prove supplied text matches the video. Provider output is evidence rather than trusted truth. No transcript bodies or research video corpus are published here.

## Technology Stack

Python 3.12, youtube-transcript-api, yt-dlp, standard-library dataclasses/enums/URL parsing and offline unittest-style tests. Docker/Cloud Run probe files are experimental tooling, not a production service guarantee.

## Testing

Fixture-based normalization/provider/contract/fallback tests and adversarial supplied validation with network/filesystem/subprocess denial. Historical cloud feasibility is distinct from offline correctness. No new tests or live retrieval ran for this task.

## Current Status

Research/prototype foundation; production retrieval gate held. Internal supplied-validation code is present despite older proposal-only docs. Public MCP orchestration, persistence and citation workflow are not established.

## Technical Documentation

- [architecture](docs/architecture.md)
- [data model](docs/data-model.md)
- [workflows](docs/workflows.md)
- [testing and validation](docs/testing-and-validation.md)
- [reliability and failure model](docs/reliability-and-failure-model.md)
- [security and authority](docs/security-and-authority.md)
- [technical decisions](docs/technical-decisions.md)
- [project status](docs/project-status.md)
- [evidence resolution](diagrams/evidence-resolution.md)

## Repository Notice

This repository contains the public technical documentation for the project. The production source code and internal development materials are maintained separately and are not published here.
