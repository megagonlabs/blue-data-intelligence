# Blue: A Data Intelligence Layer for AI Agents
AI agents are getting better at reasoning, planning, and using tools. But to complete real-world tasks, they need more than access to data—they need to understand what information exists, what it means, and how to use it across systems.
That is the role of Blue.
Blue is a data intelligence layer built for AI agents. It sits between agent frameworks and the underlying data systems, giving agents a unified way to discover, understand, and use data across heterogeneous sources—from relational databases, documents, vector stores, and knowledge graphs to the web, LLM knowledge, and user context.
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

