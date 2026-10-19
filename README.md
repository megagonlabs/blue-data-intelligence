# Blue Data Intelligence: A Data Intelligence Layer for AI Agents
AI agents are getting better at reasoning, planning, and using tools. But to complete real-world tasks, they need more than access to data—they need to understand what information exists, what it means, and how to use it across systems.
Blue is a data intelligence layer built for AI agents. It sits between agent frameworks and the underlying data systems, giving agents a unified way to discover, understand, and use data across heterogeneous sources—from relational databases, documents, vector stores, and knowledge graphs to the web, LLM knowledge, and user context.

<p align="center">
  <img src="./docs/images/data_intelligence_architecture.png" alt="Architecture" width="100%">
</p>

## Blue Data Intelligence Components

Blue data intelligence is seperated into individual github repositories:

### Foundation

- [`Data Foundation`](https://github.com/megagon-internal/blue-data) bridges raw data and AI applications. It registers, introspects, and queries heterogeneous data sources (SQL databases, document stores, graph databases, and more) and enriches them with semantic metadata, so agents know what data exists, what it means, how it relates, and how to query it safely.

### Planning and execution

- [`Data Planner`](https://github.com/megagon-internal/blue-data-planner) is the planning layer for agentic applications. It translates a natural language request into a declarative plan, a DAG of data-processing steps that Operator executes to produce the final answer.

- [`Operators`](https://github.com/megagon-internal/blue-data-ops) is the reusable execution layer for agentic applications. It compiles declarative plans into pipelines and runs them over structured data, text, vectors, and other modalities through a common interface, so steps can be discovered, validated, composed, and executed without coupling the caller to operator-specific input formats or behavior.

### Enterprise data sources

- [`Document Data Source`](https://github.com/megagon-internal/blue-data-doc-source) is a document ingestion and retrieval source for Blue Data Intelligence. It sits upstream of Blue's vector layer, converting unstructured documents into structured, provenance-aware chunk records that agents can search, cite, and reason over.

- [`Knowledge-Base Data Source`](https://github.com/megagon-internal/blue-data-kb-source) is a typed knowledge-base layer for agentic pipelines that captures, organizes, and reasons over structured knowledge extracted from documents, conversations, and other data sources.

### Agentic data sources

Many agent tasks depend on information beyond enterprise systems. These sources make LLM knowledge, the web, and user personal data queryable as first-class sources alongside enterprise data sources.

- [`LLM Data Source`](https://github.com/megagon-internal/blue-data-llm-source) is a knowledge data source which makes a language model's knowledge queryable as structured data.

- [`Web Data Source`](https://github.com/megagon-internal/blue-data-web-source) is a web ingestion and retrieval source which sits upstream of Blue's vector layer, converting live web pages into structured, provenance-aware chunk records that agents can search, cite, and reason over.

- [`User Data Source`](https://github.com/megagon-internal/blue-data-user-source) is a persistent user data system that continuously captures, organizes, and retrieves user knowledge from conversations, uploaded files, and other sources.

### Memory

- [`Agent Memory`](https://github.com/megagon-internal/Genie/) provides flexible primitives and hooks for building custom memory systems (memory blocks, parent/child ownership, typed relationships, scoped access, and optional structure views), with governance that manages memory access across multiple agents.

