---

title: Azure Cosmos DB AI Graph
description: Apply Knowledge Graphs to expand the capability of AI apps.
author: jcodella
ms.service: azure-cosmos-db
ms.subservice: nosql
ms.topic: quickstart
ms.date: 9/16/2024
ms.author: jacodel

---

# Retrieval Augmented Generated (RAG) with vector search and knowledge graphs using Azure Cosmos DB

[!INCLUDE[NoSQL](../includes/appliesto-nosql.md)]

[Cosmos AI Graph](https://aka.ms/cosmosaigraph) is an innovative solution that applies the power of Azure Cosmos DB to create AI-powered knowledge graphs. This technology integrates advanced graph database capabilities with AI to provide a robust platform for managing and querying complex data relationships. By utilizing Cosmos DB's scalability and performance, Cosmos AI Graph enables the creation of sophisticated data models that can answer various data questions and uncover hidden relationships and concepts in text data.

## What Types of questions can knowledge graphs help to answer?

- **Complex Relationship Queries**: 
   - *Question*: "What are the direct and indirect connections between Person A and Person B within a social network?"
   - *Explanation*: Graph RAG can traverse the graph to find all paths and relationships between two nodes, providing a detailed map of connections, which is difficult for Vector Search as it doesn't inherently understand relationships between entities.

- **Hierarchical Data Queries**:
   - *Question*: "What is the organizational hierarchy from the CEO down to the entry-level employees in this company?"
   - *Explanation*: Graph RAG can efficiently navigate hierarchical structures, identifying parent-child relationships and levels within the hierarchy, whereas Vector Search is more suited for finding similar items rather than understanding hierarchical relationships.

- **Contextual Path Queries**:
   - *Question*: "What are the steps involved in the supply chain from raw material procurement to the final product delivery?"
   - *Explanation*: Graph RAG can follow the specific paths and dependencies within a supply chain graph, providing a step-by-step breakdown. Vector Search, while excellent at finding similar items, lacks the capability to follow and understand the sequence of steps in a process.


When it comes to [Retrieval Augmented Generation (RAG)](rag.md), combining **Knowledge Graphs** and **Vector Search** can offer powerful capabilities that expand the range of questions that can be answered about the data. Graph RAG enhances the retrieval process by using the structured relationships within a graph, making it ideal for applications that require contextual understanding and complex querying, such as knowledge management systems and personalized content delivery. On the other hand, Vector Search excels in handling unstructured data and finding similarities based on vector embeddings, which is useful for tasks like image and document retrieval. Together, these technologies can provide a comprehensive solution that combines the strengths of both structured and unstructured data processing.


:::image type="content" source="../media/gen-ai/cosmos-ai-graph/cosmos-ai-graph-architecture.png" alt-text="Diagram of the Cosmos AI Graph infrastructure, components, and flow.":::

## OmniRAG

CosmosAIGraph features *OmniRAG*, a versatile approach to data retrieval that dynamically selects the most suitable method—be it database queries, vector searches, or knowledge graph searches—to answer user queries effectively. This ensures that each query is addressed using the optimal technique, enhancing accuracy and efficiency. For instance, a user query about hierarchical relationships would utilize graph traversal, while a query about similar documents would employ vector search, all within a unified framework provided by CosmosAIGraph. This holistic approach maximizes the strengths of each retrieval method, delivering comprehensive and contextually relevant answers.

### Example user questions and strategy used

| User Questions    | Strategy       |
|----------------|----------------|
|What is the Python Flask Library | DB RAG |
| What are its dependencies  | Graph Rag |
| What are its dependencies | Vector RAG |
| Who is the author | DB RAG  |
| What other libraries did she write | Graph Rag |
| Display a graph of all her libraries and their dependencies | Graph RAG |


## Get started

CosmosAIGraph applies Azure Cosmos DB to create AI-powered graphs and knowledge graphs, enabling sophisticated data models for applications like recommendation systems and fraud detection. It combines traditional database, vector database, and graph database capabilities with AI to manage and query complex data relationships efficiently. Get started [here!](https://aka.ms/cosmosaigraph)

## Next steps
- [Cosmos AI Graph on Azure Cosmos DB TV - YouTube](https://www.youtube.com/watch?v=0alvRmEgIpQ)
- [Vector Search with Azure Cosmos DB for NoSQL](vector-search-overview.md)
- [Tokens](tokens.md)
- [Vector Embeddings](vector-embeddings.md)
- [Retrieval Augmented Generated (RAG)](rag.md)
- [30-day Free Trial without Azure subscription](https://azure.microsoft.com/try/cosmosdb/)
- [90-day Free Trial and up to $6,000 in throughput credits with Azure AI Advantage](../ai-advantage.md)

> [!div class="nextstepaction"]
> [Use the Azure Cosmos DB lifetime free tier](../free-tier.md)