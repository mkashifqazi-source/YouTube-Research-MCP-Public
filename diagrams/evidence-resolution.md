# Existing and proposed evidence paths

~~~mermaid
flowchart TD
  U[Supported reference] --> N[Pure identity normalization]
  N --> R[Live provider request]
  R --> P[Sequential conservative provider service]
  P --> E[Provenance-rich uncertain transcript or safe error]
  I[Explicit supplied fixture data] --> V[Internal offline validation]
  V --> S[Supplied uncertain evidence or rejection]
  E -. proposed .-> O[Future common evidence operations]
  S -. proposed .-> O
  D[Future durable evidence store] -. proposed .-> O
  O -. proposed .-> C[Source-bound chunks / timestamp citations]
~~~

Solid paths represent located code boundaries. Dashed paths are proposed capabilities, not implemented integration. The internal validator is not a public MCP ingestion endpoint.
