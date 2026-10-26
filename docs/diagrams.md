# Editable diagram sources

These diagrams adapt the portfolio's public assistant workflow and model history. SVG versions are embedded in the README; keep both representations aligned.

## Assistant workflow

```mermaid
flowchart LR
  Q[Technician question] --> O[Agent orchestration: context and role-aware tools]
  K[Retrieved documentation and operational context] --> O
  T[Operational tools: KPIs, logs, sites, cells and anomalies] --> O
  R[RCA: candidate causes, lags, statistics and graphs] --> O
  O --> E[Findings and supporting evidence]
  E --> H[Technician review and next diagnostic check]
```

This does not prescribe exact call order, a fixed tool sequence, or model iteration counts.

## Model evolution

```mermaid
flowchart LR
  G[GPT API: MVP on non-production data] --> D[DeepSeek R1 7B: local inference through vLLM]
  D --> C[Qwen / Mistral: development comparisons]
```

This is development history, not a quality ranking or simultaneous deployment claim. Retrieval and tool integration remain central across iterations.
