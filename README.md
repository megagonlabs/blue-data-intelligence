# Blue: A Data Intelligence Layer for AI Agents
AI agents are getting better at reasoning, planning, and using tools. But to complete real-world tasks, they need more than access to data—they need to understand what information exists, what it means, and how to use it across systems.
That is the role of Blue.
Blue is a data intelligence layer built for AI agents. It sits between agent frameworks and the underlying data systems, giving agents a unified way to discover, understand, and use data across heterogeneous sources—from relational databases, documents, vector stores, and knowledge graphs to the web, LLM knowledge, and user context.

## ** Placeholder for data intelligence diagram**

## Bring different data sources together
Real-world tasks rarely depend on a single source of information.
An agent may need to combine internal enterprise data with documents, external web information, general knowledge from an LLM, and context about the user.
Blue brings these sources into a common data layer so they can be discovered, queried, and combined within the same workflow.
This includes both traditional data sources and sources that are especially important for agentic applications, such as the web, LLMs, and user data.
## Help agents understand the right data
Access alone is not enough.
Agents also need to understand what data represents, how different fields and sources relate to one another, and whether a particular source is useful for the task at hand.
Blue's Data Registry captures information about available data, including schemas, attributes, relationships, statistics, and semantic meaning.
This gives agents the context they need to determine what data is relevant and how it should be used.
## Turn intent into executable data workflows
Complex tasks often require more than retrieving a single piece of information.
They may involve discovering sources, running queries, filtering results, joining data, applying semantic operations, or transforming information before producing an answer.
Blue's Data Planner turns a natural-language request into a structured, executable data workflow.
These workflows can span multiple sources and operators, and can be refined or optimized based on factors such as cost, latency, and accuracy.
By representing the work as a data plan, Blue gives agents a more systematic way to complete complex, multi-source tasks.
## Work alongside existing agent frameworks
Blue is designed to work with existing agent frameworks and application architectures.
An agent framework can use Blue whenever it needs to discover, understand, retrieve, transform, or combine data across sources.
Blue can be integrated directly through Python libraries or exposed through interfaces such as MCP, REST APIs, and the command line.
This lets developers add data intelligence to agent applications while continuing to use the frameworks and architectures that already fit their needs.
## Making data more usable for agents
The next generation of agents will need more than more tools and more connectors. They will need a better way to understand and work with the data behind those tools.
Blue provides that layer.
By combining heterogeneous data sources, semantic understanding, and executable data planning, Blue helps turn raw access into usable data intelligence for AI agents.

## Blue Data Intelligence Components

Blue data intelligence is seperated into individual github repositories:

- [`Blue Data`](https://github.com/megagon-internal/blue-data) provides a unified interface to register, introspect, and query heterogeneous data sources such as SQL databases, document stores, graph databases  and enriches them with semantic metadata that makes data understandable to AI agents and language models. It sits between raw data and the AI layer, answering questions like: what data exists, what it means, how it relates, and how it can safely be queried.

- [`Data Operators`](https://github.com/megagon-internal/blue-data-ops) is a reusable data-processing layer for planners, optimizers, agents, and applications on data flows. It represents operations (pre-defined data workflows) over structured data, text, vectors, and other modalities through a common interface, so a data-processing step can be discovered, validated, composed, and executed without coupling the caller to operator-specific input formats or behavior. 

- [`Data Planner`](https://github.com/megagon-internal/blue-data-planner) is an operator-agnostic data planners that turns a request written in plain language into a declarative plan — a DAG of operator calls — runs it, and repairs it where it fails.

- [`Agentic Memory`](https://github.com/megagon-internal/Genie/) is typed building blocks for developers who build their own memory systems: memory blocks, parent/child ownership, typed relationships, scoped access, and optional structure views. 

- [`User Data Source`](https://github.com/megagon-internal/blue-data-user-source) is a persistent user data system for AI agents that continuously captures, organizes, and retrieves user knowledge from conversations, uploaded files, and other data sources.

- [`Document Datasource`](https://github.com/megagon-internal/blue-data-doc-source) is a document ingestion and retrieval source for Blue Data Intelligence. It sits upstream of Blue's vector layer, converting unstructured documents into structured, provenance-aware chunk records that AI agents can search, cite, and reason over.

- [`LLM Datasource`](https://github.com/megagon-internal/blue-data-llm-source) is a knowledge data source which makes a language model's knowledge queryable as structured data

- [`Web Datasource`](https://github.com/megagon-internal/blue-data-web-source) is a web ingestion and retrieval source whcih sits upstream of Blue's vector layer, converting live web pages into structured, provenance-aware chunk records that AI agents can search, cite, and reason over.

- [`KB Datasource`](https://github.com/megagon-internal/blue-data-kb-source) is a typed knowledge-base layer for agentic pipelines that captures, organizes, and reasons over structured knowledge extracted from documents, conversations, and other data sources

